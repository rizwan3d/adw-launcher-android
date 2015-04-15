<br>
<br>
<br>
<h1>To stay current please visit the new home for the guide <a href='http://adwthings.com/launcher/adw-theming-guide/'>here</a>.</h1>

<br><b>Disclaimer: This is a work in progress, please be patient.</b>
<br><i>original content by jbenn1980 maintained by</i><a href='http://twitter.com/klinster'>klinster</a> video by <a href='http://twitter.com/vazguard'>vazguard</a>.<br>
<br>
<br>


<br>
<br>
<hr />
<br>

<h1>Introduction</h1>
<a href='Hidden comment: 
Aside from the fact that *ADW.Launcher* comes with many customizations, you can also make themes for it and distribute them through the <a href="http://market.android.com">*Android Market*

Unknown end tag for </a>

.
'></a><br>
This guide will attempt to get you up and running so you can start making your own themes for <b>ADW.Launcher</b>. The single most important thing to note here is that you <b>must</b> build the themes with the Eclipse IDE. In other words, you are going to have to learn how to deal with Android app development from debugging your app to editing XML files among other things that entail in Android developing.<br>
<br>
<br>
<hr />
<br>

<h1>Prerequisites</h1>
The following steps must be completed in the following order<br>
<ul><li><a href='http://code.google.com/p/adw-launcher-android/wiki/ADWThemeGuide#Java_JDK_Installation'>Installing the latest Java JDK</a>
</li><li><a href='http://code.google.com/p/adw-launcher-android/wiki/ADWThemeGuide#Android_SDK_Installation'>Installing the Android SDK, updating and creating an optional Android Virtual Device</a>
</li><li><a href='http://code.google.com/p/adw-launcher-android/wiki/ADWThemeGuide#Installing_Eclipse_IDE_and_the_ADT_plug-in'>Installing Eclipse IDE and the ADT plug-in</a>
</li><li>The ADW Theme template which is <a href='http://github.com/AnderWeb/ADW.Theme-Template'>here</a> provided by AnderWeb himself.<br>
<br>
<b>You will also need some basic knowledge of:</b>
</li><li>Java<br>
</li><li>XML<br>
</li><li>Photoshop/GIMP or use any other image editor that you're comfortable with.<br>
</li><li>Time<br>
</li><li>Patience<br>
</li><li>Many sleepless nights<br>
</li><li>Some help from people willing to help, just ask<br>
</li><li>Your favorite energy/caffeinated drink or if you're on the wild side some alcoholic beverage.</li></ul>


<br>
<hr />
<br>


<h2>Java JDK Installation</h2>

<h3>For Windows</h3>

If you're completely new to making <b>ADW.Launcher</b> themes or if you've never heard of the Java JDK, chances are you do not have the Java JDK installed on your machine. So the first step to start developing <b>ADW.Launcher</b> themes is to install the latest Java JDK. I'd recommend getting JDK version 6 update (latest) since JDK version 7 is not really necessary at this point. Head on over to the Oracle site on the link below, download the version specific to your machine's architecture (x86 or x64) and follow the prompts<br>
<br>
<a href='http://www.oracle.com/technetwork/java/javase/downloads/index.html'>http://www.oracle.com/technetwork/java/javase/downloads/index.html</a>


<h3>For Linux</h3>

Download OpenJDK from your distro's repo or manually download the tarball from Oracle, do the proper symlinks and proper alternative updates.<br>
<br>
<br>
<br>
<hr />
<br>


<h2>Android SDK Installation</h2>

<h3>For Windows</h3>

For a more detailed instructions go here <a href='http://developer.android.com/sdk/installing.html'>http://developer.android.com/sdk/installing.html</a>

Download the Android SDK from here <a href='http://developer.android.com/sdk/index.html'>http://developer.android.com/sdk/index.html</a>


To download the Android SDK on Windows<br>
<br>
<ol><li>Download the executable file and follow the prompts. There are a few issues with 64 bit architecture<br>
<br>
Once you reach the final step on the SDK installer, make sure you tick the check box that says to run the <b>SDK Manager</b> and click finish.</li></ol>

The <b>SDK Manger</b> should now start up. Make sure you download at minimum the Google USB Driver along with everything in the Tools folder and the JellyBean SDK, Samples and Documentation. The optional ones being the Google TV, KYOCERA, SONY, Galaxy tab<br>
<br>
<br>
<br>
<pre><code>C:\Program Files\Android\android-sdk\<br>
	\add-ons<br>
	\docs<br>
        \extras<br>
        \google-market_billing<br>
	\market_licensing<br>
	\platforms<br>
        \platform-tools<br>
	\samples<br>
	\temp<br>
	\tools<br>
	\usb_driver<br>
	SDK Readme.txt<br>
	SDK Setup.exe<br>
