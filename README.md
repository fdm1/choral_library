# Choral library

An attempt to create a lightweight and free sveltekit choral library site. Server will be some free service. Database will be sqlite, either locally stored, or in google drive.

Any CRUD actions on the db will fetch the sqlite file, update it, and replace it where it lives.

### Developing

```bash
yarn run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

### References
- [Auth setup](https://medium.com/@uriser/authentication-in-sveltekit-with-auth-js-7ff505d584c4)
