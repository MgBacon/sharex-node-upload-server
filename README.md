# What is this?

This is a sample node.js image upload server that takes uploads from [ShareX](https://getsharex.com/) or the `index.html` and is intended for single user use. To run this server you need node v8 or higher. 

# Technical

## Setup

* clone this repository
* `cd` into this repo
* run `npm install` to install all dependencies (check their respective npm repos for the latest version number or run `npm audit` and `npm audit fix` afterwards on your own discretion)
* create a file called `config.json` in the root directory and copy paste and modify the following structure:
```
{
  //port of your server
  //can be ommited by setting it manually in server.js#L46
  "port": "exampleport", 
  "api_key": "anapikey"   //your custom api_key
}
```
* run the server via `node server.js` or your preferred way (e.g. pm2)

ShareX config sample:  
``` 
{
  "Name": "Own Uploader", // put your own name here
  //this sets the profile for all types of files, remove categories you want to path differently
  "DestinationType": "ImageUploader, TextUploader, FileUploader", 
  "RequestURL": "yoururlwithbackslash.com/upload",
  "FileFormName": "sampleFile",     //this cannot be changed
  "Headers": {
    "api_key": "anapikey"   //your api_key specified in the config above
  }
}
```