</code></pre>
<br>
<h3>For Linux</h3>
Download the Android SDK from here <a href='http://developer.android.com/sdk/index.html'>http://developer.android.com/sdk/index.html</a>
and select the Linux zip. Save the zip file to your ~/ directory (/home/username/SDKfolder). Extract the zip file to a folder called android. Inside that folder it should contain the following files and directories...<br>
<pre><code>~/android/<br>
  SDK Readme.txt<br>
  tools/<br>
  platforms/<br>
  add-ons/<br>
<br>
</code></pre>

Follow the ReadMe instructions and start the SDK Manager. Navigate to /tools and run android. Update/Download the minimum files described in the Windows section.<br>
<br>
<br>
<br>

<h3>For both - Optional: Creating an Android Virtual Device</h3>
After the downloads have finished & since we still have the SDK Manager window open we can go ahead and set-up an <b>Android Virtual Device (AVD)</b> to aid in theme creation.<br>
<br>
<ul><li>Click Virtual Devices > New<br>
</li><li>Give your device a name<br>
</li><li>Specify the target i.e. Android 2.2 - api level 8 (for froyo)<br>
</li><li>Specify the size of your virtual SD card<br>
</li><li>Click Create AVD</li></ul>

Congratulations you now have an <b>Android Virtual Device</b> on your machine to help with <b>ADW.Launcher</b> theme creation.<br>
<br>
<h4>For Windows - Intel Virtualization Tool</h4>
In order to take full advantage of the Intel x86 Atom System Image (available for ICS (4.0.3) and JellyBean currently), you need to download the Intel x86 Emulator Accelerator (HAXM) and install it.<br>
<br>
To install it you would need to navigate to wherever your android SDK folder is and look for the extras folder then go to the Intel folder and go to the Hardware_Accelerated_Execution_Manager. Follow the installer's instructions and you should be set for a more native emulator on Windows.<br>
<br>
<br>
<hr />
<br>


<h2>Installing Eclipse IDE and the ADT plug-in</h2>

Download the latest Eclipse version <b>Eclipse IDE for Java Developers</b> from here <a href='http://www.eclipse.org/downloads/'>http://www.eclipse.org/downloads/</a> remembering to choose your appropriate operating system and system architecture.<br>
<br>
<h3>For Windows</h3>

Download select the appropriate version of Eclipse taking into consideration your operating system and system architecture.<br>
Once downloaded run the .exe and follow the prompts.<br>
<br>
<h3>For Linux</h3>

If you want the latest version of the Eclipse IDE then head over to the downloads page here<br>
<br>
<a href='http://www.eclipse.org/downloads/'>http://www.eclipse.org/downloads/</a>

and download the appropriate .tar.gz version of Eclipse and remember to choose your correct system architecture.<br>
<br>
Once downloaded you should extract it and move the eclipse folder it to your home directory<br>
<br>
The directory should look like so:<br>
<br>
<pre><code> eclipse<br>
        /about_files<br>
	/configuration<br>
	/dropins<br>
	/features<br>
	/p2<br>
	/plugins<br>
	/readme<br>
	about.html<br>
	artifacts.xml<br>
        eclipse<br>
	eclipse.ini<br>
	epl-v10.html<br>
        icon.xpm<br>
        libcairo-swf.so<br>
	notice.html<br>
</code></pre>

To launch eclipse open terminal then run these commands<br>
<pre><code>cd ~/eclipse<br>
eclipse<br>
</code></pre>

Eclise should start shortly.<br>
<br>
To make the process easier, open your command prompt and type<br>
<pre><code>gedit .bashrc<br>
</code></pre>
On gedit insert the following line on the top of the file.<br>
<pre><code>#eclipse<br>
export PATH=/home/(your username)/eclipse/:$PATH<br>
</code></pre>
substitute (your username) with your current user name<br>
save and exit.<br>
<br>
You should now be able to run Eclipse from any terminal window by<br>
simply typing the command<br>
<pre><code>eclipse<br>
</code></pre>
and pressing enter.<br>
<br>
Some Distributions of Linux <i>may</i> have an older version of Eclipse in their repositories. If you choose to go that route know that you'll be fine. I've personally found no issues using Galileo, Helios or Indigo(current version)<br>
<br>
<br>
<h3>For Both: Installing The ADT Plug-in</h3>

