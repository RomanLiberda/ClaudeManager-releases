# ClaudeManager — releases

Distribution artifacts for ClaudeManager, a macOS menu bar app for keeping
several Claude accounts signed in and watching their usage.

This repository holds no source code. It exists so the app can check for
updates: Sparkle reads `appcast.xml` from here, and each version's signed,
notarised build is attached to the corresponding release.

Every build is signed with a Developer ID certificate, notarised by Apple, and
the appcast entry carries an EdDSA signature — the app refuses an update that is
not signed with the matching private key, wherever it was downloaded from.

## Install

Download the latest `.zip` from [Releases](../../releases), unzip it, and move
`ClaudeManager.app` to `/Applications`. It updates itself from then on.
