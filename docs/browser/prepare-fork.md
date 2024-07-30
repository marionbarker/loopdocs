## Prepare your Repository

### Fork LoopWorkspace

??? abstract "Section Summary (click to open/close)"
    Fork [https://github.com/LoopKit/LoopWorkspace](https://github.com/LoopKit/LoopWorkspace){: target="_blank" } into your account.

    [<span class="loop-bigger">:material-skip-forward:</span>](#configure-secrets) To skip the detailed instructions, click on [Configure <code>Secrets</code>](#configure-secrets)

!!! warning "Existing Fork"
    If you already have a fork of <code>LoopWorkspace</code>, click on [Already Have LoopWorkspace](#already-have-loopworkspace) to decide what to do. That section provides links to return you to these instructions.

1. Click this link [https://github.com/LoopKit/LoopWorkspace](https://github.com/LoopKit/LoopWorkspace){: target="_blank" } to open the <code>LoopWorkspace</code> repository owned by `LoopKit`
1. Review the highlighted locations of the graphic below (yours won't look quite like this yet, but the `Fork` button is in the same place)
1. At the upper right side of the screen, click on the word `Fork`
    * If you already have a fork, you cannot proceed, see [Already Have a LoopWorkspace](#already-have-loopworkspace)
1. Now your screen should look like the graphic below
    * Your username will be automatically filled in as the owner (`Owner`)
    * <code>LoopWorkspace</code> is the repository name (`Repository Name`)
    * Leave the selection that says "`Copy the main branch only`" checked
    * Click on the green `Create fork` button

    ![fork information for LoopWorkspace](img/gh-fork-loopworkspace.svg){width="700"}
    {align="center"}

#### Successful Fork

After creating the &nbsp;<span class="notranslate">fork</span>, your screen should be similar to the next graphic - it will say `main` for the branch instead of `dev` because this graphic was prepared before the release of `Loop 3`. You may or may not see the messages you are told to dismiss in the next two bullets. No worries if you don't see them.

* Near the top right, click on the close button :octicons-x-16: (`x`) to dismiss the `Successfully fetched` message
* In the middle, click on the `Dismiss` button to remove the "`Your branch is not protected`" message

![after creating the fork LoopWorkspace](img/gh-initial-fork-dismiss.png){width="500"}
{align="center"}

Carefully compare your screen to the graphic below paying attention to the highlighted sections.

* Note that your username is now showing
* The comment under your username indicates where the &nbsp;<span class="notranslate">fork</span>&nbsp; came from (that is a clickable link)
* The branch that is selected :octicons-git-branch-16: is `main`
* The message says "`This branch is up to date with LoopKit/LoopWorkspace:main`"

![after creating the fork LoopWorkspace](img/gh-after-fork.svg){width="700"}
{align="center"}

## Configure <code>Secrets</code>

??? abstract "Feeling confident? Planning to build more than one app? Click to see more."
    If you are already feeling overwhelmed - skip this tip.

    If you plan to build more than one app, you will be making a fork of each repository associated with each app, and then you must add the 6 <code>Secrets</code> to each repository. It is not hard but it can get tiresome.

    There is a way to enter the 6 <code>Secrets</code> only one time for all your repositories, but this requires setting up a free GitHub organization. This is also not hard, but it modifies some of the displays you see on GitHub. If you are interested, refer to [Use a GitHub Organization Account](other-apps.md#use-a-github-organization-account){: target="_blank" }

??? abstract "Section Summary (click to open/close)"
    These <code>Secrets</code> are the same for any repository for which you use `GitHub Browser Build`.

    * They are added once for a repository and work for all branches of that repository
    * They must be added to any other repository, such as <code>Loop Caregiver</code>, for which you also use `GitHub Browser Build`

    For each of the following <code>Secrets</code>, tap on "New repository secret", then add the name of the secret, along with the value you recorded for it:

    * `TEAMID`
    * `FASTLANE_ISSUER_ID`
    * `FASTLANE_KEY_ID`
    * `FASTLANE_KEY`
    * `GH_PAT`
    * `MATCH_PASSWORD`

    [<span class="loop-bigger">:material-skip-forward:</span>](identifiers.md#validate-secrets){: target="_blank" } To skip the detailed instructions, click on [Validate <code>Secrets</code>](identifiers.md#validate-secrets){: target="_blank" }.

!!! tip "`Branches` and `Repositories`"
    * These &nbsp;<span class="notranslate">Secrets</span>&nbsp; are added to your `fork of LoopWorkspace` and work for any `branch` (`main` or `dev`, for example)
    * These &nbsp;<span class="notranslate">Secrets</span>&nbsp; must be added, if desired, for [Other App](other-apps.md){: target="_blank" } `repositories`

### Prepare to Enter <code>Secrets</code>

Log into *GitHub*.

1. Return to your forked copy of <code>LoopWorkspace</code>
    * Click on your personal icon at the upper right to see the dropdown menu and select "`Your repositories`"

    ![dropdown-menu](img/gh-quick-access.png){width="200"}
    {align="center"}

1. Click on <code>LoopWorkspace</code> to open that repository
1. Click on the Settings Icon near the top right of your LoopWorkspace
    * If you don't see ⚙️ `Settings`, make your browser wider or scroll to the right
    * If you still don't see ⚙️ `Settings`, then you are **not** on your fork or you need to sign in to your *GitHub* account
    * After you click on ⚙️ `Settings`, your screen should look like the graphic below

        ![settings screen](img/gh-settings.svg){width="700"}
        {align="center"}

1. On the left side, find the `Secrets and variables` dropdown and choose <code>Actions</code>
    * After you select <code>Actions</code>, your screen should look like the graphic below

        ![action secrets and variables screen](img/gh-actions-secrets.svg){width="700"}
        {align="center"}

### Enter the <code>Secrets</code>

1. Tap on the green button at the top right of your screen labeled `New repository secret` (highlighted above)
    * A new screen appears as shown in the first graphic below
    * Do not do anything until reading the sub-bullets, examining the graphics, and proceeding to the next section where each `Secret` name is provided for you to copy and paste
        * Under `Name *`, click on `YOUR_SECRET_NAME` and paste one of the 6 secret names, as directed in [Enter Each Secret](#enter-each-secret)
        * Click inside the `Secret *` box and paste the value for that secret
        * Once you click on `Add Secret`, the secret will be added
        * The second graphic below shows `TEAMID` added and ready for save

![dialog for entering a new secret](img/new-secret-dialog.png){width="700"}
{align="center"}

![teamid secret ready to be saved](img/teamid-secret-ready-to-save.png){width="700"}
{align="center"}

#### Enter Each Secret

Enter the name of each <code>Secret</code> found in [Save Your Information](intro-summary.md#save-your-information) and your value for that `Secret`.

* Once you save a secret value, you will not be able to view what you entered, so check carefully before you hit `Add Secret`
    * You can replace the value for any secret later - but you can't view the saved value
* Be especially careful with your `TEAMID`
    * If `TEAMID` is incorrect, the initial `Actions` will succeed but `Build Loop` will fail and you will have some clean-up to do

You can copy the names of the <code>Secrets</code> by hovering to the right of each word below until you see the copy button (:material-content-copy:). Click on the button to copy the `Secret` name and paste it into *GitHub* where you see `YOUR_SECRET_NAME`. This avoids spelling errors.
``` { .text .copy }
TEAMID
```
``` { .text .copy }
FASTLANE_ISSUER_ID
```
``` { .text .copy }
FASTLANE_KEY_ID
```
``` { .text .copy }
FASTLANE_KEY
```
``` { .text .copy }
GH_PAT
```
``` { .text .copy }
MATCH_PASSWORD
```

* For the `FASTLANE_KEY` value, copy the entire contents from<br>`-----BEGIN PRIVATE KEY-----`<br> through<br>`-----END PRIVATE KEY-----`<br>
* For `MATCH_PASSWORD` value - if you did not already make up a password and save it with your other <code>Secrets</code>, do it now
    * The `MATCH_PASSWORD` must be the same for any repository using this method ([Other Apps](other-apps.md){: target="_blank" })

Once all six <code>Secrets</code> have been added to your <code>LoopWorkspace</code>, your screen should look similar to the graphic below.

* Check that all of your <code>Secrets</code> are spelled correctly
* If one is misspelled, delete it and add a `New repository secret` with the correct name

![all secrets entered](img/gh-done-adding-secrets.png){width="700"}
{align="center"}

## Next Step

The next step is to [Validate Secrets and Add Identifiers](identifiers.md).

## Extra Steps

Most people won't need the information on the rest of this page.

### Already Have&nbsp;<span translate="no">LoopWorkspace</span>?

Some people may already have a copy of <code>LoopWorkspace</code>.

If your copy is **not** from `LoopKit`, follow the [Delete and Start Fresh](#delete-and-start-fresh) directions.

If your copy is from `LoopKit`:

* Open your <code>LoopWorkspace</code> repository (`https://github.com/username/LoopWorkspace`) where you use your *GitHub* `username` in the URL
* Review the graphic in the [Configure: Successful Fork](#successful-fork) section
    * Make sure all the items highlighted by red rectangles are correct with the possible exception of your fork being up to date
* If you see a message that your *fork* is not up to date - tap on the `Sync fork` button and follow the instructions
* Continue with [Create `GitHub Personal Access Token`](secrets.md#create-github-personal-access-token)

#### Delete and Start Fresh

If your fork is not from `LoopKit`:

* Delete your LoopWorkspace repository
    * Instructions to delete a repository are found at [*GitHub* Docs](https://docs.github.com/en/repositories/creating-and-managing-repositories/deleting-a-repository){: target="_blank" }
* Return to [Fork LoopWorkspace](#fork-loopworkspace) and follow all the instructions

### Delete Identifiers

When you have already built the *Loop* app with *Xcode*, the Identifier names will not match the directions and you might have trouble deciding which ones to configure.  Your existing `Loop` identifier will have a name that starts with `XC` as shown below, where your 10-digit `TEAMID` is used.

* `Name: XC com TEAMID loopkit Loop`
* `Identifier: com.TEAMID.loopkit.Loop`

The `Identifier` that is associated with the `Loop` identifier cannot be deleted if it is already in the *App Store* but all others can. If you attempt to delete the `XC` *Loop* identifier, you may be told it cannot be deleted because it is in use in the app store. That's OK. Same for other identifiers (if you build a bunch of Apps). If a `Bundle ID` has ever been associated with an app in the *App Store*, you cannot delete the `Identifier`.

To make it easy when configuring the identifiers, go through and delete as many as you can.

* Open this link: [Certificates, Identifiers & Profiles: Identifiers List](https://developer.apple.com/account/resources/identifiers/list){: target="_blank" } on the *Apple Developer* site.
* Use the graphic below as a guide to removing identifiers
* Keep repeating the steps until you've removed all the identifiers you can (or want to) delete
* It is OK to delete an identifier even if it does have your correct `TEAMID`
    * If you try to delete the `Loop` identifier with your `TEAMID`, it will refuse, don't worry, just keep going
* Note - this graphic indicates where on this page you can find your `TEAMID`
    * If you notice an identifier with a value embedded in it that does not have your `TEAMID`, then delete it if you can and [Update <code>Secrets</code>](bb-update.md#update-secrets) with your correct `TEAMID`
    * If you try to delete a Loop identifier that does not have your `TEAMID`, but you already added to the *App Store*, it will refuse, don't worry, just keep going
    * Delete all the other identifiers first that have the same incorrect `TEAMID` and then try to delete the Loop identifier with the incorrect `TEAMID`

![steps to delete a given identifier](img/delete-identifiers.svg){width="700"}
{align="center"}

If coming here from the Errors with Browser page because you enter the wrong `TEAMID` in `Secrets` - return to that page once you've deleted as many identifiers as you can: [Errors: Wrong TEAMID in Secrets](bb-errors.md#error-wrong-teamid-in-secrets).

If you were just trying to clean up the identifiers, then follow these steps:

* Run Action: [Add Identifiers](identifiers.md#add-identifiers){: target="_blank" } to add Identifiers with the documented short names
* If you did not complete the [Add `App Group` to Identifiers](prepare-app.md#add-app-group-to-identifiers){: target="_blank" }
* If you did not complete the [Create Loop App in App Store Connect](prepare-app.md#create-loop-app-in-app-store-connect) step, do it now
* Continue with [Create Certificates](certs.md#create-certificates){: target="_blank" } and then [Build the *Loop* App](build-yml.md#build-the-loop-app){: target="_blank" }
