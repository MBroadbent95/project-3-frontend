# Bootcamp Buddy

A full-stack MERN application where software engineering 
students share and discover peer advice. Built by a team 
of 3 in an 8-day sprint with full CRUD, JWT authentication, 
and role-based access for visitors vs. registered users.

🔗 [Live App](https://bootcamp-buddyv2.netlify.app) | 
[Frontend Repo](https://github.com/MBroadbent95/project-3-frontend) | 
[Backend Repo](https://github.com/MBroadbent95/project-3-backend)

![React](https://img.shields.io/badge/React-Frontend-blue)
![Node](https://img.shields.io/badge/Node-Express-green)
![MongoDB](https://img.shields.io/badge/MongoDB-Atlas-brightgreen)
![TypeScript](https://img.shields.io/badge/TypeScript-Typed-blue)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-Styled-teal)

Back end:
- Express
- Node
- Axios
- Bcrypt
- Jsonwebtoken
- Mongoose
- TypeScript
I have included snippets of what your package file should look like in. The first image is back end, and the second is front end:

![Back End package.lock](https://i.imgur.com/VfgSUg0.png)
![Front End package.lock](https://i.imgur.com/Y7OyTsK.png)


You will likely need to have your own mongodb database up and running, and then to seed the data in order to get this working as intended.
Once you have installed all necessary dependencies & mongodb is live, you will need to:
Back end, run seed. Then once seeded, run dev.
Front end, run dev.
If you have successfully completed my steps, you should have a working preview by this point.


Timeframe & Working Team (Solo/Pair/Group):

The timeframe for this project was just under 8 days if you include the weekend. I was in a 3 person group consisting of 2 ambitious and hard working teammates Conor Hamilton and Catherine Brett.Every morning we would have a meeting to discuss the plan of action for the day and who would do each task.



Technologies Used:

Back end:
TypeScript
Express
Node
Axios
Bcrypt
JsonWebToken
Mongoose
Mongoose-Hidden
Mongoose-Unique-Validator

Front end:
HTML
TailwindCSS
Vite
Font Awesome
Ionicons
Axios
React
React-dom
React-feather
React-router-dom
React-scripts
TypeScript


Development tools:
MongoDB
Netlify
Mongo Atlas
Google Chrome Dev Tools


## Technical Decisions

- **Separated frontend and backend repos** — decoupled 
  deployment allowed independent Netlify builds for each 
  service, making it easier to debug and redeploy without 
  affecting the other.
- **JWT authentication over session-based auth** — chose 
  stateless JWT tokens to keep the backend API clean and 
  scalable, with bcrypt handling password hashing on the 
  user model.
- **TailwindCSS over BulmaCSS** — deliberately adopted 
  an unfamiliar framework mid-project to demonstrate 
  adaptability; utility-first classes gave finer control 
  over layout and spacing than Bulma's component model.
- **Role-based UI rendering** — visitor vs. authenticated 
  user states handled in React, conditionally rendering 
  the "Give Advice" CTA and edit/delete controls based on 
  token presence and matching user ID.
- **File-level task splitting to avoid merge conflicts** — 
  team agreed upfront on component ownership so each 
  developer worked in separate files, with Slack 
  notifications before any shared file was touched.


Brief
Instructions:

* Work in a team, using **git to code collaboratively**.
* **Build a full-stack application** by making your own backend and your own front-end
* **Use an Express API with mongoose** to serve your data from a Mongo database
* **Consume your API with a separate front-end** built with React
* **Be a complete product** which most likely means multiple relationships and CRUD functionality for at least a couple of models
* **Implement thoughtful user stories/wireframes** that are significant enough to help you know which features are core MVP and which you can cut
* **Have a visually impressive design** to kick your portfolio up a notch and have something to wow future clients & employers. **ALLOW** time for this.
* **Be deployed online** so it's publicly accessible.


Planning:

Planning is essential in order to complete a task as potentially complex as this one.
We knew from the outset that the more time we spent in the beginning chiseling out exactly what we wanted, the path to achieving it would be more clear and easier to travel.
We devised comprehensive wire-frames for both the front and back end of the project using an app called Excalidraw, below is the FE wireframe preview:

![Front End WireFrame](https://i.imgur.com/FyznxnK.png)
Here is the backend wireframe preview:


![Back End WireFrame](https://i.imgur.com/wEzdFqZ.png)


Build/Code Process:

It was apparent that the best place to start for our full stack project would be the back end. Once everything is functional in the back end, the front end should be far easier to build when the data is visible.

Back End:
The basic formatting of backend into components, controllers and router was very useful for us. We started to divvy out who would be writing which components. This was an effective practice as we would avoid potential merge conflicts by staying clear of each other's files. Should we need to make adjustments, we would notify our team in slack with full details of the changes we made.
Once we had assembled our components, testing was necessary to make sure it all fit together correctly, firstly the dev in the driver’s seat would seed the mongodb database. It is unnecessary for all 3 of us to test independently at this point despite the fortified testing it would provide. 
We used an app called insomnia to test all possible requests to our back end including tips (our main dataset) and users.

![Back End Router](https://i.imgur.com/gRFFVa9.png)

Insomnia proved to be a very useful tool, after testing was complete and we were satisfied with the functional back end, we then pressed on to the front end.

Front end:
For the front end, we decided to use a new CSS framework technology TailwindCSS. This was an ambitious move chosen to display the ability to learn a new and industry recommended technology. Previously we had been using an alternative CSS framework - BulmaCSS.
TailwindCSS proved to be a far more useful tool in its application by the precision and multitude of options it provided when compared to BulmaCSS, we could simply do a whole lot more with TailwindCSS.
The only real downside to TailwindCSS besides the evident learning curve was how messy it would make your HTML look… a worthy sacrifice.

We knew what we wanted to achieve in the frontend thanks to our planning stage.
This would require a smooth user experience with each page presenting a defined purpose for the user and their interaction with the data and other users.
For this we would need a clean distinction between visitor and user.
The core of our website, Tips for fellow software travelers, would fail if we denied access to visitors.
So in essence visitors could:
View Advice
Search for advice based on their search criteria.
Connect with other user’s via their posted LinkedIn and GitHub links

Users can:
Do everything a visitor can
Post New Advice
Edit their posted advice
Delete their posted advice
Edit their account information

![Logged in Example](https://i.imgur.com/xTwfKIX.png)

Only when logged in does the option to give advice present itself.

A demo account is available on request, or feel free 
to register a new account directly on the live site.

If you navigate to the log-in page, much like other popular social media apps Instagram & Facebook, you can navigate to a new page to sign up if you don’t already have an account.
I am particularly proud of the error handling here because it is dynamic and responds with specific error messages in the commonly expected format. 
If you missed a required field or needed to adjust your password to contain particular characters, you would be prompted to do so.
Only when you have met the requirements would it let you sign up.

![Sign Up Error Handling](https://i.imgur.com/WgnViOc.png)

![User Controller](https://i.imgur.com/Ty1DX0q.png)

![Sign Up Front End](https://i.imgur.com/pWaKxhH.png)


The advice page is clean with a soothing color scheme:

![Advice Page Visual](https://i.imgur.com/LjjsDaZ.png)

A search bar is also available should you wish to filter the results, it can include any words mentioned throughout the advice from name to the advice content.

Should you click through to one specific advice card you will be taken to a dedicated page with details about the advice poster and links to their GitHub & LinkedIn if they provided them.
We wanted this experience to include the opportunity to connect and network for all users and visitors.



## Challenges

**Adapting project management mid-sprint** — we started 
with Trello but found it too static once development 
became fluid. We switched to a Slack-based standup model 
with scheduled merge parties, which reduced coordination 
overhead and let us respond faster to bugs as they emerged.

**URL-based authorisation gap** — a known issue where a 
direct URL could expose the edit page for any tip. We 
implemented server-side ID matching so the edit action 
itself is protected regardless of how the page is reached, 
though frontend route-guarding remains a planned improvement.





Wins:

I am usually a stickler for effective team cohesion through a rigid roadmap, but from this project I understood that it is possible to have greater task flexibility if it’s combined with good communication and reactivity between the team.

Sections of the code in which I am proud of include error handling as mentioned above. 
Another Win of mine has been the ability to read another teammate of mine’s code and figure out which adjustments I needed to make to code which was not my own in order to get my GitHub & LinkedIn buttons to work (they were unavailable when I encountered my problem).
Legible code is just as important as the ability to figure out what needs to be done.  
I am happy that I am able to contribute and work effectively as part of a team.



## Key Learnings

- Adopted TailwindCSS cold mid-project and shipped with 
  it — confirmed I can pick up new tooling under deadline 
  pressure without it blocking delivery.
- Learned that clear file ownership is more effective 
  than trying to coordinate edits to shared files — 
  something I'd formalise earlier on a future project.
- Reading and extending a teammate's code (the LinkedIn/
  GitHub button fix) reinforced why legible, consistent 
  code matters as much as correctness.



Bugs:

A bug we encountered and couldn’t find a fix for in time was related to the browser url bar.
More specifically, if you are specific with what you enter into the url bar, you can successfully navigate to the edit page of a specified piece of advice.
The way in which the edit function was crafted, was to navigate to a new page and edit the advice based on its id. Whilst we couldn’t figure out a way to block everyone except the creator of the advice from finding their way to the page if they really wanted to, they still cannot edit the advice unless their id matches the one registered on the tip.


## Roadmap

- [ ] Comments and likes system per advice post
- [ ] Saved/favourites list for logged-in users  
- [ ] Frontend route guards to prevent unauthorised 
      access to edit pages via direct URL
- [ ] Profile picture upload and expanded user profile
- [ ] Account deletion flow
