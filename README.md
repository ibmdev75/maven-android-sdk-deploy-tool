
How to Use
----------

Download the latest Android SDK from
http://developer.android.com/sdk/index.html following the instructions
there.

Apache Maven 3.1.1 or higher is required!
 
- For the default usage of the deployer install **all platforms and
add-on apis**, ensure that all folder in the platforms folder have
names like android-3, android-4 and so on.  

- If you find names using the platform version (e.g. 15) in the folder
name reinstall that platform from the android tool.

- In a similar manner the folder names in add-ons have to use the
pattern addon-google_apis-google-3 up to addon-google_apis-google-15.

- If the folder names are different reinstall the add-ons as well

Set up the environment variable ANDROID_HOME to contain the absolute
 folder you just installed the SDK to (e.g. under bash: export
 ANDROID_HOME=/opt/android_sdk_linux) and ensure that the folder for
 ANDROID_HOME and all files within are readable by the current user

Run the command

    mvn install

in the root folder of this project (same as README you are just
reading) to install all platforms and add-on apis

To install only a certain sdk level use

    mvn install -P 1.5
    mvn install -P 1.6
    mvn install -P 2.1
    mvn install -P 2.2
    mvn install -P 2.3.3
    mvn install -P 3.0
    mvn install -P 3.1
    mvn install -P 3.2
    mvn install -P 4.0
    mvn install -P 4.0.3
    mvn install -P 4.1
    mvn install -P 4.2
    mvn install -P 4.3
    mvn install -P 4.4
    mvn install -P 4.4W
    mvn install -P 5.0
    mvn install -P 5.1

As a result you should find the android.jar and maps.jar and a number of other
libraries in your users local repository (~/.m2/repository/) and you can therefore
use the following dependencies in your project

For the core platforms providing the Android API use

```xml
<dependency>
  <groupId>android</groupId>
  <artifactId>android</artifactId>
  <version>x.y.z</version>
  <scope>provided</scope>
</dependency>
```
with versions of 

```xml
  <version>1.5_r4</version>
  <version>1.6_r3</version>
  <version>2.1_r3</version>
  <version>2.2_r3</version>
  <version>2.3.3_r2</version>
  <version>3.0_r2</version>
  <version>3.1_r3</version>
  <version>3.2_r1</version>
  <version>4.0_r4</version>
  <version>4.0.3_r5</version>
  <version>4.1.2_r5</version>
  <version>4.2.2_r3</version>
  <version>4.3.1_r3</version>
  <version>4.4.2_r4</version>
  <version>4.4W.2_r2</version>
  <version>5.0_r2</version>
  <version>5.1_r1</version>
```

For the maps add ons use a dependency

```xml
<dependency>
  <groupId>com.google.android.maps</groupId>
  <artifactId>maps</artifactId>
  <version>x.y.z</version>
  <scope>provided</scope>
</dependency>
```

with versions of 3_r3, 4_r2, 7_r1, 8_r2, 11_r1, 12_r1, 
13_r1, 14_r2, 15_r2, 16_r3, 17_r3, 18_r3, 19_r10, 21_r1

For the usb add on

```xml
<dependency>
  <groupId>com.android.future</groupId>
  <artifactId>usb</artifactId>
  <version>x.y.z</version>
  <scope>provided</scope>
</dependency>
```

with versions of 10_r2, 12_r1, 13_r1, 14_r2, 15_r2, 16_r3, 17_r3, 
18_r3, 19_r4, 21_r1


Android SDK Maven Repositories

The Maven repositories from the Android SDK for Google and Android are copied to the local repository or uploaded to 
a remote repository manager just like they are in the SDK and contain all components from these repositories. 
Currently they are in the package space com.android.support and com.google.android and present the preferred components 
for usage. Specifically the various compatibility and support libraries as Android Archives:

```xml
<dependency>
  <groupId>com.android.support</groupId>
  <artifactId>appcompat-v7</artifactId>
  <version>x.y.z</version>
  <type>aar</type>
</dependency>
```

with versions 18.0.0, 19.0.0, 19.0.1, 19.1.0, 20.0.0, 21.0.0, 21.0.2, 21.0.3

```xml
<dependency>
  <groupId>com.android.support</groupId>
  <artifactId>cardview-v7</artifactId>
  <version>x.y.z</version>
  <type>aar</type>
</dependency>
```

with versions 21.0.0, 21.0.2, 21.0.3

```xml
<dependency>
  <groupId>com.android.support</groupId>
  <artifactId>gridlayout-v7</artifactId>
  <version>x.y.z</version>
  <type>aar</type>
</dependency>
```

with versions 13.0.0, 18.0.0, 19.0.0, 19.0.1, 19.1.0, 20.0.0, 21.0.0, 21.0.2, 21.0.3

