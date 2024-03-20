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
