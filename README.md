# Social Blog API
- Clone and Install dependencies
- Set up some required ENV VARS
- Test the app: `npm run dev`, then open `localhost:5000` on the browser.
- [API Documentation](https://documenter.getpostman.com/view/7621298/T1Dv8F6p?version=latest#a071427d-c177-49b5-b7be-50c3456b9aac)

### Project structure

```
|- bin/
|- controllers/
|- helpers/
|- middlewares/
|- models/
|- public/
|- routes/
|- app.js
```

- Authentication
```javascript
/** 
 * @route POST api/auth/login 
 * @route GET api/auth/logout 
 */
```
- User model
```javascript
/** 
 * @route POST api/users - Register
 * @route GET api/users?page=1&limit=20
 * @route GET api/users/me - Get current user
 * @route POST api/users/me/avatar - Upload avatar
 * @route PUT api/users/me - Update user info
 * @route PUT api/users/me/password - Change Password
 */
```
- Blog model
```javascript
/** 
 * @route GET api/blogs?page=1&limit=10 - Get blogs with pagination
 * @route GET api/users/:id/blogs?page=1&limit=20 - Get blogs from user
 * @route GET api/blogs/friends?page=1&limit=20 - Get blogs from friends
 * @route GET api/blogs/:id - Get blog detail
 * @route POST api/blogs/:id - Create a new blog
 * @route PUT api/blogs/:id - Update a blog
 * @route DELETE api/blogs/:id - Remove a blog
 */
```
- Review model
```javascript
/** 
 * @route GET api/blogs/:id/reviews?page=1&limit=10 - Get reiviews from a blog
 * @route POST api/blogs/:id/reviews - Create new review for a blog
 * @route PUT api/blogs/:id/reviews/:id - Update review
 * @route DELETE api/blogs/:id/reviews/:id - Delete review
 */
```
- Reaction
```javascript
/** 
 * @route POST api/reactions
 */
```
- Friends
```javascript
/** 
 * @route GET api/friends/manage/:id - Get the list of friends
 * @route GET api/friends/add/:id - Get the list of friend requests
 * @route POST api/friends/add/:id - Send friend request
 * @route POST api/friends/manage/:id - Accept Request
 * @route DELETE api/friends/add/:id - Remove Friend request
 * @route DELETE api/friends/manage/:id - Decline Request
 */
```
