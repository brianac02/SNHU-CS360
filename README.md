# SNHU-CS360

Briefly summarize the requirements and goals of the app you developed. What user needs was this app designed to address?

  The WeightTracker app was developed to provide users with a simple and secure way to record their daily weight and track progress toward a personal goal. The app includes account creation and login functionality, a database to store weight entries and goal weight, and a grid display to review past entries. It also offers an optional SMS notification feature to alert users when they reach their goal weight. Overall, the app was designed to meet the needs of individuals who want a straightforward, no-frills tool to stay consistent and accountable in their weight-loss journey.

What screens and features were necessary to support user needs and produce a user-centered UI for the app? How did your UI designs keep users in mind? Why were your designs successful?

  To support the main user needs, the app needed three core screens: a Login/Create Account screen, a Dashboard/History screen with a grid of past weight entries, and an Add Weight screen for entering a new daily value. A Settings/SMS screen was also necessary so   users could opt into notifications, enter a phone number, and control permissions without it being forced on them.

The UI keeps users in mind by following a clear, predictable flow: sign in, see your history/goal, add a new entry, with obvious “back/cancel” exits so users never feel trapped. Inputs are simple (weight + auto-date), buttons are labeled in plain language, and the dashboard groups information so users can understand progress at a glance instead of hunting through menus. The designs were successful because they reduce effort and confusion: the most common actions are always visible, the screens don’t overload the user with options, and optional features (like SMS) are separated into settings so the app stays usable even if a user declines permissions.

How did you approach the process of coding your app? What techniques or strategies did you use? How could those techniques or strategies be applied in the future?

  I approached coding the app by building it in small, testable chunks instead of trying to do everything at once. I started with the navigation and basic screen flow, then added the database “shell” and hooked up CRUD features one at a time (create/save a weight, read into the grid, delete a row, update via replace). I used consistent naming conventions, separated responsibilities (Activities for UI flow, a DB helper for table creation, simple model/adapter classes for the RecyclerView), and relied on Logcat/Toast messages to verify each feature worked before moving on. In the future, these same strategies apply to bigger apps: break work into milestones, isolate logic into reusable classes, test each feature early in the emulator, and keep code organized so you can scale without everything turning into one massive, fragile file.

How did you test to ensure your code was functional? Why is this process important, and what did it reveal?

  I tested the app by running it frequently in the Android Emulator and checking Logcat for errors after every major change, instead of waiting until the end. I verified each feature through simple “real user” flows: creating an account, logging in, navigating between screens, adding a weight, confirming it appeared in the grid, deleting a row, and trying edge cases like blank fields or duplicate entries for the same day. I also tested both outcomes of the SMS permission request (Allow vs Deny) to make sure the app still worked normally if permission was denied and only attempted notifications when settings were enabled.

This process is important because mobile apps can fail for small reasons—like a wrong view ID, a missing manifest entry, or a database schema typo—and those issues are much easier to fix when you catch them immediately. Testing revealed problems early, like database table creation errors (SQL syntax/constraints), crashes caused by invalid IDs or missing default activities, and logic issues where settings didn’t actually affect behavior until preferences were properly wired up. Overall, it helped confirm the app was stable, that core workflows worked end-to-end, and that optional features didn’t break the experience for users who don’t enable them.

Consider the full app design and development process from initial planning to finalization. Where did you have to innovate to overcome a challenge?

  Throughout the entire development process, the name of the game was innovation. One thing I wanted to do was to be unique in my design or, at the very least, attempt to be. In the DashboardActivity, I tried to get creative with the way data was displayed to help give the app more of an individual look and feel, using the CardView to display the target weight to really make it stand out, and using the RecyclerView to display the list of previous weights as the days go on. 

In what specific component of your mobile app were you particularly successful in demonstrating your knowledge, skills, and experience?

  The aforementioned section was actually where I felt the most successful in demonstrating my knowledge and skills. Forcing myself to learn new strategies and structures on the fly and make it work seamlessly is something that I feel is only able to be accomplished with some level of experience - albeit it wasn't the most difficult or complex design or idea, it was still new relative to me, as was all of the front end design and such, which made it stand out the most to me. 
