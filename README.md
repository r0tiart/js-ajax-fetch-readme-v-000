# JavaScript fetch()

## Objectives

1. Explain how to use `fetch()` in modern browsers
2. Describe the differences between `fetch()`, `jquery.ajax()` and `XMLHttpRequest`
3. Get data from a remote endpoint using `fetch()`

## Introduction

Basically, `fetch()` is awesome, and it has vastly simplified getting information on the web.

We can have students start with unauthenticated calls like

```javascript
fetch('https://reddit.com/r/aww/hot.json').
    then(res => res.json()).
    then(json => console.log(json))
```

Which is just about the coolest thing

If there's time (after the intro, getting them into the promise-like syntax, etc.), it might be worth having them sign up for a service and pass tokens in the `headers` part of the options, e.g.,

```javascript
fetch(`https://api.github.com/users/${username}`, { 
  headers: { 
    Authorization: 'token ${token}'
  }
}).then(res => res.json()).then(json => console.log(json))
```

As they'll be doing this with Twitter in the next lesson anyway

