# Architecture

## Code LInks

```
https://github.com/ta-dachi/hpd-backend - holds the code for the backend of hpd
https://github.com/ta-dachi/hpd-frontend - Holds the code for the frontend of hpd
https://github.com/ta-dachi/hpd-docs - Holds the docs and has a writeup on it
````

## Demo URLs

```
hpd demo:

https://master.d22ijxb4vxc8i3.amplifyapp.com/login
```

## Writeup / Presentation

- It was a fun software assignment.
- Software (hpd) is split between *frontend* and *backend*.
  - Allows for developers that have stronger backend skills to focus on backend and vice versa.
  - Fullstack devs can seamlessly switch between the two while developing.
- **Frontend**
  - Chose Vue3, TypeORM, without previous experience with those tech.
    - Worked previously with Angular and React and wanted to see differences.
    - Overall pleasant experience. Impressed by the ease of reactivity using Ref.
    - Build is hosted on AWS Amplify. Hosting platform for full stack applications. 
    - Authentication was done with Cognito and AWS Amplify UI components. 
      - Able to get authentication implemented in hours versus days
- **Backend**
  - Chose serverless
    - Past experience with serverless
    - Can build endpoints fairly quickly
    - Is using TypeORM but decided to not use its ORM capabilities due to time constraints
      - Using only SQL
  - Chose AWS RDS using PostgresSQL to persist contacts
    - I have preference for mature (boring) tech
    - hand wrote the sql. code is in *hpd-backend*
- **Problems and Thoughts**
  - Time spent more on frontend as was not familiar with Vue and TypeORM
  - Schema was missing some contact fields email
  - Decided to add a contact_number_default field to match the wireframe
  - Did not have time to make the UI pretty 
  - Did not have time to improve UI/UX (User experience)
  - Prioritized functionality
    - Reasoned another developer can be brought up to focus on the UI/UX
  - Was not able to write tests due to time



## Technologies Used

#### Backend
- Typescript
- TypeORM (https://typeorm.io/)
- AWS RDS PostgresSQL (https://aws.amazon.com/rds/postgresql/)
- Serverless (https://www.serverless.com/)
- Cognito (https://aws.amazon.com/cognito/)

#### Frontend
- Typescript
- Vue v3 (https://vuejs.org/)
- Nuxt (https://nuxtjs.org/docs/get-started/installation/)
- Tailwind (https://tailwindcss.com/)
- AWS Amplify (https://docs.amplify.aws/start/getting-started/installation/q/integration/react/#option-2-follow-the-instructions)


## "Low Hanging Fruit" Tasks
- Format phone numbers 1234567890 to (123) 456-7890
- Sortable contacts, names, numbers
- Minor UI and styling improvements
- Add warning before allowing destructive events e.g remove
- Show Created/Updated on timestamps in correct timezone
- Add popups, snackbars to show successful add/edit/deletions
- Change contact number type from textboxes to selectboxes (Cell, Work, Home, etc)

## High Priority Tasks
- Router guards for authenticated routes
- Unit Tests for certain endpoints and Integration tests for important workflows
- Improve upon *is_default* boolean. There could be multiple numbers that are set *is_default* to *true*.
- MFA (Multi-factored Authentication). Cognito supports this.
- Go beyond just contacts
- Export Contacts
- Database redundancy and backups