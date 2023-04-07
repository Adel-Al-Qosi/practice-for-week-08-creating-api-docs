# API Documentation
## Purpose
The purpose of this API is to provide access to posts, comments, and likes for a social media platform.

## Audience
The target audience for this API documentation is developers who will be integrating with the social media platform.

## Endpoints
Get all the posts
URL: /posts
Method: GET
Description: Returns all posts.
Response body: Array of post objects.
Create a new post
URL: /posts
Method: POST
Description: Creates a new post.
Request body: Post object.
Response status codes:
201 CREATED: The post was created successfully.
400 BAD REQUEST: The request body was invalid.
## Edit a post
URL: /posts/:postId
Method: PUT or PATCH
Description: Updates an existing post.
Request body: Post object.
Response status codes:
200 OK: The post was updated successfully.
400 BAD REQUEST: The request body was invalid.
404 NOT FOUND: The specified post was not found.
Create a new user
URL: /users
Method: POST
## Description: Creates a new user.
Request body: User object.
Response status codes:
201 CREATED: The user was created successfully.
400 BAD REQUEST: The request body was invalid.
Get the comments for a post
URL: /posts/:postId/comments
Method: GET
Description: Returns all comments for a specified post.
## Response body: Array of comment objects.
Create a comment for a post
URL: /posts/:postId/comments
Method: POST
Description: Creates a new comment for a specified post.
Request body: Comment object.
Response status codes:
201 CREATED: The comment was created successfully.
400 BAD REQUEST: The request body was invalid.
Edit a comment for a post
URL: /posts/:postId/comments/:commentId
Method: PUT or PATCH
Description: Updates an existing comment for a specified post.
Request body: Comment object.
Response status codes:
200 OK: The comment was updated successfully.
400 BAD REQUEST: The request body was invalid.
404 NOT FOUND: The specified comment was not found.
Delete a comment for a post
URL: /posts/:postId/comments/:commentId
Method: DELETE
Description: Deletes an existing comment for a specified post.
Response status codes:
204 NO CONTENT: The comment was deleted successfully.
404 NOT FOUND: The specified comment was not found.
Add a like for a post
URL: /posts/:postId/likes
Method: POST
Description: Adds a like for a specified post.
Request body: Like object.
Response status codes:
201 CREATED: The like was added successfully.
400 BAD REQUEST: The request body was invalid.
Remove a like for a post
URL: /posts/:postId/likes/:likeId
Method: DELETE
Description: Removes a like for a specified post.
Response status codes:
204 NO CONTENT: The like was removed successfully.
404 NOT FOUND: The specified like was not found.
Get all the posts of a user
URL: /users/:userId/posts
Method: GET
Description: