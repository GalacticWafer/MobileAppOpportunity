# MobileAppOpportunity

The following is a transcript of the MobileAppOpportunity.mov file viewable by MSU Denver students at:
https://discord.com/channels/480073060561453078/821072160990691378/1333835662083756133

- Engineer1: CI-CD pipeline & iOS fork.
  - One engineer will begin by setting up the CI-CD pipeline for the project as it stands currently. Then, start researching if we can use/leverage Flutter, Kotlin Multiplatform, or other such techniques to build targeted code for Android and iOS at the same time, given the limitation that we are designing a keyboard. Keyboard applications are not the same as most apps due to their ability to control and capture input. It is possible that we have unusual limitations, and any limitations should be explicitly listed in the report. Engineer1 must also include an analysis of which portions of the code, if any, could be used with the solution they consider to be the most plausible for saving on overall effort. The report is expected to be completed within the first 6 weeks but may take longer and require prototyping on the side. After Engineer1 presents their findings, they should start creating the iOS app, along with unit tests, converting as much of the codebase as possible to shared code and/or iOS. When this work is complete:
  - MVP:
    - CI-CD pipeline that builds the app
    - The multiplatform support report included as part of a presentation with at least one slide
    - A decision about how to store the iOS branch and setting up that branch
  - Stretch goal:
    - Code generation for all classes that do not use Android-specific code (i.e., anything that AI can help you do relatively quickly). I will help you identify these parts of the code.

- Engineer2: Board position and sizing refactor + Test automation.
  - A refactor is needed to change how size and scaling are calculated. Engineer2 should be proactive in learning how my internal sizing API works by using paired programming, documentation, meetings, code walkthroughs, or any other means they request, all at their discretion. This is a bottleneck feature, which Engineer3 will start off assisting with to make these changes quickly (estimated 2-4 weeks).  
  - Next, begin writing automated tests in Appium to run tests on physical devices without human intervention. I have experience with Appium and can point you in the right direction on most issues with it.
  - MVP is a single test that runs each gesture on a keyboard and ensures that each gesture with the `PressKey` operation assigned to it works as expected.
  - Stretch goal: To additionally test `SendInput`, `RemappedSymbolLookup`, `SwitchLayer`, and `SwitchScreens`. If you finish these, keep going or help another team member.

- Engineer3: Board position and sizing refactor + Build-Your-Own-Screen (BYOK) UI
  - Engineer3 starts out working with Engineer2 because the refactor is needed before moving forward.
  - Engineer3's first solo task and MVP will be to implement positioning of all the elements in the mock-up of the BYOK screen, which I will provide.
  - MVP is to implement navigation to the next screen for:
    - A scroll view of all the layers of a keyboard in cyclical order
    - Controls for:
      - Save Keyboard to internal app data – Toast a message to the user
      - Load Keyboard from internal app data – Goes to a non-functional scroll view of all keyboards. It should also have a non-functional search box aligned to one of the top corners
      - Add Keyboard – Goes to a non-functional input text popup to collect the name
      - Change Keyboard (basically save then load) – Toast a saved message to the user, then goes to a non-functional scroll view of all keyboards. It should also have a non-functional search box aligned to one of the top corners
      - Add Layer to current keyboard – Goes to a non-functional input text popup to collect the name
      - Remove Layer – Goes to a non-functional, vertical scroll view of all keyboards, with non-functional delete buttons to the right of each entry

- Engineer4: Membership, Login, Welcome
  - Carry out research to determine the best way to implement OAuth across mobile devices
  - MVP: Implement the concept of a `User` as necessary in our Android codebase with the following constraints:
    1. User can be one of:
      1. Free tier
      2. Paid tier
    2. Free tier users have the following restrictions:
      1. Restrict ability to download/upload the keyboard as a JSON file
      2. Restrict the ability to change the colors and themes
  - Implement OAuth to take payments on Android.
  - Stretch goal:
    - First screen has login or try free
    - Check if it's the first run or not, and if it is:
      - Go through an interactive slide show teaching how to perform each gesture, with the option to skip.
      - Show a sequence of popups the first time the settings menu is opened, explaining each button in the settings menu.
    - Allow the user to use the board right away by having a welcome screen with the logo. We need to add OAuth so we can start taking payments.

## NOTE
- #### You may assume more than one Engineer role.
- #### You will be a valuable member of this team even if we have less than 4 Engineers.

Now, what's in it for you? If every team member meets their MVP, then each team member will get a 2.5% royalty on profits, netting a combined 10% stakeholdership in the code, under the condition that you remain responsible for keeping the code you added up to date and compliant with Google Play Store and/or Apple Store.

MessagEase has over 5K premium users. If we can get that many sales at $50 per sale, then each team member will make $6,250. Not bad for a senior project, especially if we can grow the number of users or find new add-ons for a subscription model. I believe this is fair because much of the work has already been done. This codebase just surpassed 30K lines of code last week and is almost a year old, so I've been putting in work!
