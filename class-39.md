# Class 38 - React III

## What is React Context, and how does it help in managing state and data sharing in a React application?

React context allows us to pass down and use (consume) data in whatever component we need in our React app without using props.

In other words, React context allows us to share data (state) across our components more easily.

React context is great when you are passing data that can be used in any component in your application.

## Explain the useContext Hook and how it can be used to access data from a React Context within a functional component

The `useContext` hook allows us to consume data from a React context within a functional component.

- Create context using the createContext method.

    ```javascript
    const MyContext = React.createContext(defaultValue);
    ```

- Take your created context and wrap the context provider around your component tree.

    ```javascript
    <MyContext.Provider value={/* some value */}>
        <MyComponent />
    </MyContext.Provider>
    ```

- Put any value you like on your context provider using the value prop.

    ```javascript
    <MyContext.Provider value={/* some value */}>
    ```

- Read that value within any component by using the context consumer.

    ```javascript
    <MyContext.Consumer>
        {value => /* render something based on the context value */}
    </MyContext.Consumer>
    ```

    or using the useContext hook.

    ```javascript
    const value = useContext(MyContext);
    ```

## Describe the purpose of Next.js, and provide an example from the Vercel Next.js Examples reading on how it can be used to build a scalable web application

Next.js handles the tooling and configuration needed for React, and provides additional structure, features, and optimizations for your application.

- Flexibility and Scalability: Next.js abstracts complexity while allowing rendering choices on a per-page basis, making it scalable as applications grow.

- Performance Optimizations: Next.js handles various performance optimizations like code splitting and caching, making it easier to ship high-performance applications to users.

- Great Developer Experience: Next.js offers features like React Fast Refresh, easy Webpack customization, built-in TypeScript support, and simplified asset handling, enhancing the developer experience.

- Versatile Deployment Options: Next.js can be deployed to various platforms, including Vercel, AWS, or self-hosted environments, with support for incremental adoption.

- Community: Next.js has an active and supportive community, with involvement from Google and React core team members, making it a widely adopted and trusted framework.

Example for creating a Next.js app with the rest template:

```bash
npx create-next-app --example api-routes-rest api-routes-rest-app
```
