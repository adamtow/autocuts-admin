
# Autocuts and the Autocuts Admin
Autocuts is a background shortcut manager for iOS 13. It runs silently behind the scenes while you use your iOS device throughout the day, intelligently running shortcuts in the background based on triggers such as time, location, web activity and more. Best of all, it executes your shortcuts with absolutely zero tapping of confirmation buttons. 

For those of whom who have wanted Personal Automations in iOS 13 to be a little more, say, automated, Autocuts is the shortcut you need to use!

## Requirements, Download and Installation

Autocuts is made up of two primary shortcuts, with two additional shortcuts being critical must-have add-ons you will want to have installed on all of your iOS devices: 

- **Autocuts**: the background shortcut that runs continually as you use your iOS device via the Open App personal automation feature of Shortcuts in iOS 13.1. 
- **Autocuts Admin**: the shortcut for creating, viewing, and managing your list of background shortcuts. 
- **LimitKit**: an event logging and rate limiter for shortcuts. LimitKit allows you to run your shortcuts on a pre-set cadence such as once a minute, five minutes, thirty minutes, hour, week, or more. 
- **Location Triggers**: shortcut that manages all of your location-based shortcut triggers. 

## How it works
Autocuts takes advantage of the Open App personal automation feature of Shortcuts in iOS 13.1. By using your iOS device like you normally do throughout the day, Autocuts will be constantly running in the background, where it is responsible for running other shortcuts in the background. 

You can also connect third-party web services such as IFTTT, Zapier, and Dropbox directly with your iOS device. A triggered event from the web can create an Autocut file that will automatically run a shortcut on your device. 

You can even deliver Autocut files to other iOS users and run shortcuts remotely on their own devices!


### Advanced
Visit Autocuts Admin's Settings page for additional options for controlling Autocuts.

- Verify Shortcuts: When checked, Autocuts Admin will generate a list of shortcuts that Autocuts will match against when running. If a shortcut does not exist, it will not run.
- Log Activity: Autocuts will write a log file of its activity on iCloud Drive > Shortcuts > Autocuts > log-{devicename}.txt.
- Notify After Evaluation: When run, Autocuts will notify you of the Autocuts it ran, skipped, or removed

## What is an Autocut?
An Autocut is a text file stored on iCloud Drive or Dropbox that instructs Autocuts to run a shortcut automatically while you use your iOS device during the day. Each Autocut has the following properties
- shortcut: the shortcut to run.\n\n• date: the date and time that an Autocut can first be run.
- expires: the amount of time in minutes after the scheduled date that an Autocut can still be run. Shortcuts of expired Autocuts will not run. Autocuts can also be set to never expire.
- device: the name of the iOS device that can run this Autocut. Leave blank to run the Autocut on any device.
- activate: set to true to open the Shortcuts app before running the Autocut's shortcut. Used for those shortcuts that do not run properly in the background.
- input: text input that will be sent to an Autocut's shortcut when run.

## Creating Autocuts
Autocuts can be created in a number of ways. Any shortcut or application that can write to the Shortcuts folder on iCloud Drive or a Dropbox folder can create an Autocut.

Some examples include:

- Autocuts Admin: the shortcut you are using now features an assistant that walks tou step-by-step in creating an Autocut.
- API: Send the Autocuts Admin a specially-formatted dictionary to create and schedule Autocuts from a third-party shortcut.
- IFTTT or Zapier: any trigger can write an Autocut text file to an Autocuts Dropbox source folder.


## Destination Services        
Destination services deliver Autocuts to local and remote sources. Autocuts Admin supports the following destination services:

- iCloud Drive: a folder within the Shortcuts folder on iCloud Drive. Make sure to add this folder path as a source if you want Autocuts on this device to process them.
- Dropbox: A folder on Dropbox where to store your Autocut files. Make sure to add this folder path as a source if you want Autocuts on this device to process them.
- IFTTT: Requires a Maker Webhooks Event name and API key to send a webhook to IFTTT which should create an Autocut file on Dropbox.
- Zapier: Requires catch hook URL to send an Autocut to Zapier. The Zap should then create the Autocut file on Dropbox.

## LimitKit
By default, the Open App personal automation will cause Autocuts to run every time you open one of the selected apps.

LimitKit allows you to control the frequency at which Autocuts will perform its evaluation.

For example, you can configure Autocuts to run every minute, five minutes, thirty minutes, or hour. While it is in-between evaluation periods, Autocuts will exit much more quickly when run from the Open App personal automation.


In order to run shortcuts automatically in the background, you need to have the Autocuts shortcut installed.

With Autocuts Admin, you can create, manage, and view all shortcuts that are scheduled to run automatically as you use your iOS device throughout the day.Tap Install Autocuts from the Autocuts Admin Home screen to get the latest version of Autocuts.

## Getting Started
"To run your shortcuts automatically, Autocuts must be configured to run each time you open your most commonly used apps.

1. Tap **Automation** in Shortcuts.
2. Tap the **+** button.
3. Tap **Create Personal Automation**.
4. Choose **Open App**.
5. Select the apps you use often and tap **Done**. 
6. Tap **Next**.
7. Tap **Add Action**.
8. Add a **Run Shortcut** action and set it to Autocuts.
9. Tap **Show More** and disable **Show While Running**.
10. Tap **Next** and disable **Ask Before Running**.
11. Tap **Done**.

![Autocuts Setup #1](https://adamtow.github.io/autocuts-admin/images/autocuts-personal-automation-1.png)

![Autocuts Setup #2](https://adamtow.github.io/autocuts-admin/images/autocuts-personal-automation-2.png)

![Autocuts Setup #3](https://adamtow.github.io/autocuts-admin/images/autocuts-personal-automation-3.png)

Now, whenever you open one of your selected apps, Autocuts will run in the background.

Autocuts created by Autocuts Admin or a Destination Service will be processed and their shortcuts run.

You can limit how often Autocuts performs its evaluation by installing LimitKit and configuring Autocut's LimitKit Interval in Settings.

### Sources
Autocut Sources are folders on iCloud Drive or Dropbox that hold your Autocut files.

When you add a source to Autocuts using Autocuts Admin, any file whose filename begins with "Autocut" or "autocut" will be processed whenever Autocuts runs.

If an Autocut file is valid for the current time and has not expired, the shortcut specified in the Autocut will run.

#### ADVANCED
Setting up shared Dropbox folders as Autocut sources will allow shortcuts to run automatically on remote iOS devices as their owners use them throughout the day.


## Settings
To modify settings for both Autocuts and Autocuts Admin, tap Settings from the Autocuts Admin Home screen.

![Autocuts Admin Settings](https://adamtow.github.io/autocuts-admin/images/autocuts-settings.png)




## Limitations
Normally, Autocuts will not work unless you are actively using your phone throughout the day. If you want Autocuts to be running 24/7, you should create a shortcut that has a repeat loop calling Autocuts every 60 seconds. You should keep the Shortcuts app open. Switching to another application will likely terminate the shortcut, as Shortcuts in iOS 13 do not run very long on their own in the background.

## Troubleshooting
Shortcut automation in iOS is a new and evolving technology. You may encounter the following issues when using Autocuts.

- **XPC connection to the extension was interrupted**: It could be a temporary error on the part of iOS or one of the shortcuts you are trying to run may have experienced an error.
- **Your shortcuts do not run**: Turn on Use Logs and Notify Activity in Autocuts Admin Settings to see exactly what's happening when Autocuts runs. Run Autocuts from the Shortcuts app and from an Open App automation to see if there's a reproducible difference.
- **You are offline**: Autocuts does not evaluate Dropbox sources if you are not connected to the internet.
