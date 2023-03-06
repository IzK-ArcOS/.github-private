# Well hello there

> **Note**: Considering the fact that you are a part of the ArcOS organization, I must point you towards our discord server where most common discussions take place: [ArcOS Discord](https://discord.gg/ARjRM6uNqf)

You're currently reading the ArcOS Private Readme for members of the organization. As a reminder, ArcOS is a project in which we aim to create an Operating System Environment (OSE) in your browser. This readme is for those who work on ArcOS.

Oh, by the way, **Thank you** for developing ArcOS. All help we can get is greatly appreciated.

## ArcOS... In Electron?

ArcOS currently runs in your browser. You go to a runtime URL in your browser and you're there. No need to install anything or run any commands, it's as easy as that. Though, as fun as that may seem, this won't suffice forever. My vision for ArcOS back in February of 2021 was to make it a fullscreen immersive experience by using the Electron framework. That is how it was for over a year before I abandoned that idea in favour of maintainability and code clarity.

I still stand by the fact that this "immersive" concept is a fun idea that must be educated at some point.

To do this, we'll be bundling the ArcOS backend and ArcOS frontend into one Electron application just like I did in my `SchoolSystem-*` project. There we ran the API on the NodeJS runtime and just displayed the frontend in the Electron runtime. In that project the frontend was set to always connect to `localhost:2804`, which is where the `SchoolSystem-API-v1` was pointed to in the NodeJS runtime.

With ArcOS I want to take a similar approach. Have a backend running on the NodeJS instance and then connect the frontend to the backend automatically. Though, I don't want to create a seperate repository for it. With SchoolSystem I had a frontend for the desktop app and a frontend for the web version. With ArcOS, I want to be able to toggle the web version to the desktop version on command, without the need for creating another sub-project within this organization.

I'm thinking of using the `navigator.userAgent` variable to allow the frontend to detect if it's running in the electron app or not. For instance, we can add a string to the userAgent which can then be detected by the frontend:

```ts
// Set the user agent
navigator.userAgent += "arcos-electron";

// Detect the electron app
function isElectron() {
  return navigator.userAgent.includes("arcos-electron");
}

function amazingFunction() {
  if (isElectron()) return false;

  // Do something
}
```

## ...Why?

Because. Just, because.
