<div align="center">
<img src="/images/appiumwithpython_en.png">
</div>

<i>This is the english version of <a href="https://github.com/clarabez/appium">Appium Course in portuguese</a>, which is recommend by <a href="https://github.com/appium/appium/tree/master/sample-code/python#tutorial">Appium official documentation</a>.</i>

This tutorial is a guide to teach you how to setup your environment to use Appium tool for functional test automation on mobile devices. Among other things, I highlight following points as main learning:

<ul>
    <li>Understand how Appium tool works and how to setup this application on following platforms: Windows, Linux and Mac;</li>
    <li>How to instantiate an emulated Android device through Android Studio;</li>
    <li>How to install an application form Play Store in your emulated device;</li>
    <li>How to map elements on the application from your emulated device;</li>
    <li>How to start UI tests in your application by using Appium tool combined with Python programming language.</li>
</ul>

___

**This tutorial is organized on following sections:**

<ul>
    <li>Introduction</li>
    <li>Environment setup</li>
    <ul>
        <li>Download everything we need</li>
        <li>Windows setup</li>
        <li>Linux setup</li>
        <li>Mac setup</li>
        <li>Simplified setup for all platforms</li>
        <li>Appium installation</li>
    </ul>
    <li>Appium Doctor: how to validate if everything is configured properly?</li>
    <li>Checklist</li>
    <li>Starting with Appium</li>
    <li>ADB commands></li>
    <li>Emulating an Android device through Android Studio</li>
</ul>

___

**Tutorials here**

