# Reddit API Documentation

`const API = "https://reddit-backend-w8g7.onrender.com"`

## GET /

### Request:

```js
fetch(`${API}/`);
```

### Response:

````js
{
  "success": true,
  "message": "Welcome to the Reddit server!"
}

## GET /posts

### Request:

```js
fetch(`${API}/posts`);
````

### Response:

```js
{
  "success": true,
  "posts": [
    {
      "id": "0a817d6e-be92-430e-a6f4-719801738c64",
      "text": "mac vs windows.",
      "title": "Macbook",
      "userId": "9029ed5c-9056-4654-b568-0bf7fd92071b",
      "subredditId": "f3e47327-808e-4343-b6d9-bed030c2e9ff",
      "parentId": null,
      "user": {
        "id": "9029ed5c-9056-4654-b568-0bf7fd92071b",
        "username": "abdel",
        "password": "$2b$10$fIgbTBZV.9qY8Y65geHWMeh0hkg7gjY8uM.QVJCx5OvwZ5/C66TFi"
      },
      "subreddit": {
        "id": "f3e47327-808e-4343-b6d9-bed030c2e9ff",
        "name": "Technology",
        "userId": "b741adcd-36f2-4d83-af9b-a52f91804aa5"
      },
      "upvotes": [
        {
          "id": "93a73c28-e65e-4da1-9bd2-6443601b5565",
          "userId": "9029ed5c-9056-4654-b568-0bf7fd92071b",
          "postId": "0a817d6e-be92-430e-a6f4-719801738c64"
        },
        {
          "id": "bae7b0b0-7148-4fda-8afc-0c106aad3bbc",
          "userId": "ad520caf-c665-43f1-9534-660cd071ba50",
          "postId": "0a817d6e-be92-430e-a6f4-719801738c64"
        }
      ],
      "downvotes": [
        {
          "id": "e07b5fbb-9254-4633-9255-82fd4be58683",
          "userId": "ad520caf-c665-43f1-9534-660cd071ba50",
          "postId": "0a817d6e-be92-430e-a6f4-719801738c64"
        }
      ],
      "children": []
    },
    {
      "id": "280c3437-69aa-4f35-bd67-2d11b5cf0596",
      "text": "how much is btc worth",
      "title": "btc",
      "userId": "b741adcd-36f2-4d83-af9b-a52f91804aa5",
      "subredditId": "88e8718f-931f-4e64-8849-67cabb6cb94a",
      "parentId": null,
      "user": {
        "id": "b741adcd-36f2-4d83-af9b-a52f91804aa5",
        "username": "katie",
        "password": "$2b$10$oFyb0maubaWpAOUZmv8HYekCILQwiMGxsRLVQl2hlzxMC3bepiDBu"
      },
      "subreddit": {
        "id": "88e8718f-931f-4e64-8849-67cabb6cb94a",
        "name": "Crypto",
        "userId": "b741adcd-36f2-4d83-af9b-a52f91804aa5"
      },
      "upvotes": [
        {
          "id": "4e6cd525-ae64-464d-9720-fa51bb7b6db4",
          "userId": "b741adcd-36f2-4d83-af9b-a52f91804aa5",
          "postId": "280c3437-69aa-4f35-bd67-2d11b5cf0596"
        }
      ],
      "downvotes": [],
      "children": [
        {
          "id": "67836f3e-0695-407e-bd0e-77d2dcb71101",
          "text": "im a child",
          "title": "child",
          "userId": "03ca1281-ddb3-4421-a8f6-22c76b6a99b8",
          "subredditId": "88e8718f-931f-4e64-8849-67cabb6cb94a",
          "parentId": "280c3437-69aa-4f35-bd67-2d11b5cf0596"
        }
      ]
    },
    {
      "id": "2ef5c34d-9c82-423d-bc84-aaeb0176c5d5",
      "text": "mac vs windows.",
      "title": null,
      "userId": "3b11d233-fe14-4678-b000-7c2d51dba71a",
      "subredditId": "f3e47327-808e-4343-b6d9-bed030c2e9ff",
      "parentId": null,
      "user": {
        "id": "3b11d233-fe14-4678-b000-7c2d51dba71a",
        "username": "santa2",
        "password": "$2b$10$smCPXzEaBYjpy7oVDqb/Xecl7hk4RvonKscxFIDBIHtiB6b4zoIq2"
      },
      "subreddit": {
        "id": "f3e47327-808e-4343-b6d9-bed030c2e9ff",
        "name": "Technology",
        "userId": "b741adcd-36f2-4d83-af9b-a52f91804aa5"
      },
      "upvotes": [],
      "downvotes": [],
      "children": []
    },
    {
      "id": "50b8c518-c080-4869-a05f-a91ea84f6499",
      "text": "when is the oscars?",
      "title": "oscars",
      "userId": "b741adcd-36f2-4d83-af9b-a52f91804aa5",
      "subredditId": "9e30964a-015f-458c-842c-47382d519f13",
      "parentId": null,
      "user": {
        "id": "b741adcd-36f2-4d83-af9b-a52f91804aa5",
        "username": "katie",
        "password": "$2b$10$oFyb0maubaWpAOUZmv8HYekCILQwiMGxsRLVQl2hlzxMC3bepiDBu"
      },
      "subreddit": {
        "id": "9e30964a-015f-458c-842c-47382d519f13",
        "name": "Fashion",
        "userId": "b741adcd-36f2-4d83-af9b-a52f91804aa5"
      },
      "upvotes": [],
      "downvotes": [
        {
          "id": "c5b3d324-186c-4a88-a438-b0b183331fdf",
          "userId": "b741adcd-36f2-4d83-af9b-a52f91804aa5",
          "postId": "50b8c518-c080-4869-a05f-a91ea84f6499"
        }
      ],
      "children": []
    },
    {
      "id": "67836f3e-0695-407e-bd0e-77d2dcb71101",
      "text": "im a child",
      "title": "child",
      "userId": "03ca1281-ddb3-4421-a8f6-22c76b6a99b8",
      "subredditId": "88e8718f-931f-4e64-8849-67cabb6cb94a",
      "parentId": "280c3437-69aa-4f35-bd67-2d11b5cf0596",
      "user": {
        "id": "03ca1281-ddb3-4421-a8f6-22c76b6a99b8",
        "username": "max",
        "password": "$2b$10$1fUlSLlsIkD8ZYBHVhInoeJlbK7rlALp3tdByLanLbuy5Yjc.xBJq"
      },
      "subreddit": {
        "id": "88e8718f-931f-4e64-8849-67cabb6cb94a",
        "name": "Crypto",
        "userId": "b741adcd-36f2-4d83-af9b-a52f91804aa5"
      },
      "upvotes": [],
      "downvotes": [
        {
          "id": "5748b489-339c-417a-bc65-19dde01189a2",
          "userId": "ad520caf-c665-43f1-9534-660cd071ba50",
          "postId": "67836f3e-0695-407e-bd0e-77d2dcb71101"
        }
      ],
      "children": [
        {
          "id": "72950195-eca7-45ef-bf4f-89c096d98fd2",
          "text": "im a grandchild",
          "title": "grandchild",
          "userId": "9029ed5c-9056-4654-b568-0bf7fd92071b",
          "subredditId": "9e30964a-015f-458c-842c-47382d519f13",
          "parentId": "67836f3e-0695-407e-bd0e-77d2dcb71101"
        }
      ]
    },
    {
      "id": "72950195-eca7-45ef-bf4f-89c096d98fd2",
      "text": "im a grandchild",
      "title": "grandchild",
      "userId": "9029ed5c-9056-4654-b568-0bf7fd92071b",
      "subredditId": "9e30964a-015f-458c-842c-47382d519f13",
      "parentId": "67836f3e-0695-407e-bd0e-77d2dcb71101",
      "user": {
        "id": "9029ed5c-9056-4654-b568-0bf7fd92071b",
        "username": "abdel",
        "password": "$2b$10$fIgbTBZV.9qY8Y65geHWMeh0hkg7gjY8uM.QVJCx5OvwZ5/C66TFi"
      },
      "subreddit": {
        "id": "9e30964a-015f-458c-842c-47382d519f13",
        "name": "Fashion",
        "userId": "b741adcd-36f2-4d83-af9b-a52f91804aa5"
      },
      "upvotes": [],
      "downvotes": [
        {
          "id": "1b872683-102b-46ec-87ec-df7745cb9497",
          "userId": "ad520caf-c665-43f1-9534-660cd071ba50",
          "postId": "72950195-eca7-45ef-bf4f-89c096d98fd2"
        }
      ],
      "children": []
    },
    {
      "id": "fc7a3bed-ee85-4fbd-bcdc-a5384be8dfc0",
      "text": "I think I saw an alien outside the mall",
      "title": "Aliens",
      "userId": "b741adcd-36f2-4d83-af9b-a52f91804aa5",
      "subredditId": "f3e47327-808e-4343-b6d9-bed030c2e9ff",
      "parentId": null,
      "user": {
        "id": "b741adcd-36f2-4d83-af9b-a52f91804aa5",
        "username": "katie",
        "password": "$2b$10$oFyb0maubaWpAOUZmv8HYekCILQwiMGxsRLVQl2hlzxMC3bepiDBu"
      },
      "subreddit": {
        "id": "f3e47327-808e-4343-b6d9-bed030c2e9ff",
        "name": "Technology",
        "userId": "b741adcd-36f2-4d83-af9b-a52f91804aa5"
      },
      "upvotes": [
        {
          "id": "06037689-4b32-455d-b5b5-19da011dc3c0",
          "userId": "ad520caf-c665-43f1-9534-660cd071ba50",
          "postId": "fc7a3bed-ee85-4fbd-bcdc-a5384be8dfc0"
        },
        {
          "id": "39a49529-412c-4918-9a76-19656794a845",
          "userId": "b741adcd-36f2-4d83-af9b-a52f91804aa5",
          "postId": "fc7a3bed-ee85-4fbd-bcdc-a5384be8dfc0"
        },
        {
          "id": "86d3f4d6-b105-41dd-83e5-c8f819ffd9d4",
          "userId": "9029ed5c-9056-4654-b568-0bf7fd92071b",
          "postId": "fc7a3bed-ee85-4fbd-bcdc-a5384be8dfc0"
        }
      ],
      "downvotes": [
        {
          "id": "8769280e-bb7c-43c9-b996-fe403b96fa18",
          "userId": "9029ed5c-9056-4654-b568-0bf7fd92071b",
          "postId": "fc7a3bed-ee85-4fbd-bcdc-a5384be8dfc0"
        }
      ],
      "children": []
    }
  ]
}
```

## POST /posts

### Request:

```js
fetch(`${API}/posts`, {
  method: "POST",
  headers: {
    "Content-Type": "application/json",
    Authorization:
      "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOiIzYjExZDIzMy1mZTE0LTQ2NzgtYjAwMC03YzJkNTFkYmE3MWEiLCJpYXQiOjE2OTQ1MjE5Nzl9.6qiWcCWgOA3Wvie8pjimOs1j8irhOQy6WfdVUNhUhkU",
  },
  body: JSON.stringify({
    title: "Review of the new iphone 13 mini", // optional
    text: "it's pretty good!",
    subredditId: "f3e47327-808e-4343-b6d9-bed030c2e9ff",
    parentId: null, // optional
  }),
});
```

### Response:

```js
{
  "success": true,
  "post": {
    "id": "65ce7d00-1a16-41af-b333-58cc84d9ffd4",
    "text": "it's pretty good!",
    "title": "Review of the new iphone 13 mini",
    "userId": "03ca1281-ddb3-4421-a8f6-22c76b6a99b8",
    "subredditId": "f3e47327-808e-4343-b6d9-bed030c2e9ff",
    "parentId": null
  }
}
```

## PUT /posts/:postId

### Request:

```js
fetch(`${API}/posts/28006818-1695-4984-83e9-bf0e6a864e08`, {
  method: "PUT",
  headers: {
    "Content-Type": "application/json",
    Authorization:
      "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOiIzYjExZDIzMy1mZTE0LTQ2NzgtYjAwMC03YzJkNTFkYmE3MWEiLCJpYXQiOjE2OTQ1MjE5Nzl9.6qiWcCWgOA3Wvie8pjimOs1j8irhOQy6WfdVUNhUhkU",
  },
  body: JSON.stringify({
    title: "Review of the new iphone 13 mini - Updated!", // optional
    text: "it's not actually that good!", // optional
  }),
});
```

### Response:

```js
{
  "success": true,
  "post": {
    "id": "65ce7d00-1a16-41af-b333-58cc84d9ffd4",
    "text": "it's not actually that good!",
    "title": "Review of the new iphone 13 mini - Updated!",
    "userId": "03ca1281-ddb3-4421-a8f6-22c76b6a99b8",
    "subredditId": "f3e47327-808e-4343-b6d9-bed030c2e9ff",
    "parentId": null
  }
}
```

## DELETE /posts/:postId

### Request:

```js
fetch(`${API}/posts/65ce7d00-1a16-41af-b333-58cc84d9ffd4`, {
  method: "DELETE",
  headers: {
    Authorization:
      "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOiIwM2NhMTI4MS1kZGIzLTQ0MjEtYThmNi0yMmM3NmI2YTk5YjgiLCJpYXQiOjE2OTQ0MzUxNzJ9.AbFuHRnxTB1Ztgcf2S4nwn2NjuvGmV96iUx3TJN5zFk",
  },
});
```

### Response:

```js
{
  "success": true,
  "post": {
    "id": "65ce7d00-1a16-41af-b333-58cc84d9ffd4",
    "text": "it's not actually that good!",
    "title": "Review of the new iphone 13 mini - Updated!",
    "userId": "03ca1281-ddb3-4421-a8f6-22c76b6a99b8",
    "subredditId": "f3e47327-808e-4343-b6d9-bed030c2e9ff",
    "parentId": null
  }
}
```