```xml
<dependency>
  <groupId>com.android.support</groupId>
  <artifactId>leanback-v17</artifactId>
  <version>x.y.z</version>
  <type>aar</type>
</dependency>
```

with versions 21.0.0, 21.0.2, 21.0.3

```xml
<dependency>
  <groupId>com.android.support</groupId>
  <artifactId>mediarouter-v7</artifactId>
  <version>x.y.z</version>
  <type>aar</type>
</dependency>
```

with versions 18.0.0, 19.0.0, 19.0.1, 19.1.0, 20.0.0, 21.0.0, 21.0.2, 21.0.3

```xml
<dependency>
  <groupId>com.android.support</groupId>
  <artifactId>palette-v7</artifactId>
  <version>x.y.z</version>
  <type>aar</type>
</dependency>
```

with versions 21.0.0, 21.0.2, 21.0.3

```xml
<dependency>
  <groupId>com.android.support</groupId>
  <artifactId>recyclerview-v7</artifactId>
  <version>x.y.z</version>
  <type>aar</type>
</dependency>
```

with versions 21.0.0, 21.0.2, 21.0.3

```xml
<dependency>
  <groupId>com.android.support</groupId>
  <artifactId>support-v13</artifactId>
  <version>x.y.z</version>
  <type>aar</type>
</dependency>
```

with versions 13.0.0, 18.0.0, 19.0.0, 19.0.1, 19.1.0, 20.0.0, 21.0.0, 21.0.2, 21.0.3

```xml
<dependency>
  <groupId>com.android.support</groupId>
  <artifactId>support-v4</artifactId>
  <version>x.y.z</version>
  <type>aar</type>
</dependency>
```

with versions 13.0.0, 18.0.0, 19.0.0, 19.0.1, 19.1.0, 20.0.0, 21.0.0, 21.0.2, 21.0.3

Besides the artifacts provided for the compatibility libraries from the Android SDK Maven Repositories 
the following are also provided. 
For the compatibility extra (ATTENTION! Do NOT use provided scope!!) 

```xml
<dependency>
  <groupId>android.support</groupId>
  <artifactId>compatibility-v4</artifactId>
  <version>21.0.3</version>
</dependency>

<dependency>
  <groupId>android.support</groupId>
  <artifactId>compatibility-v13</artifactId>
  <version>21.0.3</version>
</dependency>
```

