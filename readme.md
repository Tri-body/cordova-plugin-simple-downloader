## cordova-plugin-simple-downloader

a cordova plugin to simple download file, return file md5, only for android platfrom.

### Install/UnInstall

install from github repository using this command

```sh
cordova plugin add https://github.com/Tri-body/cordova-plugin-simple-downloader
```

or install from npmjs package using this command

```
cordova plugin add cordova-plugin-simple-downloader
```

uninstall using this command

```sh
cordova plugin remove cordova-plugin-simple-downloader
```

### How to Use

```js
SimpleDownloader.download(
  'http://127.0.0.1:8080/xxx.mp4',
  '/storage/emulated/0/Android/data/<appid>/files/', // can't use file:///storage...
  'yyy.mp4',
  (md5) => {
    console.log('ok', md5);
  },
  e => {
    console.error('error: ', e);
  },
  true // if true, success callback return file md5, default false.
);
```
