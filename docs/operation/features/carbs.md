# Meal Entry (Carbs, Proteins and Fats)

![Loop toolbar](img/toolbar-meal.svg){width="300"}
{align="center"}

To start a new meal entry, tap on the green meal icon in the toolbar at the bottom left of the status screen. Your Loop app will open to Add Carb Entry screen, but you should think of this as a meal entry. Many Loopers increase the carbohydrate grams amount to cover the expected effect of protein and adjust the expected absorption time for fat. For simplicity, the rest of this page just refers to carbs because all the figures show carbs or carbohydrates in the menus.  

Below are step by step instructions on how to record meals in Loop, but first, here are a few methods that you cannot use: you cannot use your pump's bolus wizard, you cannot use your pump's carb entry screen, and you cannot use Nightscout's careportal.

![Add a carb entry](img/add-carb-entry.svg){width="900"}
{align="center"}

## New Meals

Once you're in the Add Carb Entry screen, to start recording your meal, simply enter the desired number of carbs in the `Amount Consumed` line.  

The default `Date` is the current date and time, but you can easily scroll the time forward or back.  If you had inadvertently missed recording an earlier meal, just scroll the time back to when that food started to absorb.  If you want to prebolus some portion of the meal that you're about to eat, just scroll the time forward.  You can prebolus part of your meal with the current time, and then record a second entry by scrolling the time forward for an hour or two to prebolus for a steak that may not start absorbing right away.  

Next, you'll want to select your Food Type. This is not required - you can just accept the default and keep going. Initially, there are 4 options: lollipop, taco, pizza and plate.  The default food type is taco, which has a default absorption time of 3 hours. You can either tap on the food icon that most closely resembles what you're eating, or tap on the plate to reveal even more food icons.  Pick the lollipop if the food that you're going to be eating has a 2 hour absorption, the taco for 3 hour absorption or the pizza for 4 hour absorption.  If you tap on plate, there are lots more food icons for you to choose from, and they're arranged based upon how long each food takes to absorb, OR you have the option to tap on the `abc` that appears in the lower left corner and manually type in your food entry.  

The next step is to set your `Absorption Time`. You can accept the default absorption times of 2, 3 or 4 hours OR you can enter any time that you'd like up to 8 hours. Loop will initially estimate your absorption time at 150% of the time that you enter.  As a result, carbs entered using the taco icon will initially be treated as 4.5 hour absorption.  As Loop observes the BG impacts of the meal, Loop will shorten the meal's absorption time or increase the number of carbs to be absorbed, as well as adjust insulin delivery.  

You do not have to enter all carbs for a meal at the same absorption or eating time.  If you want to enter some of the meal's carbs as faster and some as slower, you can log the meal over several individual entries.  For example, for meals that have sugary carbs as well as slow acting carbs (Chinese food), you may want to do record some carbs as lollipop and some as pizza. Another example would be steak and potatoes, you may want to record the potatoes with a current start time and taco absorption and the steak with a start time of 1-2 hours into the future and a 5 hour absorption time.

When you are done recording a given food entry, press `Continue` and the Meal Bolus tool will open.  

![Record a meal bolus](img/meal-bolus.svg){width="900"}
{align="center"}

You can tap on the `Recommended` line and that value will be transferred to the Bolus line, OR tap on 0.0u on the `Bolus` row and type in your desired bolus amount OR `Save Without Bolusing` The `Save Without Bolusing` option is used if you'd like to add to your meal entry or do not want to accept a bolus right now.  The meal entry is NOT saved until you either `Deliver` or `Save Without Bolusing`. The graph at the top of the Meal Bolus screen will show your BG prediction based upon your meal entry and desired bolus amount. You can adjust your desired bolus amount or click `<Carb Entry` to adjust your meal entry and then return to Meal Bolus to see how your BG prediction changes.  When you're ready to bolus, click `Deliver`.  If you start a bolus and plan to add additional meal entries, you will probably need to `Save without Bolusing` for the next entry because Loop will be in mid-bolus.  After entering the rest of the meal, don't forget to [bolus manually](bolus.md).

