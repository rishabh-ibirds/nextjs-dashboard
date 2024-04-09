#### WIL

- css modules
- clsx library
- **FONT :**  Next.js automatically optimizes fonts in the application when you use the next/font module. It downloads font files at build time and hosts them with your other static assets. This means when a user visits your application, there are no additional network requests for fonts which would impact performance. (check app/ui/fonts.ts)
- **Image :** (import => import Image from 'next/image'). The <Image> Component is an extension of the HTML <img> tag, and comes with automatic image optimization.
- Routes
- **layout.tsx :** A wrapper that is applied to all pages accessed throught that route. A root layout.tsx is mandatory and is applied to all the pages of the site
- Link
- usePathName
- deploying to vercel
- connecting with postgres on vercel
- seeding data to postgres (created a script seed.js and added to scripts in package json to run via npm run seed)
- no need to use apis to fetch data from backend as the app behaves like server side component
- use of await to fetch data before rendering
- waterfall (await) vs parallel (Promise.all, Promise.allSettled) data fetching
- static vs dynamic rendering
- Streaming with chunks
- loading.tsx
- **Route Groups :** Route groups allow you to organize files into logical groups without affecting the URL path structure. When you create a new folder using parentheses (), the name won't be included in the URL path. So /dashboard/(overview)/page.tsx becomes /dashboard.
- using <Suspense> for streaming, partial prerendering 
- **defaultValue vs. value / Controlled vs. Uncontrolled**
If you're using state to manage the value of an input, you'd use the value attribute to make it a controlled component. This means React would manage the input's state. However, since you're not using state, you can use defaultValue. This means the native input will manage its own state. This is okay since you're saving the search query to the URL instead of state.
- **Page components accept a prop called [searchParams](https://nextjs.org/docs/app/api-reference/file-conventions/page)**
- if you want to read the params from the client, use the useSearchParams() hook as this avoids having to go back to the server. for server side componenets use searchParams as prop
- debouncing
- In React, you can use the action attribute in the < form > element to invoke actions. The action will automatically receive the native FormData object, containing the captured data.
<br><br>
In HTML, you'd pass a URL to the action attribute. This URL would be the destination where your form data should be submitted (usually an API endpoint). However, in React, the action attribute is considered a special prop - meaning React builds on top of it to allow actions to be invoked.
<br><br>
Behind the scenes, Server Actions create a POST API endpoint. This is why you don't need to create API endpoints manually when using Server Actions.
- Next.js has a Client-side Router Cache that stores the route segments in the user's browser for a time. Along with prefetching, this cache ensures that users can quickly navigate between routes while reducing the number of requests made to the server. If you want to clear this cache and trigger a new request to the server, you can do this with the ***revalidatePath***.
- **Dynamic Route :** You can create dynamic route segments by wrapping a folder's name in square brackets. For example, **[id], [post]** or **[slug]**.
- error handling with **error.tsx** and **notFound** hook
- **useFormState** hook takes two arguments: (action, initialState). Returns two values: [state, dispatch].<br>
```const [state, dispatch] = useFormState(createInvoice, initialState);```
- **auth.config.ts**
- adding metadata
- using layout.tsx to set metadata format across the app
