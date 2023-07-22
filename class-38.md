# Class 38 - React II

## How does lifting state up in a React application help with managing data flow and what are the benefits of using this approach?

Sometimes, you want the state of two components to always change together. To do it, remove state from both of them, move it to their closest common parent, and then pass it down to them via props. This is known as lifting state up, and it’s one of the most common things you will do writing React code.

The main benefit of this approach is that you can share the state between several components. This way, you can make sure that the state of all components is always in sync.

## Explain the concept of conditional rendering in React and provide an example of how to implement it in a component

Your components will often need to display different things depending on different conditions. In React, you can conditionally render JSX using JavaScript syntax like if statements, &&, and ? : operators.

```JS
function UserGreeting(props) {
  return <h1>Welcome back!</h1>;
}

function GuestGreeting(props) {
  return <h1>Please sign up.</h1>;
}

function Greeting(props) {
  const isLoggedIn = props.isLoggedIn;
  if (isLoggedIn) {
    return <UserGreeting />;
  }
  return <GuestGreeting />;
}
```

in this example, we have a function that takes a prop called isLoggedIn, and if it's true, it will return the UserGreeting component, and if it's false, it will return the GuestGreeting component.

## What are the main principles behind “Thinking in React” and how do they guide the process of designing and building a React application?

The main principles behind “Thinking in React” are:

- Start With A Mock:

    Imagine that you already have a JSON API and a mockup from a designer.
- Break the UI into a component hierarchy

    The first thing you’ll want to do is to draw boxes around every component (and subcomponent) in the mock and give them all names.

- Build a static version in React

    The easiest way is to build a version that takes your data model and renders the UI but has no interactivity.
- Find the minimal but complete representation of UI state

    To make your UI interactive, you need to be able to trigger changes to your underlying data model. React achieves this with state.
- Identify where your state should live

    React is all about one-way data flow down the component hierarchy. It may not be immediately clear which component should own what state.
- Add inverse data flow

    React doesn’t require a special API to implement this. Components can simply pass callbacks as props to child components, and child components can call those functions directly.
