## Update the *Loop* App

**This page is only relevant when building with a browser.**

**For *Mac-Xcode* updates, please see: [Updating/Rebuilding](../build/updating.md)**

???+ info "Time Estimate (click to open/close)"
    Build the *Loop* App

    - Check *Apple* account status: 5 minutes
    - Update version if a new one is available: 5 minutes
        - If needed, update your configuration for automatic builds: 10 minutes
    - Start the Build: 30 sec
    - Wait for the build to complete and appear in the *TestFlight* app on your phone
        * about an hour
        * depends on *GitHub*, *Apple* and *TestFlight*

???+ abstract "Page Summary (click to open/close)"
    **The *Loop* app must be built at least every 90 days when you build with a browser - this is *TestFlight* requirement.**

    Follow the instructions for automatic build as part of the update to Loop 3.2.4: see [How to Update or Rebuild](#how-to-update-or-rebuild).

    If you are running `Loop-dev`, be sure to review [Build Development Version](#build-development-version)

    * You should be following along with zulipchat when using the `dev branch`
    * Summary build updates can be found under the [One-Time Changes](#one-time-changes) section

???+ question "FAQs (click to open/close)"
    - **"What is an update?"** Anytime you want to change versions or if your *TestFlight* build is about to expire, follow the instructions on this page.
    - **"Do I delete my old Loop app first?"** Definitely **not**! If you keep your Loop app on your phone, your Loop settings (and existing pod) will continue to work the same after the update. Seamless.
    - **"Do I need to start a new pod when I update?"** No. Your existing pod session will continue seamlessly if you are using the same Developer Account as the last time you built.
    - **"What if I'm using a new/different developer account?"** If you aren't building with the same developer account used when your existing app was built, then you will be installing a brand new (second) Loop app on your phone. Your existing pod won't work with the new app, so you might want to time this transition when you are due to change pods. Delete the old app once you get the new one all set up.
    - **Do I need a computer?** No.
    - **Can I do this on my phone?** Yes, especially after you update your *GitHub* token to `No Expiration`.
    - **Did the directions change?** Yes. We now recommend you select a *GitHub* Personal Access Token that never expires and supports automatic update and rebuild released with version 3.2.4. It simplifies the build every 90-day process significantly.
    - **How do I set my *GitHub* `Personal Access Token` to never expire and to support the automatic rebuild feature?** See this section [Regenerate Token](#regenerate-token).
    - **What happens to my existing builds when I change my *GitHub* Personal Access Token?** Nothing. The <code>GH_PAT</code> only affect future builds. Previous build are available for the full 90 days.

## When to Update or Rebuild

Under ordinary circumstances, you do not *have to* rebuild or update your *Loop* app until *TestFlight* forces you to (90 days). However, there is no harm in building more frequently. With the release of 3.2.4, you can set up automatic builds that check for updates once a week and builds once a month.

* You control when the new app is installed on your phone, refer to: [Install on Phone: Disable Automatic Install from *TestFlight*](gh-deploy.md#disable-automatic-install-from-testflight)
* You always want a build available in the *TestFlight* app
    * You can use *TestFlight* to quickly install the app if you loose or break your phone and need to replace it
    * You can use *TestFlight* to quickly install the app if someone accidentally deletes the app from your phone

## How to Update or Rebuild

!!! abstract "Summary of Update Steps"
    * [Accept Agreements](#accept-agreements)
    * [Update `Fork`](#update-fork)
    * [Build the *Loop* App](#build-the-loop-app)
    * [Wait for *TestFlight*](#wait-for-testflight)
    * [Install on Phone](#install-on-phone)

    Ignore the email that says you need to fix "issues" in your app. You are not selling the app in the app store; so no action is required. The app you built is for personal use for you or a family member.

### Accept Agreements

Sign in to your [Apple Developer account](https://developer.apple.com/account). If there are agreements you have not accepted, you will get errors when you try to Build that indicate your *Apple* <code>Secrets</code> are incorrect - that is very unlikely. You may also need to update your credit card information if it has changed, for example, if there is a new expiration date.

If you need detailed instructions, click on the [<code>Apple Program License Agreement</code>](https://support.pushpay.com/s/article/Accepting-the-Apple-Program-License-Agreement) help page.

* Accept the `Apple Program License Agreement` (only)
    * You do NOT need to accept anything related to the `Paid Applications Schedule Agreement`
    * That is only required when you sell an app through the `App Store`

!!! warning "Wait After You Agree"
    It typically takes 15 minutes before your updated agreement is available so you can complete your build.

    If your build with browser fails, wait longer. An hour wait was reported by one person.

### Update `Fork`

Open your *GitHub* account and select your&nbsp;<span translate="no">LoopWorkspace</span>&nbsp;`repository` from your `repositories` list.

#### Special Instructions for Update

When updating from&nbsp;<span translate="no">Loop</span>&nbsp;3.2.x to 3.2.4, you will need to take some extra steps. Once those steps are completed, your &nbsp;<span translate="no">Loop</span>&nbsp;app will be automatically updated and automatically built at least once a month.

!!! question "Can I Opt Out?"
    Yes - you can opt out of the automatic build.

    * The default instructions configure automatic update and automatic build
    * The instructions to opt-out of some or all of these automations start at [Modify Automatic Building](#modify-automatic-building)

Here is a summary of the extra steps; each step has an associated link. You need to do all of them.

1. Confirm the status of your &nbsp;<span translate="no">*GitHub* Personal Access Token</span>
    * Recommended permission scope is `repo, workflow` and set to never expire
    * You can check this using directions at [<span translate="no">*GitHub* Personal Access Token</span>](#github-personal-access-token)
1. Follow the directions for [Manual Update](#manual-update) for your fork
1. [Build the *Loop* App](#build-the-loop-app)

#### Manual Update

![message displayed when your fork of LoopWorkspace is behind LoopKit version](img/github-build-check-fork-status.svg){width="700"}
{align="center"}

* If your `fork` is up to date with LoopKit version, you will see the message `This branch is up to date with LoopKit/LoopWorkspace:{branch}` - there is no need to build again unless your Loop app in *TestFlight* is about to expire - in which case, proceed to [Build the *Loop* App](#build-the-loop-app)
* If your `fork` shows a message such as `This branch is 3 commits behind LoopKit:main` and you want to update and build, then click `Sync Fork` by tapping where the red rectangle is shown in the graphic above, then in the pop-up window, tap on `Update branch`
* If your `fork` shows a message such as `This branch is 3 commits behind LoopKit:main and 4 commits ahead of LoopKit:main`; you might need to manually sync and choose to `discard changes`; you can always customize again after the update

!!! question "Building a different branch"
    Do I need to do anything special to build a different branch?

    Yes: please follow instructions at [Build Development Version](#build-development-version)

### Build the *Loop* App

Refer to the graphic below for the first four steps:

1. Click on the "`Actions`" tab of your <code>LoopWorkspace</code> repository.
1. On the left side, click on "4. `Build Loop`".
1. On the right side, click "`Run Workflow`" to show a drop-down menu
    * You will see your default branch (typically `main`)
    * You can select a different branch, but typically, you run the default
1. Tap the green button that says "`Run workflow`".

    ![build loop using github actions](img/action-04-build-loop.svg){width="700"}
    {align="center"}

1. Wait a few minutes to make sure there is not an early failure
    * If this action fails, head over to [Action: Build Loop Errors](gh-errors.md#action-build-loop-errors)
1. If the process appears to be happening without an error, go do something else for a while. The build should take about 20-30 minutes.
1. You should get several emails
    * one says build succeeded (or failed)
    * one says *TestFlight* is ready (typically half-hour after build succeeds)
    * Ignore the one that says you need to fix "issues" in your app. You are not selling the app in the app store; so no action is required. The app you built is for personal use for you or a family member.
1. Your app should eventually appear on [`App Store Connect`](https://appstoreconnect.apple.com/apps).

If you have successfully built the *Loop* app, version 3.2.4 with automatic build configuration enabled, and later decide to manually build Loop, all that is required is to run the action: Build Loop for your fork and skip ahead to [Wait for *TestFlight*](#wait-for-testflight).

### Wait for &nbsp;<span translate="no">TestFlight</span>

You'll receive an App Store Connect email confirming that the build has completed processing, and a &nbsp;<span translate="no">TestFlight</span>&nbsp;email confirming the new app is ready to test.

* If you get an email that the action failed, then return to your repository and look for Build Action error messages
    * Click on the most recent Build job with the red x by it
    * If the details show this message, [`Could not install WWDR certificate`](gh-errors.md#could-not-install-wwdr-certificate)
         * This means *Apple* did not reply to *GitHub* as fast as *GitHub* expected
         * Make sure your developer account is in good standing and that there are no agreements that need to be accepted
        * Repeat the build (previous step)

The updated app will show up in your&nbsp;<span translate="no">TestFlight</span>&nbsp;app.

* Your new app will have "Expires in 90 days"
    * It takes time for the update to show up in the&nbsp;<span translate="no">TestFlight</span>&nbsp;app
    * There may be older builds that are still in&nbsp;<span translate="no">TestFlight</span>
* You will also see a build number in parentheses, that number increments each build

### Install on Phone

#### TestFlight Automatic Update Disabled

Option 1: If you chose to [Disable Automatic Install from *TestFlight*](../gh-actions/gh-deploy.md#disable-automatic-install-from-testflight), you control when to install the app on the phone.

* **This is the recommended option**
* Open *TestFlight* on your phone and click `Install` as shown in the GIF below
* If you are building for a child, follow the [*TestFlight* for a Child](gh-deploy.md#testflight-for-a-child) instructions again

![install Loop from &nbsp;<span translate="no">TestFlight</span>](img/testflight-install-loop.gif){width="300"}
{align="center"}

#### TestFlight Automatic Update Enabled

Option 2: If you chose to enable Automatic Updates from *TestFlight* for the *Loop* app, the updated build will be installed over your existing app as soon as it uploaded to *TestFlight*.

* In this case, when you look at the&nbsp;<span translate="no">TestFlight</span>&nbsp;app on your phone, the app should have installed automatically
* Refer to the GIF above, the message will say `Open` instead of `Install`

## *TestFlight* Expiration Warning

For version 3.3.0 and newer, the usual [<span translate="no">Loop</span> expiration notification system](../operation/features/notifications.md#loop-app-expiration-notification) alerts the user when the app is within 20 days of expiration. In addition to that modal alert, the user can examine the bottom of the Settings screen at any time to see the expected expiration date and time.

![expiration warning on settings for testflight example](../version/img/expiration-warning-testflight.svg){width="300"}
{align="center"}

## <span translate="no">GitHub Personal Access Token</span>

Your *GitHub* `Personal Access Token` should be configured:

* `Never expire`
* `repo, workflow` permission scope

Refer to [Modify Automatic Building](#modify-automatic-building) if you don't want to accept the default recommendation to automatically update and build.

If you are not logged in to *GitHub* and have not logged in recently, then you may see the authentication screen when doing the steps below.

Authenticate if requested by clicking on the green `Send SMS` button or entering your password.

![two-factor authentication for access to tokens](img/gh-sms-access-screen.png){width="300"}
{align="center"}

Once you are authenticated, you will have access to view your personal access token.

### Modify `Personal Access Token`

If your `Personal Access Token` has not expired but does not have the correct permission, you should modify it. Do not regenerate it.

Click on the link to view your token and compare it to the graphic below.

* [Link to access your *GitHub* `Personal Access Token`](https://github.com/settings/tokens)

![access token with correct permissions](img/gh-token-correct-permission.png){width="600"}
{align="center"}

The graphic above has a blue rectangle added to indicate where you should see your token. If yours does not look like this, click on the link (`FastLane Access Token`) to open a new display. Watch the GIF below - there are 4 frames, the last one has the Update token button.

1. Click on the link (`FastLane Access Token`) to open a new display
1. This example has no workflow or repo checks in it
1. Add a check to the workflow box
1. Scroll all the way to the bottom of the screen and click on the green `Update token` button

![configure access token permissions](img/update-personal-access-token.gif ){width="600"}
{align="center"}

After you click on the `Update token` button, your `FastLane Access Token` should now show `repo, workflow` and look like the earlier graphic above.

The only reason to regenerate a token is if it is set to expire. Do not do the next section unless you have to.

### Regenerate Token

If your `Personal Access Token` has expired or has an expiration date, you can regenerate the new one at any time.

!!! tip "Update new GH_PAT to <code>Secrets</code>"
    After you get your new token, immediately add it to your <code>Secrets</code> for any app you build with this method. You don't have to rebuild the app, but it's a good idea to at least run `Action 1. Validate Secrets` for each repository to make sure you did not make a mistake.

You can regenerate your *GitHub* `Personal Access Token` at any time by clicking on the link below. (Right-click, control-click to open in a new browser tab.)

* [Link to access your &nbsp;<span translate="no">GitHub Personal Access Token</span>](https://github.com/settings/tokens)

!!! question "Your existing &nbsp;<span translate="no">TestFlight</span> builds are fine"
    The yellow &nbsp;<span translate="no">GitHub</span> warning by the `Regenerate Token` button is for new builds you make in the future.

    Previous builds are still available in &nbsp;<span translate="no">TestFlight</span> and are not affected by this action.

The `FastLane Access Token` is a clickable link.

![list of personal access tokens on github](img/gh-token-list.png){width="600"}
{align="center"}

After you click on `FastLane Access Token` your screen should be similar to the graphic below.

Note - selecting the `workflow` check box below is new. If yours does not show that selection, add it before you click on Regenerate token (red highlight in graphic below).

![review of fastlane access token on github](img/gh-token-review.svg){width="600"}
{align="center"}

Click on Regenerate token (red highlight in previous graphic) to see screen similar to next graphic. 

* Most Loopers will have classic personal access tokens
    * If you are a developer who needs to use the fine-grained (by repository) option, that's fine

Be sure to change the Expiration from `30 days` to `No Expiration`. When you select `No Expiration` a &nbsp;<span translate="no">GitHub</span> warning appears. Click on the green `Regenerate Token` button (red highlight in following graphic).

![regenerate fastlane access token on github](img/gh-token-no-expiration.svg){width="600"}
{align="center"}

The next screen shows your new token. Copy the token using the copy icon and save it along with your other secret settings.

![copy fastlane access token on github](img/gh-token-to-copy.png){width="600"}
{align="center"}

The next step is to update GH_PAT in your <code>Secrets</code>. (If you build other apps with this method - update the GH_PAT for all of them right now - do not forget.)

### Update <code>Secrets</code>

This example is for updating GH_PAT in the <code>Secrets</code> for your `repository`, but the same method can be applied when changing any of the <code>Secrets</code>.

Open the `repository` for which you will update <code>Secrets</code>. On the far right is a Settings selection. If you don't see Settings (if last item on row is Insights), then you are **not** on your `fork` or you need to sign in to your *GitHub* account. You should see `username/LoopWorkspace` with `forked` from `LoopKit/LoopWorkspace` underneath.

Refer to the GIF for help. There are 3 frames.

![screen showing repository secrets list](img/update-secret-gh-pat.gif){width="500"}
{align="center"}

1. Tap on Settings, then scroll down until you see `Secrets and variables` on the left side and click on the drop down indicator to display `Actions`.
1. Keep scrolling on the same screen, past the `Action secrets / New repository secret` row, until you see the list of your current <code>Secrets</code>. 
1. Click on the GH_PAT, tap on the pencil and enter the new token in the form. Click on Update Secret to complete the action.

Scroll all the way to the top of the screen and tap on your LoopWorkspace link. Then follow the [How to Update or Rebuild](#how-to-update-or-rebuild) instructions to start a new build.

## Build Development Version

You can build any desired branch (available at LoopKit/LoopWorkspace) using the *GitHub* Browser build method. This section is suitable if you have already built either dev or main branch using the [GitHub First-Time](gh-first-time.md) instructions.

**No matter the method used to build Loop for any branch other than main, you are testing development code. Please read this link now before continuing.**

* **[What's going on in the dev branch](../version/development.md#whats-going-on-in-the-dev-branch)**

The graphics show the dev branch. If you want a different branch, just substitute that branch name for dev.

!!! tip "Overview of what you will do"
    1. Your `LoopWorkspace fork` must have the `branch` you want
        * You will either add it or make sure it is up to date
        * You cannot just rename your existing branch to dev - you must get the dev branch from LoopKit
    1. When you select the action `4. Build Loop` and then click on the `Run Workflow` dropdown, you must select `dev` there before clicking the green `Run workflow` button - see [Build `Branch`](#build-branch)


### Check Current `Branch`

Your `LoopWorkspace fork` is at `https://github.com/username/LoopWorkspace` where you substitute your actual *GitHub* `username`. You need to be logged into *GitHub*. Review the graphic below as you go through the steps.

1. Click on the `branch` icon to display the `branches` as shown in the lower half of the graphic below:
    * If the `branch` you want is not listed, then continue with Step 2
    * Otherwise, skip ahead to [Update `Branch`](#update-branch)
1. Click on the `New branch` button and follow the [Add `Branch`](#add-branch) steps

![steps to add a branch](img/add-branch-01.svg){width="700"}
{align="center"}

### Add `Branch`

Each step in the list below matches with the number in the graphic. In the top half of the graphic, the left side shows the initial display and the right side shows the display after making the indicated selections:

1. Click on the drop down menu labeled 1 in the graphic and choose LoopKit/LoopWorkspace as show in the top right graphic
2. Click on the drop down menu labeled 2 in the graphic and choose dev
3. Click on the `Branch` name box labeled 3 in the graphic and type dev
    * The branch name in your `fork` should always match the branch name you are adding; check that you type it correctly
4. Review the dialog items to make sure everything is correct and then tap on Create branch

![steps to add a branch continued](img/add-branch-02.svg){width="700"}
{align="center"}

### Update `Branch`

Tap the `Code` button (upper left) and ensure this branch in your `fork` is up to date.

* Select the desired branch in the dropdown menu (this graphic shows dev branch)
* If the message indicates this branch is "behind", tap on the sync `fork` button and then the Update branch button

![message displayed when your fork of LoopWorkspace is behind LoopKit version](img/github-build-check-fork-status.svg){width="700"}
{align="center"}

### One-Time Changes

Look in this section for one-time changes for building dev with a browser that require special, one-time actions. 

**26-July-2023**

The `bundle ID` for the "`widget`" changed from "`SmallStatusWidget`" to the more descriptive "`LoopWidgetExtension`".

The table in LoopDocs (for main) will be updated after the next release.

For those using dev, you must follow these one-time steps:

1. Sync your fork to latest version of dev
1. Run the Action for Add Identifiers (this adds "`LoopWidgetExtension`" to identifiers)
    * Open the [Certificates, Identifiers & Profiles: Identifiers List](https://developer.apple.com/account/resources/identifiers/list) page.
    * Click on the "`LoopWidgetExtension`" identifier
    * Edit the App Group to include `group.com.TEAMID.loopkit.LoopGroup` where you use your `TEAMID`
1. Run the Action for Create Certificates
1. Run the Action for Build Loop


### Build `Branch`

If you want a branch to be the one you build all the time, you may choose to [Change Default `Branch`](#change-default-branch). This is not necessary except for special cases.

If you have one branch as default, for example main, and choose to build a different branch, there is an extra step when you `Build Loop`. Refer to step 4 in the graphic below. Use the branch dropdown menu to select the branch you want before hitting the green Run workflow button.

![build loop using github actions](img/action-04-build-loop.svg){width="700"}
{align="center"}

!!! 

## Change Default `Branch`

There can be several reasons why you would change your default branch.

* It can be convenient to have the branch you build most be configured as the default branch
* The branch you want to build has a different workflow than your default branch (not typical)
    * In this case, you **must** modify the default branch
    * Check the zulipchat conversation about the branch you are testing to see if it is necessary to make it default

These are the steps to modify the default branch.

For this example, we show how to change from a default branch of `main` to a default branch of `dev`. Note - only the owner of the repository can take this action and they must be logged in. Otherwise the Settings tab does not appear.

For the numbered steps below, refer to the graphic found under each group of steps.

1. Click on the Settings Icon near the top right of your LoopWorkspace
    * You may need to scroll down to see the `Default Branch` as shown in the graphic
    * Do not tap on the Branches tab to the left under Code and Automation, that is not the correct menu

    ![show default branch](img/gh-settings-branch-01.svg){width="700"}
    {align="center"}

1. To the right of the default branch name there is a pencil and a left-right arrow icon
    * Tap on the left-right arrow icon to bring up the `Switch default branch to another branch` dialog
1. Click on the dropdown next to the current default branch, in this example, `main`
1. Select the desired default branch, in this example, `dev`
1. Click on the `Update` button

    ![modify default branch](img/gh-settings-branch-02.svg){width="700"}
    {align="center"}

1. You will be presented with an are-you-sure question.
    * Click on the red `I understand, update the default branch.` button

    ![confirm default branch](img/gh-settings-branch-03.svg){width="400"}
    {align="center"}

Your default branch has been changed.

## Modify Automatic Building

For someone using [development code](#build-development-version) for their own use, they probably want to decide when to update their `fork` to the most recent commit. They can still have the advantage of automatic building without automatic updates. There may be other configurations someone would choose. These options are added to Loop 3.3.0 and later.

You can affect the default behavior:

1. [Modify Automatic Schedule](#modify-automatic-schedule)
1. [Disable Automatic Actions](#disable-automatic-actions)

### Modify Automatic Schedule

You can modify the automation by creating and using some variables.

To configure the automated build more granularly involves creating up to two environment variables: `SCHEDULED_BUILD` and/or `SCHEDULED_SYNC`. See [How to configure a variable](#how-to-configure-a-variable). 

Note that the weekly and monthly `Build Loop` actions will continue, but the actions are modified if one or more of these variables is set to false. **A successful Action Log will still appear, even if no automatic activity happens**.

* If you want to manually decide when to update your repository to the latest commit, but you want the monthly builds and keep-alive to continue: set `SCHEDULED_SYNC` to false and either do not create `SCHEDULED_BUILD` or set it to true
* If you want to only build when an update has been found: set `SCHEDULED_BUILD` to false and either do not create `SCHEDULED_SYNC` or set it to true
    * **Warning**: if no updates to your default branch are detected within 90 days, your previous TestFlight build may expire requiring a manual build

|`SCHEDULED _SYNC`|`SCHEDULED _BUILD`|Automatic Actions|
|---|---|---|
| `true` (or NA) | `true` (or NA) | keep-alive, weekly update check (auto update/build), monthly build with auto update|
| `true` (or NA) | `false` | keep-alive, weekly update check with auto update, only builds if update detected|
| `false` | `true` (or NA) | keep-alive, monthly build, no auto update |
| `false` | `false` | no automatic activity, no keep-alive|

### How to configure a variable

1. Go to the "Settings" tab of your LoopWorkspace repository.
2. Click on `Secrets and Variables`.
3. Click on `Actions`
4. You will now see a page titled *Actions secrets and variables*. Click on the `Variables` tab
5. To disable ONLY scheduled building, do the following:
    - Click on the green `New repository variable` button (upper right)
    - Type `SCHEDULED_BUILD` in the "Name" field
    - Type `false` in the "Value" field
    - Click the green `Add variable` button to save.
7. To disable scheduled syncing, add a variable:
    - Click on the green `New repository variable` button (upper right)
    - - Type `SCHEDULED_SYNC` in the "Name" field
    - Type `false` in the "Value" field
    - Click the green `Add variable` button to save
  
Your build will run on the following conditions:

- Default behaviour:
    - Run weekly, every Wednesday at 08:00 UTC to check for changes; if there are changes, it will update your repository and build
    - Run monthly, every first of the month at 06:00 UTC, if there are changes, it will update your repository; regardless of changes, it will build
    - Each time the action runs, it makes a keep-alive commit to the `alive` branch if necessary
- If you disable any automation (both variables set to `false`), no updates, keep-alive or building happens when `Build Loop` runs
- If you disabled just scheduled synchronization (`SCHEDULED_SYNC` set to`false`), it will only run once a month, on the first of the month, no update will happen; keep-alive will run
- If you disabled just scheduled build (`SCHEDULED_BUILD` set to`false`), it will run once weekly, every Wednesday, to check for changes; if there are changes, it will update and build; keep-alive will run

### Disable Automatic Actions

To enable the scheduled build and sync, the `GH_PAT` must hold the `workflow` permission scopes. This permission serves as the enabler for automatic and scheduled builds with browser build. To disable this, follow these steps:

1. Go to your [FastLane Access Token](https://github.com/settings/tokens)
1. If it says `repo`, `workflow` next to the `FastLane Access Token` link, then automatic building is enabled
1. To disable automatic update and build, click on the link to open the token detail view
    * Click to uncheck the `workflow` box
    * Click to check the `repo` box
1. Scroll all the way down to and click the green `Update token` button
1. Your token now holds only the `repo` permission

If you choose not to have automatic building enabled, be sure the `GH_PAT` has `repo` scope or you won't be able to manually build.

## Stop Building

What if I decide I don't want the automatic building feature?

* If you are using the released version of Loop, please leave automatic building running
    * Please read [TestFlight Automatic Updates](gh-deploy.md#testflight-automatic-updates) on how to configure TestFlight so you choose when the updated app gets installed on your phone
    * Otherwise, you may see the dreaded "Loop Beta has expired" message, have a Loop that won't open and not have a version ready to go in TestFlight that you can install within a few seconds

* If you are taking a break from Loop and want to stop monthly Build emails, consider disabling actions for the `Build Loop` action for your app.
    * [GitHub Directions to Disable and Enable a Workflow](https://docs.github.com/en/actions/using-workflows/disabling-and-enabling-a-workflow#disabling-a-workflow)
    * It is the Build action that kicks off the update and build steps, so simply disabling the one action is sufficient

* If you are done with Loop, you can delete the whole repository; but you should be sure about this because you'll need to start over with [Configure to Use Browser](gh-first-time.md) to restore ability to build Loop with GitHub.

## Historical Interest Only

### Historical One-Time Changes

You don't need this - it is left for historical reasons for people who have been following along with dev.

**26-July-2023**

The `bundle ID` for the "`widget`" changed from "`SmallStatusWidget`" to the more descriptive "`LoopWidgetExtension`".

The table in LoopDocs (for main) will be updated after the next release.

For those using dev, you must follow these one-time steps:

1. Sync your `fork` to latest version of dev
1. Run the Action for Add Identifiers (this adds "`LoopWidgetExtension`" to identifiers)
    * Open the [Certificates, Identifiers & Profiles: Identifiers List](https://developer.apple.com/account/resources/identifiers/list) page.
    * Click on the "`LoopWidgetExtension`" identifier
    * Edit the App Group to include `group.com.TEAMID.loopkit.LoopGroup` where you use your `TEAMID`
1. Run the Action for Create Certificates
1. Run the Action for `Build Loop`

**03-July-2023**

1. Libre support was added to dev (03 July 2023) using the LibreTransmitter code
    * This requires (one-time) that the `Actions` for `2. Add Identifiers` and `3. Create Certificates` be run before attempting `4. Build Loop`
    * The LibreTransmitter code requires `Near Field Communication` and doing these steps automatically adds the required capability
1. Automatic update and automatic monthly build was added to dev (13 July 2023)
    * Once a month, *GitHub* will attempt to update and build Loop from your `default branch` using the instructions in the `Action: 4. Build Loop` (`build_loop.yml` file) and send the new app to *TestFlight*
    * As part of this monthly build, *GitHub* will check to see if updates are required for your `default branch`
    * When updates are not required, it just builds the app
    * When updates are required:
        * If it can figure out how to do the `sync` automatically, it does so
        * If it cannot figure out how to do the `sync` automatically, the `Action` to `4. Build Loop` will fail and you will need to take manual steps
    * You will get an email that the `Build` either succeeded or failed

!!! info "Automatic Update Requirements"
    To enable the automatic update and rebuild, two steps are required. These are one-time steps.

    * The GH_PAT must be updated (not regenerated) to add `workflow`
        * Examine your [`FastLane Access Token`](https://github.com/settings/tokens)
        * If it says `repo, workflow`, then no further action is needed for your GH_PAT
        * If it say `repo` only, then click on the `FastLane Access Token` link, click to add a check to the `workflow` box and scroll all the way down to select the green `Update token` button
    * A new branch called `alive` must be created from the LoopKit `dev` branch
        * This is now created automatically for you

### Create the `alive branch` Manually

The `alive branch` will receive some additional commits to its history. This is part of automating the process. The `alive branch` is not used for building the app. You do not need to interact with it. Make sure you don't already have an `alive branch`. If you do and you are getting errors, then delete the `alive branch` and try again.

1. Go to the `Code` tab of your `repository`
1. Click the `branch` icon dropdown button, and then View all branches
1. Click the green `New branch` button (upper right)
1. Type `alive` in the `New branch name` field
1. Select `LoopKit/LoopWorkspace` as `Source`
1. Select `dev` in the `branch` dropdown.
1. Click the green `Create new branch` button