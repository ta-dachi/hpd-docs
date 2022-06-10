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
  - Improve ability to comprehend code because both backend and frontend is in one language: JS/TS
- **Frontend**
  - Chose Vue3 without previous experience with those tech.
    - Worked previously with Angular and React and wanted to see differences.
    - Overall pleasant experience. Impressed by the ease of reactivity using Ref.
    - Global state management through *pinia* was straightfoward.
    - Build is hosted on AWS Amplify. Hosting platform for full stack applications. 
    - Authentication was done with Cognito and AWS Amplify UI components. 
      - Able to get authentication implemented in hours versus days.
      - Can support MFA, Email Verification, SMS, Federated Login (Google, FB, Apple)
- **Backend**.
  - Chose serverless, A framework that makes working with and writing AWS lambdas easier
    - Benefits of lambdas are:
      - No servers to manage
      - Inexpensive for certain workloads and scenarios
    - Past experience with serverless.
    - Can build endpoints fairly quickly.
    - Is using TypeORM but decided to not use its ORM capabilities due to time constraints.
      - Using only SQL.
  - Chose AWS RDS using PostgresSQL to persist contacts.
    - I have preference for mature (boring) tech.
    - Wrote the sql. Code is in *hpd-backend*.
- **Problems and Thoughts**
  - Time spent more on frontend as was not familiar with Vue.
  - Schema was missing some contact fields email.
    - Reasoned email is a often used alternative to calling.
  - Decided to add a contact_number_default field to match the wireframe.
    - Reasoned that a default way to contact someone will reduce time trying to reach the person.
  - Did not have time to make the UI pretty.
  - Did not have time to improve UI/UX (User experience).
  - Prioritized functionality.
  - Was not able to write tests due to time.
  - Was not able to write better validation on the frontend.
    - particularly for phone numbers and email.
    - related to my inexperience with Vue3.



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
- MFA (Multi-factored Authentication). Cognito supports this.
- Go beyond just contacts
- Export Contacts
- Database redundancy and backups