If you find that the above `<dependency>` fails due to conflicts, your project and it's dependencies may 
both depend on the compatibility extra.  The first option is to add an `<exclude>` 
clause to each dependency that uses the library, 
as [described here](https://groups.google.com/forum/#!msg/actionbarsherlock/2cLR48IArck/U8--60QxeTkJ).  This works 
with command line builds but it may not work with your IDE.

If you have problems with `<exclude>`, another option is to override the `<groupid>`, `<artifactid>`, and `<version>` 
properties used by the deployer to match Google's published library.

Then override `support-v4` or `support-v13` during installation:

    mvn install -Dextras.compatibility.v4.groupid=com.google.android \
                -Dextras.compatibility.v4.artifactid=support-v4 \
                -Dextras.compatibility.v4.version.prefix=r

    mvn install -Dextras.compatibility.v13.groupid=com.google.android \
                -Dextras.compatibility.v13.artifactid=support-v13 \
                -Dextras.compatibility.v13.version.prefix=r

In order to use v7 extra, both dependencies (apklib & jar) are needed

```xml
<dependency>
  <groupId>android.support</groupId>
  <artifactId>compatibility-v7</artifactId>
  <version>21.0.3</version>
  <type>apklib</type>
</dependency>

<dependency>
  <groupId>android.support</groupId>
  <artifactId>compatibility-v7</artifactId>
  <version>21.0.3</version>
  <type>jar</type>
</dependency>
```

For the v7 appcompat library additional dependencies (apklib & jar) are required (Deprecated)

```xml
<dependency>
  <groupId>android.support</groupId>
  <artifactId>compatibility-v7-appcompat</artifactId>
  <version>21.0.3</version>
  <type>apklib</type>
</dependency>

<dependency>
  <groupId>android.support</groupId>
  <artifactId>compatibility-v7-appcompat</artifactId>
  <version>21.0.3</version>
  <type>jar</type>
</dependency>
```

The v7 appcompat library an Android Archive dependency (aar) as provided by the Android SDK Google repository

```xml
<dependency>
  <groupId>com.android.support</groupId>
  <artifactId>appcompat-v7</artifactId>
  <version>21.0.3</version>
  <type>aar</type>
</dependency>
```
with versions 18.

For the v7 gridlayout library additional dependencies (apklib & jar) are required (Deprecated)

```xml
<dependency>
  <groupId>android.support</groupId>
  <artifactId>compatibility-v7-gridlayout</artifactId>
  <version>21.0.3/version>
  <type>apklib</type>
</dependency>

<dependency>
  <groupId>android.support</groupId>
  <artifactId>compatibility-v7-gridlayout</artifactId>
  <version>20.0.0</version>
  <type>jar</type>
</dependency>
```

For the v7 gridlayout library an additional dependency (aar) is required

```xml
<dependency>
  <groupId>com.android.support</groupId>
  <artifactId>gridlayout-v7</artifactId>
  <version>21.0.0-rc1</version>
  <type>aar</type>
</dependency>
```

For the v7 mediarouter library additional dependencies (apklib & jar) are required (Deprecated)

```xml
<dependency>
  <groupId>android.support</groupId>
  <artifactId>compatibility-v7-mediarouter</artifactId>
  <version>20.0.0</version>
  <type>apklib</type>
</dependency>

<dependency>
  <groupId>android.support</groupId>
  <artifactId>compatibility-v7-mediarouter</artifactId>
  <version>20.0.0</version>
  <type>jar</type>
</dependency>
```

For the Google Analytics extra (ATTENTION! Do NOT use provided scope!!) (Deprecated)
See: https://developers.google.com/analytics/devguides/collection/android/v4/
Google Analytics V2
```xml
<dependency>
  <groupId>com.google.android.analytics</groupId>
  <artifactId>analytics</artifactId>
  <version>3.0.0</version>
</dependency>
```

For the Google AdMob Ads extra (ATTENTION! Do NOT use provided scope!!) (Deprecated)
See: http://googleadsdeveloper.blogspot.ca/2014/02/since-joining-google-play-services-back.html 

```xml
<dependency>
  <groupId>com.google.android.admob</groupId>
  <artifactId>admob</artifactId>
  <version>6.4.1-r11.0.0</version>
</dependency>
```

For the Google Cloud Messaging Library extra client library (ATTENTION! Do NOT use provided scope!!) (Deprecated)

```xml
<dependency>
  <groupId>com.google.android.gcm</groupId>
  <artifactId>gcm-client</artifactId>
  <version>3.0.0</version>
</dependency>
```

For the Google Cloud Messaging Library extra server library (ATTENTION! Do NOT use provided scope!!)

You will need to run the extras/gcm module manually since it is deactivated
due to GCM being deprecated by Google in the Android SDK.

```xml
<dependency>
  <groupId>com.google.android.gcm</groupId>
  <artifactId>gcm-server</artifactId>
  <version>3.0.0</version>
</dependency>
```
    
For the Android annotations tools 

```xml
<dependency>
  <groupId>com.google.android.annotations</groupId>
  <artifactId>annotations</artifactId>
  <version>22.6.2</version>
  <scope>provided</scope>
</dependency>
```

For the uiautomator jar

```xml
<dependency>
  <groupId>android.test.uiautomator</groupId>
  <artifactId>uiautomator</artifactId>
  <version>4.1.2_r4</version>
  <scope>provided</scope>
</dependency>
````

with versions 4.1.2_r4, 4.2.2_r2, 4.3_r2, 4.4.2_r3
    
For the Google Play Services extra (ATTENTION! Do NOT use provided scope!!) (Deprecated)

```xml
<dependency>
  <groupId>com.google.android.gms</groupId>
  <artifactId>google-play-services</artifactId>
  <version>16.0.0</version>
  <type>apklib</type>
</dependency>
<dependency>
  <groupId>com.google.android.gms</groupId>
  <artifactId>google-play-services</artifactId>
  <version>16.0.0</version>
  <type>jar</type>
</dependency>
```

For the Google Play Services extra (ATTENTION! Do NOT use provided scope!!)

```xml
<dependency>
  <groupId>com.google.android.gms</groupId>
  <artifactId>play-services</artifactId>
  <version>4.4.52</version>
  <type>aar</type>
</dependency>
```

For the Google Play Services for Froyo extra (ATTENTION! Do NOT use provided scope!!)

```xml
<dependency>
  <groupId>com.google.android.gms</groupId>
  <artifactId>google-play-services-for-froyo</artifactId>
  <version>12.0.0</version>
  <type>apklib</type>
</dependency>
<dependency>
  <groupId>com.google.android.gms</groupId>
  <artifactId>google-play-services-for-froyo</artifactId>
  <version>12.0.0</version>
  <type>jar</type>
</dependency>
```

For the Google Play APK Expansion extra (ATTENTION! Do NOT use provided scope!!)

```xml
<dependency>
  <groupId>com.google.android.apk.expansion</groupId>
  <artifactId>play-apk-expansion-downloader</artifactId>
  <version>3.0.0</version>
  <type>apklib</type>
</dependency>
<dependency>
  <groupId>com.google.android.apk.expansion</groupId>
  <artifactId>play-apk-expansion-zip</artifactId>
  <version>3.0.0</version>
  <type>apklib</type>
</dependency>
```

For the Google Play Licensing extra (ATTENTION! Do NOT use provided scope!!)

```xml
<dependency>
  <groupId>com.google.android.licensing</groupId>
  <artifactId>play-licensing</artifactId>
  <version>2.0.0</version>
  <type>apklib</type>
</dependency>
```

For Google Glass development

```xml
<!-- For development on ICS with GDK -->
<dependency>
	<groupId>android</groupId>
	<artifactId>android</artifactId>
	<version>4.0.3_r3</version>
	<scope>provided</scope>
</dependency>
<dependency>
	<groupId>com.google.android.gdk</groupId>
	<artifactId>gdk</artifactId>
	<version>15_r2</version>
	<scope>provided</scope>
</dependency>

<!-- For development on KitKat with GDK -->
<dependency>
    <groupId>android</groupId>
    <artifactId>android</artifactId>
    <version>4.4.2_r3</version>
    <scope>provided</scope>
</dependency>
<dependency>
    <groupId>com.google.android.gdk</groupId>
    <artifactId>gdk</artifactId>
    <version>19_r4</version>
    <scope>provided</scope>
</dependency>
```

To install only a specific module use

    mvn clean install -N

in any parent folder of the desired package and then the usual
                                  1
    mvn clean install

For example to install only the compatibility v4 extra you can do the
following

    mvn clean install -N
    cd extras
    mvn clean install -N
    cd compatibility-v4
    mvn clean install

Similar for only API level 12 add on use

    mvn clean install -N
    cd add-ons
    mvn clean install -N
    cd google-apis-12
    mvn clean install

The same could be done with deploy


How To Use for Deploying Onto Remote Server
-------------------------------------------

The above deployment works fine for one machine, but what if you need
to supply a whole team of developers and a cluster of build machines
with the artifacts? Then it is best to deploy to a repository manager 
like Sonatype Nexus.

As a condition you need to have a repository server used by all
those machines and the following process will deploy to this server,
which will in turn provide the artifacts to all the machines.

Edit the repo.url property in the pom.xml to point to the repository you want to publish to. The recommended practice
is to have a separate repository for the Android components and expose it via a repository group. The repository needs
to be in Maven 2 format and use a release policy (not snapshots). For repeated runs of the deployer, you need to ensure
to allow redeployment into the specific repository. By default this is not the case for release repositories! 

Then add a server with the credentials to your settings.xml.

```xml
<settings>
  <servers>
    <server>
      <id>android.repo</id>
      <username>your username</username>
      <password>your password</password>
    </server>
  </servers>
</settings>
```

Run the command

    mvn deploy

in the root folder of this project (same as README you are just
reading), you can also use the same profile options for the different
api level. As a result you should find the artifact in the repository
of your remote server

For more information about this stuff look at the documentation for
the maven-deploy-plugin.


Javadoc
-------

It is possible to create javadoc artifacts for the platforms
where available in the sdk. To call it use

    mvn clean install -Pall,with-javadoc

and the respective javadoc jars will be created and also installed.
This also works for deployment to a repository server

    mvn clean deploy -Pall,with-javadoc

Mailinglist - Questions
-----------------------

Please direct any questions to the community at the Maven Android
Developers mailing list at
http://groups.google.com/group/maven-android-developers
 
Known problems
-------------

- Platforms and Add on folder names changes in SDK

When updating an existing android sdk install the add-ons subfolder
can sometimes be reused and their contents be updates so you could end
up with e.g. the google maps-4r2 in a folder named
google_apis-4_r01. To work around this just uninstall the affected
add-on and reinstall it with the android sdk tool.

Similarly the platform specific folder used to be e.g. android-1.5 and
is now android-3 using the api level as the numeric identifier. If
your SDK install uses the old folder names for any platform simply
reinstall that platform with the android tool.

In a similar manner the folder for the support libraries in the the sdk
used to be compatibility and is now support

The Add ons used different folder names as well. The Maven Android SDK
Deployer' is adapted to the lastet naming
scheme. To do that yourself remove all "Google APIs by Google Inc" in
the android SDK manager and install them again.

Similar problem occurs with the extras version identifier. If the folders 
naming is 100% allright and you receive the messages about not finding 
some artifacts - remove extras and reinstall them back. That's because Google
changed the version identifier naming policy. For example for support extras 
it was 19, now it's 19.0.1

Issues
------

If you find any problems or would like to suggest a feature, please
feel free to file an issue on github at
http://github.com/mosabua/maven-android-sdk-deployer/issues

Potential todo items
--------------------

- add custom pom files for install/deploy that eg. define dependency
  from maps to android jar

- maybe some sort of reporting of errors, failures and success as well
