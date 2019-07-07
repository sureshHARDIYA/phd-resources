## [`ReactJS`](https://reactjs.org/)

ReactJS is a component-based JavaScript library that follows the declarative programming paradigm. The declarative views can be utilized to create complex interactive UI which serves as the presentational component of the web[[1]](#1). The library is easy to learn, promotes code reusability, offers lightweight DOM for better performance, enforces unidirectional data flow, ensures Search Engine Optimizations (SEO), forms the views of Model View Controller(MVC) architecture and supports virtual DOM.

## `Redux`

With the great prevalence of web applications and companies transforming from traditional desktop-based systems to web-based systems, there are now a multitude of opportunities on the World Wide Web. There are various programming languages for server-side scripting (SSR), client-side scripting, presentation logic (HTML and CSS), and query languages. JavaScript is one of the most popular languages on the web, and it encompasses several frameworks that assist in its development, compilation, and production. React is one of the most popular JavaScript frameworks, and it is developed and distributed by Facebook. While React helps in building highly sophisticated, interactive user interfaces, Redux, on the other hand, is getting very popular in the frontend community for state management [[2]](#2).

## `Redux Saga`

`Redux-saga` is a third-party JavaScript library that helps to easily and efficiently manage an application's side effects, including asynchronous activities such as fetching data and accessing browser cache. Mukhiya and Hung outline the essential importance of using redux-saga in a web application [[3]](#3). We can use the image used in this paper as a reference to better understand the need for redux-saga. To explain it in one sentence, we can say that redux-saga is responsible for handling side effects. Saga uses [ES6 Generators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function*) to make asynchronous flows easy to read, write, and test. If you are not familiar with generators, it would be best to pause before the next section and read up on them. Here is a couple of [suggested articles:](https://redux-saga.js.org/docs/ExternalResources.html).

## `Immutable JS`

The home page for immutable JS briefs the merits of using the library. However, it is a bit difficult to understand. In this section, we will explain the importance of immutable JS in simple terms. The use of Immutable JS is a hot topic of discussion in the frontend community. A couple of important aspects of immutability are that it increases predictability and performance and allows for mutation tracking. In addition to that, immutable JS provides a convenient way to modify deeply nested properties. Let us explore two problems it solves. The examples is taken from [[2]](#2).

### The data reference problem

A lot of bloggers and developers seem to accuse Immutable JS of certain things, without understanding its core concepts. React is not just about building interactive UI/UX interfaces; it is about performance. The purpose of its development was to be performant and to only update the DOM when required, and also, to only update the portion that was required to be updated. An optimized React app should contain simple, stateless functional components, and can have a `shouldComponentUpdate` that returns `false`:

```
shouldComponentUpdate(nextProps, nextState) {
   return false;
}
```

You should be familiar with React life cycle functions. The most notable function in the React component life cycle is shouldComponentUpdate, and it is expected to return false whenever possible. Why? Well, as the name suggests, this ensures that the component, with `shouldComponentUpdate` returning `false`, will never re-render, making the `React` app extremely performant.

Our primary goal should be to compare old props and states with new props and states; if they are not changed, the component should never re-render. However, remember that in `JavaScript`, equality checks can be sophisticated. Consider the equality in primary data types:

```
33 === 33
'yoshimi' === 'yoshmi'
false === false
```

Let's look at the equality in complex objects and arrays, as follows:

```
const object1 = { prop: ‘simpleValue’ };
const object2 = { prop: ‘simpleValue’ };
console.log(object1 === object2);   // false
```

The `object1` and `object2` appear to be the same, but their references are different. As these two objects are judged to be different, equaling them within the `shouldComponentUpdate` function naively will make our component needlessly re-render. Data comes from Redux reducers. If these reducers are not set correctly, they will be presented with different references, which will cause the component to re-render every time. This is one of the major problems with respect to performance.

### Reference handling

When we start to work on a real application, sooner or later, we come across deeply nested objects. We assume that there is a need to compare the objects with the previous values. One way to achieve this is to loop through each object recursively. We can imagine that this computation will be expensive and will require another solution.

Another way to solve this is by inspecting the reference. However, this requires us to preserve the reference if nothing has changed, and to also change the reference if any of the nested object/array prop values have changed. This task is very complicated. Although there are some libraries that help in deep comparing the objects, if we want to do it in a clean, optimized way, immutable JS is our solution. Facebook developers faced these obstacles in the very early stages of development, and hence, they developed immutable JS to overcome the issues.

## `GraphQL`

- [How does `GraphQL` work?](https://skmukhiya.netlify.com/how-does-graphql-work/)
- [How is `GraphQL` queries validated and executed?]

## `Redux-Form`

[`Redux-Form`](https://github.com/erikras/redux-form) is one of most popular libraries for creating form-based solutions for `react/redux` based web-applications. The need of `react/redux` has been justified in above section. In this section, we are going to justify the need of `redux-form` in our application. The main reason to use `redux-form` is, it allows to keep form data in the sate. Having said that, it raises another question - why do we need to store the form data in the state?

### Why do we need to store form data in the state?

React follows unidirectional data flow, which basically means the data (the component state or application state if you are using a state manager like Redux) flows down the component tree and events on the UI that changes this data will update only the part of the UI that is under the data source. With that React was the first library to be able to easily render a UI that just represents a group of data that is not actually in the DOM, and that brings up another concept, called `controlled components`. Now, another question, what is `controlled components?`

Controlled components are just HTML inputs that always receive its value as a property. It also receives an event handler that will update the state when the user interacts with it.

```
const ControlledInput = ({ value, eventHandler }) => (
 <input value={value} onChange={eventHandler} />
)
```
It means that when the user types the letter "P" on the input, what is visible is not the same "P", it may be an identical "P" that comes from the state, or whatever the event handler has put in there. By having all the application state in the JavaScript app and using controlled components we get a single source of truth and take full control over the application behavior.

In the context of a form, our React component is able to:

- do instant validation;
- control the input value format;
- enable, disable, show or hide components given the state;
- handle dynamic inputs.

Now that is known why to keep the form data in the state and the reason if that makes sense for an application we can come back to our main subject. Given that the application uses `React` and `Redux` there are two main options:

- implements for each field an event handler that dispatches an action creators, and the reducer that will receive the action, all the redux stuff.
- we could use a library that does all this work for us.

`Redux-Form` is a great option to do that job to you. It keeps track of all common application form state such as:

- The fields that are in the form
- The values of each field
- The focused field
- If the field values are valid
- The fields that the user have interacted with
- If the form is being submitted
- If is happening any `asynchronous validation

## `mongoDB`

## `Ant Design Pro`

## Reference

1. Redux Quick Start Guide: A Beginner's Guide to Managing App State with Redux, James Lee, Tao Wei, Suresh Kumar Mukhiya, Packt Publishing, Feb 28, 2019
