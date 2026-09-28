# Emergency-Support-Network
https://github.com/cmu-fse-sa3/f26-esn
# Emergency Support Network — Frontend Case Study

A mobile-first interface for a course team project about helping neighbors communicate during an emergency. This repository is a showcase of the frontend work I contributed, using fictional users and data. It is not the complete team application or a service intended for real emergencies.

## The experience

A new visitor starts on a welcome screen, creates an account, sees a short introduction, and enters the community directory. A returning member can log in directly. The interface also gives people a clear path to the public wall and shows confirmation when they log out.

[Add a short demo GIF or a link to a video here.]

## What I worked on

I built and refined the welcome, account setup, registration, introduction, and community directory pages. My work included mobile layouts, form validation, consistent error messages, and the navigation between these screens. I also connected my frontend pages to the team's backend flows and worked with teammates to resolve integration issues.

The backend and the broader application were team efforts. This repository focuses on the parts I can share and explain personally.

## A few decisions behind the UI

- **Make the first action obvious.** The welcome page gives a visitor one clear way into the community, while the account setup flow handles new and returning members.
- **Keep feedback in one place.** Empty fields, existing usernames, and invalid credentials should produce clear messages near the form instead of leaving people guessing.
- **Design for a phone first.** The core screens use a single-column layout and keep the next action easy to find on a small screen.
- **Make state changes visible.** The logout flow confirms that the member has been marked offline before returning to the welcome page.

## How the project evolved

Our team worked in two-week iterations, with the scope changing as we went. I updated the frontend as the account and directory flows became clearer, reviewed integration points with teammates, and adjusted the pages after testing the flow on smaller screens.

[Optional: Add one specific before-and-after example here—what feedback you received, what you changed, and why.]

## What this repository contains

[Describe only what you actually publish: for example, a standalone frontend demo, screenshots, a short walkthrough, and notes on your design decisions.]

The original course repository, teammates' code, course handouts, credentials, and real user information are not included.

## Run the demo

[Add accurate installation and run instructions if you publish a working demo. Remove this section if the repository contains only a case study and screenshots.]

## Looking back

This project taught me how much of frontend engineering happens between screens: defining what each action means, making failures understandable, and keeping the user flow coherent while different people build different parts of the system.
