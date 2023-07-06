# ArcOS Policy
In this document follows a list of policies which ArcOS developers are required to follow in order to prevent issues, conflicts or otherwise.

## In context of:
| Context | Explanation |
|---------|-------------|
| The Board | the leaders and owner of the project |
| The Backend Development Team (BDT) | those assigned to work on ArcAPI |
| The Frontend Development Team (FDT) | those assigned to work on the ArcOS Runtime Frontend itself |
| The Landing Development Team (LDT) | those assigned to work on the ArcOS Landing page and anything related to it |
| External Beta Testers (EBT) | people assigned to beta test ArcOS before a release |
| The General Running Development Board (GRDB) | The ArcOS Project Board on GitHub |
| The Design Team (DT) | Users responsible for auditing designs and verifying wallpapers before addition to the codebase. |
| Quality Control (QC) | team members responsible for checking a release candidate (a build compiled right before release) to eliminate any bugs and imperfections |

## Team Assignments
| Team | Members |
|------|---------|
| The Board | Izaak |
| BDT | Space, Izaak |
| FDT | Space, Izaak |
| LDT | Izaak, Siege |
| DT | Izaak, Siege |
| QC | Siege, Izaak |


The Policy
- Applications which are created by external parties that are intended to be built-in to the final frontend are required to be delivered to the frontend repository through a pull request so that it can be checked and later merged into the _master_ branch.
- Major changes to the ArcOS general user interface must be coordinated with the Board before the changes can have their development started. If the Board denies the UI change then the development cycle of said change is prohibited from starting or must be seized as quickly as possible. Do not waste time on features that won’t make it to production.
- If you discover a major bug during development that requires immediate attention, create an issue on the Frontend or Backend and notify the responsible teams
- Changes to states are **strictly prohibited**. You may not change the states in any way without coordination with the Board. Changes to states will only be performed by the Board, with an issue made on the GitHub indicating exactly what will change, and how the change may or may not affect your specific development cycle.
- The purging of applications can be performed by searching the project for any references of its ID, assets or other files, after which it can be removed from the import and deleted from the filesystem. Do keep in mind that only deprecated applications may be deleted. Do not delete any core applications such as the File Manager without prior coordination with the Board.
- Changes to the userdata on the frontend side may not be done without communication towards the Backend Team so that any required ArcAPI Database modifications can be made. This is to ensure that new ArcAPI users won’t have missing user properties in their initial userdata.
- The implementation of new desktop features in the _Shell_, _Wallpaper_ or _Desktop Icons_ are considered **core features**. These features must be known to the rest of the team before proceeding with the development cycle. Do not start development before given a Go from the Board.
- Homemade wallpapers from third-party individuals must be listed in the **Credits** section of the **Izk-ArcOS/ArcOS-Frontend** repository. Run new wallpapers by DT before adding it.
- Got an idea for a new theme? Go into a **deployed** ArcOS instance, apply the **ArcOS Dark** theme. Change the settings how you want the theme to be. Custom wallpapers are allowed. Be sure to test the theme with both light- and dark mode before proceeding. Go to the **Appearance** page in **Settings** and save the theme with a suitable name. Right-click the newly created theme and click “**Save to ArcFS.**” **File Manager** will open. Click the “open-with” icon on the selected file and select the **Text Editor**. Copy the file contents and send it to the Design Team for verification. Deploy it in the default theme store if you receive permission to do so from DT.
- Once third-party wallpapers become an official part of ArcOS they can be used throughout the entirety of the project, they aren’t constrained to the ArcOS Desktop.
- **_DO NOT SHARE DEVELOPMENT API’S WITH EXTERNALS._** API’s registered for the developers **cannot** be shared with external parties. They are strictly confidential and may contain data that could impact the development cycle if leaked.
- Beware of wallpaper IDs. Changes to an _**img**_ ID can change the background that the user has applied to their account. Do not alter the ID of already existing images, only add new ones when permitted.
- Release publishes can only be performed by the Board. Version changes will be performed by an admin, final error checks performed by QC, and then the release notes written and the executable released.
- **The desktop app runtime is locked.** Any changes that have to be made to the ArcOS Desktop App Runtime (either Electron or Tauri) have to be made by the Board or any other directly permitted developer. This is to ensure that the desktop app keeps operating smoothly as the updates roll out.
- Keep ArcOS information to yourself. You are an ArcOS developer. Features that have not yet made it to the codebase should not be shared with the public until they have made their first written commit on their respective GitHub repositories.
- Keep new designs original. _We need to differ from Windows, macOS and Linux in order to make ArcOS stand out from the rest._ Designs you create have to differentiate from those three major operating systems.
- Draft any new ideas on the GRDB. Got a new idea? Put it in the Queue on the GRDB so that the other developers and the general public can see what is going on. If it’s a major feature that will change ArcOS in any large way, do not publish it to the GRDB and tell the Board about the idea so they can write it down somewhere separated from the general public.
