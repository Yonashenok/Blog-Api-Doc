# Blog API Documentation

## Description

This will allow your api to be used in retrieves a list of all user posts,get all the comments for give post, create a comments for post, for example, a mobile app or a CLI application.

## Table of Contents

- [Authentication](#authentication)
- [Endpoints](#endpoints)
  - [GET /api/v1/users/user_id/posts](#get-users)
  - [GET /api/v1/users/user_id/posts/post_id/comments](#get-usersidb)
  - [POST /api/v1/users/user_id/posts/post_id/comments](#post-users)

## Endpoints

### GET /api/v1/users/user_id/posts

This endpoint retrieves a list of all user posts.

#### Request

```
http://localhost:3000/api/v1/users/2/posts
```

#### Response

```
{
  "success": true,
  "data": [
    {
      "id": 9,
      "title": "rails is awesome",
      "text": "the first post ever",
      "bio": null,
      "comments_counter": 0,
      "likes_counter": 0,
      "created_at": "2023-10-11T15:18:32.105Z",
      "updated_at": "2023-10-11T15:18:32.105Z",
      "author_id": 2,
      "user": {
        "id": 2,
        "name": "foo ",
        "photo": "https://picsum.photos/id/64/200",
        "bio": "Techer from poland",
        "post_counter": 0,
        "created_at": "2023-10-10T14:53:37.645Z",
        "updated_at": "2023-10-10T15:53:07.940Z",
        "email": "foo24@gamil.com",
        "role": "user"
      },
      "comments": [
        {
          "id": 12,
          "text": "i love this post",
          "created_at": "2023-10-12T04:34:59.392Z",
          "updated_at": "2023-10-12T04:34:59.392Z",
          "user_id": 2,
          "post_id": 9
        }
      ]
    }
  ]
}

```

### GET /api/v1/users/user_id/posts/post_id/comments

This endpoint get all the comments for give post.

#### Request

```
http://localhost:3000/api/v1/users/2/posts/11/comments
```

#### Response

```
{
  "success": true,
  "data": [
    {
      "id": 14,
      "text": "testing comment",
      "created_at": "2023-10-12T06:12:04.159Z",
      "updated_at": "2023-10-12T06:12:04.159Z",
      "user_id": 2,
      "post_id": 11,
      "user": {
        "id": 2,
        "name": "foo ",
        "photo": "https://picsum.photos/id/64/200",
        "bio": "Techer from poland",
        "post_counter": 0,
        "created_at": "2023-10-10T14:53:37.645Z",
        "updated_at": "2023-10-10T15:53:07.940Z",
        "email": "foo24@gamil.com",
        "role": "user"
      }
    }
  ]
}
```

### POST /api/v1/users/user_id/posts/post_id/comments

This endpoint create a comments for post.

#### Request

```
http://localhost:3000/api/v1/users/2/posts/11/comments
```

#### Response

```
{
  "success": true,
  "data": [
    {
      "id": 15,
      "text": "testing comment",
      "created_at": "2023-10-12T06:12:04.159Z",
      "updated_at": "2023-10-12T06:12:04.159Z",
      "user_id": 2,
      "post_id": 11,
      "user": {
        "id": 2,
        "name": "foo ",
        "photo": "https://picsum.photos/id/64/200",
        "bio": "Techer from poland",
        "post_counter": 0,
        "created_at": "2023-10-10T14:53:37.645Z",
        "updated_at": "2023-10-10T15:53:07.940Z",
        "email": "foo24@gamil.com",
        "role": "user"
      }
    }
  ]
}
```
