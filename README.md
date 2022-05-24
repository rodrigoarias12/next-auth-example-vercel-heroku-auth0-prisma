> The example repository is maintained from a [monorepo](https://github.com/nextauthjs/next-auth/tree/main/apps/example-nextjs). Pull Requests should be opened against [`nextauthjs/next-auth`](https://github.com/nextauthjs/next-auth).

<p align="center">
   <br/>
   <a href="https://next-auth.js.org" target="_blank"><img width="150px" src="https://next-auth.js.org/img/logo/logo-sm.png" /></a>
   <h3 align="center">NextAuth.js Vercel Auth0 Prisma ORM Heroku Example App</h3>
   <p align="center">
   Open Source. Full Stack. Own Your Data.
   </p>
</p>

## Overview

This fork to NextAuth.js is a complete open source authentication solution. This example uses the Auth0 provider , Heroku / Postgresql and sets roles in the prisma schema. 

This is an example application that shows how `next-auth` is applied to use these roles for authorization using jwt and session on the basic Next.js app.

The deployed version can be found at [`https://next-auth-example-vercel-heroku-auth0-prisma.vercel.app/`](https://next-auth-example-vercel-heroku-auth0-prisma.vercel.app/)
## Technologies

- Next.js(React)
- TypeScript
- Prisma
- NextAuth
- Auth0
- Postgresql 

### About NextAuth.js

NextAuth.js is an easy to implement, full-stack (client/server) open source authentication library originally designed for [Next.js](https://nextjs.org) and [Serverless](https://vercel.com). Our goal is to [support even more frameworks](https://github.com/nextauthjs/next-auth/issues/2294) in the future.

Go to [next-auth.js.org](https://next-auth.js.org) for more information and documentation.

> *NextAuth.js is not officially associated with Vercel or Next.js.*

## Getting Started

### 1. Clone the repository and install dependencies

```
git clone https://github.com/rodrigoarias12/next-auth-example-vercel-heroku-auth0-prisma.git
cd next-auth-example-vercel-heroku-auth0-prisma
npm install
```

### 2. Configure your local environment

Copy the .env.local.example file in this directory to .env (which will be ignored by Git):

```
cp .env.local.example .env
```

The next steps configure environment .env file

#### Database

A database is needed to persist user accounts and set roles for authorization users.

1-Create Account in Heroku and copy DATABASE_URL

2-Add details for Database in .env file
```
#DATABASE HEROKU
DATABASE_URL=
```
3-Push db in heroku
```
npx prisma db push
npx prisma generate
```

### 3. Configure Authentication Providers

1-Create account in Auth0

2-Add details for Auth0 from auth0 manager and complete the .env file

```
#Auth0
AUTH0_CLIENT_ID=
AUTH0_CLIENT_SECRET=
AUTH0_ISSUER_BASE_URL=
```

### 4. Start the application

To run your site locally, use:

```
npm run dev
```

To run it in production mode, use:

```
npm run build
npm run start
```

### 5. Preparing for Production with vercel
Deploying NextAuth.js only requires a few steps. First create an account in vercel and integrate with github. 
Then configure environment variables in the vercel dashboard.
Remember to configure your Auth0 config for callbacks. 


Follow the [Deployment documentation](https://next-auth.js.org/deployment)

## Acknowledgements

<a href="https://vercel.com?utm_source=nextauthjs&utm_campaign=oss">
<img width="170px" src="https://raw.githubusercontent.com/nextauthjs/next-auth/canary/www/static/img/powered-by-vercel.svg" alt="Powered By Vercel" />
</a>
<p align="left">Thanks to Vercel sponsoring this project by allowing it to be deployed for free for the entire NextAuth.js Team</p>

## License

ISC

