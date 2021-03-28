# Bolus

![img/toolbar.png](img/toolbar.png){width="300"}
{align="center"}

Bolus entries can be made manually through the bolus tool (double orange triangles) in the toolbar, either as part of a meal bolus or as a correction for a high BG.

## Meal Bolus

[Click here for Meal Entry](carbs.md)

![img/below-min.svg](img/below-min.svg){width="300"}
{align="center"}

## Correction Bolus

Loop reassesses your insulin needs every 5 minutes, also known as a Loop interval.  If Loop is calculating that your BG will not be able to stay within your correction range through the use of high temp basals alone within 30 minutes, you will see a Recommended amount to bolus when you click on the Bolus tool, this Recommended bolus is known as a “correction bolus”.

If you are using the Master branch, correction boluses will not be delivered automatically, they must be delivered by you, the user. Loop will not give an alert when a correction bolus is being offered, the bolus entry tool must be clicked to check for one. The Loop pill in Nightscout will display when Loop has a recommended bolus calculated. In a well-tuned Loop with decent carb counting, correction boluses should be infrequently needed.  If you are not continually clicking on the bolus tool and happen to miss the recommended correction bolus, Master branch will increase your temp basals for as long as it takes to deliver the required insulin (and of course, reassessing this decision every Loop interval).

If you are using AB, Loop will deliver the recommended bolus via either temp basals or boluses, depending upon your Dosing Strategy.

## Starting Bolus Notification

A new status line will appear when Loop is sending a bolus command to the pump. Just above the main screen's glucose chart, you will see a "starting bolus" indicator.

![img/starting_bolus.png](img/starting_bolus.png){width="300"}
{align="center"}

## Bolus Failure Notifications

On occasion, you will receive notification that a bolus may have failed. In some of these cases, the bolus actually will begin delivery. On a Medtronic pump, you should always check the pump screen to verify the bolus status before attempting to redeliver a failed bolus.  Omnipod users should .....
