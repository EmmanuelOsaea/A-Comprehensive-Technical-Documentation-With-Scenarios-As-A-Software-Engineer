# Example: React Component with API Integration 

```import React,  { useEffect, useState } from 'react';

// UserPassword function
function UserPassword() {
 return (
 <div>
<label htmlFor ="password">Password:</label>
<input type="password" id="password" name="password />
 </div>
 );
}

function UserProfile({ userId }) {
const [user, setUser] = useState(null);

useEffect(() => {
async function fetchUser() {
const response = await fetch
const data = await response.json(`/api/users/${userId}`);
setUser(data);
}
fetchUser();
}, [userId]);

if (!user) return <p>Loading..</p>;

return (
<div>
{/*This replaces user info display with Userpassword */}
<UserPassword />
</div>
);
}

export default UserProfile;
```
