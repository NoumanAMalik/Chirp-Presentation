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
- Frontend and Framework: Next.js and JavaScript
- CSS: TailWindCSS
- Component Library: Daisy UI
- Backend: Supabase, which has a Postgres SQL database
- API: Supabase Javascript Client
- User Authentication: Clerk dev, which is a full solution for User Management
- Hosting: Vercel

### Challenges
- First challange I faced, was with Supabase.
   - The reason I first chose Supabase, is because it offers both, a database and authentication in a single package.
   - So, I thought it would be easier to use. But I was wrong. I kept facing issues where Supabase wouldn't store the users current session.
   - Which meant, that when a user reloaded the page, they would need to login again.
   - Because of this, I switched to Clerk dev, which takes care of the session management, allowing the user to reload the page without needing to authenticate again.

![100k calls](/supabaseDatabase.png)
- Another issue I had was dealing with state and useEffect when trying to load messages from the database.
   - I had a problem where the result of the database call was a Promise, and I would save that as React State.
   - But, if you save a Promise to React State it would never resolve. So, I had a useEffect that would run on every render of the page, and I would save all the messages in another state.
   - This would then create an infinite loop that I didn't notice was happening, where the useEffect would get all the messages, then update the state, which causes a re-render, which would then call the useEffect again, and this would infinitely loop.

### Future Work
- Make the website look nicer to improve the overall feel
- Have a search to find users based on their username or name attached to their profile
- Incorporate private messages
- Add in a subscription service that is available to subscribe to users with special benefits depending on the user.


### Therefore
- Chirp as a platform is in the very early stages but has unlimited potential. With the ground being set and the start coming together the way it did we think chirp can go as far as we take it.

Thank you for your attention.
