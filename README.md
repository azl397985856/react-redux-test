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
 
> cause react is data driven, so why not testing your apps by testing the data?

# Unit Test
I beliveve all of you heard of test pyramid. if not, see : [TestPyramid -by Martin Fowler](https://martinfowler.com/bliki/TestPyramid.html). So unit test is quiet important.

# E2E test
since all the unit tests passed and the coverage high enough, probably the 70% of the mistakes can be prevented.
so to make better apps, we should also design and pass E2E test. 

consider that:

```
var a = 0;
function A() {
   a++;
   ...
   return a ;
}

function B() {
   a++;
   ...
   return a;
}

```
A and B can work fine separately. but what if they interact with each other. 
see also : [You Don't Know JS: Async & Performance](https://github.com/getify/You-Dont-Know-JS/blob/master/async%20%26%20performance/ch1.md)

# Reference

[jest](http://facebook.github.io/jest/)

[enzyme](http://airbnb.io/enzyme/)

[enzyme-to-json](https://github.com/adriantoine/enzyme-to-json)

[ant design 测试的发展历程](https://my.oschina.net/wanjubang/blog/1503597)

[react test utilities](https://facebook.github.io/react/docs/test-utils.html#findrendereddomcomponentwithtag)
