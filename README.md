# What is this?

This is a sample node.js image upload server that takes uploads from [ShareX](https://getsharex.com/) and is intended to single user use. To run this server you need node v8 or higher. 

# Technical

## Installation

* clone this repository
* `cd` into this repo
* run `npm install` to install all dependencies
* create a `uploads` folder in the root directory
* start the server via `node server.js`
* create a file called `config.json` in the root directory and copy paste and modify the following structure:
```
{
  "port": "exampleport", //port your server will run on
  "url": "yoururlwithbackslash.com/", //your domain name where you want to upload to
  "api_key": "anapikey"   //your custom api_key
}
```
ShareX config sample:  
``` 
{
  "Name": "Own Uploader", // put your own name here
  "DestinationType": "ImageUploader, TextUploader, FileUploader", //this sets the profile for all types of files, remove categories you want to path differently
  "RequestURL": "yoururlwithbackslash.com/upload",
  "FileFormName": "sampleFile",     //this cannot be changed
  "Headers": {
    "api_key": "anapikey"   //your api_key specified in the config above
  }
}
```
## Future Features

* file size limit
* custom upload header for ShareX
* Viewing and organizing your uploaded files via web dashboard
* multiple users
