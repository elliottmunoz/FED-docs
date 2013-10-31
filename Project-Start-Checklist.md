# Targets

* Collect window size data if possible. Code:

```
_gaq.push(['_trackEvent', 'Viewport', 'Size',               width + 'x' + height, 0, true]);
_gaq.push(['_trackEvent', 'Viewport', 'Width',              width + 'x' + height, width, true]);
_gaq.push(['_trackEvent', 'Viewport', 'Height',             width + 'x' + height, height, true]);
_gaq.push(['_trackEvent', 'Viewport', 'Aspect Ratio X 100', width + 'x' + height, Math.round((width / height) * 100), true]);
```

* Establish window size targets (suggested):
  * Average size
  * Near-min size
  * Near-max size
  * For fullscreen sites, carousels, etc:
    * Average aspect ratio
    * Near-min aspect ratio
    * Near-max aspect ratio
* Establish size targets:
  * Total page size without images
  * Total page size with images
* Establish speed targets:
  * Use a fixed internet speed - http://nshipster.com/network-link-conditioner/
    * US avg. is ~5mbps - http://en.wikipedia.org/wiki/Internet_in_the_United_States#Access_speed
    * Mobile is ~2.5mbps - http://www.telecompetitor.com/cisco-average-north-american-mobile-data-connection-is-2-6-mbps/
  * Speed targets to think about (targets may differ at different screen size):
    * DOMContentLoaded time
    * Complete initial load time
* Establish other targets:
  * Unused CSS thresholds
  * FPS while scrolling
  * ???

<hr>

# Project Management

Discuss with PMs:

* Custom statuses. 'Blocked', 'On Staging', 'Deployed'?
* Milestone definition. Suggestions:
  * Setup
  * Browser QA
  * Buildout
  * JS features
  * [CMS projects] Admin abilities
  * [CMS projects] Templates
  * QA fixes
  * Pre-launch
  * Post-launch
* QA process
* Browser testing and who's responsible for what
* Project updates:
  * Format of daily updates from FEDs
  * Format of weekly updates from PMs
    * Should include hours used v. remaining for FED

<hr>

# Standalone (no Rails, no CMS)

* Identify potential server-side issues
  * If there seem like a lot, float the idea of having a back-end dev on retainer

<hr>

# Rails

Discuss with devs:

* Convenience:
  * Is there a way to develop 'flat' pages in the app, using site assets?
  * Are there special restrictions or domain name issues that make the app difficult to test on a local vertial machine?
* View development:
  * Are devs developing views ahead of FEDs?
  * Are devs developing views ahead of final UX/design?
  * Discuss implications and preferences.
* Environments and branching:
  * Is it alright to move features into master for PMs to verify?
  * Can FEDs deploy to integration?
  * Can FEDs deploy to feature branches?
* Testing:
  * How will interactions be tested? (suggestion: data-test attributes)
  * Are FEDs responsible for testing all JS features?
* Sample data - can project devs:
  * create basic sample data for every new model/relationship they write?
  * set up a sample data structure that FEDs can easily edit?
