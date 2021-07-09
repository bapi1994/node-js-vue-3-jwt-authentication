# Vue 3 Authentication with JWT, Vuex and Vue Router

## Flow for User Registration and User Login

![vue-3-authentication-jwt-example-flow](vue-3-authentication-jwt-example-flow.png)


## Note:
Open `src/services/auth-header.js` and modify `return` statement for appropriate back-end.

```js
export default function authHeader() {
  let user = JSON.parse(localStorage.getItem('user'));

  if (user && user.accessToken) {
    return { Authorization: 'Bearer ' + user.accessToken }; // for Spring Boot back-end
    // return { 'x-access-token': user.accessToken };       // for Node.js Express back-end
  } else {
    return {};
  }
}
```


## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
