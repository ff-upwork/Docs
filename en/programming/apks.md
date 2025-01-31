
{
  "date" : "2022-02-06",
  "keywords": [ ".apks file", "extension", "format","APK Set Archive", "how to open .apks file","apks file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "APKS File - APK Set Archive",
  "description":"Learn about what is an APKS file?",
  "linktitle" : "APKS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2022-02-06"
}

## What is an APKS file?

A file with .apks extension is an archive file that is a collection of Android package **APK** files. Each individual APK file in the APKS file is generated keeping in view various aspects of the devices. These include architecture, language, screen density, and other device features. APKS files are generated by **bundletool**. It is used to build Android App Bundle and convert app bundle into difererent APKs for deployment on devices.

## APKS File Format - More Information

APKS files are saved as compressed files using [ZIP](/compression/zip/) file format.

## How to generate an APKS file?

When the Android App Bundle (AAB) is ready, its behaviour on Google Play store can be tested for deployment to a device. APKS files can be generated, for this purpose, from AAB files and installed on test devices using the Google's Android [bundletool](https://developer.android.com/tools/bundletool). It provides command line tools to create the APKS archive file from APKs using the following command.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
```

In order to deploy the APKs to a device, the APKS file can be signed with the device signing information as follow.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
--ks=/MyApp/keystore.jks
--ks-pass=file:/MyApp/keystore.pwd
--ks-key-alias=MyKeyAlias
--key-pass=file:/MyApp/key.pwd
```

## References

 * [bundletool - commandline](https://developer.android.com/tools/bundletool)
