There are a small number of bugs in this codebase. Nothing prevents it from running, it just runs incorrectly.
You will have to compare the behavior to the spec below to catch errors. 

Please make one commit for each error you fix, then submit a single PR at the end with an explanation of what you did.

# Spec
## Frontend
- The homepage shows a list of workouts. They should have green headers per entry.
- Each entry shown should have the number of reps and the weight in kg. Make sure these numbers match the values in the database.
- The page should not be blank. I'm telling you now that you will see a blank page when you start, and I'll give you a hint-- it's because of a syntax mistake between App.jsx and Home.jsx. I'll give you another hint-- what is different between how I imported Navbar and Home?
- The home page should render as a grid, not a list. Hint: There is a very small syntax error causing this.

## Backend
- The list of all workouts should be sorted with the newest entry first.
- Updating a workout should update all fields with the new information.

# Setup
Regardless of your team, you will need to setup both to be able to test. You will need to have Node 20 or newer installed on your computer to use the npm commands.

## Backend
1. Clone the repo, `cd backend`, then run `npm install` to install packages.
2. Copy `.env.example` to `.env` and update it with the credentials I provided.
3. `npm run dev`, then wait for the message `connected to db & listening on port 4000`

## Frontend
Do this in a separate terminal. You will need to run both simultaneously.
1. `cd frontend` then `npm install` then `npm run dev`
2. Open the link provided in the console by ctrl clicking, or just type it into your web browser.

## Postman
NetNinja will explain it to you very well. It basically lets you make requests manually and save them. This will be invaluable for testing that everything performs to spec.

# Reference
This project is entirely based on  the NetNinja intro to MERN series on youtube. We are using Vite instead of Create React App (it was deprecated) but it is almost entirely the same. Components are .jsx, and we use npm run dev in the frontend, too. The proxy is placed differently, but don't worry about that.

# Submission
Submit a single pull request with all your fixed bugs. Each commit should only fix one bug (one!), so it's easy to see what you did. You don't need to find every bug to submit, so send in what you have.

1. Fork the repo. Click **Fork** in the top right of this page on GitHub. This gives you your own copy that you're allowed to push to.
2. Clone **your fork**, not this repo. If you clone this one, you'll get a "permission denied" error when you try to push.
   ```
   git clone https://github.com/<your-username>/acm-ht2-test.git
   ```
3. Make a new branch.
   ```
   git switch -c bug-fixes
   ```
4. Fix one bug, then commit it with a message saying what you fixed. Then fix another bug, commit it, etc.
   ```
   git add .
   git commit -m "Sort workouts newest first"
   ```
5. Push your branch to your fork.
   ```
   git push -u origin bug-fixes
   ```
6. Open the PR. Go to your fork on GitHub and click the **Compare & pull request** button that pops up. Make sure it says you're merging your fork's `bug-fixes` into `LightningFish27/acm-ht2-test`'s `main`. In the description, list each bug you found: what was wrong, how you found it (which Postman request, what you saw on the page, etc.), and how you fixed it.

Found another bug after opening your PR? Just commit and `git push` again. The PR updates by itself, no need to open a new one.