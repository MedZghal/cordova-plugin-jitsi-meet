# cordova-plugin-jitsi-meet
Cordova plugin for jitsi meet native sdk

---

## update note

permision helper added ( for android ) 

## how to use
```javascript
declare var jitsiplugin: any;

jitsiplugin.loadURL('https://meet.jit.si/xxxxxx', null, (data) => {
    if (data === 'CONFERENCE_WILL_LEAVE') {
        jitsiplugin.destroy((dataDestroy) => {
            // on Destroy
            console.log('On Destroy : ', dataDestroy);
        }, (err) => {
            // on Error
            console.log('On Error : ', err);
        });
    }
    }, (err) => {
        // on load url was not work
        console.log('On load url was not work : ', err);
    });
```

---

## how to build for ionic

```bash
ionic cordova plugin add https://github.com/sesangsokuro/cordova-plugin-jitsi-meet

ionic cordova plugin add cordova-plugin-compat

( for cordova permision helper )

ionic cordova build android
```
