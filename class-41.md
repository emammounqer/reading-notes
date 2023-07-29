# Class 41 - React IV

## Explain the concept of dynamic routes in Next.js and how they differ from static routes

The dynamic routes are used to render the same page with different data, for example, if you have a page that shows a product, you can use the dynamic routes to show different products, and the dynamic routes are used to create the pages for the products, and the static routes are used to create the pages that are not dynamic, like the about page, or the contact us page.

## Describe the process of deploying a Next.js application. What are the key steps involved, and what are some deployment platforms you can use?

- Create a Next.js app
- Push to GitHub
- The easiest way to deploy Next.js to production is to use the Vercel platform
  - Deploy to Vercel
  - Create a Vercel account
  - Import your GitHub project
  - You’ll need to Install Vercel for GitHub. You can give it access to All Repositories.
Once you’ve installed Vercel, import nextjs-blog.

Next.js can be deployed to any hosting provider that supports Node.js. , some deployment platforms are:

- Vercel
- Netlify
- Heroku

## How does Next.js handle static file serving? Discuss the default folder structure for storing static assets and explain how to reference them in a Next.js application

Next.js can serve static files, like images, under a folder called public in the root directory. Files inside public can then be referenced by your code starting from the base URL (/).

For example, if you add an image to public/my-image.png, the following code will access the image:

```js
function MyImage() {
  return <img src="/my-image.png" alt="my image" />
}

export default MyImage
```