To install ADT Plug-in the Android Development Tool (additional instructions can be found here <a href='http://developer.android.com/sdk/eclipse-adt.html/'>http://developer.android.com/sdk/eclipse-adt.html/</a>)<br>
<br>
Start Eclipse, then select Help > Install New Software.<br>
<br>
In the Available Software dialog, click Add....<br>
<br>
In the Add Site dialog that appears, enter a name for the remote site (for example, "Android Plugin") in the "Name" field.<br>
<br>
In the "Location" field, enter this URL:<br>
<br>
<a href='https://dl-ssl.google.com/android/eclipse/'>https://dl-ssl.google.com/android/eclipse/</a>

Note: If you have trouble acquiring the plugin, you can try using "http" in the URL, instead of "https" (https is preferred for security reasons).<br>
<br>
Click OK.<br>
<br>
Back in the Available Software view, you should now see "Developer Tools" along with Native Tools added to the list. Select the checkbox next to Developer Tools only and make sure you uncheck the Native Tools pakage, this will automatically select the nested tools Android DDMS and Android Development Tools. Click Next.<br>
<br>
In the resulting Install Details dialog, the Android DDMS and Android Development Tools features are listed. Click Next to read and accept the license agreement and install any dependencies, then click Finish.<br>
<br>
Restart Eclipse.<br>
<br>
<h3>Connecting the Android SDK to Eclipse</h3>

This would be the opportune time to link up Eclipse to the Android SDK. To do this we let Eclipse restart. Once it restarts we navigate to Window and select Preferences. On the Preferences window we select Android (this option is found on the right). Once you select Android, you'll notice a warning stating that you haven't specified a location. To fix this, simply navigate to the appropriate directory. If you've followed the instructions on this guide then the directory of interest is the root of your C drive - C:\android. This tells Eclipse where the Android SDK is located.<br>
<br>
<br>
<br>
<hr />
<br>


<h1>Getting ADW.Launcher Onto Your Virtual Device</h1>

Download the .apk file the downloads list to your desktop<br>
<br>
<a href='http://code.google.com/p/adw-launcher-android/downloads/list'>http://code.google.com/p/adw-launcher-android/downloads/list</a>

Make sure to download the appropriate version to suit your needs.<br>
<br>
<b>The following instructions are for a minimum Virtual Machine of Level 7 and using the standalone version of ADW. If you want to use</b>

<h3>For Windows</h3>

Browse to your Android SDK installation (C:\Android)<br>
<br>
<ul><li>Open the platform-tools folder<br>
</li><li>Copy or Move the .apk file you downloaded to this directory (C:\android\platform-tools)<br>
</li><li>Run the Android.bat file, this will start the Android SDK & AVD Manager (there should already be a Virtual Device that you created earlier listed)<br>
</li><li>Click your virtual device & Click Start.<br>
</li><li>On the <i>Launch Options</i> window <b>Uncheck</b> <i>Scale display to real size</i> as the window may be larger than your monitor resolution can handle<br>
</li><li>Click Launch,  this will start the Android virtual device emulator (it may take a minute or two to load)</li></ul>

Once started you can navigate around with the mouse by clicking & dragging on the screen (to simulate your finger) or by clicking<br>
<br>
<ul><li>Open your Command Prompt/Terminal<br>
</li><li>Change the directory to C:\android\platform-tools ( cd C:\android\platform-tools )<br>
<br>
Run the following command:</li></ul>

<pre><code>adb install ADW.Launcher_v115_standalone.apk                                                     <br>
</code></pre>

The following code should appear in your command prompt:<br>
<pre><code>C:\android\platform-tools&gt;adb install ADW.Launcher_v115_standalone.apk<br>
1183 KB/s (1357755 bytes in 1.120s)                          <br>
        pkg: /data/local/tmp/ADW.Launcher_v115_standalone.apk<br>
Success                                                      <br>
</code></pre>

Now click on the Home button on your emulated device & you should be given the option to choose between your Home screen launchers<br>
<br>
ADW.Launcher is now installed on your virtual android device<br>
<br>
<h3>For Linux</h3>

Browse to your Android SDK installation (/android)<br>
<br>
<ul><li>Open the platform-tools folder<br>
</li><li>Copy or Move the .apk file you downloaded to this directory (/android/platform-tools)<br>
</li><li>Run the android file located under /tools, this will start the Android SDK & AVD Manager (there should already be a Virtual Device that you created earlier listed)<br>
</li><li>Click your virtual device & Click Start.<br>
</li><li>On the <i>Launch Options</i> window <b>Uncheck</b> <i>Scale display to real size</i> as the window may be larger than your monitor resolution can handle<br>
</li><li>Click Launch,  this will start the Android virtual device emulator (it may take a minute or two to load)</li></ul>

Once started you can navigate around with the mouse by clicking & dragging on the screen (to simulate your finger) or by clicking<br>
<br>
<ul><li>Open your Command Prompt/Terminal<br>
</li><li>Change the directory to /android/platform-tools ( cd /android/platform-tools )<br>
<br>
Run the following command:</li></ul>

<pre><code>adb install ADW.Launcher_v115_standalone.apk                                                     <br>
</code></pre>

The following code should appear in your command prompt:<br>
<pre><code>/android/platform-tools&gt;adb install ADW.Launcher_v115_standalone.apk<br>
1183 KB/s (1357755 bytes in 1.120s)                          <br>
        pkg: /data/local/tmp/ADW.Launcher_v115_standalone.apk<br>
Success                                                      <br>
</code></pre>

<b>If you're having issues with ADB not recognizing your device you need to update your UDEV rules to include your device</b>

<br>
<hr />
<br>



<h1>Getting Started On Your ADW.Launcher Theme</h1>

Grab the ADW.Launcher theme template from Anderweb's Github here<br>
<br>
<a href='http://github.com/AnderWeb/ADW.Theme-Template/archives/master'>http://github.com/AnderWeb/ADW.Theme-Template/archives/master</a>

Extract the template to a new folder. Name the folder to whatever your theme name is. For these instructional purposes we're going go ahead and call it "My Cool ADW Theme". Your folder should now contain the following:<br>
<br>
<pre><code>My Cool ADW Theme\<br>
	\res<br>
	\src<br>
        ADW_Template2.iml<br>
	AndroidManifest.xml<br>
        COPYING<br>
        README<br>
	default.properties	<br>
</code></pre>

You can leave folder anywhere just as long as it's accessible to you since you'll be constantly opening it and updating the contents inside the \res folder.<br>
<br>
Now with that out of the way, we must run Eclipse and import our project to the workspace.<br>
<br>
These instructions are found on the README file. This guide contains a few relevant updates from the README file so read them close and carefully<br>
<br>
<b>Loading the template into eclipse:</b>
<ul><li>Configure your Eclipse Worskpace to use Java 1.6 (very Important!)<br>
</li><li>On Eclipse, Go to file and select New > Android Project<br>
</li><li>On the New Android Project screen, select "Project from existing source" and browse to your template's directory.<br>
</li><li><b>Set the build target to Android 2.2</b>
</li><li>Click finish.</li></ul>

<b>Modify the app packagename and path (under</b>\src\x.x.x<b>&</b>\gen\x.x.x<b>, you should change it from x.x.x to your.package.name)</b>
<ul><li>On eclipse, look into your project explorer\package explorer, rightclick the x.x.x package and select "Refactor->Rename..." and follow the instructions.<br>
</li><li>To open the package explorer window (if not already open) Click Window > Show View > Package explorer</li></ul>

<b>Editing the AndroidManifest.xml:</b>
<ul><li>EDIT ONLY the packagename AND versioncode/versionname to suit your needs.<br>
</li><li>If you remove/change the installLocation param, your theme could not be loaded on boot on froyo phones.<br>
</li><li>If you remove/change the "org.adw.launcher.THEMES" intent filter and/or the "android.intent.category.DEFAULT" category, your theme won't be visible to ADW.Launcher users.<br>
</li><li>This template is preconfigured to NOT show on the application drawer so users don't get bloated with theme icons on their app drawers.</li></ul>

<ul><li>Edit the res/values/theme_config.xml to your needs.</li></ul>

<ul><li>Edit the different drawables in there.<br>
<br>
<h2>Custom Icon Naming - Video and Databases</h2></li></ul>

<a href='http://www.youtube.com/watch?feature=player_embedded&v=bCLRd7fBaa4' target='_blank'><img src='http://img.youtube.com/vi/bCLRd7fBaa4/0.jpg' width='425' height=344 /></a><br>
<br>
As the video states, there is an extensive and ever growing list of Android application activity names. Just navigate to the following website and search for the application name you are looking for.<br>
<a href='http://adwlauncher.wikia.com/wiki/Theme_Icon_Name_Database'>http://adwlauncher.wikia.com/wiki/Theme_Icon_Name_Database</a>
<br>And remember to please contribute so everyone can benefit.<br>
<br>
There is another Android application activity name database put together by <a href='http://twitter.com/JonFHancock'>@JonFHancock</a>. Simply navigate to his website - <a href='http://activities.droidicon.com/'>http://activities.droidicon.com/</a> and run a search for the app you're looking for but be prepared if multiple names come up. In some circumstances you may have to try them all.<br>
If you're interested in helping Jon's database grow then install the app that he developed called <b>Android Activities</b>. Download it for free from the <a href='https://market.android.com/details?id=com.droidicon.androidactivities'>Android Market</a>.<br>
<a href='Hidden comment: 
* Rename res/xml/noShader.xml to shader.xml to enable icon shading. See the file for instructions on writing a shader.

* To put icons in the ADW Icon pack to be used in ADW.Launcher, just edit the res/values/icon_pack.xml file and add lines like the following one:

<pre><code>        <item>png_finelane_no_extension</item>
        One line per icon to be shown in the icon pack. Use only images, not xml drawables.
        EXAMPLES:
        	res/drawable/icon1.png --> <item>icon1</item>
        	res/drawable-hdpi/my_cool_icon.png --> <item>my_cool_icon</item>
		FULL FILE:
			<?xml version="1.0" encoding="utf-8"?>
			<resources>
			    <string-array name="icon_pack" translatable="false">
			    	<item>icon1</item>
			    	<item>my_cool_icon</item>
			    </string-array>
			</resources>
</code></pre>

* To use a custom font on your theme, put the TTF file in res/assets/themefont.ttf.
Make sure the font is working, some BIG (in filesize) fonts or bad encoded fonts can cause problems.

* Export the apk from Eclipse as every other android app.*
'></a><br>
<br>
<br>
<hr />
<br>


<h1>Signing and Exporting Your Theme</h1>

To export an application for use on a physical device or to upload to the market, you to sign the application with what's called a keystore or signing key.<br>
<br>
Setting up your signing key is relatively straight forward thanks to Eclipse and the ADT plug-in. All you have to do is export your theme in one of two ways. One is navigate to File > Export, select the Android folder and choose Export Android Application and hit next. On the next window hit the browse button. Here is where you'll specify which project we want to export. In this case it will be our theme. The second way is to simply right-click on the project folder from the Package Explorer and navigate to Android Tools > Export Singed Application. The prompt will then ask you for a keystore's location and password. First timers will have to click the on the Create New Keystore radio button. Now it will just be a matter of simply following the prompts. It'll guide you through the necessary steps which are giving your keystore a name, an expiration (in years) and ask you to store it on a location. Store it in a safe location.<br>
<br>
<br>
Once you reach the final step, the window will ask you to point to a location on your computer to save the application package to and the application's name. Make sure you remember what folder/path you choose and make sure that the name ends in the .apk suffix.<br>
<br>
<br>
For example: Continuing with the "My Cool ADW Theme" example from earlier - which can be found <a href='http://code.google.com/p/adw-launcher-android/wiki/ADWThemeGuide#Android_SDK_Installation'>here</a> To export our signed application. we simply export the project by following one of the steps described above. Once we get to the last window, we can change the auto-generated name to a better one to reflect the name of the theme or if we're satisfied with My Cool ADW Theme.apk name then all we have to do is specify a path. Please make sure to remember to include the prefix <b>.apk</b>. When all looks OK we can now go ahead and click on the Finish button and wait a few seconds or minutes depending on your computer's processing speed for Eclipse to create the APK.<br>
<br>
<br>
You should now end up with an Android package/application ready to be installed to your phone or to the Android Device Emulator.<br>
<br>
<br>
<b>IMPORTANT:</b> If your application is error free in Eclipse it doesn't always translate to a perfectly functioning Application. Some times it may force close and cause you to ask <b>WHY?</b> but that's where the debugging aspect comes into play.<br>
<br>
<br>
For additional information or help with signing Android applications please visit the Official Android site. It provides more information on how to sign your applications manually if that is what you choose.<br>
<br>
<br>
<a href='http://developer.android.com/guide/publishing/app-signing.html'>http://developer.android.com/guide/publishing/app-signing.html</a>


<br>
<hr />
<br>