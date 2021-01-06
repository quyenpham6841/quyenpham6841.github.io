# Setup flutter for web
```bash
flutter channel beta

flutter upgrade

flutter config --enable-web
```
# Build project
```bash
flutter build web
```
It will create folder named “web” in the "build" directory

# PWA configuration
## Config manifest.json file
Open and edit manifest.json file in "/build/web" folder manualy.

Or generate automatically at:
[Web App Manifest Generator](https://app-manifest.firebaseapp.com/)

start_url should be your index.html file. *Example:*
```json
    "start_url": "/index.html",
```

## Favicon & App Icon Generator (mobile device)
More information at: https://kodytechnolab.com/develop-and-launch-progressive-web-app

# Deploy PWA
**Note: It must be served over https**
## Deploy on github.io
Create a new repository named *username*.github.io, where *username* is your username (or organization name) on GitHub.
