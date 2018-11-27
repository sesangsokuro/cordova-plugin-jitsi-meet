# cordova-plugin-jitsi-meet
Cordova plugin for jitsi meet react native sdk

---

## update note

permision helper added ( for android ) / 2018-11-27

## how to use

var room_url = 'https://meet.jit.si/room_name';

```javascript
plugins.JitsiPlugin.loadURL(room_url, null, function(data) {
  if(data === "CONFERENCE_WILL_LEAVE"){
    plugins.JitsiPlugin.destroy( function(data) {
      // on Destroy
      console.log("Destroy");
    }, function (err) {
      // on Error
      console.log("Error");
    });
  }
}, function(err) {
  // on load url was not work
  console.log("Error : ", err);
});
```

---

## how to build for ionic

```bash
ionic plugin add https://github.com/sesangsokuro/cordova-plugin-jitsi-meet

ionic plugin add cordova-plugin-compat

( for cordova permision helper )

ionic build andorid
```
