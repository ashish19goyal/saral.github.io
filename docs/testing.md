---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
title: Testing
nav_order: 5
---
## Testing Ideology
- Customers have some expectations from the application on how it should behave. Its best that we only test based on customer provided test cases.
- Auto generated code doesn't have to be tested. It is assumed that all auto-generated code is hardened by Saral.

## Methodology
- Customer triggers a run of the application from the Saral UI
- Depending on the type of the application, Saral will record the interactions with the application
  - Browser UI: Run the application in chromium and record all interactions
  - Console UI: Record the commands issue to the application
  - Rest API: Record the rest API calls made to the application
- Present the recording to the user as a text file
- Ask user to generalize the output patterns (potentially using AI)
- When the user submits the final test report, it is recorded for running as a regression test case

## Regression testing
- Before every publish, all regression tests are validated
- Users can optionally run regression test on their branches on-demand