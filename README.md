# CCStopper <!-- omit in toc --> 
Stops Adobe's pesky background apps and more 😉

## Table of Contents <!-- omit in toc -->
- [Install/Run](#installrun)
- [v1.2.3-pre.2 Changelog](#v123-pre2-changelog)
- [Features](#features)
- [FAQ](#faq)
- [Issues](#issues)
- [Contributing](#contributing)
  - [Alternate Distributions/Modifications](#alternate-distributionsmodifications)
  - [Adding Entries to Hosts Blocklist](#adding-entries-to-hosts-blocklist)
- [Disclaimer/Notice](#disclaimernotice)


## Install/Run
### One Line - v1.2.3+ Only <!-- omit in toc -->
> ⚠️ By using the commands below, you're running remote code that can be compromised/broken anytime. Everything is open-source, but it's still more risky than a manual installation. Proceed with caution. ⚠️

#### Powershell Commands <!-- omit in toc -->

| Powershell Command | Description | Run as admin? |
|-------------|-------------|:-------------:|
| `irm https://ccstopper.netlify.app/run \| iex`      |  Runs CCStopper once.      | No |
| `irm https://ccstopper.netlify.app/shortcut \| iex`      |  Creates desktop shortcut that runs the command above.  | Yes |
| `irm https://ccstopper.netlify.app/install \| iex`      |  Installs CCStopper and creates a desktop shortcut. Works offline, however it won't automatically update. To uninstall/reinstall, run this command again.     | Yes |


### Manual Install <!-- omit in toc -->
1. Get the latest [release](https://github.com/eaaasun/CCStopper/releases/latest)
2. Extract the ZIP file (This is important, CCStopper may not work without additional files.)
3. Run CCStopper.bat
4. Select an option
5. Prevent profit (for Adobe)

## v1.2.3-pre.2 Changelog
- One-line install/run 
  - thanks [MAS](https://github.com/massgravel/Microsoft-Activation-Scripts) for the idea
  - see [below](#one-line-installrun) for commands
- The hosts file module write/remove addresses in a different way
  - it *should* migrate old entries, but it hasn't been extensively tested
- New module for patching the creative cloud app 
  - credit to AbsentForeskin on the genP discord
  - requires restart after patching
- Created logo for shortcut icons (its very original trust)

###### Read previous changelogs from [the releases](https://github.com/eaaasun/CCStopper/releases) <!-- omit in toc -->

## Features
> Please do not list options by number (i.e. "select option 1, then run option 3") if you are creating a guide or asking a question that uses CCStopper. To reduce confusion, use the names of the options. Thank you.

> All patches are reversible by running the same patch again.

- Stop running Adobe background processes
- Internet Patches
  - Firewall Block - Creates firewall rule to block the credit card prompt. See [issue #42](https://github.com/eaaasun/CCStopper/issues/42) if it does not work.
  - Add to Hosts - Blocks unnecessary Adobe servers in the hosts file.
- System Patches
  - Creative Cloud App - Replaces the 'start trial' button in the Creative Cloud app.
  - Genuine Checker - Locks Genuine Checker files.
  - Hide CCFolder - Hides the Creative Cloud folder in Windows Explorer.

## FAQ
<details>
<summary>Why administrator permissions?</summary>

> This script needs those permissions to modify files and settings. CCStopper is fully open source for auditing.</details>

<details>
<summary>Is this a virus?</summary>

> Virus detections are false positives. CCStopper is fully open source for auditing.
</details>

<details>
<summary>I found a bug/issue! What do I do?</summary>

> Before submitting an issue, update to the latest version and check [the issues page](https://github.com/eaaasun/CCStopper/issues) to see if your issue is there. Please read through the issue form before submitting so the bug can be patched ASAP.
</details>

<details>
<summary>Is this available for MacOS?</summary>

> It is not available for MacOS, and I won't port it to MacOS as long as I use Windows. 
</details>

<details>
<summary>Will more features be added?</summary>

> Yes! If I am actively working on features, they will be listed in the [dev branch](https://github.com/eaaasun/ccstopper/tree/dev). Open an issue [here](https://github.com/eaaasun/CCStopper/discussions/new?category=feature-request) to suggest a feature.
</details>

<details>
<summary>Is there any way to support the project?</summary>

> Please donate your time! If you have Powershell/Batch knowledge, contribute to the project! If not, finding bugs and suggesting features is just as helpful!
</details>

## Issues
Found a bug? Something not working? Please open an issue! Please read through the issue form, and check for existing/closed issues before submitting.

## Contributing
> Want to support this project? Please donate your time! If you have Powershell/Batch knowledge, contribute to the project! If not, finding bugs and suggesting features is just as helpful!
### Alternate Distributions/Modifications
> I cannot offer any support for CCStopper unless it's a release from this repository.

I have no problems with this and enjoy seeing what people do with my code! Please make sure that your fork complies with this repository's license, and that the user knows it's a fork of CCStopper. Also, if you make any improvements, please consider making a pull request!

### Adding Entries to Hosts Blocklist
The `data` branch of CCStopper contains a `hosts.txt` file that has a list of addresses that CCStopper will block. If you think an address from adobe should be blocked, open a pull request with the address added to the bottom of the list. Also state why the address should be added to the hosts block.

## Disclaimer/Notice

**Disclaimer:** This script is in an early stage, and offered as-is. There will be *many* bugs. I am not responsible for any damage, loss of data, or thermonuclear wars caused by these scripts. I am not affiliated with Adobe.

**Notice:** Don't use this tool for piracy. It's illegal, and multi-billion dollar companies like Adobe _need_ to profit off unreliable and overpriced software. Piracy _helps_ Adobe by increasing their market dominance.

<h6 align="center">Made with &lt;3, and &lt;/3 for Adobe</h6>
