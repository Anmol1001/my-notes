**To conditionally render component it better to use " ? : " condition rather that &&**


**What units are used for styling dimensions in React Native?**
	Display points, which vary by device pixel density

**What is the purpose of StyleSheet.create() in React Native?**
	To validate style types and ensure styles are correct
**What is a recommended approach for using icons in mobile UIs?**
	Use icon buttons instead of text, which makes mobile apps feel nicer and allows less text on the screen. Expo icons library is a convenient way to quickly add icons to an app.
**What potential performance issue exists when using SVGs in React Native?**
	SVGs can be performance-intensive, especially on Android. If an app uses many SVGs, it might slow down significantly. Small PNGs are often preferred for rendering icons in React Native.
**Why use `npx expo install` instead of standard package managers like npm or yarn?**
	npx expo install ensures SDK compatibility, checking that the library being installed works with the current Expo SDK version. This helps prevent version conflicts with native modules.
**What determines which package manager (yarn, npm, pnpm) is used during installation?**
	The lock file in the project determines the package manager. If a yarn.lock file exists, yarn will be used; if package-lock.json exists, npm will be used; if pnpm-lock.yaml exists, pnpm will be used.