![Bolus when below correction range](img/below-min.svg){width="300"}
{align="center"}

If your BG is below your correction range, Loop's Recommended bolus will have a small warning above it stating that "Current glucose of xx is below correction range".  You can either skip the bolus OR enter a portion or all of the Recommended bolus.  If your BG is below your suspend threshold, Loop will not recommend a bolus.  If this happens, you can calculate the bolus using your carbohydrate ratio and enter a portion or all of this amount OR you can set a 15 minute timer and wait for your BG to start to rise and then reassess when and how much to bolus.

## Automatic-Bolus (AB) Branch

Loopers who are using AB still typically prebolus and/or  bolus for meals. The amount of `Recommended` insulin that will appear in the Meal Bolus screen will be the full amount of the bolus (not 40%).  As discussed above, you can accept this recommendation or enter a different amount, however, and this is **very important**, if your Dosing Strategy is set to Automatic Bolus, by entering less than the recommended amount and tapping `Deliver` or tapping `Save Without Bolusing`, you are telling Loop to deliver the remaining recommended insulin in the future using 40% of recommended bolus at each successive Loop interval.

## Edit Meals

You can watch the progression of the Loop's observations of your meal by tapping on the Active Carbohydrates chart at the bottom of Loop's main screen and watching the insulin counteraction effects (ICE) on the Carbohydrates screen to see the same-day history of the meals that you have recorded.

![Edit a carb entry](img/edit-carb-entry.svg){width="900"}
{align="center"}

The information available on the Carbohydrates screen disappears for any meals not still active at midnight, so if you're looking for details as to how a particular meal absorbed, you need to screenshot or otherwise capture this information before midnight. Previous entries can be modified or deleted through this screen. To adjust an entry, simply tap on it (you don't need to tap the `Edit Carb Entry` at the top of the screen). You can change a prebolus time, add/subtract carb entries, or adjust absorption times (even mid-meal). To delete an entry, you first tap `Edit Carb Entry` and tap on the red circle to the left of the entry that you would like to delete. It is a little counterintuitive, but the `Edit Carb Entry` button let's you delete, but not edit an entry. Adjusting a meal entry can be a particularly useful tool when:

* You did not finish an entire meal that you bolused for,
* You did not get to eat the meal at the time you originally expected,
* You ate more servings than originally entered, or
* You suspect your carb count was in error because BGs are rising more/less than expected.<br/><br/>

![Delete carb entry](img/delete-carb-entry.svg){width="900"}
{align="center"}

## Avoid Double Meal Entries

!!! info "Be Aware"
    If you have accidentally made duplicate entries for the same meal, click on the Active Carbohydrates chart in the main Loop screen and tap `Edit Carb Entry` to delete the redundant entries.  Deleting the meal entry will not impact the insulin that has already been delivered, but it will alert Loop to adjust your BG projection for purposes of calculating future insulin delivery.

## Third Party Apps

If you use a 3rd party app, such as My Fitness Pal, to enter and track carbs and that app also stores the carb values in Apple Health, Loop will read those values from Apple Health and use them in calculating temp basal rates. Entries from 3rd party apps cannot be removed from within Loop.  You will have to edit them in the third party app, or from the Health app. Because of this potential for confusion, it is recommended to turn off Loop's ability to read other apps' carbohydrate data from with the Health app. You are asked if you want to enable this when Loop is first installed. After installation, you can also go to the Settings App -> Privacy -> Health -> Loop and scroll down to the Allow Loop to Read Data section to turn off `Carbohydrates`.

## Carb Absorption Model

More information about the way Loop models the [Carbohydrate Effect](../algorithm/prediction.md#carbohydrate-effect) can be found the algorithm page.
