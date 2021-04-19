# Step 14: Build Loop app

!!! danger "Time Estimate"
    - 60-80 minutes if first time builder
    - 10-15 minutes if a repeat builder

!!! info "Summary"
    - Open the Loop code you downloaded in [Step 13](step13.md)
    - Connect the phone to the computer
    - Set the phone to not lock for awhile
    - Trust the computer (on the phone)
    - Select your phone from the top of the device list
    - Register the device
    - Sign the 4 targets
    - Press the build button
    - Enter computer password four times during the build (if this is your first ever build)
    - Watch in awe as you just built your very own Loop app

!!! warning "FAQs"
    - **"I got a build error! YIKES...what do I do?"** Check out the [Build Errors](build_errors.md) page for solutions.
    - **"The build seems to take a long time, is that normal?"** Yes, the first build of a new download will take quite a long time. Just be patient, one of the build steps may take *much* longer than all the others. The build process does always end in a success or failure message, so just wait it out until you see one of those displayed.

## Open Loop project in Xcode

Go to your Downloads folder, open your downloaded Loop code folder and double click on Loop.xcodeproj. If you downloaded master branch, your folder would be named `Loop-master` and similar for `Loop-automatic-bolus` download.

![img/loop_code.png](img/loop_code.png){width="750"}
{align="center"}

A warning may appear asking if you really want to open it, click Open. Xcode will get itself organized, this may take a few minutes.  

![img/loop_open.jpg](img/loop_open.jpg){width="450"}
{align="center"}

Once Xcode has finished indexing, the Loop project's various folders and files will appear in the far left column. We are now going to make three important sets of clicks:

1. First click: At the very top of all the folders and files listed, click on the blue "Loop". This will populate the middle part of the Xcode window with some information. **If a couple of little boxes appear saying "The folder “DerivedWatchAssets.xcassets” doesn’t exist."...just click the ok buttons and ignore those. They may come up a couple of times during your build if you are using dev branch right now...don't worry, won't be a problem.**

    ![img/loop-first-click.png](img/loop-first-click.png){width="550"}
    {align="center"}

2. Second (set of) clicks: Now click on the box in the middle screen to reveal the targets column underneath that box. The four targets we will sign in the upcoming steps are now easily viewable. The four targets are Loop, Loop Status Extension, Watch App, and WatchApp Extension. Select the Loop target, shown in the screenshot below. It will be highlighted in blue to let you know it is selected.

    ![img/loop-second-click.png](img/loop-second-click.png){width="550"}
    {align="center"}

3. Third Click: With the Loop target selected, click on the "Signing & Capabilities" up near the top of the screen. After you click on that, you should see a "Signing" section occupying the bulk of your middle window. If you are missing the "Signing & Capabilities" section and didn't have to click somewhere else to see that part...that means you have missed updating to Xcode 11 from an older version of Xcode. Please go back and update Xcode now.

![img/loop-third-click.png](img/loop-third-click.png){width="550"}
{align="center"}

## Connect Your iPhone to Computer

Connect your iPhone via cable to the computer, select your iPhone from the very top of the drop-down list.  Your **iPhone’s personal name** should be at the top of the list. Don't accidentally select the generic iOS simulators listed below your iPhone's name.  

!!! info "Helpful Tips"

    - If this is the first time your iPhone has been plugged into this computer, you will need to open the iPhone and select "Trust this Computer" before your device will be useable in the menu selection.
    - If this is the first time your watch has been paired to the iPhone, you will need to select "Trust this Computer" on your watch.

!!! danger "Most Common Mistake"

    - The most common mistake in this step is not selecting your actual phone as shown in the second screenshot below. The default list is just a name of general phone models under a subheading called "iOS Simulators"...don't be fooled by those. Your ACTUAL phone will be up above that list of all the various simulator phone models.  You may need to scroll to the top of the list to see it.  Make sure you select your actual phone, not just a simulator phone model.

![img/select_device.png](img/select_device.png){width="750"}
{align="center"}

![img/your_device.png](img/your_device.png){width="650"}
{align="center"}

