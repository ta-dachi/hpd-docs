# Architecture

## Demo URLs

```
https://master.d22ijxb4vxc8i3.amplifyapp.com
```

## Writeup

- Software is split between *frontend* and *backend*
  - Allows for developers that have stronger backend skills to focus on backend and vice versa
  - 


## Technologies Used

#### Backend
- Typescript
- TypeORM (https://typeorm.io/)
- AWS RDS for PostgresSQL (https://aws.amazon.com/rds/postgresql/)
- Serverless (https://www.serverless.com/)
- Cognito (https://aws.amazon.com/cognito/)

#### Frontend
- Typescript
- Vue v3 (https://vuejs.org/)
- Nuxt (https://nuxtjs.org/docs/get-started/installation/)
- Tailwind (https://tailwindcss.com/)
- AWS Amplify (https://docs.amplify.aws/start/getting-started/installation/q/integration/react/#option-2-follow-the-instructions)

## Possible Improvements
- Stronger password validation > 8 char minimum.
- Email Verification.
- MFA (Multi-factored Authentication). Cognito supports this.