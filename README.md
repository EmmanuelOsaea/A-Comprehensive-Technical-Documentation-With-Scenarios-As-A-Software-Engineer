# Back-End: Node.js + Express Api

server.js









# Docker Compose for Local Development
 docker-compose.yml

 ```version: '3'




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

# Example: Express.js API Endpoint 
```
const express = require('express');
const app = express();

app.get('/api/users/:id', async (req, res) => {
const userId = req.params.id;
// Simulate database fetch
const user = await getUserFromDatabase(userId);
if (!user) return res.status(404).json({ error: 'User not detected' })
res.json(user);
});

function getUserFromDatabase(id) {
// Mock database call
return Promise.resolve({id, name: 'Yale', email: 'Yaled2269@gmail.com' password: 'Sqeshb#*#5W;!?'
}

app.listen(4000, () => {
 console.log('Server running on port 4000');
 });
 ```

