### Downloader Cordova Download Plugin

Cordova plugin for downloading files from server.

### Supported Platforms

- Android
- iOS

### Installation

### 1) 
Télécharger le dossier <strong>ionic-3-4-downloader-manager-master<strong> avec le boutton CLONE OR DOWNLOAD

### 2) 
Dézziper le dossier téléchargé.

### 3)
Si vous avez déjà un dossier <strong> PLUGINS <strong> ajouter le dossier <strong>ionic-3-4-downloader-manager-master<strong> téléchargé au paravant.

### 4)
Mettez le dossier  <strong>ionic-3-4-downloader-manager-master<strong> dans votre dossier <strong> PLUGINS </strong> de votre projet IONIC.   
 
Si vous avez déjà BUILD votre apk(ANDROID) ou app(IOS) taper la commande <strong>ionic cordova platform rm android<strong>
ou <strong>ionic cordova platform rm ios<strong> (dans votre projet IONIC) ,
Au cas ou ce n'est pas encore faits, Tapez la commande <strong>ionic cordova platform add android<strong> ou <strong>ionic cordova platform add ios<strong>
⚠️⚠️  LE dossier PLUGINS s'ajoutera AUTOMATIQUEMENT dans votre Projet IONIC

### 4)
Ajoutez manuellement <strong>ionic-3-4-downloader-manager-master<strong>  dans votre dossier <strong> PLUGINS <strong> de votre projet IONIC.
   
### 5)
Puis faites <strong>ionic cordova platform add android<strong> à nouveau !
   
### 6) 
COPIER COLLER LE CODE EN DESSOUS QUI DEMONTRE COMMENT UTILISER LE PLUGIN
    
🔥🔥🔥🔥 FORCE A VOUS !!!


⚠️⚠️⚠️⚠️ (si vous avez un problème de ionic-app-scripts taper la commande NPM INSTALL) 
⚠️⚠️⚠️⚠️ (if you have a ionic-app-scripts promblem run NPM INSTALL) 

### Usage Android

```js
var Downloader = window.plugins.Downloader;

var downloadSuccessCallback = function(result) {
       // result is an object
        {
            path: "file:///storage/sdcard0/documents/My Pdf.pdf", // Returns full file path
            file: "My Pdf.pdf", // Returns Filename
            folder: "documents" // Returns folder name
        }
       console.log(result.file); // My Pdf.pdf
};

var downloadErrorCallback = function(error) {
    // error: string
};

var options = {
    title: 'Downloading File', // Download Notification Title
    url: "http://www.website.com/file.pdf", // File Url
    path: "My Pdf.pdf", // The File Name with extension
    description: 'The pdf file is downloading', // Download description Notification String
    visible: true, // This download is visible and shows in the notifications while in progress and after completion.
    folder: "documents" // Folder to save the downloaded file, if not exist it will be created
}

Downloader.download(options, downloadSuccessCallback, downloadErrorCallback);
```
<img align="center" src="image/android.png" />

### Usage iOS

```js
var Downloader = window.plugins.Downloader;

var downloadSuccessCallback = function(folder) {
       // folder: string where the file has been downloaded
};

var downloadErrorCallback = function(error) {
    // error: string
};


var options = {
    url: "http://87.76.16.10/test10.zip", // File Url
    path: "test10.zip", // The File Name with extension
}

Downloader.download(options, downloadSuccessCallback, downloadErrorCallback);
```
<img align="center" src="image/ios.png" />

### Get download folder

The file will be downloaded within the device storage not SdCard.(Android)

WARNING: `will overwrite existing file if it already exists.`

License
--------

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
