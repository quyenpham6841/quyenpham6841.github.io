**More information: [here](https://kodytechnolab.com/develop-and-launch-progressive-web-app)**
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

**Example:**

```json
{
    "name": "Lift Up",
    "short_name": "Lift Up",
    "start_url": "/index.html",
    "display": "standalone",
    "background_color": "#0175C2",
    "theme_color": "#0175C2",
    "description": "LiftUp cross-platform app",
    "orientation": "portrait-primary",
    "prefer_related_applications": false,
    "icons": [
        {
            "src": "icons/Icon-192.png",
            "sizes": "192x192",
            "type": "image/png"
        },
        {
            "src": "icons/Icon-512.png",
            "sizes": "512x512",
            "type": "image/png"
        }
    ]
}
```

Or generate automatically at:
[Web App Manifest Generator](https://app-manifest.firebaseapp.com/)

start_url should be your index.html file.

## Favicon & App Icon Generator (mobile device)
More information at: https://kodytechnolab.com/develop-and-launch-progressive-web-app

# Deploy PWA
**Note: It must be served over https**
## Deploy on github.io
Create a new repository named *username*.github.io, where *username* is your username (or organization name) on GitHub.
