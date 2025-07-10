# kneecap-browser-extension

**This is a Hard fork of OsaSoft's better-youtube-subscriptions extension that aims to integrate with the larger kneecap media project.**

While youtube-better-subscriptions focuses specifically on hiding unwanted videos from youtube, 
this fork aims to sync youtube subscriptions, watch history, and algorithm presentation to their own self hosted kneecap server.

See tummyslyunopened/kneecap-server for a larger explaination of the kneecap project. 

Additionally we will aim to integrate subscriptions from other platforms (which are separately synced to the kneecap server) 
including rss podcasts and audiobook chapters into the youtube web UI. 

## Alpha Roadmap

**Adopt additional UI Tweaks**
 - [ ] Adopt hide-youtube-thumbnails functionality

**Sync youtube account state with self hosted kneecap server**
 - [ ] Add option to dump content of watch history from extension-DB to kneecap-server-DB
 - [ ] Create extension-db for storing youtube subscriptions list
 - [ ] add option to scrape subscriptions list from subscription management page to extension-DB
 - [ ] add option to dump content of subscriptions list from extension-DB to kneecap-server-DB

**Sync kneecap feed state with the web extension**
 - [ ] add DB sync for kneecap-server feed database
       
**Create integrated kneecap subscriptions UI for youtube**
 - [ ] populate kneecap feed entries with titles, thumbnails, etc directly into the youtube subscriptions feed

**Security Review**
 - [ ] Verify integrity of CI / CD
   - [ ] Ensure all secrets and certificates are guarded
   - [ ] Perform Risk analyses and mitigations for each dependency inclusion
   - [ ] Enable signed commits and signatures on zip packages
   - [ ] enable strict alerts for review on changes to CI (including public disclosure)
   - [ ] Include self checks within the extension itself to alert user on evidence of tampering (soft DRM)
 - [ ] Extension behavior
   - [ ] Encrypt user data at rest including subscriptionlist, watch history, kneecap feed, kneecap-server communication details
   - [ ] Incrementally Decrypt data required for kneecap functionality. 
   - [ ] Ensure Encryption in transit between kneecap-server and kneecap-web-extension
   - [ ] Sanitize all input and output between kneecap-server and kneecap-web-extension

## Installation
There is no intention to get this extension approved in any webstore. 
Additionally no zip file will be packaged for release until all sub components of the larger kneecap project 
have met their alpha roadmap goals.

For an overview of the current alpha roadmap status of each component view [kneecap Alpha Roadmap]()

In the meantime, if you wish to try out the application in its current state please view the [kneecap Onboarding]().
This component extension can be loaded using the following instructions: [Installing Web Extensions From a Git Repository]().

## Contribution 
PRs are not welcome at this time, but I am taking lots of feedback on discord

## Excerpts From Youtube better subscriptions original README
This plugin aims to make navigating YouTube's subscription grid easier by allowing users to hide watched videos.

- Previously Available for Firefox: https://addons.mozilla.org/cs/firefox/addon/youtube-better-subscriptions/
- Previously Available for Chrome: https://chrome.google.com/webstore/detail/better-subscriptions-for/fkchdogohkjpnhfkganifkbbjcjofbjf

- The icon for the marked watched Button is based on: https://commons.wikimedia.org/wiki/File:OOjs_UI_icon_eye.svg published under the CC-BY-SA-3.0, the modified version is licensed under CC-BY-SA-4.0
- The icon for the settings Button is taken based on: https://commons.wikimedia.org/wiki/File:OOjs_UI_icon_settings.svg published under the MIT licence, , the modified version is licensed under MIT
- The addon as a whole is still licensed under the GPLv3
