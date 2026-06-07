# Planio Downloads

Public release assets for Planio Desktop.

This repository does not contain Planio source code. It only hosts public
downloadable assets through GitHub Releases.

## Current macOS Download

The latest macOS universal DMG should be available at:

```text
https://github.com/cvegu/planio-downloads/releases/latest/download/Planio-latest-universal.dmg
```

## Release Assets

Each macOS release should include:

- `Planio_0.1.0_universal.dmg`
- `Planio-latest-universal.dmg`

The versioned file is kept for traceability. The `latest` file is used by
`planio.tech/download`.

## Publishing A New macOS Release

From `planio-desktop-macos`:

```bash
npm run build:local
npm run verify:mac:universal
```

Expected output:

```text
Architectures: x86_64 arm64
LSMinimumSystemVersion: 12.0
```

Copy the generated DMG and upload it to this repository's GitHub Release as
both:

```text
Planio_X.Y.Z_universal.dmg
Planio-latest-universal.dmg
```

For the current `0.1.0` release:

```text
Planio_0.1.0_universal.dmg
Planio-latest-universal.dmg
```

## Important

Do not commit DMG files to git. Upload them only as GitHub Release assets.

The `planio-web` project should use:

```text
NEXT_PUBLIC_MAC_DOWNLOAD_URL=https://github.com/cvegu/planio-downloads/releases/latest/download/Planio-latest-universal.dmg
```
