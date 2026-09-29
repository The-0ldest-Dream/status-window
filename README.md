# Status Window

Status Window is a personal, browser-based system for tracking progress,
managing quests, and viewing personal statistics. It is designed to run
as a website and can also be installed as an app in supported browsers.

## Features

-   Track personal progress and statistics.
-   Manage quests and custom lists.
-   View progress and activity visualizations.
-   Save system data in the browser.
-   Use the interface in supported desktop and mobile browsers.
-   Install the website as an app when browser and hosting requirements
    are met.
-   Optional offline support through a service worker.

> The exact features and interface may change as Status Window develops.
> This README describes the project generally and is intended to remain
> useful across future versions.

## Getting Started

### Run locally

1.  Keep the main HTML file and the service worker file in the same
    project folder.
2.  The main HTML file should be named `index.html` when using GitHub
    Pages.
3.  The service worker should be named `sw.js` if the HTML registers
    that filename.
4.  Open the folder using a local web server, such as the Live Server
    extension in Visual Studio Code.
5.  Open the local server URL in your browser.

Opening the HTML file directly using a `file://` address may prevent
some browser features, including service-worker functionality, from
working.

## Publish with GitHub Pages

1.  Create a repository on GitHub.
2.  Upload the project files to the repository's root folder.
3.  Ensure the main page is named `index.html`.
4.  In the repository, open **Settings → Pages**.
5.  Under **Build and deployment**, choose **Deploy from a branch**.
6.  Select the `main` branch and the `/ (root)` folder, then save.
7.  After deployment completes, open the published URL shown in the
    Pages settings.

GitHub Pages provides HTTPS, which is needed for service workers and
browser installation features on a public website.

## Install as an App

When hosted on HTTPS (or run locally through `localhost`), supported
browsers may offer an option to install Status Window as an app.

-   **Chrome:** Check the address bar or browser menu for an install
    option.
-   **Microsoft Edge:** Check **Apps** in the browser menu for an
    install option.

The browser controls whether and when the installation option appears.
It cannot be forced to display in every browser or situation.

## Offline Support

The optional service worker can cache same-origin requests so that
previously loaded resources may remain available when the network is
unavailable.

Offline behavior depends on which resources have already been cached and
on the browser's storage policies. Test offline use after publishing or
making significant changes.

## Updating Status Window

To publish a newer version:

1.  Update the project files.
2.  Keep required filenames and file locations consistent with the
    references in the HTML.
3.  Upload or replace the changed files in the GitHub repository.
4.  Commit the changes and allow GitHub Pages to redeploy.
5.  Refresh the website. If an older copy is still shown, close and
    reopen the app or clear the site's cached data in the browser.

This README is intended to be version-independent. It does not need to
be edited for ordinary feature updates or new system versions. Update it
only if the project's name, basic purpose, setup process, hosting
method, or other long-term instructions change.

## Data and Privacy

Status Window may store user-entered information in the browser.
Browser-stored data is generally specific to that browser and device,
and may be lost if site data is cleared or the browser is reset. Unless
a separate synchronization or backup feature is implemented, do not
assume that data automatically transfers between devices.

Use a device and browser you trust, and avoid entering sensitive
information.

## Project Files

A simple deployment may include:

-   `index.html` --- the main Status Window application.
-   `sw.js` --- the optional service worker used for offline caching.

Additional assets or files may be required as the project evolves. Keep
any referenced files in the locations expected by the application.

## License

No license is specified for this project. All rights remain with the
respective owner unless a license is added.