## Sign Four Targets

Once you select your device (your iPhone's name), you are ready to start signing the four targets. Start with the Loop target, the first one on the target list.  Under the "Signing" area, ensure that you have "All" selected near the top and then select the dropdown menu where it currently says "none". Choose your team that you'd like to sign with. If you select a team name with (personal team), your app will expire after 7 days. If you select a team name without that (personal team), your app will last a full year.  If you never signed up for a [Free Developer Account](step9.md#add-apple-id), you will not have a (personal team) showing. Make sure you keep the "automatically manage signing" box checked above the team selection area.

![img/team.png](img/team.png){width="750"}
{align="center"}

Once you choose your signing team, Xcode will automatically generate provisioning profiles and signing certificates.  If this is the first time you are building on this iPhone with this developer account, you may be prompted to register the device.  Simply click on the "Register Device" button to confirm.

![img/register_device.png](img/register_device.png){width="750"}
{align="center"}

## Free Account

!!! danger "Free Developer Account Users: READ ME"

    If you are using a free developer account to sign your targets, you will need to do an extra step. As a free developer, you are restricted from building apps that have Siri or push notification capabilities built-in. Loop has both of these capabilities, so you will need to disable them before proceeding on with signing and building your app. The push notification capability is used for setting remote overrides; disabling it will not affect regular notifications, e.g., "Loop Failure" with minutes since last Green Loop, "Pump Reservoir Low", etc. Click on the small x next to the Siri and push notification lines located at the bottom of your Signing & Capabilities page. You need to do this in both the Loop and WatchApp Extension targets.

    ![img/siri-errors.png](img/siri-errors.png){width="750"}
    {align="center"}

A successfully signed target will have a provisioning profile and signing certificate similar to the screenshot below.  Click on each of the three remaining targets, and repeat the signing steps by choosing the same team name as you selected in the first target. The four targets that must be signed prior to building the Loop app are Loop, Loop Status Extension, Watch App, and WatchApp Extension.

![Xcode window showing the four targets that must be signed](img/success.png){width="750"}
{align="center"}

## Code Customizations

**New Loop users**: Customizations are not a required part of any Loop build. As you gain experience in how you use your Loop app, you may want to customize some of the features. First time builders are encouraged to build with the standard, default code. You can always update your Loop app to add customizations at a later time, using the same download. Subsequent build time is must faster (a few minutes) than the initial build for a given download.

If you want any custom configurations to your Loop or Loop Apple Watch apps, now is the time to make them before you build on the Mac and copy the Loop app to your iPhone. Follow the step-by-step instructions on the [Code Customizations](code_customization.md) page. If you are a person familiar with Apple's Swift language, feel free to make your own customizations as well.

When you've finished your customizations, come on back to this section and continue on with the rest of the build.

## Pair your Apple Watch

**New Apple Watch users**: If you have an unopened Apple watch and want to use it with Loop, first pair the watch with the iPhone before continuing to the next steps.  If you get a new watch after building the Loop app, you'll need to redo your Loop build. (Don't worry, it's as easy as pressing play on your saved Loop project.)

**Existing Apple Watch users**: Please update your watchOS prior to building the Loop app.  The current version of Loop requires watchOS 4.1 or newer.

## SAFETY INTERMISSION

STOP STOP STOP ... This intermission is about safety.

Some new users input settings and start using the Loop app without fully understanding the effects of the configuration values. This advice is inserted in the middle of the build process to make it more obvious.

![alt](https://media.giphy.com/media/xT9DPJVjlYHwWsZRxm/source.gif)

!!! warning "DO NOT WING THE SETUP"

    Sorry to shout - better to get your attention now before a mistake is made.

    - **Continue to use these docs to finish setting up your app after it builds**.
    - **DO NOT ENTER ONE LOOP APP SETTING WITHOUT HAVING THE DOCS OPEN AND FOLLOWING ALONG AT THE SAME TIME.**
    - **The Loop app automatically doses insulin based on your configuration settings and your meal entries.**

The section in these docs called "Set up App" (look for it now at the top of your webpage - it's a menu title) needs to be used to input all the [settings](../operation/overview.md) in your Loop app when it is done building. READ ALONG WITH THE DOCS to enter those settings. There are important safety tips and advice in there. And then after you finish setup, you need to read the "Operate" section BEFORE YOU OPERATE LOOP. Don't bolus for a meal, or enter a meal, until you've read through the Operate section.

Please heed the advice about using the setup and operate sections. People have ignored this advice and gotten themselves (or their child) into a dangerous situation by entering incorrect settings and going straight to Closed Loop before understanding how Loop operates. They skim and think that's good enough. Not a bad idea to skim one time, but then go back and read it more thoroughly once you are oriented.

There is a lot of information. The two most important warnings are highlighted here.

!!! warning "TOP TWO SAFETY MISTAKES YOU SHOULD AVOID"
    1. Do not enter settings if you are unsure of the correct value or what the setting means. Don't just guess an ISF, carb ratio, basal rate, or maximum delivery limits. If you don't know your settings or know what the terms mean, stop and try one of these steps:

        - [Search](../index.md#how-to-use-these-docs) the docs for the term: all the settings terms are defined in the docs.
        - Ask your endo if you don't have established values for those settings.
        - Still confused - this is a time to post on a [Loop Social Media](../index.md#stay-in-the-loop) site rather than guess.

            Example post: "I've read the docs but I'm still confused about xxx".  You may get a link back to a specific section of one page.  Read that section first. If that doesn't clarify things, then reply in that same post with what confuses you.

            Please - pick one site; work with one mentor; do not post is multiple places at once.<br/><br/>


    2. Once Carb entries are saved using the [Carb Entry to Meal Bolus Menus](../operation/features/carbs.md) or the [Edit Carb](../operation/features/carbs.md*edit-meals) feature, Loop will provide increased insulin to handle that entry.

          - The Loop app is an automated insulin delivery system and if it thinks you have carbs on board, it will try to give you appropriate insulin for those carbs.
          - **You must delete or edit a saved carb entry if you no longer want Loop to provide insulin for it.**
          - The [Apple Health Permissions](health.md#loop-permissions) should be configured so that Loop can write Carbohydrates (report to other apps), but Loop should **NOT** have permission to read Carbohydrates (that may be entered from other apps, or from a mistaken Blood Glucose entry in the wrong place).

Now that the Safety Intermission is done, you can continue on with the last step in building your app.

## Build Loop

Have you signed the four targets? Are you done with any customizations? Has your Apple watch been paired and updated? Is your iPhone unlocked and plugged into the computer?

Let’s finish the installation of the Loop app onto your iPhone. Double-check to make sure your iPhone's name is still selected and then press the “build” button to start Xcode on its way.

!!! info "Helpful Tips"

    - The final step of a successful build is for Xcode to copy the completed build to your iPhone; if your phone is locked, Xcode pops up a message letting you know.  Unlock your phone to continue.

![img/build_button.png](img/build_button.png){width="750"}
{align="center"}

You’ll see the progression of the build in the status window (top middle of Xcode). New builds can take about 40-60 minutes depending on the speed of the computer and the internet.  **Just be patient.**  The progress will get "stuck" on one step/task for a very long time, and then the others will fly by. Not every step is equal in duration. Do not give up on the build.

**Xcode will ALWAYS tell you eventually that the build either succeeded or failed via a short (self-disappearing) pop-up message on the computer display. If you miss the message, you can look at the top of the Xcode window to see a "Running Loop..." (success) or "Build Failed" (failure) message where the step progress was previously counting down.**

!!! danger "Are you the impatient type?"

    If you just simply can't bear the uncertainty of not seeing that things are progressing, you can take a peek "under the hood" and watch the individual build steps by clicking on the report navigator icon and then the build row at the top of the list. You can watch the slow list of scheme building while you wait.

    ![img/build-scheme.png](img/build-scheme.png){width="650"}
    {align="center"}

!!! info "First Time Builder or First Time on this Computer"

    Sometime during your first build on a computer, be ready for a codesign/keychain access prompt that you will see part-way through the build process.


    ![img/keychain-prompt.png](img/keychain-prompt.png){width="350"}
    {align="center"}


    This prompt above, when you see it, requires you to enter your computer password (the one you use to log in) and then select "Always Allow". It is normal for this prompt to come up four times in a row even after you enter the correct password. In frustration, people think the prompt must be broken because it keeps reappearing and then people will press deny or cancel. **Don't press deny.** Keep entering your computer password and pressing the "Always Allow" button as many times as it takes (four times to be exact; one for each target in Xcode). After four times of successful password entry, the build will continue.

!!! warning "While you are waiting..."

    While you are waiting for the build to complete, check out two pages:

    - [Read Loop Troubleshooting](../troubleshooting/yellow-red-loop.md).
    - And if you plan to use an Omnipod: [Pod Pairing Toubleshooting](../troubleshooting/pod-pairing.md)

    Ok, back to the building instructions.

## Build Finished

!!! info "First time building on a new device?"

    If this is the first time you have installed an app on your iPhone using your developer account, you may get a warning like below after a successful build. Don't worry, Loop usually installed just fine on the phone but needs you to do an extra step on the phone before Loop app can open. Just follow the directions shown in the warning for what you need to do on your iPhone. Go to Settings->General->Device Management (or profiles, Profiles & Device Management on newer iOS) and enable trust for your Developer Account. If you are missing the Device Management/Profiles option in your iPhone settings, then head over to [this Build Error section](build_errors.md#device-management-could-not-launch-loop) to find the solution.

    ![img/trust_device.jpg](img/trust_device.jpg){width="750"}
    {align="center"}

!!! danger "BUILD SUCCEEDED"

    Congrats! If the build is successful, you'll see the message or "Running Loop..." across the top of the Xcode window.

    Your brand new Loop app will have a screen open immediately on the iPhone asking about allowing Loop notifications and Health App access. `Allow` Loop to send you notifications. In the next screen that follows that, click on the `Turn All Categories On` line and then **immediately turn OFF the permission to read Carbohydrates**.  (This is a [safety feature](health.md#loop-permissions).) Click `Allow` in the upper right corner.


    ![img/health-start.JPEG](img/health-start.svg){width="450"}
    {align="center"}

    **You can unplug your phone from the computer now.** You will get an Xcode message window that says `Lost connection to the debugger on "<your phone name>"`.  Just click OK.

    Next, you will use the [Set up App](../operation/overview.md) section of this website to keep proceeding safely.

!!! warning "FAQ: But what about those yellow alerts that remain in Xcode? Should I worry about them?"

    If you see yellow alerts after your build is done...those are not an issue. Whether your build succeeded or failed...the yellow warnings play no role in either outcome. Don't try to resolve them or fret about them. They mean nothing to the successful use of your Loop app.

    ![img/yellow-warnings.png](img/yellow-warnings.png){width="750"}
    {align="center"}

!!! danger "BUILD FAILED"

    Don't despair. Build failures are pretty easily fixed. If you get a message that your build failed and see **RED ERROR** messages, just go to the [Build Errors](build_errors.md) page to find the steps to fix your build error based on the message displayed.


    ![img/general-error.jpg](img/general-error.jpg){width="750"}
    {align="center"}

## Summary

If your build failed, you need to proceed to the [Build Errors](build_errors.md) page to find the solution. Please head there to find the help you need.

If your build was successful but your phone was locked, you will see an Xcode message window that says `Unlock <your phone name> to Continue`. Simply unlock the phone and the app will be copied onto your phone.

If no build errors, you're done building your Loop app.

The next step is to unplug your phone.  You will now get an Xcode message window that says `Lost connection to the debugger on "<your phone name"`.  Just click OK. This is because you unplugged your phone.  The Loop app is still running on your phone and your are ready for the Set up App menu.

![alt](https://media.giphy.com/media/l0MYt5jPR6QX5pnqM/giphy.gif)

## Next steps

Go straight to the [`Set up App`](../operation/overview.md) menu and work through the page to proceed safely.
