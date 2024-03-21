# Exploratory Testing for the Monefy Android App (Free Version)

## Scope of the Exploratory Testing

Test object: Monefy Android App for Android, lite (free) version

Tools for testing: Xray Exploratory App
The test sessions will be executed with the app installed on a real mobile phone, downloaded directly from the Google Play Store.

## Charters

### Charter 1 - New incomes\expenses
Explore new incomes and new expenses to verify if the stored data is consistent with the user data

Time limit: 45 min

### Charter 2 - Data Backup
Explore the Data Backup section to verify if the backup function is reliable

The Data Backup can be found at: Options Menu- Settings -  Data Backup

Time limit: 45 min

### Charter 3 - Balance Chart
Explore the balance chart to check its usage is intuitive and user-friendly.

Time limit: 45 min

## Findings from the charters.

### Charter 1
I missed that the currency couldn't be displayed using the currency default decimal separator. For instance, 100 Brazilian reais are usually expressed as R$100,00, but this doesn't happen in the app.

### Charter 2
Timestamps are stored using the regional format of the system. It's better to transform timestamps into a standard format.

### Charter 3
* Resizing the chart was annoying and not the most intuitive.
* Rotating the screen caused the chart to display some elements out of their correct place for milliseconds after te rotaion. It was fixed after less than a second.

  
## Prioritisation

I listed some of the risks I identified:

ID  | Risk         | Type          | Likelihood    | Impact
----| ------------ | ------------- | ------------- | -------------
1 | App might not meet user's needs | non-functional | Low | Critical
2 | Non user-friendly | non-functional | Medium | Major
3 | Main functionalities not working | functional | Low | Critical
4 | Error on handling inputs | functional | Medium | Moderate
5 | Performance issues | system risk | Medium | Moderate
6 | Security Issues | system risk | Low | Critical
7 | Data Backup | system risk | High | Moderate
8 | Data Restoring | system risk | High | Moderate

As the APP is already up and running, business risks are out of the scope.

Due to the constraint of time, I selected the above-listed charters as they cover some of the most important features and they will help to mitigate some of the risks identified in the table.

I would start with checking the balance chart. It's the first thing that users will notice and it must be flawless in its design and on its functionalities. So we would be partially mitigating risks #1, #2 and #3

Then, I'd check the process of adding expenses and incomes. It's also a core functionality that must be user-friendly and user error proofing. So, risks #3 and #4 are covered in this charter.

Last, the option to save in the cloud. It's an important functionality and exploring it would help to mitigate risks #6, #7 and #8

## How much time you have planned for each charter?

As mentioned in the charters themselves, 45 minutes for each. It's not the standard value but it fits our objective

## What kind of risks you need to mitigate for this type of application?

Functionality risks, UI-based risks, storage risks, security risks.
