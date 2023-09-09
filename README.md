# Reddit API Documentation

`const API = "https://reddit-backend-w8g7.onrender.com"`

## GET /messages

### Request:

```js
fetch(`${API}/messages`);
```

### Response:

```js
{
  "success": true,
  "messages": [
    {
      "id": "22f146a7-9ccd-4be0-8aa4-79f18c09747b",
      "createdAt": "2023-09-04T19:31:27.794Z",
      "text": "Cool!",
      "parentId": null,
      "likes": 0,
      "children": []
    },
    {
      "id": "52bc023a-69d6-41f3-a2ad-2c9a1c8b375d",
      "createdAt": "2023-09-04T20:47:58.973Z",
      "text": "Coding is cool!",
      "parentId": null,
      "likes": 0,
      "children": []
    },
    {
      "id": "74275b9a-9249-4719-aa43-3775ceacdd8a",
      "createdAt": "2023-09-04T19:32:00.492Z",
      "text": "sdf",
      "parentId": null,
      "likes": 1,
      "children": [
        {
          "id": "9fc343b0-2c21-4f50-afe8-4760c8678aa5",
          "createdAt": "2023-09-04T19:32:04.118Z",
          "text": "wer",
          "parentId": "74275b9a-9249-4719-aa43-3775ceacdd8a",
          "likes": 2,
          "children": []
        }
      ]
    }
  ]
}
```

## POST /messages

### Request:

```js
fetch(`${API}/messages`, {
  method: "POST",
  headers: {
    "Content-Type": "application/json",
  },
  body: JSON.stringify({
    text: "hello back!",
    parentId: "9760cfca-b8ce-4aed-b0d8-b8fdf7be3c62", // optional field
  }),
});
```

### Response:

```js
{
  "success": true,
  "message": {
    "id": "28006818-1695-4984-83e9-bf0e6a864e08",
    "createdAt": "2023-09-05T12:56:22.642Z",
    "text": "hello back!",
    "parentId": "9760cfca-b8ce-4aed-b0d8-b8fdf7be3c62",
    "likes": 0
  }
}
```

## PUT /messages/:messageId

### Request:

```js
fetch(`${API}/messages/28006818-1695-4984-83e9-bf0e6a864e08`, {
  method: "PUT",
  headers: {
    "Content-Type": "application/json",
  },
  body: JSON.stringify({
    text: "HELLO BACK!", // optional field
    likes: 10, // optional field
  }),
});
```

### Response:

```js
{
  "success": true,
  "message": {
    "id": "28006818-1695-4984-83e9-bf0e6a864e08",
    "createdAt": "2023-09-05T12:56:22.642Z",
    "text": "HELLO BACK!",
    "parentId": "9760cfca-b8ce-4aed-b0d8-b8fdf7be3c62",
    "likes": 10
  }
}
```

## DELETE /messages/:messageId

### Request:

```js
fetch(`${API}/messages/28006818-1695-4984-83e9-bf0e6a864e08`, {
  method: "DELETE",
});
```

### Response:

```js
{
  "success": true,
  "message": {
    "id": "28006818-1695-4984-83e9-bf0e6a864e08",
    "createdAt": "2023-09-05T12:56:22.642Z",
    "text": "HELLO BACK!",
    "parentId": "9760cfca-b8ce-4aed-b0d8-b8fdf7be3c62",
    "likes": 10
  }
}
```