- [Tutorial #1: Installing an application on an emulated Android device](https://github.com/clarabez/appium/blob/master/README.md#tutorial-1-instalando-uma-aplica%C3%A7%C3%A3o-no-meu-dispositivo-android-emulado)
- [Tutorial #2: Desired Capabilities: what are them and how to use them to start a session on Appium](https://github.com/clarabez/appium/blob/master/README.md#tutorial-2-desired-capabilities-como-iniciar-uma-sess%C3%A3o-com-o-appium)
- [Tutorial #3: Identifying elements on our application](https://github.com/clarabez/appium/blob/master/README.md#tutorial-3-identificando-os-elementos-da-nossa-aplica%C3%A7%C3%A3o)
- [Tutorial #4: Performing gestures activities by using Appium](https://github.com/clarabez/appium/blob/master/README.md#tutorial-4-realizando-atividades-de-gestos-via-appium)
- [Tutorial #5: Performing a very simple flow of functional test](https://github.com/clarabez/appium/blob/master/README.md#tutorial-5-realizando-um-fluxo-simples-de-teste-funcional)
- [Tutorial #6: Recording our actions and turning them into Python code](https://github.com/clarabez/appium/blob/master/README.md#tutorial-6-gravando-nossas-a%C3%A7%C3%B5es-e-transformando-isso-em-c%C3%B3digo)
- [Tutorial #7: Arithmetic operations with Android native Calculator](https://github.com/clarabez/appium/blob/master/README.md#tutorial-7-opera%C3%A7%C3%B5es-aritm%C3%A9ticas-com-a-calculadora-nativa-do-android)
- [Tutorial #8: Replicating all previous activities with Python](https://github.com/clarabez/appium/blob/master/README.md#tutorial-8-replicando-tudo-o-que-fiz-utilizando-apenas-python)
- [Tutorial #9: Arithmetic operations with Android native Calculator - Phase 2](https://github.com/clarabez/appium/blob/master/README.md#tutorial-9-opera%C3%A7%C3%B5es-aritm%C3%A9ticas-com-a-calculadora-nativa-do-android---fase-2)
- [Tutorial #10: Arithmetic operations with Android native Calculator - Phase 3: organizing the code with design patterns and making functional test flow](https://github.com/clarabez/appium/blob/master/README.md#tutorial-10-opera%C3%A7%C3%B5es-aritm%C3%A9ticas-com-a-calculadora-nativa-do-android---fase-3-organizando-o-c%C3%B3digo-com-padr%C3%B5es-de-projeto-e-realizando-fluxo-de-teste-funcional)

___

I will try to always (or whenever is possible) adjust the content here and insert new tutorials as well. Fell free to suggest improvements or corrections, just make contact <i>&#128525;</i>

I've started this tutorial because when I decided to learn about Appium I had to access different sources of content and practice them a lot, make notes about tips, create tutorials for myself, etc, just to make clear the understanding about the tool. I hope these tutorials be useful for you and I also encourage you to share everything you learn here <i>&#129304;</i>

___

<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/appiumIntroduction.png">
</p>

# Few information about Appium

_Appium_ is an open-source and multi-platform tool (this means that it will work for Windows, Linux e Mac) focused in UI interactions for mobile devices, making possible software automation for applications: natives, hybrids and web ones for Android, iOS and Windows platforms.

I personally consider Appium an excellent tool to start with software automation studies for mobile devices; or even to those ones who already work with software automation and would like to discover a new tool/framework.

**Important links for this section:**

[Appium official web page](http://appium.io)

[Appium official page on GitHub](https://github.com/appium/)

As I wrote before, the main objective of _Appium_ is testing applications on mobile devices, and those applications may be classified in three different categories: natives, hybrids and web. What is the difference between them?
  - **Natives:** those applications which were developed specifically for Android or iOS, that is, applications developed from their SDKs.
  - **Hybrids:** those applications which are developed with HTML, CSS, JavaScript and which are compatible with any platform (Android, iOS, Windows).
  - **Web:** those applications which are accessible by using an URL, like a web page.

___

<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/setup.png">
</p>

In this section we are gonna describe all the necessary steps to set up our environment for Windows, Linux or Mac. I personally use MacOS for all my projects, so some examples are more detailed for this SO.

**A very important tip:**

Here I will give details for every SO, but you also have an option of use a simplified model of setup (it works exactly the same). The main advantage of this is that you may save time with settings and avoid unnecessary headache - trust me :) If you think this is the best setup mode for you, jut go ahead to "Simplified setup for Windows/Linux/Mac" topic. The same procedure is used for any operational system.

# Download everything we will need

In this course, we will use some essentials tools to practice our automation activities. So, here are some links to download them (all of them are common for Windows, Mac or Linux):

  - **Appium Desktop:** this is the protagonist of our course. [Download it here](https://github.com/appium/appium-desktop/releases/tag/v1.13.0). Check that this link has options for each Operational System (OS), so download only that one specific for your OS.
  
  - **JDK (JAVA Development Kit):** https://www.java.com/pt_BR/download/ 

  - **Android Studio:** the main tool to develop content for Android Platform. Here some features are available like for example Android Virtual Device (AVD) which focus is to instantiate Android devices with some Android version. I will teach how to do that. [Download it here](https://developer.android.com/studio?hl=pt-br).
   
  - **IDE:** according to your preference for language, choose an IDE. I strongly suggest you PyCharm or VSCode. Feel free to use any other else. In my projects I always use PyCharm. Check links for each one:

  - PyCharm: https://www.jetbrains.com/pycharm/
  
  - VSCode: https://code.visualstudio.com/
  
  After downloading all those content, now we can go ahead with setup. We have two options for environment setup: the most complex one and the most simplified one. For both cases we have a step by step guide with all the necessary details and information for each one.
  
# Environment variables - Mac:

After installing Appium Desktop, JAVA, Android Studio, your IDE, etc, now it is time to setup environment variables to make sure your OS recognize all the process, applications, etc, in a very effective way.
For that, start your terminal (or cmd, for Windows), identify installation path for each package and export it for your PATH variable.
Basically, identify the path location for Android, copy it and past it on PATH field.

For example, for macOS, usually the location for Android is:

```bash
/Users/user_name/Library/Android/sdk
```

So, from this initial path location we will find others important paths, like:
```bash
/Users/user_name/Library/Android/sdk/platform-tools
/Users/user_name/Library/Android/sdk/tools
/Users/user_name/Library/Android/sdk/build-tools
```

Once you identify those path locations on your computer, now it is time to export these values to PATH variable, like expressed bellow:

```bash
export ANDROID_HOME=/your/path/to/Android/sdk 
export PATH=$ANDROID_HOME/platform-tools:$PATH 
export PATH=$ANDROID_HOME/tools:$PATH 
export PATH=$ANDROID_HOME/build-tools:$PATH 
export JAVA_HOME=/your/path/to/jdk1.8.0_112.jdk/Contents/Home 
export PATH=$JAVA_HOME/bin:$PATH
```

# Environment variables - Windows:

When you download and install JDK in your Windows environment, it is time to setup environment variables. Check following instructions for that:
1. System properties >> Advanced settings of system >> Environment variables >> User variables >> New.
2. Name your new variable as "JAVA_HOME" and as value insert the path location for your jre file, for example, "C:\Program Files\Java\jdk1.2.2_2\jre".
3. In System Variables section, double click on "Path" and insert "%JAVA_HOME%\bin" expression. That means that you are inserting the same value previously define for JAVA_HOME, but also incrementing with \bin folder.
4. Just confirm changes by clicking OK button and setup has been finished.

Now, download and install Android SDK and go ahead with following instructions:
1. Follow the same step described on previous #1 to achieve environment variables field.
2. Now, name your new variable as "ANDROID_HOME" and as value insert the path location for your Android SDK, for example, "C:\android-sdk".
3. Now it is time to add this variable value to your global variable: "%ANDROID_HOME%\platform-tools" and also "%ANDROID_HOME\tools%".
4. Just confirm changes by clicking OK button and setup has been finished.
    
# Environment variables - Linux:

Environment variables setup for Linux has a very similar procedure for Mac. All you have to do is identify the exactly installation path for JDK and Android and apply (by using export function) those paths to your global setting setup file, in this case, "~/.bashrc".

For example, usually the path location for Linux is:

```bash
/Users/user_name/Library/Android/sdk
```

So, from this location folder we will identify all the others necessary paths for SDK setup:

```bash
/Users/user_name/Library/Android/sdk/platform-tools
/Users/user_name/Library/Android/sdk/tools
/Users/user_name/Library/Android/sdk/build-tools
```

When you identify these path locations in your computer, it is time to export them for PATH variable, like explained below:

```bash
export ANDROID_HOME=/your/path/to/Android/sdk 
export PATH=$ANDROID_HOME/platform-tools:$PATH 
export PATH=$ANDROID_HOME/tools:$PATH 
export PATH=$ANDROID_HOME/build-tools:$PATH 
export JAVA_HOME=/your/path/to/jdk1.8.0_112.jdk/Contents/Home 
export PATH=$JAVA_HOME/bin:$PATH
```

**Tip #1 - Windows/Linux/Mac:**

To identify your JAVA_HOME folder location, just use following command in your terminal:

```bash
which java
```

The response for that command should be the location for your JAVA. If nothing is returned, that means that JAVA is not installed in your computer.

**Tip #2 - Linux/Mac:**

Sometimes the defined values are erased and all the configs are lost. To avoid that, do not forget to save the content for your bashrc (Linux) or your bash_profile (macOS). After save those values, do not forget to "compile" your file to refresh your changes:

For macOS:

```bash
source ~./bash_profile
```

For Linux:

```bash
source ~/.bashrc
```

# Simplified way for Windows/Linux/Mac

I know setting an environment for development sometimes may be really boring or painful. There is a simplified way for Appium. To use it, open your Appium Desktop, and manually insert your location paths for ANDROID_HOME and JAVA_HOME. This is really simple, just follow the steps:

Open Appium Desktop, click on "Edit Configurations" button.

<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/appiumFirstScreen.png">
</p>

When you click on "Edit Configurations", you will face a popup with 2 fields: ANDROID_HOME and JAVA_HOME. Just identify those paths in your computer (follow the commands on setup section for each OS) copy and paste them on the respective fields and then click on "Save and Restart". That is it, your Appium Desktop setup has been finished successfully :)

<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/appiumSecondScreen.png">
</p>

___

# Installing Appium

Appim Desktop installation is really simple and does not require additional procedure - besides Android and JDK. All you have to do is download Appium Desktop thru official Appium page (link are available in the very first lines of this doc) or thru command line:

```bash
npm install -g appium
```

**WARNING:** Do not install Appium with sudo.

**Tip - What is npm?**

Npm is the download manager for node.js packages.

___

<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/appium-doctor.png">
</p>

# How to validate if everything went fine?

A very nice functionality offered by Appium is <em>Appium-doctor</em> package, which functionality is about checking all the necessary things for your environment work properly. If anything is missing, Appium-doctor warns you exactly which one is missing. It also confirms the expected packages installed. To install Appium-doctor, just use following command in your terminal:

```bash
npm install -g appium-doctor --android
```

**Tip:**
We are using **--android** flag to indicate the platform name that we are gonna use Appium tool. For example, if we were use iOS instead of Android, we would use **--ios--** flag.

After install <em>Appium-doctor</em>, just call it by terminal:

```bash
appium-doctor
```
Here is an example of how is the content return of <em>"Appium-doctor"</em> on terminal:
```bash
➜  bin appium-doctor
info AppiumDoctor Appium Doctor v.1.10.0
info AppiumDoctor ### Diagnostic for necessary dependencies starting ###
info AppiumDoctor  ✔ The Node.js binary was found at: /usr/local/bin/node
info AppiumDoctor  ✔ Node version is 8.11.4
WARN AppiumDoctor  ✖ Xcode is NOT installed!
info AppiumDoctor  ✔ Xcode Command Line Tools are installed in: /Library/Developer/CommandLineTools
info AppiumDoctor  ✔ DevToolsSecurity is enabled.
info AppiumDoctor  ✔ The Authorization DB is set up properly.
info AppiumDoctor  ✔ Carthage was found at: /usr/local/bin/carthage
info AppiumDoctor  ✔ HOME is set to: /Users/BEZERRA
WARN AppiumDoctor  ✖ ANDROID_HOME is NOT set!
WARN AppiumDoctor  ✖ JAVA_HOME is NOT set!
WARN AppiumDoctor  ✖ adb could not be found because ANDROID_HOME is NOT set!
WARN AppiumDoctor  ✖ android could not be found because ANDROID_HOME is NOT set!
WARN AppiumDoctor  ✖ emulator could not be found because ANDROID_HOME is NOT set!
WARN AppiumDoctor  ✖ Bin directory for $JAVA_HOME is not set
info AppiumDoctor ### Diagnostic for necessary dependencies completed, 7 fixes needed. ###
```

Everything with **✔** symbol means that installation is fine for that package.
If something has **✖** symbol, that means that package is *NOT* properly installed or identified. In those cases, you should adjust it.

**Xcode** package is specific for iOS, so, for Android use, we should not worry about it.

___
# Checklist of everything we did so far

If you just arrived here in this section, that means that probably your setup is ready and now you are able to use all the Appium's resource! Here is our checklist:

- Appium Desktop **✔**
- Android Studio (with AVD package) **✔**
- JAVA **✔**
- IDE **✔**
- Environment Setup **✔**

___

<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/appiumStarting.png">
</p>

# Starting with Appium

Everything has been downloaded and installed, now it is time to finally start with Appium Desktop.
As soon as we start Appium Desktop, this is the initial screen that we have the first contact

<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/appiumFirstScreen.png">
</p>

Check we already have 2 fields filed with information:

**HOST:** 0.0.0.0<br>
**Port:** 4723

Those values are default from Appium and indicate that your requisitions (do you remember Appium is based on HTTP server?) will use 0.0.0.0 host as address, and the service will run in 4723 port. If you want to change one of those values (when other service is running at the same port number, for example) just change it manually by clicking on **Advanced** button located on **Simple** tab. You also can change and export those values by clicking on **Presets** button. I, personally, never had to change any default value. If you want a advice, do not change those values if you do not have a good reason for that :)

Main screen has been explained, now we can go ahead clicking on **Start Server** and check our second screen of Appium: HTTP listener. Check that this listener indicates exactly the address where our service is running (those values were inserted on <i>Host</i> and <i>Port</i> fields from our previous screen - we are using default values).

<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/AppiumStarted2.png">
</p>


The next Appium's screen is about creating a new session - this expression is used to indicates a calling for Appium. To access it, click on search icon with **Start Inspector Session** message (as described on next image):

<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/startsession.png">
</p>

Now we see so many fields on the next screen for Appium. We can proceed with <i>Custom Server</i> tab, this is selected by default. Besides that, we also have following fields already completed with information:

**Remote Host:**  127.0.0.1<br>
**Remote Path:** /wd/hub<br>
**Remote Port:** 4327<br>

**Remote Port** was already explained it previously. **Remote Host** uses <i>localhost</i> value for the service, and you can change it if you want so. If you do not want to change anything, we can keep using default values. **Remote Path** has also a default value from Appium and I never had to change it, so, lets keep using it as default value.

**Now it is time to learn about one of the most important points to  start learning how Appium works: understand the Desired Capabilities function** (I will list below the Appium's official link for desired capabilities). Thought desired capabilities is possible to indicates to Appium what exactly you want to test or interact with.

<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/appiumscreen3.png">
</p>

As explained previously, Appium works through HTTP requisition and, as a pattern for that kind of communication, we use JSON file format to send/receive any message. Appium has a graphic interface option with input field with text format, but, when typing on them, JSON format is instantly being converted. So, it is up to you to write it directly in JSON format or use text field. It works in both ways, no difference =)

To start a new session with Appium we will need to fill at least 2 fields:

```bash
{
    'platformName': 'Android',
    'deviceName': '<InserirOnomeDoSeuDispositivoAqui>'
}
```

**Warning:** to understand how to get the value of your device's name, you need to check one of our next sections about [ADB commands](https://github.com/clarabez/appium/blob/master/README.md#comandos-adb).

Desired capabilities names are very clear about their purpose. <i>'platformName'</i> indicates the name of the platform that you are gonna use: Android, Windows or iOS.
The name of our device is indicated on <i>'deviceName'</i> key, and we can obtain this value by using <i>'adb devices'</i> command that we already explained previously. So, here is an example of how to fill those basic fields and the related JSON converted content:

<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/desiredcap1.png">
</p>


**Appium's official page for Desired Capabilities:** <br>http://appium.io/docs/en/writing-running-appium/caps/

___

# How to emulate an Android device using Android Studio

We can use Appium in real devices, emulated devices or even in a farm of devices from Amazon, which work just like cloud computing concept, where resources are allocated according to user demands, and the value payed is based on what was really used.
In our course I will use an emulated device to perform our tests. This is a really good option because you may choose the kind of device you want to use, the Android version, the display size and some others details. So, this way, it is possible to validate the same apk in different scenarios varying hardware settings. This touches in a very peculiar point of Android: granularity of Android versions: https://developer.android.com/about/dashboards?hl=pt-br

**But before start anything... what is an emulated device?**<br>

An emulated device is the instance (oriented object concept) of a new device which simulates a real cell phone; this instantiation happens from the local resources of your computer. It is very similar to a virtual machine, where the Operation System (OS image) will be some official version of Android; and the "machine" will be a copy of one cell phone, including aspects like screen size.

For that, we are gonna use a default resource of <i>Android Studio</i> to instantiate our emulated device: the <i>Android Virtual Device Manager</i>. To access this feature, open your <i>Android Studio</i> and follow these steps to reach following icon:

<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/avdmanager.png">
</p>

As soon as you click on <i>AVD Manager</i> icon, following popup will open and you have to click on <i>+ Create Virtual Device...</i> to create a new emulated device, just like following image:

<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/avdmanager2.png">
</p>

In this new screen, we shall choose which kind of device we want to create: TV, phone, wear OS, tablet; we can also choose the brand, screen size and resolution and density as well. You may emulate any of those devices, including variations of the same device. But, lets keep focused on **phone**, and I personally really like using <i>Pixel 2</i> model in my studies, as it is a Google product and has a very common size of screen, etc, but feel free to pick any other device you want and think is better for your case. So, choose your device and click on <i>Next</i> button.

<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/avdmanager3.png">
</p>

Once your product has been defined for your studies, now it is time to choose the Android version you will use in your emulated device. Check that Android Studio has a list with some options for different Android versions available to download. In this exact moment (july/2020), **Android Q** is the most recent version at the market and it is possible to download **Android R** Beta version. For these tutorials, I am using **Android P**. The reason for that is that release is more stable comparing to Android Q image, for example. But feel free to use any other version you think is better for you. You also can create different devices (watch, TV, etc) with different Android version to try which one is better for your necessities. If the image is not available for you, just clock on "download". If it is already downloaded, just select the image version you want and go ahead with <i>Next</i> button.

<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/avdmanager4.png">
</p>

I am using following settings for my emulated device:<br>
**Device model:** Pixel 2<br>
**Android version:** Android P<br>

So, now your emulated device has been created. Try to perform some actions on it like open any application, use access buttons like home, back and recent apps, etc. Also, try some gestures like accessing quick menu on screen by scrolling down gesture from top to down screen.

With your emulated device, now you have a lot of possibilities to explore your Android with ADB commands. We will talk about it on next section.

**Some important points about this topic:**
- In few weeks I intend to release the content about how to emulate an iOS device.
- There are others tools focused in Android device emulation but, from those I've tried, none was really better than Android Studio. For that reason, I really prefer to keep my studies in Android Studio and I suggest it for that.
___

<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/adb.png">
</p>

# ADB commands

ADB is a shorten for Android Debug Bridge. As the expression suggests, it works like a "bridge" between your computer and your mobile device by using command line. Through ADB commands, it is possible to manipulate your device using commands in a very practical way, like:
- Install/Uninstall applications;
- Change internal properties, like: time to turn screen on/off, lock/unlock screen, etc.
- Enable/disable connection settings, like: wifi, sim data connection, airplane mode.
- Transfer/control internal files;
- Restart and turn off device - it does not work to turn it on (but some frameworks promise to solve it).

It is also possible to automate some routine activities combining ADB commands and Python Scripts.

Well, ADB is a very huge topic and it certainly deserves a specific repository to explain it. Check my repository about ADB commands: [repo comandosadb](https://github.com/clarabez/comandosadb) (it is still under construction).

**Some important links for this section:**<br>
**Few information about ADB commands:** https://developer.android.com/studio/command-line/adb?hl=pt-br<br>
**Python Script:** https://realpython.com/run-python-scripts/<br>
**My repository on GitHub for ADB commands:** https://github.com/clarabez/comandosadb<br>

___

<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/appiumTutorials.png">
</p>

# Tutorial #1: Installing an application on an emulated Android device

**To perform this tutorial, you must have:**
<ul>
    <li>Active emulated device - step by step is described on our previous section</li>
    <li>ADB working fine in your terminal</li>
    <li>Play Store account</li>
</ul>

First of all, you need to choose any application on Play Store. Lately, I have used **Casas Bahia** application, because it has a lot of mapped elements, different menu options, items and a really usability - which makes easier our learning process. So, let's search for Casas Bahia application on Play Store. Application page looks like so:

<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/casasbahia.png">
</p>

Now, just copy the URL value from main application page. In my case, my value is as follows:

https://play.google.com/store/apps/details?id=com.novapontocom.casasbahia

Now, we are gonna access a web page called Evozi, responsible to download any application from Play Store. All you have to do is indicate the URL value of the application on Play Store, like so:

<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/evozi.png">
</p>

Now, just click on **Generate Download Link** and your application will be downloaded with <i>.apk</i> format. Save it in any folder and let's install it in your device. We can do it by two different ways: holding and dragging; or using ADB commands. Let's try it in those different ways.

**Holding and dragging:**
This is the most simple way to install our application. For that, just make sure your emulated device is active and, in parallel, open the path with your downloaded application. Now, hold your application and drag it to your emulated device. That is it! Check a <i>Installing...</i> message on screen and, few seconds after that, your application will be listed on your app tray. Open it and make sure your application is working fine!

**Using ADB commands:**<br>
This is the most elegant way. Just open your terminal, go to the path of your application (via terminal) and use following command:

```bash
adb install nome-do-apk
```

With that, application must be installed properly and be displayed in your app tray.

**Note:**<br>
Usually, popular applications from Play Store are updated at every period of time and, in those updates, maybe some application stop working on your device. For example, already happened to me of using an application which stopped working after some change, because architecture value of the application also has changed, so it become incompatible with my emulated device. If something like this happens to you, I suggest you to pick up another application to keep with your studies. 

**Proposed activities:**<br>
Try to download any application from Play Store and try to install it on your emulated device by using ADB command and also holding and dragging it. 

**Links used in this tutorial:**<br>
**Evozi - APK Downloader:** https://apps.evozi.com/apk-downloader/<br>
**Google Play Store:** https://play.google.com/store/apps?hl=pt_BR<br>

___
# Tutorial #2: Desired Capabilities: what are them and how to use them to start a session on Appium

**To perform this tutorial, you must have:**
<ul>
    <li>Active emulated device - step by step is described on our previous section</li>
    <li>ADB working fine in your terminal</li>
    <li>Application from Play Store already installed in your device</li>
    <li>Appium Desktop installed and working fine</li>
</ul>

In case you did not see [**Starging with Appium**](https://insertlinkhere.com), I recommend you check it before proceed with next tutorials, especially because we need to understand the concept of <i>Desired Capabilites</i> for Appium. Highlighting what was already said on there, <i>Desired Capabilites</i> are a very special concept and indicates what we want to test with Appium.

As explained on [Appium official documentation page about Desired Capabilites](http://appium.io/docs/en/writing-running-appium/caps/), we have a very huge list of options of capabilities, since the most generic to the most specific one. Here we will try those different capabilities.

**Desired Capabilities - generic way**

For that, we will need to identify only <i>platformName</i> and <i>deviceName</i> values, which means the platform name (Android, iOS, Windows) and the product name (serial number), respectively. The first value is very simple to associate, just indicate the platform you are using. For our studies, I will use Android. To check your <i>Serial Number</i> value, use following ADB command in your terminal:

```bash
    adb devices
```

Terminal's output will return something like this:

<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/adb%20devices.png">
</p>

As soon as we use ADB command <i>adb devices</i>, ADB service is started and the ID value of our product is returned. In my case, my id value is: **emulator-5554**. That is the value I will use for <i>deviceName</i> field.

**Very important information:** 
I am using an emulated device, so the output on my terminal (previous figure) is the default value for serial number when you are using <i>Android Device Manager</i>. If you are using a real device, the serial number value will have a different structure. In some cases, numbers only; in others cases numbers and letters combined. This value is unique and immutable. That means every real device will keep its unique serial number value for life.
Here are the values I will use as current <i>Desired Capabilities</i>:

```bash
{
    'platformName': 'Android',
    'deviceName': 'emulator-5554'
}
```

Now with the identified values, we can start Appium and then reach <i>Desired Capabilites</i> tab, and so fill the fields like follows:

<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/desired_generic.png">
</p>

Check that I inserted the value only on <i>Desired Capabilities</i> tab and, automatically, Appium converts the content into JSON on next screen, highlighted with my cursor. Other important tip: I suggest you to save this configuration, because we will use it in our next tutorials. For that, just click on **Save As**. To edit any other capability already saved, just access <i>Save Capability Sets</i> tab and edit it.

Now, just click on **Start Session** button to start a session with Appium based on defined information on desired capabilities. If everything goes fine and the fields are correct (that means, device connected and compatible, etc) next screen is displayed:

<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/appimstarted1.png">
</p>

This is the initial screen for Appium, we will see it a lot in our next classes. It is already possible to see that Appium took a screenshot at the moment we started our session. This is another characteristic of Appium: it reflects, at initial screen, exactly where you were when you started a session. Ok, let's check how to start a session being more specific about what we want Appium deals with.

**Desired Capabilities - specific way**

Previously we checked how to create a generic session using Appium, and we also knew some screens and specific characteristics at every action we achieved.
The main reason of initialise a session in a very specific way is to tell Appium **exactly** the screen we want to start our session test.

**Example:**<br>

Let's try to automate our Android native Calculator. This application will be our specific focus. For that, lets increase our <i>Desired Capabilities</i> values, using the same saved set we used previously, but this time we also need to fill: <i>appPackage</i> and <i>appActivity</i>. Here are explanation for those fields:

**appPackage:**
<br>
The package name of your application. This is defined at application development level.

**appActivity:**
<br>
In mobile development, we call every screen under development as "activity". This capability value is basically to indicate which screen of the application you want to call when we start a new session.

**How to collect these values?**
<br>
Using ADB commands! <3 For that, let's use our device under test and open the test application. Go to the test activity - that screen you want to start a session. After that, connect your device to your computer, open your terminal and insert following command:
```bash
    adb shell dumpsys window windows | grep -E 'mCurrentFocus'
```

Visually, it is displayed like so:

<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/adbcurrentfocus.png">
</p>

Note that I am highlighting only a piece of the returned code:

```bash
com.android.calculator2/com.android.calculator2.Calculator
```

Here is the piece of the returned code that we are gonna use for both <i>appPackage</i> and <i>appActivity</i>. The division between them is this "/" (bar). Package value is the piece of code before "/" (bar). Beyond the bar, is the piece of code for activity value. Now, just copy and paste values like so:

```bash
{
    'platformName': 'Android',
    'deviceName': 'emulator-5554'
    'appPackage': 'com.android.calculator2',
    'appActivity': 'com.android.calculator2.Calculator'
}
```

Visually, updated content is like so (highlighting the most recent update on JSON):
<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/desireddetailed.png">
</p>

Now, with all values identified and filled, you may save again this config clicking on <i>Save As...</i> and then start a session by clicking on <i>Start Session</i>. When a new session is initialised, you will see that now Appium takes a screenshot directly in Calculator application, what we defined previously on <i>appPackage</i> and <i>appActivity</i> fields. Check your test device (emulated or real), it will be at the same screen:

<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/appiumdetailed.png">
</p>

**Proposed activities:**<br>
Try to use ADB command presented in this tutorial to identify activity and package values for different applications, including that one you downloaded on Tutorial #1.

**Important links for this tutorial:**<br>
Appium official page for Desired Capabilities: http://appium.io/docs/en/writing-running-appium/caps/

___
# Tutorial #3: Identifying elements on our application

**To perform this tutorial, you must have:**
<ul>
    <li>Tutorial #2</li>
</ul>

Working with <i>webDriver</i> makes easier the activity of identifying elements of applications. Other tools like UIAutomator (also from Android Studio) can map elements as well. If you ever have worked with Selenium, so you probably know that, to identify a web element, just perform a double click (or right click) and click "inspect element". That is it. The web page will be inspected and all the structure is displayed.

So, mapping a web element is not that hard. The challenge is HOW to identify these elements, making sure you are using best practices, most efficient techniques, etc, in a way your code will work fine and also making sure you are writing a clear code keeping maintainability of your project.

<br>
**Which one is the best practice?** <br>

In a perfect world, all the elements of any application are identified, mapped in accordance with development best practices, with unique and intuitive IDs values. Other excellent world is when you, a tester, are working very close to your development team, where communication is clear and it is possible to request any adjustment about elements mapping. But.. we know these scenarios are very specifics and sometimes (or the most of times..) we will work with third party applications, and so we have work with what is available on there.

A good practice is using a piece of static value when you are working with dynamic IDs. In case of using dynamic IDs, its values are being updated at every access; usually it happens due to the framework used at development level. A good practice to deal with this? CSS Selector.

In some cases, you will work with elements organised hierarchically. In these cases, try to keep mapping in a very short hierarchical structure.

Other important tip is dividing values (in case of long expressions values) where you will find XPATH; so turn it into shorten expressions, like this example:

```bash
<button type=“submit” class=“signup-button button--black button--active”>Signup Here!</button>
```

With this very simple example using XPATH, where we can see a long expression as value, we can optimize de identification like so:

```bash
WebElement signupXPath = browser.findElement(By.xpath(“//button[contains(@id, ‘signup-button’)]”));
```

Besides, in a very similar way, we can identify the element using CSS selector practice:

```bash
WebElement signupCSS = browser.findElement(By.cssSelector(“button[class*=‘signup-button’]”));
```

With some of these advices and others good practices (not listed here, so far) your element will be mapped properly, in a more legible way and avoiding future break of values :)

**What practice should I avoid?** <br>
There are a lot of bad ways to map elements. One of them is using pure XPATH value, without any kind of handling or something; dynamic IDs are also a strategy to pay attention and define best practices to use them - as dynamic values change at every event.

**Identifying elements with Appium:**<br>
To identify elements, just perform a double click (or right cursor click) on page (or activity) and, on lateral bar, you will see a list of options of values that may be useful for your project.

<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/appiumIdentifyElements.png">
</p>
<br>

In my screenshot I am using element "9" as example and so I have 2 options to deal with this element mapping: id and xpath. As element number "9" has unique ID and I can see it is a unique value (I could see it by clicking in every element and checking their values), so, I decided that using ID as value is the best option for this case.

**Proposed activities:**
<br>
Let's keep practicing, so I suggest you to check the difference between the elements of your application. Also, try to map elements of any other application and check the presence of different types like ID or Xpath.
___
# Tutorial #4: Performing gestures activities by using Appium

**To perform this tutorial, you must have:**
<ul>
    <li>Active emulated (or real) device - step by step on previous section</li>
    <li>ADB installed and working fine in your terminal</li>
    <li>Application from Play Store already installed in your test device</li>
    <li>Appium Desktop installed and working fine</li>
</ul>
<br>
When we are talking about mobile testing, one of the most critical (and more asked) point is: **GESTURES**. Besides that, one of the most notorious changes on Android Q was the inclusion of new gestures for the main activities of this platform - for example, the 3 main buttons (recents, home, back) on main screen. By using code, it is not that simple to simulate a "drag and drop" gesture to close an application, for example. Here is another advantage of using Appium: it makes easier to turn into code any simulated gesture in your device <3 that is amazing, right? =)

We will divide this tutorial into 2 moments, one for each functionality: <i>Swipe by Coordinates</i> and <i>Tap by Coordinates</i>.

**Swipe by Coordinates - drag to a specific coordinate**

<i>Swipe</i> action is one of the most used gesture on Android, either to access quick menu (upper or bottom sides), or change screen, force close applications, insert password, lock/unlock screen, etc. To simulate this action by using Appium, just use gesture button (highlighted on next image):

<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/SwipeByCoordinates.png">
</p>

Let's try this functionality. For this example, I will access upper menu down on my Android emulated device. The first thing is initialise my Appium session for my emulated Android device; after that, I will perform scroll down gesture from the top of screen to something like the middle of the screen.

<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/gifcoordinates.gif">
</p>

Check that when <i>Swipe</i> functionality is active and my mouse cursor in pointed to any position of the screen, we can see X and Y exactly position values at upper left corner. That value means your location at screen based on pixels, in accordance with screen size of your device. To simulate scroll down action, I clicked right on middle of screen and got the location value of my click. After that, I come some centimeters down and performed another click. After that, Appium performs the same action and reproduces on emulated device.

**Tap by Coordinates - Click in any specific position on screen**

We do not have to say the importance of a gesture on screen for a mobile device, right? :) This action is totally dependent of X and Y position on screen; sometimes this is a hard challenge for automation. But Appium also help us with this, and you may find this functionality by using following button:

<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/TapByCoordinates.png">
</p>

Let's exemplify this functionality. For that I will open an application from my home screen, just clicking on the exactly position of the application at screen. Let's see how it works:

<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/tapcoordinategif.gif">
</p>

"Tap by coordinates" function is simpler than "Swipe" one, once it is performed by an unique click. At the same way, X and Y position values are updated as soon as we move cursor at screen. I clicked at the Dialer app location; that is enough to Appium collects the value position and then perform the click.

**Proposed activities:**

Try to use <i>swipe</i> and <i>tap</i> functionalities in others screens, menus or applications.

___
# Tutorial #5: Performing a very simple flow of functional test

Now that we already know Appium's main functionalities, it is time to combine some of them by performing a functional test in an application. As we are starting, I will perform this test by using Android's native Calculator application. As we are talking about functional tests, let's start structuring this test case:

<b>Test scenario:</b><br>
Perform arithmetic operations
<br>
<table style="width:100%">
  <caption>Test Case #1 - Perform sum operation with 2 valid input values</caption>
  <tr>
    <th>Setup</th>
    <th>Step by step</th>
    <th>Expected results</th>
  </tr>
  <tr>
    <td>1. Connected device (real or emulated)<br>
        2. Initialised Appium session<br>
        3. Initialised Calculator application<br>
    </td>
    <td>1. Insert 1 valid input value<br>
        2. Apply sum operator<br>
        3. Insert another valid input valie<br>
        4. Check result
    </td>
    <td>
        1. Number is inserted properly<br>
        2. Operator is inserted properly<br>
        3. Number is inserted properly<br>
        4. Output result returns the sum of previous 2 valid numbers.
    </td>
  </tr>
</table>

This test case is very simple, I will perform the sum of values 2 and 3:

<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/soma_gif.gif">
</p>

There is no secret, just click on elements following the defined flow and verifying output's return. We will validate this return by using programming language soon :)
___
# Tutorial #6: Recording our actions and turning them into Python code

**To perform this tutorial, you must have:**
<ul>
    <li>Active device (real or emulated)</li>
    <li>Initialised Appium session</li>
    <li>Initialised Calculator application</li>
</ul>

Now it is time to check another very important functionality of Appium: converting actions into programming language. Any action you perform in your device, either just to start any application or something more detailed like using <i>swipe</i> or <i>tap coordinates</i> functionalities.

In my opinion, this is one of the most important advantages of using Appium for automation, specially if you are starting in this world or if you did not have so much contact with any programming language - in a general way or specifically for any language. Appium is able to convert into code to following languages: Python, JAVA, Ruby, RobotFramework and JS.

Recording functionality is available thru following icon:

<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/StartRecordingIcone.png">
</p>

Just click on this icon and make sure to activate "Select elements" function, which is located by left size of <i>swipe</i> button. I am highlighting it on next image. By clicking on test icon, we have to click on <i>Tap</i> button, which will perform click action on element. It is also highlighted here:

<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/RecordTap1.png">
</p>

Now, to practice it, let's perform any action and repeat the same flow we performed previously, but this time we will record every performed action:

<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/recordsomagif.gif">
</p>

Check that as we are tapping on our calculator's digits, code is being generated on **Recorder** field, right at the right side :) the code already creates variables receiving element's values, making easier actions with <i>.click</i>, for example. For Python, my generated code output was:

```bash
el1 = driver.find_element_by_id("com.android.calculator2:id/digit_2")
el1.click()
el2 = driver.find_element_by_accessibility_id("plus")
el2.click()
el3 = driver.find_element_by_id("com.android.calculator2:id/digit_3")
el3.click()
el4 = driver.find_element_by_accessibility_id("equals")
el4.click()

```


This generated code is related only to values itself and not to import/resources that you might need. But, it is also possible to generate these detailed code by using <i>BoilerPlate Code</i> button as exemplified on next picture:

<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/boilerplatecode.png">
</p>

All the code may generated thru this functionality, including all the necessary imports and resources. The code for Python is like follows:

```bash
# This sample code uses the Appium python client
# pip install Appium-Python-Client
# Then you can paste this into a file and simply run with Python

from appium import webdriver

caps = {}
caps["platformName"] = "Android"
caps["deviceName"] = "AppiumP"
caps["appPackage"] = "com.android.calculator2"
caps["appActivity"] = "com.android.calculator2.Calculator"

driver = webdriver.Remote("http://127.0.0.1:4723/wd/hub", caps)

el1 = driver.find_element_by_id("com.android.calculator2:id/digit_2")
el1.click()
el2 = driver.find_element_by_accessibility_id("plus")
el2.click()
el3 = driver.find_element_by_id("com.android.calculator2:id/digit_3")
el3.click()
el4 = driver.find_element_by_accessibility_id("equals")
el4.click()

driver.quit()
```

Appium makes our automation job so much easier when we can generate an initial code. All we have to do is adapt the code to our pattern or make some basic adjustments.

On our next tutorials, we will be more focused on the code, so we will also bring more details about Appium with Python.

**Proposed activities:**
Now that you already know to record your actions and turn it into code, we may perform additional flows to our Calculator (or even any other application) to generate actions with gestures, for example. After that, just export the code and make some adjustments according to your pattern.
___
# Tutorial #7: Arithmetic operations with Android native Calculator

From here on, we will change the difficult level of our activities. We will add some more difficulties, but not too much - do not worry, we will combine some of our learned Appium's features.

**To perform this tutorial, you must have:**
<ul>
    <li>Active device (real or emulated)</li>
    <li>Initialised Appium session</li>
    <li>Initialised Calculator application</li>
</ul>

On **"Tutorial #5: Performing a very simple flow of functional test"** we checked a very simple flow to sum two integers numbers. Now that we already know how to turn our actions into code, we will use add some of those actions to our Calcultor activity, applying the others arithmetic operators: subtraction, division, multiplication.

For that, I will use **Record** functionality again, once I want to generate the code of those actions by using Python. Here is a gif showing how to perform this sequence:


<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/oparitimeticas.gif">
</p>

Note that, as I am using **Record** function, the python code is being dynamically generated and, by the end, generated python code is like follows:

```bash
# This sample code uses the Appium python client
# pip install Appium-Python-Client
# Then you can paste this into a file and simply run with Python

from appium import webdriver

caps = {}
caps["platformName"] = "Android"
caps["deviceName"] = "AppiumP"
caps["appPackage"] = "com.android.calculator2"
caps["appActivity"] = "com.android.calculator2.Calculator"

driver = webdriver.Remote("http://127.0.0.1:4723/wd/hub", caps)

el1 = driver.find_element_by_id("com.android.calculator2:id/digit_1")
el1.click()
el2 = driver.find_element_by_accessibility_id("plus")
el2.click()
el3 = driver.find_element_by_id("com.android.calculator2:id/digit_3")
el3.click()
el4 = driver.find_element_by_accessibility_id("equals")
el4.click()
el5 = driver.find_element_by_accessibility_id("multiply")
el5.click()
el6 = driver.find_element_by_id("com.android.calculator2:id/digit_2")
el6.click()
el7 = driver.find_element_by_accessibility_id("equals")
el7.click()
el8 = driver.find_element_by_accessibility_id("minus")
el8.click()
el9 = driver.find_element_by_id("com.android.calculator2:id/digit_1")
el9.click()
el10 = driver.find_element_by_accessibility_id("equals")
el10.click()
el11 = driver.find_element_by_accessibility_id("divide")
el11.click()
el12 = driver.find_element_by_id("com.android.calculator2:id/digit_2")
el12.click()
el13 = driver.find_element_by_accessibility_id("equals")
el13.click()

driver.quit()
```

Ok, now Appium has generated a lot of useful code for us, giving us an idea of how our automation project for Calculator must go on. We already have some buttons and operators mapped.

**Proposed activities:**
<br><br>
Keep mapping the remaining elements of the Calculator. Try to map all of them.

___
# Tutorial #8: Replicating all previous activities with Python

**To perform this tutorial, you must have:**
<ul>
    <li>Active device (real or emulated)</li>
    <li>Initialised Appium session</li>
    <li>Initialised Calculator app</li>
</ul>

We had a lot of fun with previous tutorials and we've met main Appium's functionalities which can be easily accessed by graphical interface, basically clicking on buttons, elements and collecting information and generated codes.

Now, we can start using our IDE (in my case, I am using PyCharm, but feel free to use whatever you like to write your code) to replicate into code everything we did here with Appium. This time, we will use Python. Let's start mapping elements we did not map before :)

As I am using PyCharm, then I created a new project and then a new python file, and then installed following packages on terminal for my project:

1. Selenium:

```bash
pip install selenium
```

2. Appium:

```bash
npm install -g appium
```

The beginning of everything is importing the necessary library to start using Appium's resources in any programming language. We already talked that Appium and Selenium have a lot in common, remember that? Here is a explicit way to show it out, as they use <i>webdriver</i> libraries' resources. Let's import <i>webdriver</i> to start our project:

```bash
from appium import webdriver
```

As discussed previously on [Iniciando com o Appium](https://github.com/clarabez/appium/blob/master/README.md#iniciando-com-o-appium) section, **Desired Capabilities** is a very important concept for Appium because it is the responsible to establish HTTP connection between Appium and our test device, besides indicates if we want to initialise our device (without point to any application) or we want to start our session by any specific screen, by using following keys: <i>appPackage</i> and <i>appActivity</i>. On our previous examples, we already had an idea of how it works, which is thru a dictionary with following content:

```bash
caps = {}
caps["platformName"] = "Android"
caps["deviceName"] = "AppiumP"
caps["appPackage"] = "com.android.calculator2"
caps["appActivity"] = "com.android.calculator2.Calculator"
```

A <i>caps</i> dictionary has been created informing: platform name, device name, necessary information for Calculator application. Gently reminder, those information were generated by Appium, I just copied and pasted then to my IDE, no extra adjustment was made.

Other very important point is how connection is established. Appium returns following:

```bash
driver = webdriver.Remote("http://127.0.0.1:4723/wd/hub", caps)
```

That is when we start using <i>WebDriver's</i> library resources. I created a variable called **driver** which receives a new connection instance; this instance starts by calling <i>Remote</i> resource. Two parameters has been passed for this call:
1. Service location: <i>"http://127.0.0.1:4723/wd/hub"</i>, which is the default value already defined by Appium. This is an "append" of following values: Remote Host + Remote Port + Remote Path.
2. <i>Desired capabilities:</i> As we talked (a lot!) before, a dictionary has been created to store keys-values for whatever I want Appium deals with. All we have to do is indicates the name of our dictionary. 

From the code generated by Appium, I did some adjustments and my code started like so:

```bash
from appium import webdriver

desired_cap = {
    "platformName": "Android",
    "deviceName": "AppiumP",
    "appPackage": "com.android.calculator2",
    "appActivity": "com.android.calculator2.Calculator"
}

driver = webdriver.Remote('http://localhost:4723/wd/hub', desired_cap)
```

With those few information is already possible to establish a session with Appium by using Python. Here is a image of my initial project:

<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/python1.png">
</p>

Check that, as soon as I executed this code, <i>listenning</i> feature from Appium, in parallel, started to consume what was informed on our dictionary.

After that, python execution was finished and, on Appium, <i>status code</i> 200 was returned, indicating our requisition was successfully made - remember that by the end Appium works with HTTP requisition and that is more explicit when we analyse log's output:  

<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/python2.png">
</p>

As output, check your test device (real or emulated) that, on screen, test application will be displayed and activated on screen - in this case, Android native Calculator:

<p align="center">
<img src="https://github.com/clarabez/appium/blob/master/images/python3.png">
</p>

After all, with just few lines of python code an Appium session could be started in a test device. Output is our Calculator application screen displayed on test device.

**Proposed activities:**
<br><br>
Try to explore some native resources from webdriver library. If you do not know it, I strongly recommend that you research about this library and try to explore more interesting functionalities for your project.
___
# Tutorial #9: Arithmetic operations with Android native Calculator - Phase 2

**To perform this tutorial, you must have:**
<ul>
    <li>Active device (real or emulated)</li>
    <li>Tutorial #8</li>
</ul>

On previous tutorial, we saw how to start an Appium session by using Python code: <i>importing resources, inform desired capabilites, webdriver</i>. This start is basically the same (in structure way) for all the projects you will realise using Appium. Now, let's start mapping some of our elements like numbers and operators.

Here is the code generated by Appium:

```bash
el1 = driver.find_element_by_id("com.android.calculator2:id/digit_1")
el1.click()
el2 = driver.find_element_by_accessibility_id("plus")
el2.click()
el3 = driver.find_element_by_id("com.android.calculator2:id/digit_3")
el3.click()
el4 = driver.find_element_by_accessibility_id("equals")
el4.click()
el5 = driver.find_element_by_accessibility_id("multiply")
el5.click()
el6 = driver.find_element_by_id("com.android.calculator2:id/digit_2")
el6.click()
el7 = driver.find_element_by_accessibility_id("equals")
el7.click()
el8 = driver.find_element_by_accessibility_id("minus")
el8.click()
el9 = driver.find_element_by_id("com.android.calculator2:id/digit_1")
el9.click()
el10 = driver.find_element_by_accessibility_id("equals")
el10.click()
el11 = driver.find_element_by_accessibility_id("divide")
el11.click()
el12 = driver.find_element_by_id("com.android.calculator2:id/digit_2")
el12.click()
el13 = driver.find_element_by_accessibility_id("equals")
el13.click()
```

Now it is time to organise our code and also identify all the remaining elements of our application. **Very useful tip:** as Calculator is a small application (just few elements), I took the decision of mapping all them all. However, in an automation project, where usually we have huge applications of complex web pages with a lot of flows or elements, map just what you will really use into your project. Otherwise, your effort will be mostly concentrated in elements mapping, and that is not we want to =)

After some basic adjustments, I organized my code as follows:

```bash
from appium import webdriver

desired_cap = {
    "platformName": "Android",
    "deviceName": "emulator-5554",
    "appPackage": "com.android.calculator2",
    "appActivity": "com.android.calculator2.Calculator"
}

driver = webdriver.Remote('http://localhost:4723/wd/hub', desired_cap)

# numbers
num1 = driver.find_element_by_id("com.android.calculator2:id/digit_1")
num2 = driver.find_element_by_id("com.android.calculator2:id/digit_2")
num3 = driver.find_element_by_id("com.android.calculator2:id/digit_3")
num4 = driver.find_element_by_id("com.android.calculator2:id/digit_4")
num5 = driver.find_element_by_id("com.android.calculator2:id/digit_5")
num6 = driver.find_element_by_id("com.android.calculator2:id/digit_6")
num7 = driver.find_element_by_id("com.android.calculator2:id/digit_7")
num8 = driver.find_element_by_id("com.android.calculator2:id/digit_8")
num9 = driver.find_element_by_id("com.android.calculator2:id/digit_9")
num0 = driver.find_element_by_id("com.android.calculator2:id/digit_0")

# operators
op_mais = driver.find_element_by_accessibility_id("plus")
op_multi = driver.find_element_by_accessibility_id("multiply")
op_menos = driver.find_element_by_accessibility_id("minus")
op_div = driver.find_element_by_accessibility_id("divide")

# common
op_igual = driver.find_element_by_accessibility_id("equals")
```

We have some mapped elements already, but how could we perform arithmetic operations itself? The most basic and simple solution is reproducing the test behavior in a sequential way, like following example for sum operator:

```bash
num1.click()
op_mais.click()
num2.click()
op_igual.click()

print('O resultado da soma foi: ', result.text)
```

Now we know that it is possible to start a output's validation. Thus, now we can compare if the returned value on Calculator's output is the same as when we perform a sum operation by using Python code. In a very simples way, I did like this: 

```bash
somapython = int(num1.text) + int(num2.text)
somaappium = int(result.text)

print('O resultado da soma via Appium foi: ', somaappium)
print('O resultado da soma via Python foi: ', somapython)

assert somapython == int(result.text), 'Resultados divergentes entre o python e o Appium'
```

My resolution was creating a variable to store the result of sum operation using Python (<i>somapython</i>) and another variable to store the value on result field on Calculator Application by using Appium (<i>somaappium</i>).

Then, print on screen the results for both Appium and Python results and then use <i>assert</i> resource to compare those values. If result are equals, validation is PASS and nothing is returned on scree; else, that means, if values are not equals, an error message is returned on terminal: **'Resultados divergentes entre o python e o Appium'**. #TODO

Use <i>assertions</i> in your automation projects is super important. Without using <i>assertions</i> it is not possible to compare the obtained and the expected results, in other words, it is not possible to validate if the collected results is in accordance with the expected of if that is a <i>bug</i>.

**Proposed activities:**<br><br>
Now that we've worked directly to the code, I suggest you to complete keep coding what we have done so far, adding the remaining operators like subtraction, division and multiplication. Do not forget to use <i>assertions</i> and, taking the opportunity, I also suggest you to search more about the importance of using assertions for software testing context.
___
# Tutorial #10: Arithmetic operations with Android native Calculator - Phase 3: organizing the code with design patterns and making functional test flow

**To perform this tutorial, you must have:**
<ul>
    <li>Tutorial #9</li>
</ul>


**Important tip:**<br>
The code generated here is commited in this repository :)

Ok, we already have a functional code, but no pattern was applied. This kind of code is called <i>espaguette</i> :)

Now it is time to start organizing our code, grouping some related actions, using classes, constructors, and some others Python's and Objects Oriented Programming concepts.  

The first thing that I am gonna do is start using some design patterns concepts (we will not give further information about this topic here) to turn our code more legible, more structural for automation and easier to maintain. For that, I will isolate the code responsible for Appium connection in a separated file, called <i>webdriver.py</i>, located in a path with the same name:

```bash
from appium import webdriver


class Driver:
    def __init__(self):
        desired_cap = {
            'platformName': 'Android',
            'deviceName': 'AppiumP',
            'appPackage': 'com.android.calculator2',
            'appActivity': 'com.android.calculator2.Calculator'
        }
        self.instance = webdriver.Remote('http://localhost:4723/wd/hub', desired_cap)

```

For these code, I created a class called **Driver** and for this class I created a constructor called **__init__**, where all the characteristics related to the object will be listed. Then, I modified the expression which starts the service from "drive" to "instance", just make clear the reading.

Then, I created a folder called 'pageobjects' and in this same folder I will create a file called Calc.py, where I will register all the elements and actions from this main Calculator application screen. If Calculator application had more screens (or more <i>activities</i>), we would create a file for each screen to keep our code more organized and clear. We are doing this way because we are using page objects pattern.

Calc.py file starts importing some Selenium library resources:

```bash
from webdriver.webdriver import Driver
from selenium.webdriver.support import expected_conditions as EC
from selenium.webdriver.support.wait import WebDriverWait
from appium.webdriver.common.mobileby import MobileBy
```

<i>Expected conditions</i> >> I gave him EC nickname - to reduce his name as it is a long expression. This resource is used to indicate the value for the expected condition.
<i>WebDriverWait</i> >> This resource is an excellent solution to eliminate the very famous "time.sleep" from our code. This resource basically waits for some specific element to be reachable and may also receive a <i>timeout</i> value. This is called implicit wait.
<i>MobileBy</i> >> This resource is responsible to indicate that we are in a mobile context, so we can use specific content for that.

After imports, it is time to create a class, which name I called Calculadora. For that class, I alse created a constructor to identify the elements responsible to characterize our class and, consequently, the objects that we are gonna instantiate from it. Beside elements, we will also create methods related to the behavior of that class, our Calculator, which are the actios of sum, subtraction, division and multiplication.

Before initialise the reconstruction of our elements, it worth to say that all the numeric digits (from 0 to 9) from our Calculator have prefix, changing only the last digit of the element. With this information, we may try to optimize that. So, I decided to create a method to deal with that. Thus, I will firstly map only the operators elements and most general ones like the result. Our mapping structure is like so:

```bash
class Calculadora:
    def __init__(self, driver):
        self.driver = driver
        self.result = WebDriverWait(self.driver.instance, 10).until(EC.presence_of_element_located(
            MobileBy.ID, 'com.android.calculator2:id/result'
        ))
        self.soma = WebDriverWait(self.driver.instance, 10).until(EC.presence_of_element_located(
            MobileBy.ACCESSIBILITY_ID, 'plus'
        ))
        self.divisao = WebDriverWait(self.driver.instance, 10).until(EC.presence_of_element_located(
            MobileBy.ACCESSIBILITY_ID, 'divide'
        ))
        self.multiplicacao = WebDriverWait(self.driver.instance, 10).until(EC.presence_of_element_located(
            MobileBy.ACCESSIBILITY_ID, 'multiply'
        ))
        self.subtracao = WebDriverWait(self.driver.instance, 10).until(EC.presence_of_element_located(
            MobileBy.ACCESSIBILITY_ID, 'minus'
        ))
```

After mapping those elements, it is tome to start the main methods of our Calculator application. As told before, I will use a special method to identify digits, as they share the same prefix changing only the last digit. My code is like so:
```bash
    def clicknumber(self, numero):
        _num = str(numero)
        self.driver.instance.find_element(MobileBy.ID, 'com.android.calculator2:id/digit_' + _num).click()
        assert _num in self.result.text, 'Resultado no result não é o esperado com o valor inserido'
```

This solution is only a suggestion to optimize our code. You may do something like this or event propose any other solution.

Now let me introduce you _unitTest_ library to control test flow for our application. By using this library, we will use two very important methods: _setUp()_ and _tearDown()_. Those methods are essentials for any software automation project. The objective of setUp method is prepare whatever is necessary to start our tests; tearDown method finishes test execution by closing all the used services for our environment test.
To use all of this into a design patter, I will create a folder called "tests" and, in this folder, I will create a Python file called CalculadoraTestes.py, where I will import all the necessary files for our project and, when constructing our class, I will define that this class is test case type (unittest.TestCase). This is a very simple file and on it we will write our Setup and TearDown methods (pay attention for that) and also methods related to our test cases. Every method starting with "test_" expression will be executed as a test - this is a very good resource from UnitTest library. The order of this execution (in case you have more than 1 metho with "test_") is ordered according to the distribution of those methods into your code.

Well, summarizing what we've done, our project is composed by following folders:

- Webdriver >> Our Appium connection isolated.
- PageObjects >> Here is where our elements are mapped. For each page we have a class - not necessarily in separated files. All elements and functionalities for related page are identified and solved here. 
- Tests >> Here we will create starting and ending methods and all the necessary tests. SetUp is the method responsible to start our execution. TearDown is the responsible to finish our execution. Every method starting with "test_" expression will be executed like a test. Those functionalities are resources from _unitTest_ library.

This way, we finish basic tutorials for Appium with Python course, by using Android native Calculator Application.

**Proposed activities:**

- As we did not detail a design pattern here and which one would be a good practice here, I propose you to search different design patterns for Python Projects, especially for software automation.
- Look for others resources from Selenium library.
- Look for unitTest library resources.
- As we proposed sum function here, I suggest you to keep automating with others operators.
- What do you think about automating a scientific calculator? That is the perfect moment for that! =)
- Would like to try your new automation skills by automating any other application from Play Store? That is also an excellent idea! Do not forget to share your project with the community! <3