# help-desk (hpd)

## Demo URLs

```
https://master.d22ijxb4vxc8i3.amplifyapp.com
```

## Frontend Quickstart

Source for the frontend can be found here: https://github.com/ta-dachi/hpd-frontend

```
cd frontend
npm install
...
...
npm run dev
````

## Backend Quickstart

#### Test Endpoints locally

Source for the frontend can be found here: https://github.com/ta-dachi/hpd-backend

```
serverless offline
OR
npx serverless offline
...
...
...
Offline [http for lambda] listening on http://localhost:3002
Function names exposed for local invocation by aws-sdk:
           * hello: backend-dev-hello
           * add_employee: backend-dev-add_employee

   ┌────────────────────────────────────────────────────────────────────────────────┐
   │                                                                                │
   │   POST | http://localhost:3000/dev/hello                                       │
   │   POST | http://localhost:3000/2015-03-31/functions/hello/invocations          │
   │   POST | http://localhost:3000/dev/add_employee                                │
   │   POST | http://localhost:3000/2015-03-31/functions/add_employee/invocations   │
   │                                                                                │
```

## Gotchas

#### Redirects for single page web apps (SPA)

See https://docs.aws.amazon.com/amplify/latest/userguide/redirects.html

