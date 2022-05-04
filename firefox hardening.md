## Firefox Hardening
---

**settings**
- General > Browsing:
Uncheck `Recommend extensions as you browse` & `Recommend features as you browse`
- Home:
`Uncheck all`
- Search > Default Search Engine:
`DuckDuckGo`
- Privacy & Security > Enchance Tracking Protection
`Strict`
- Send "Do not track"
`Always`
- Logins and Passwords:
`Uncheck all`
- Firefox Data Collection and Use:
`Uncheck all`
- Enable `HTTPS-Only` Mode in all windows
---

**about:config**

- Set to 1:
```txt
browser.uidensity
```
- Set to true:
```txt
layers.acceleration.force-enabled	
```
```txt
gfx.webrender.all
```
- Set to 127:
```txt
gfx.font_rendering.fontconfig.max_generic_substitutions
```
- Set to 96:
```txt
layout.css.dpi
```

- Set all to false:
```txt
browser.newtabpage.activity-stream.feeds.telemetry
```
```txt
browser.ping-centre.telemetry
```
```txt
browser.tabs.crashReporting.sendReport
```
```txt
toolkit.telemetry.unified
```
- Remove link
```txt
toolkit.telemetry.server
```
----

**extensions**

- Ublock origin (Settings > Filter lists > Check `AdGuard URL Tracking Protection`)

- Bitwarden

- Metamask 

- Phantom 
