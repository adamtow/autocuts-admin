
# Autocuts
Autocuts brings automatic running of shortcuts — with no zero confirmation required — based on time, location, and web activity. A background shortcut manager, Autocuts works intelligently behind the scenes to execute shortcuts automatically while you use your iOS device during the day. 

For those who have been wanting Personal Automations in iOS 13 to be a little more, say, automated, Autocuts is for you. Stop confirming and start running your time, location, and web-based shortcuts automatically with Autocuts!

****

## Download
Autocuts is part of the **Autocuts Suite** set of automation shortcuts for iOS from [Adam Tow](https://tow.com):

[Download Autocuts Suite Installer from RoutineHub.co &raquo;](https://routinehub.co/shortcut/3661)

- **Autocuts**: the shortcut manager that runs your shortcuts continually in the background throughout the day.
- **Autocuts Admin**: the shortcut for creating, viewing, and managing your list of background shortcuts. 
- **Location Triggers**: shortcut that manages and runs all of your automatic, location-based shortcut triggers. 
- **LimitKit**: an event logging and rate limiter for shortcuts. LimitKit allows you to set the run cadence of your shortcuts (e.g. one minute, fifteen minutes, two hours, three weeks, etc.).

### System Requirements
- Autocuts Suite requires iOS 13.1 or higher.
- You must allow untrusted shortcuts from Settings &gt; Shortcuts in order to install any third-party shortcut such as Autocuts.
- Autocuts needs access to the following:
	- iCloud Drive
	- Notifications
	- Dropbox
	- Location
	- Contacts

****

## Why Autocuts?
Personal Automations in iOS 13 continues the progress made by Workflow and Shortcuts in iOS 12 to bring powerful, user-friendly automation tools to iOS. A number of the triggers, however, share a common weakness; they require the user to tap on a confirmation button to actually run a shortcut.

For many people, this makes a lot of sense, and it's understandable why Apple has taken a more conservative approach to automation in iOS 13. For the rest of us who can't wait for iOS to bring that Ask Before Running toggle to time and location personal automations, Autocuts has been made for you!

### How Autocuts Works
Autocuts takes advantage of the **Open App** personal automation feature of Shortcuts in iOS 13.1. Assigning Autocuts to run whenever you open your most used apps allows it to constantly monitor for shortcuts to run automatically in the background. 

You can also connect third-party web services such as IFTTT, Zapier, and Dropbox directly with your iOS device. With Autocuts, a web-based trigger can now automatically run a shortcut on your iOS devices. Even more amazing is the ability for Autocuts to run a shortcut automatically on a remote user's iOS device.

****

## Getting Started
In order to run shortcuts automatically in the background, you must have the Autocuts shortcut installed.

With Autocuts Admin, you can create, manage, and view all shortcuts that are scheduled to run automatically as you use your iOS device throughout the day. Tap **Install Autocuts** from the Autocuts Admin Home screen to get the latest version of Autocuts.

### Creating the Autocut Open App Personal Automation 

Next, Autocuts must be configured to run each time you open your most commonly used apps.

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

Now, whenever you open one of your selected apps, Autocuts will run in the background and evaluate all Autocut files located in monitored iCloud or Dropbox folders. If allowed, the shortcuts referenced by the Autocut files are run automatically.

> The biggest downside to running Autocuts in this fashion is the notification banner that appears each and every time a personal automation is running. This notification banner currently cannot be disabled in any Notification setting on iOS. Hopefully a future version of iOS will allow the user to disable this banner or see the banner turn into some sort of indicator in the status bar. 

****

### Creating Your First Autocut
Follow these instructions to create your first shortcut that runs automatically without confirmation:

1. Open **Autocuts Admin**.
2. Tap **New Autocut**.
3. Choose the shortcut you want to run automatically. ![Select a shortcut to run with your new Autocut](https://adamtow.github.io/autocuts-admin/images/new-autocut-1.png)
4. If your shortcut requires input, select what you want to send it when the Autocut runs. If the shortcut fully supports Autocuts, tapping **Custom from Shortcut** may present custom UI from the shortcut to collect the input necessary for the shortcut to run properly.
5. Decide whether the shortcut can run in the background or if the Shortcuts app needs to be frontmost before running the shortcut. **NOTE**: *Not all shortcuts can run properly in the background, so please refer to this [section on writing background-aware shortcuts](#background).* ![Enter the shortcut input, decide whether it can run in the background, and set the date it can first run](https://adamtow.github.io/autocuts-admin/images/new-autocut-2.png)
6. Select the date and time when the Autocut will become active.
7. Set an expiration time for the Autocut or set it to never expire. If Autocuts runs across an expired Autocut, it will delete the Autocut and not run its shortcut.
8. For Autocuts that do not expire and if you have [LimitKit](#limitkit) support enabled, you can set the run cadence for your shortcut. While Autocuts will run continuously, you may not want your shortcut to run every time. With LimitKit, you can have your shortcut wait at least X number of seconds, minutes, hours, days, weeks, months, or even years, before it can run again. ![Decide whether the AutoCut expires and its LimitKit run interval (optional)](https://adamtow.github.io/autocuts-admin/images/new-autocut-3.png)
9. Select an action that will occur when the Autocut successfully runs. You can disable the Autocut, reset it, delete it, or do nothing.
10. Choose whether this Autocut will only run on the iOS device you're currently using, or whether it will run on any iOS device that has the Autocut. You can also specify a custom device name here. Autocuts with a device name restriction will not run on those devices that do not have the name defined in the Autocut.
11. Name your Autocut. If you leave the name blank, the shortcut name will be displayed in Autocuts' interface. ![Choose what happens after the shortcut runs successfully and restrict the shortcut to run on certain devices](https://adamtow.github.io/autocuts-admin/images/new-autocut-4.png)
12. Select a destination for your Autocut. You can send Autocuts to remote iOS devices and other users by taking advantage of [Destinations Services](#destinations).
13. The Autocut will now be completed, and you will be taken to the Autocuts listing page. Tap on the Autocut to view the details that you just entered.

![Choose which destination to create the Autocut in](https://adamtow.github.io/autocuts-admin/images/new-autocut-5.png)

****

### Sources
Autocut Sources are folders on iCloud Drive or Dropbox that hold your Autocut files.

When you add a source to Autocuts using Autocuts Admin, any file whose filename begins with "Autocut" or "autocut" will be processed whenever Autocuts runs.

#### Allowed Shortcuts
By default, any shortcut referenced in an Autocut within a source can be run automatically in the background. To restrict which shortcuts can be run from a source, perform the following:

1. Tap **Sources** from the **Autocuts Admin** Home screen.
2. Tap **Set Allowed Shortcuts**.
3. Select the shortcuts you want to restrict only to this source. Don't select anything to allow any shortcut to run from an Autocut.
4. Tap **Done**.

The names of the shortcuts will appear at the top of the source dialog window.

#### Shared Sources
Setting up shared Dropbox folders as Autocut sources will allow shortcuts to run automatically on remote iOS devices as their owners use them throughout the day.

****

<span id="services"></span> 
## Destination Services        
Destination services deliver Autocuts to local and remote sources. Autocuts Admin supports the following destination services:

- **iCloud Drive**: a folder within the Shortcuts folder on iCloud Drive. Make sure to add this folder path as a source if you want Autocuts on this device to process them.
- **Dropbox**: A folder on Dropbox where to store your Autocut files. Make sure to add this folder path as a source if you want Autocuts on this device to process them.
- **IFTTT**: Requires a Maker Webhooks Event name and API key to send a webhook to IFTTT which should create an Autocut file on Dropbox.
- **Zapier**: Requires catch hook URL to send an Autocut to Zapier. The Zap should then create the Autocut file on Dropbox.

### Zapier
Any trigger on Zapier can now run shortcuts automatically on your iOS devices with Autocuts. All you need to do is create a file that resides on Dropbox after a triggering event has occurred.

A Zapier destination requires a catch hook url. You create one from within Zapier. Enter that when prompted by Autocuts Admin.

![Choose which destination to create the Autocut in](https://adamtow.github.io/autocuts-admin/images/destination-zapier-1.png)

![Choose which destination to create the Autocut in](https://adamtow.github.io/autocuts-admin/images/destination-zapier-2.png)

### IFTTT
Any trigger on IFTTT can now run shortcuts automatically on your iOS devices with Autocuts. All you need to do is create a file that resides on Dropbox after a triggering event has occurred.

In the example below, we're creating a Destination Service with IFTTT that makes use of the Maker Events Webhooks app. You'll need a [Maker Webhooks API Key](https://ifttt.com/maker_webhooks).

![Choose which destination to create the Autocut in](https://adamtow.github.io/autocuts-admin/images/destination-ifttt.png)

You will also need the Event Name to send the web hook to.

### Home Automations and Zapier and IFTTT
If you have an iPad, HomePod, or Apple TV serving as a HomeKit hub in your residence, you can now have them remotely call shortcuts running on your device using Autocuts.

A stripped down version of Shortcuts runs with the Home Automations section of the Home app. One of the supported actions is Get Contents of URL, which is perfect for sending webhook requests to services like IFTTT and Zapier. Here's an example using the Time of Day trigger:

1. Open the **Home** app.
2. Tap the **Automation** tab.
3. Tap **New Automation**.
4. Choose your triggering event. In this case, we'll choose the time of day and set the trigger to occur at 7:00 am.
5. Tap **Next**.\
\
![Setting up an Autocut via Home Automation](https://adamtow.github.io/autocuts-admin/images/home-automation-1.png)\
&nbsp;
6. Scroll to the bottom of your rooms and accessories and tap **Convert to Shortcut**.
7. Remove the first action.
8. Tap the **+** button.
9. Enter **Dictionary** in the search field and add the action to the shortcut.
9. Enter **Get Contents of URL** in the search field and add the **Get Contents of URL** action to your shortcut.
10. Edit the dictionary so that it matches the Autocut you want to run. For details on the Autocut dictionary format, please refer to [the API section below](#api).\
```
{
		"name": "Morning Routine",
		"shortcut": "Morning Routine",
		"expires": 60,
		"onSuccess": delete,
		"active: true,
		"activate": true
}
```\
This specifies an Autocut that runs the Morning Routine shortcut. It deletes itself on success and activates Shortcuts to run in the forehand (because it speaks out the morning details to the user). It also expires in 60 minutes in case the user slept in too much!\
&nbsp;
11. Tap **Show More** in the Get Contents of URL action.
12. Tap Method and choose **POST**.
13. Tap **JSON** in Request Body.
14. Tap Add new field and choose Text.
15. Enter `value1` for the key.
16. Add the Dictionary variable to value field.
17. Tap **URL**.
18. Enter your **IFTTT Webhooks URL**.
19. Tap **Next**.
20. It's always a good idea to test that the automation is working, so tap **Test This Automation**. If everything worked properly, the Autocut text file will be created in your Dropbox folder via the IFTTT webhook.

![Using IFTTT to create an Autocut on a Dropbox source](https://adamtow.github.io/autocuts-admin/images/home-automation-2.png)\

Now, at 7:00 am, your HomeKit Hub will send a webhook request to Zapier or IFTTT and add an Autocut to your monitored source folder on Dropbox. At any point between 7:00 am and 8:00 am, all the user has to do is pick up the iOS device and run one of the Open Apps personal automation apps that was assigned to launch Autocuts. [If all goes well](#troubleshooting), the shortcut will run automatically, without the user having to do anything at all!

<span id="limitkit"></span>
## LimitKit
By default, the Open App personal automation will cause Autocuts to run every time you open one of the selected apps.

LimitKit allows you to control the frequency at which Autocuts will perform its evaluation.

For example, you can configure Autocuts to run every minute, five minutes, thirty minutes, or hour. While it is in-between evaluation periods, Autocuts will exit much more quickly when run from the Open App personal automation.


****

## Settings
To modify settings for both Autocuts and Autocuts Admin, tap Settings from the Autocuts Admin Home screen.

![Autocuts Admin Settings](https://adamtow.github.io/autocuts-admin/images/autocuts-settings.png)

### Verify Shortcuts
If this setting is enabled, Autocuts will compare the shortcut it is trying to run with a pre-generated list of shortcuts. This list is automatically created whenever you launch the Autocuts Admin shortcut. If the shortcut does not exist on the device, Autocuts will skip over it. 

If you are constantly adding and creating shortcuts, you should run Autocuts Admin periodically to regenerate the list of shortcuts. 

If the setting is not enabled and Autocuts tries to launch a shortcut that does not exist, an error will occur and prevent any remaining Autocuts from running. 

> Developer Note: Autocuts cannot use the Get My Shortcuts action to retrieve an updated list of shortcuts running in the background without iOS raising an error during a personal automation. 

### Log Activity
When enabled, Autocuts will write to a log file, detailing what it does during every evaluation. The log file is located in iCloud Drive in the Shortcuts/Autocuts folder. 

### Notify After Evaluation
If enabled, Autocuts will display a notification banner of the current log entry. This is useful when you are developing and troubleshooting your Autocuts. This feature is only available if you have the Log Activity setting enabled. 

### Use LimitKit
[LimitKit is an event logging system and rating limiting tool](https://adamtow.github.io/limitkit) for shortcuts. Autocuts takes advantage of LimitKit to prevent itself and other background shortcuts from calling themselves unnecessarily too many times.

When the Open App personal automation is used with multiple apps, iOS will try to launch your shortcut in the background every time you switch to one of the selected applications. If you switch between apps frequently, you can see how this might cause errors and instability with your shortcuts.

LimitKit allows shortcut developers to limit the number of times a shortcut can run its primary function based on intervals of seconds, minutes, hours, days, weeks, months, or even years. 

By enabling LimitKit support in Autocuts, you can not only control how often Autocuts kicks off its evaluation process but also how frequently your Autocut shortcuts run.

#### LimitKit Interval
Set the interval for how often Autocuts will run in minutes. Use whole numbers, so no negative numbers or fractions.

With or without using LimitKit, the Autocuts shortcut will run during an Open App personal automation. However, the shortcut will exit much more quickly and consume less processing resources if you have enabled LimitKit with a reasonable interval (say 1-5 minutes).

![This Autocut shortcut will run every five minutes.](https://adamtow.github.io/autocuts-admin/images/limitkit-autocut.png)

### Default Expiration Time
Configure the default expiration time for your Autocuts here. If you miss the window for running an Autocut, it will expire and be removed from your list of Autocuts. 

Set to 0 if you want your Autocuts to never expire.

### Use Default Service with API
If you use the Autocuts API to create new Autocuts and have multiple destination services defined, a window will appear for each Autocut you create asking you where to send the Autocut. Enabling this setting will cause your Autocuts to be placed using the Default iCloud Destination Service.

### Change Language
Currently, Autocuts has been localized for the English language, the shortcut is fully ready to be localized. Create your own localization file and submit a pull request on the [Autocuts Admin GitHub page](https://github.com/adamtow/autocuts-admin).

### Check for Update
Checks for an update to the app via [RoutineHub.co](https://routinehub.co).

### Reset
Reset Autocuts and Autocuts Admin's settings or erase all information regarding your destination services and sources. 

Erasing content **does not** delete any files in your source folders. So, if you re-add those sources to Autocuts, the Autocuts may reappear. Please visit the source folders directly and delete those files you do not need.

****

<span id="api"></span> 
## Autocuts API

### What is an Autocut?
An Autocut is a text file stored on iCloud Drive or Dropbox that instructs Autocuts to run a shortcut automatically while you use your iOS device during the day. Each Autocut has a number of properties, including:

- **shortcut**: the shortcut to run.
- **input**: text input that will be sent to the shortcut when run.
- **date**: the date and time that an Autocut can first be run.
- **expires**: the amount of time in minutes after the scheduled date that an Autocut can still be run. Shortcuts of expired Autocuts will not run. Autocuts can also be set to never expire.
- **device**: the name of the iOS device that can run this Autocut. When blank, the shortcut will run on any device.
- **activate**: set to true to open the Shortcuts app before running the Autocut's shortcut. Used for those shortcuts that do not run properly in the background.
- **onSuccess**: what happens to the Autocut after successfully running. You can choose between doing nothing, disabling the Autocut, resetting it, or deleting it.
- **limitkit**: options for controlling how often the shortcut can run via [LimitKit](#limitkit).

### Creating Autocuts
Autocuts can be created in a number of ways. Any shortcut or application that can write to the Shortcuts folder on iCloud Drive or a Dropbox folder can create an Autocut.

Some examples include:

- **Autocuts Admin**: the shortcut you are using now features an assistant that walks tou step-by-step in creating an Autocut.
- **API**: Send the Autocuts Admin a specially-formatted dictionary to create and schedule Autocuts from a third-party shortcut.
- **IFTTT or Zapier**: any trigger can write an Autocut text file to an Autocuts Dropbox source folder.

****

<span id="faq"></span> 
## Frequently Asked Questions

### If I go to sleep, will Autocuts keep running my shortcuts in the background?

The short answer is no. The trigger for Autocuts to run is you have to use your iPhone and opens apps that are tied to the Open App personal automation that runs Autocuts. If you are not using your iOS device, Autocuts won't be triggered.

The long answer is maybe. If you want Autocuts while you're asleep, consider creating a shortcut that calls Autocuts every 60 seconds or so. You should keep the Shortcuts app open. Switching to another application will likely remove or suspend Shortcuts from memory. Your shortcut may want to lower the brightness of the display and 

<span id="troubleshooting"></span> 
## Troubleshooting
Shortcut automation in iOS is a new and evolving technology. You may encounter the following issues when using Autocuts.

- **XPC connection to the extension was interrupted**: It could be a temporary error on the part of iOS or one of the shortcuts you are trying to run may have experienced an error. This error more commonly occurs with Autocuts that have the `activate` flag set to true, meaning they try to switch back to the Shortcuts app in order to operate.
- **Your shortcuts do not run**: Turn on Use Logs and Notify Activity in Autocuts Admin Settings to see exactly what's happening when Autocuts runs. Run Autocuts from the Shortcuts app and from an Open App automation to see if there's a reproducible difference.
- **You are offline**: Autocuts does not evaluate Dropbox sources if you are not connected to the internet.
