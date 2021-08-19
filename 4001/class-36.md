## What are the advantages of storing tokens in “Cookies” vs “Local Storage”
Cookies are automatically saved, sent and removed by the browser. When doing browser level navigation, only cookies are sent. Sharing the same session across subdomains can easily be done with cookies. Cookies have a special flag called httpOnly, which means that malicious JS code cannot send the access token to the attacker.



## Explain 3rd party cookies.
[ref](https://cookie-script.com/all-you-need-to-know-about-third-party-cookies.html)
Third-party cookies are cookies that are set by a website other than the one you are currently on. For example, you can have a "Like" button on your website which will store a cookie on a visitor's computer, that cookie can later be accessed by Facebook to identify visitors and see which websites they visited



## How do pixel tags work?
[ref](https://en.ryte.com/wiki/Tracking_Pixel)
A tracking pixel (also called 1x1 pixel or pixel tag) is a graphic with dimensions of 1x1 pixels that is loaded when a user visits a webpage or opens an email. 
The website operator or sender of an email adds the tracking pixel using a code in the website’s HTML code or email. This code contains an external link to the pixel server. If a user visits the destination website, the HTML code is processed by the client – usually the user’s browser. The browser follows the link and opens the (invisible) graphic. This is registered and noted in the server’s log files.



## Term


### cookies
[ref](https://en.wikipedia.org/wiki/HTTP_cookie)
also called web cookies, Internet cookies, browser cookies, or simply cookies) are small blocks of data created by a web server while a user is browsing a website and placed on the user's computer or other device by the user’s web browser. Cookies are placed on the device used to access a website, and more than one cookie may be placed on a user’s device during a session.
Cookies serve useful and sometimes essential functions on the web.


### authorization
[ref](https://en.wikipedia.org/wiki/Authorization)
Authorization is the function of specifying access rights/privileges to resources, which is related to general information security and computer security, and to access control in particular.[1] More formally, "to authorize" is to define an access policy.




### access control
[ref](https://en.wikipedia.org/wiki/Network_Access_Control)
 Access Control (NAC) is a computer networking solution that uses a set of protocols to define and implement a policy that describes how to secure access to network nodes by devices when they initially attempt to access the network.[citation needed] NAC might integrate the automatic remediation process (fixing non-compliant nodes before allowing access) into the network systems, allowing the network infrastructure such as routers, switches and firewalls to work together with back office servers and end user computing equipment to ensure the information system is operating securely before interoperability is allowed. A basic form of NAC is the 802.1X standard.




## Redux

Redux is a predictable state container for JavaScript apps. It helps you write applications that behave consistently, run in different environments (client, server, and native), and are easy to test.

It provides a solid, stable, and mature solution to managing state in your React application. Through a handful of small, useful patterns, Redux can transform your application from a total mess of confusing and scattered state, into a delightfully organized, easy to understand modern JavaScript powerhouse.


### Testing redux reducers with Jest


Usually reducer consists of initial state and switch statement to handle every action.
Sometimes one switch/case may handle few actions, because the business logic is the same and outcome should be the same. Some example GET_POST and UPDATE_POST should update the same store and produce same outcome.
It’s important to test reducers. That’s where business logic should happen and where new application state is formed based on external (API) or internal response.


##### Boilerplate
it starts with boilerplate setup and writing empty tests just to outline what needs to be tested. I like to to test the initial state and then every switch/case in the reducer to see if action.payload will produce expected store.


```
import reducer from './getPostsReducer';
import * as types from '../actions/posts/getPostsReduxAction';
import expect from 'expect';

describe('team reducer', () => {
  it('should return the initial state');
  it('should handle GET_POST_SUCCESS');
  it('should handle UPDATE_POST_SUCCESS');
  it('should handle GET_POST_FAIL');
  it('should handle GET_POST_START');
});
```

#### Add tests and mock data
you can just start filling in the tests one by one. also can create mock files and store the API response at the time of testing. So you can test agains “real” data. This strategy uncovered few accidental API changes where the response was changed without any warning. Instead of blaming anyone, we can just look at the mock data and see what’s expected on the front end.

```
import reducer from './getPostReducer';
import * as actions from '../actions/posts/getPost';
import { UPDATE_POST_SUCCESS } from '../actions/posts/updatePost';
import expect from 'expect';
import getPostMock from '../mocks/getPostMock';

describe('post reducer', () => {
  it('should return the initial state', () => {
    expect(reducer(undefined, {})).toEqual({});
  });

  it('should handle GET_POST_START', () => {
    const startAction = {
      type: actions.GET_POST_START
    };
    // it's empty on purpose because it's just starting to fetch posts
    expect(reducer({}, startAction)).toEqual({});
  });

  it('should handle GET_POST_SUCCESS', () => {
    const successAction = {
      type: actions.GET_POST_SUCCESS,
      post: getPostMock.data, // important to pass correct payload, that's what the tests are for ;)
    };
    expect(reducer({}, successAction)).toEqual(getPostMock.data);
  });

  it('should handle UPDATE_POST_SUCCESS', () => {
    const updateAction = {
      type: UPDATE_POST_SUCCESS,
      post: getPostMock.data,
    };
    expect(reducer({}, updateAction)).toEqual(getPostMock.data);
  });

  it('should handle GET_POST_FAIL', () => {
    const failAction = {
      type: actions.GET_POST_FAIL,
      error: { success: false },
    };
    expect(reducer({}, failAction)).toEqual({ error: { success: false } });
  });
});
```



