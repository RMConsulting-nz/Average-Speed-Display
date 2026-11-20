# Average-Speed-Display

A simple app that tracks current and average speed. Intended for use when driving between average speed cameras.

It's a phone web app (iPhone and Android) that shows your **current speed** and your **average speed since you pressed Start**, in km/h. It's built for average speed camera sections, where the cameras work out your average speed between two points.

- Top third: current speed
- Bottom two-thirds: average speed, which turns **red** when it goes above your speed limit
- Settings: set the speed limit (default 100 km/h). It's remembered on your phone.
- Keeps the screen awake while running and works with patchy reception once it has loaded.

## Install it

Open the app link: **https://rmconsulting-nz.github.io/Average-Speed-Display/**

**iPhone**
1. Open the link in **Safari**.
2. Tap the **Share** button, then **Add to Home Screen**.
3. Open it from the new icon. The first time you press Start, allow location access.

If it says location access is off: Settings → Privacy & Security → Location Services → Safari Websites → *While Using the App*.

**Android**
1. Open the link in **Chrome**.
2. Tap the **⋮** menu, then **Add to Home screen** or **Install app**.
3. Open it from the new icon. The first time you press Start, allow location access.

If it says location access is off: in Chrome, tap the icon to the left of the address bar → Permissions → Location → *Allow*. Also check that Location is turned on in your phone's quick settings.

## How to use it

Press **Start** as you pass the first camera, and **Stop** after the second. The average is distance travelled ÷ time taken, which is how the cameras measure it. The average clock waits until the GPS has a steady signal (usually a few seconds), and the average shows a dash for its first 5 seconds while it settles. That stops a rough first GPS reading from showing a false high average, and GPS warm-up time can't make it look lower than it is. Pressing Start a few seconds before the first camera gives it time to settle.

Phone GPS is good, but it's not the camera's equipment. Treat the app as a guide and keep a margin under the limit.

**Safety:** a passenger should operate it, or put the phone in a dash mount and just glance at it. Don't handle the phone while driving.

## Files

Plain HTML, CSS and JavaScript. No build step.

- `index.html`: the whole app
- `manifest.webmanifest`, `icon-*.png`: home-screen app setup
- `sw.js`: offline caching

## Licence

MIT. See [LICENSE](LICENSE). You're welcome to use, change and share this app. If you build on it, a credit to **Rachel Mackay | On Purpose** would be appreciated.
