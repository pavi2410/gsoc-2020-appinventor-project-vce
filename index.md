# Intro

A Visible Component Extension or VCE is a type of extension which is able to provide Mock preview of what a component running on a real device would like. It leverages the existing mechanism set in place to write Mocks for the internal components. This doc aims to provide every bit of information required to make a VCE of your own.

# Background
## About Me
## My Experience with MIT App Inventor Open Source Project
## My Mentors
## My Exterience with GSoC

# My contributions
- [PR #2223 @ mit-cml/appinventor-sources](https://github.com/mit-cml/appinventor-sources/pull/2223)
- [Branch with the new iFrame-based sandbox implementation](https://github.com/pavi2410/appinventor-sources/tree/mvce3) `WIP`

# Demo

# Technical Challenges
- Creating JavaScript sandbox to securely evaluate third-party extensions' Mock
- Getting GWT to work with dynamically loaded external JavaScript code

# Future Work
- Can't create more than one instance of a VCE `WIP`
- Reloading the page causes a runtime error, making VCE implementation useless `WIP`
- Implement callback messaging system with iframe
- Mock Container support
- More and more rigorous testing.
