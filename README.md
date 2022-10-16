# u0Launcher

Normally when you install unc0ver through TrollStore and try to jailbreak with it, it fails with a codesigning error because unc0ver expects amfid to be running in the background in order to patch it. However when unc0ver is installed through TrollStore, amfid doesn't get invoked in the unc0ver launch process because it launches through App Store fast path, which does not ask amfid for verification.

u0Launcher is an App that first sends an empty XPC message to amfid to make it start up and then jumps to unc0ver. This fixes the codesigning error.

## How to use

1. Install unc0ver through TrollStore

2. Install u0Launcher through TrollStore

3. When jailbreaking, launch u0Launcher instead of unc0ver, it will do the neccessary fix up and then jump to unc0ver and when you then press the jailbreak button, it will work.