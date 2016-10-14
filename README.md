### web2py Vue Scaffold App (compatible with Cordova)

This app provides an example of a scaffold app based on:

- web2py (for serverside logic, database abstraction, and auth)
- vue.js (for single page rsponsive app)
- whoosh (for full text search)
- stupid.css (for style)

It is based on https://github.com/web2py/scaffold but all the code is in static/index.html and static/js/custom.js

To use without cordova, this is a normal web2py app. Just install and open it.

To use with cordova, simply edit static/js/custom.js and make BASE point to the URL of your server, than mount static/ as cordova/www/ and process it with Cordova. Example:

```
cordova create myapp com.example.hello MyApp
cordova platform add browser
cordova platform add android
cordova platform add ios

cd myapp
rm -r www
ln -s /path/to/web2py/applications/myapp/static/ www/
        
cordova build browser
cordova build android
cordova build ios

cordova run browser
cordova run android
cordova run ios
```