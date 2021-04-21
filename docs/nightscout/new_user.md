# New Nightscout Users

!!! info "Is Nightscout Required for Loop?"

    Nightscout is not required, but is recommended for Loop.

    - A Nightscout site provides a dashboard for remote viewing of Loop actions including the temporary basal rates Loop is setting, the current insulin on board, or a recent bolus and carb entry
    - A Nightscout site provides reports for retrospective review of your settings
    - You will want a Nightscout site:
        - If you are a parent of a little Loop user
        - If you want to see Loop's actions anywhere other than the Looper's iPhone
        - If you want to ask a mentor for help adjusting your settings

There are two options for setting up Nightscout; one option requires a small fee but automates both the setup and periodic updating, the other option can be "free" or lower cost but requires your effort to build and update. You choose which works best for you. Isn't it nice to have options?

## T1Pal (paid service)

[T1Pal is a paid NS hosting](https://t1pal.com/) company.  There is a hosting fee required which is used to help ensure Nightscout runs without limits and receives improvements.  Setup is simple and loop plugins are configured automatically during the setup guide.

* Select [Get Started](https://www.t1pal.com/getting-started/starting/home) to register an account at [T1Pal](https://www.t1pal.com/).  You will need to enter your credit card, which helps ensure Nightscout is running correctly.
* Select "visualize treatments" in the setup menu and select "loop."

![img/t1pal_configure.png](img/t1pal_configure.png){width="450"}
{align="center"}

## Traditional DIY

The [Nightscout](https://nightscout.github.io) documentation points to a free hosting option using Heroku, but "free" may come with a cost.  Please read this thoughtful article [Remember, #WeAreNotWaiting not #ItsAllFree](https://www.diabettech.com/wearenotwaiting/remember-wearenotwaiting-not-itsallfree/).

The free options have data quotas monthly and shorter-term CPU quotas.  If you exceed those quotas, you may be facing a monthly data-use bill or being locked out of NS for about 12 hours until the quotas reset.  As you start to use Nightscout more intensively for alarms, watches, etc., it is possible that you may exceed your quotas. If you can afford to pay a monthly fee to increase those caps, then you may choose to do so.

### Setup Nightscout

The documentation and instructions for building your own Nightscout site have recently been completely overhauled and are WONDERFUL!

Please visit [The Nightscout site](https://nightscout.github.io) to read the introductory material and then proceed to the Installation page for directions on how to set up your new Nightscout website.

### Add Loop variables to Nightscout

There are a few Loop-specific variables you should configure to get the most out of your Nigghtscout site. Follow the [instructions to retrofit an existing Nightscout site](update_user.md#step-2-editadd-config-vars).

## Add Nightscout to Loop

Once you finish setting up your new Nightscout site, don't forget to [enter the website into your Loop settings](../operation/loop-settings/services.md#nightscout)! This way Loop will have access to your Nightscout site to upload all the wonderful data.

## Troubleshooting

If your Nightscout site is not showing CGM (and Loop, if you are Looping) data within about 10 minutes of finishing your setup, then please follow these steps [here](troublehoot.md) to troubleshoot.
