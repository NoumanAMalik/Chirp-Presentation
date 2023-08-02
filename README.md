# Chirp Presentation
## By Nouman and Danny

### App and Features
 - This is our attempt at remaking twitter
 - Features include:
    - User Authentication: With email and password
    - Choosing a username
    - Seeing all the tweets on the timeline
    - Adding a post to the timeline

### Programming Languages and Technologies
- For the framework we are using Next.js and JavaScript
- The styling and css is from TailwindCSS and a component library, Daisy UI
- The backend database is a Postgres database hosted by Supabase
- Then to communicate with the database, we are using the Supabase JavaScipt API Client
- For User Authentication and Session Management, we are using Clerk dev. Clerk is an all in one solution for User Management, and they give a good free teir that we are utilizing
- And finally, the web app is hosted on Vercel

### Challenges
- First challange I faced, was with Supabase. The reason I first chose Supabase, is because it offers both, a database and authentication in a single package. So, I thought it would be easier to use. But I was wrong. I kept facing issues where Supabase wouldn't store the uses current session.
