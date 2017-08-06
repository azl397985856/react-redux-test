# Intro 
best-practice for project which using react as view layer and redux as state manager.

# Motivation
the ideal is that I can represent the condition by the snapshoot collect by anything whatever. for eample, I have a collector
which is quite simple:

```js
window.onerror = errorMsg => {
   fetch('xxxxx/logs/error', {
    body: {
      state: window.store.getState(),
      errorMsg
    }
   })
}

```

developers could represent the condition merely by "importing" the state colleted by the colletor. And enjoy 
debugging at localhost.

seems nothing to do with testing? yeah...  plz be more patient.

thinking about what makes the ideal come true. yeah, **data driven**  just like many tools
support importing and exporting their config.

so we can merely testing the state, if the state is correct ,we can conclude that
the apps work well, otherwise fail.  I call it **state orented test**
 
