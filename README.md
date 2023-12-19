# Reddit API Documentation

## POST /users/register

### Request:

```js
fetch(`${API}/users/register`, {
  method: "POST",
  body: JSON.stringify({
    username: "max2",
    password: "123",
  }),
});
```

### Response:

```js
{
  "success": true,
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOiI2MDY1MjQ3Ny0yZDY1LTQzYzctYTJmMS1mMzU4ZTQyMGQxYWEiLCJpYXQiOjE2OTQ1Mjk3MDh9.a1HjJulV55JAwyKfKt8sTjpq0AKgGcahBNM1efgFE5g"
}
```

## POST /users/login

### Request:

```js
fetch(`${API}/users/login`, {
  method: "POST",
  body: JSON.stringify({
    username: "max2",
    password: "123",
  }),
});
```

### Response:

```js
{
  "success": true,
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOiI2MDY1MjQ3Ny0yZDY1LTQzYzctYTJmMS1mMzU4ZTQyMGQxYWEiLCJpYXQiOjE2OTQ1Mjk3MDh9.a1HjJulV55JAwyKfKt8sTjpq0AKgGcahBNM1efgFE5g"
}
```

## POST /users/logout

### Request:

```js
fetch(`${API}/users/login`, {
  method: "POST",
  body: JSON.stringify({
    username: "max2",
    password: "123",
  }),
});
```

### Response:

```js
{
  "success": true
}
```

## POST /posts

### Request:

```js
fetch(`${API}/posts`, {
  method: "POST",
  body: JSON.stringify({
    title: "I saw bigfoot.",
    message:
      "AITA I saw bigfoot and I didn't really care that much and just kept on driving.",
    subredditId: "a811872e-ac82-4a7d-8432-25ff2b3d9300",
  }),
});
```

### Response:

```js
{
  "success": true,
  "post": {
    "id": "11e3e2e3-cbc2-43ac-a27a-6e8249cd0b5a",
    "title": "I saw bigfoot.",
    "message": "AITA I saw bigfoot and I didn't really care that much and just kept on driving.",
    "userId": "c6e05954-1c2e-4f14-92e0-5827266b5a2e",
    "subredditId": "a811872e-ac82-4a7d-8432-25ff2b3d9300",
    "parentId": null
  }
}
```

## PUT /posts/:postId

### Request:

```js
fetch(`${API}/posts/11e3e2e3-cbc2-43ac-a27a-6e8249cd0b5a`, {
  method: "PUT",
  body: JSON.stringify({
    title: "Review of the new iphone 13 mini - Updated!", // optional
    message: "it's not actually that good!", // optional
  }),
});
```

### Response:

```js
{
  "success": true,
  "post": {
    "id": "11e3e2e3-cbc2-43ac-a27a-6e8249cd0b5a",
    "title": "Review of the new iphone 13 mini - Updated!",
    "message": "it's not actually that good!",
    "userId": "c6e05954-1c2e-4f14-92e0-5827266b5a2e",
    "subredditId": "a811872e-ac82-4a7d-8432-25ff2b3d9300",
    "parentId": null
  }
}
```

## DELETE /posts/:postId

### Request:

```js
fetch(`${API}/posts/65ce7d00-1a16-41af-b333-58cc84d9ffd4`, {
  method: "DELETE",
});
```

### Response:

```js
{
  "success": true,
  "post": {
    "id": "11e3e2e3-cbc2-43ac-a27a-6e8249cd0b5a",
    "title": "Review of the new iphone 13 mini - Updated!",
    "message": "it's not actually that good!",
    "userId": "c6e05954-1c2e-4f14-92e0-5827266b5a2e",
    "subredditId": "a811872e-ac82-4a7d-8432-25ff2b3d9300",
    "parentId": null
  }
}
```

## POST /subreddits

### Request:

```js
fetch(`${API}/subreddits`, {
  method: "POST",
  body: JSON.stringify({
    name: "programminghumor",
  }),
});
```

### Response:

```js
{
  "success": true,
  "subreddit": {
    "id": "971df805-0536-4339-b572-6d1096260c34",
    "name": "programminghumor",
    "userId": "c6e05954-1c2e-4f14-92e0-5827266b5a2e"
  }
}
```

## POST /votes

### Request:

```js
fetch(`${API}/votes`, {
  method: "POST",
  body: JSON.stringify({
    postId: "11e3e2e3-cbc2-43ac-a27a-6e8249cd0b5a",
    isUpvote: true,
  }),
});
```

### Response:

```js
{
  "success": true,
  "vote": {
    "id": "76c01611-6b6c-43a3-bc39-b10abe21c3f2",
    "userId": "c6e05954-1c2e-4f14-92e0-5827266b5a2e",
    "postId": "11e3e2e3-cbc2-43ac-a27a-6e8249cd0b5a",
    "isUpvote": true
  }
}
```
