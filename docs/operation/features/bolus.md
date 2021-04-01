# Bolus

![Loop toolbar](img/toolbar-bolus.svg){width="300"}
{align="center"}

Bolus entries can be made manually through the bolus tool (double orange triangles) in the toolbar, either as part of a meal bolus or as a correction for a high BG.

## Meal Bolus

[Click here for Meal Entry](carbs.md)

## Correction Bolus

Loop reassesses your insulin needs every time a new BG reading is detected, typically every 5 minutes. If Loop predicts that your BG will be above the high end of your correction range at the end of the Duration of Insulin Activity (DIA) and that your BG will not dip below the suspend threshold at any point during that time period, it will calculate a Correction Bolus. Loop will not give an alert when a correction bolus is being recommended, the bolus entry tool must be clicked to check for one. The Loop pill in Nightscout will display when Loop is recommending a correction bolus.

* If you are using the master branch or the automatic-bolus branch with `Dosing Strategy` set to `Temp Basal`
    * Loop will provide increased temp basals for as long as it takes to bring predicted BG into range
    * The increased temp basals are subject to your Delivery Limits.
    <br/><br/>

* If you are using the automatic-bolus branch with `Dosing Strategy` set to `Automatic Bolus`
    * Loop will automatically deliver 40% of the correction bolus at each successive loop interval
    * Each automatic bolus is subject to your Delivery Limits


## Starting Bolus Notification

When the phone is in portrait mode, a bolus status line will appear below the Heads Up Display when Loop is sending a bolus command to the pump. The "starting bolus" indicator is shown in the figure below.

![Bolus status indicator](img/bolus-start-progress-cancel.svg){width="900"}
{align="center"}

Once the bolus begins, the bolused xx of yy with the circle display begins. If you change your mind, just click on the bolus status line to cancel your bolus.  If you see a 'pump is suspended notice' in the bolus status line after cancelling your bolus, just tap on it to resume pump operations.


## Bolus Failure Notifications

On occasion, you will receive notification that a bolus may have failed. If you're using AB, this can often be because a bolus is already being delivered. In some of these cases, the bolus was delivered. On a Medtronic pump, you should check the pump screen to verify the bolus status before attempting to redeliver a failed bolus.  Omnipod users can hear the clicks if the room is quiet enough.

If you get an uncertain delivery message, you may still see the "bolused xx of yy" display continue for as long as it would have taken to actually deliver the bolus. This display is driven by a timer and logic on the phone. (Loop is not asking the pump repeatedly - "are you done yet"). Loop has mostly been updated so that the next time it contacts the pump it determines whether that bolus actually went through or not and will update the screen.  Look at the Event History screen (accessed by tapping the Active Insulin or Insulin Delivery plots).

If the uncertain delivery is not resolved by the next cycle or by doing a Read Pod Status for Pod or Get Recent History for Medtronic, please tap on Loop Settings, Issue Report and email it to yourself. Then post on Facebook or Zulipchat, explain what happened and say you have an Issue Report. Someone should reach out to you.
