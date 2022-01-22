# json-server-demo-1

#link
https://github.com/typicode/json-server

#install json server
npm install -g json-server

#db.json
{
    "posts": [
      { "id": 1, "title": "json-server", "author": "typicode" }
    ],
    "comments": [
      { "id": 1, "body": "some comment 1", "postId": 1 },
      { "id": 2, "body": "some comment 2", "postId": 1 }
    ],
    "profile": { "name": "typicode" }
}


#command
json-server --watch db.json


#Link Test
localhost:3000/
localhost:3000/db
localhost:3000/posts
localhost:3000/posts/1
localhost:3000/comments
localhost:3000/comments/1
localhost:3000/profile



#Customer Routes
{
  "/api/*": "/$1",
  "/:resource/:id/show": "/:resource/:id",
  "/posts/:category": "/posts?category=:category",
  "/articles\\?id=:id": "/posts/:id"
}

#command 
json-server db.json --routes routes.json