Create an app with the following items:

1. Create an endpoint called `/random-users` that returns random users from this endpoint `https://randomuser.me/api?results=10`.

2. Create an endpoint called `/users`, this should support the following methods:

- POST: create a new user and save it in a database / in-memory / wherever you want.
- GET: return the saved users mixed with random users from the first endpoint.
- DELETE: delete a previously created user

For both tasks:

- Create a commit once you finish adding a new endpoint. Write meaningful commit messages.
- Code should be properly formatted.
- Endpoints should return meaningful error messages where needed.
- You can use any framework to create the app.
- Use only the users with a truthy `id.value` from the randomuser API.
- The returned users should follow this schema/type:

```typescript
type User = {
  id: string;
  firstName: string;
  lastName: string;
  email: string;
  phoneNumber: string;
  picture: string;
};
```

Example:

```json
[
  {
    "id": "3225415T",
    "firstName": "Christina",
    "lastName": "Campbell",
    "email": "christina.campbell@example.com",
    "phoneNumber": "081-309-3369",
    "picture": "https://randomuser.me/api/portraits/women/91.jpg"
  },
  {
    "id": "604502907",
    "firstName": "Yasemin",
    "lastName": "Taşçı",
    "email": "yasemin.tasci@example.com",
    "phoneNumber": "0490-974-187",
    "picture": "https://randomuser.me/api/portraits/men/33.jpg"
  }
]
```
