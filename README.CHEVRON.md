# fs-admin (Chevron)

**Required API (0.15):** `symlink`, `makeTree`, `recursiveCopy`,
`createWriteStream`, `unlink`.

- Darwin command install: `src/command-installer.js` (`symlink` / `makeTree`)
- Packaged install: `script/lib/install-application.js` (`recursiveCopy`)
- Privileged save: `text-buffer` `createWriteStream`

text-buffer declared `fs-admin@^0.19.0` (same JS API, N-API). Chevron pins
**0.15.0** everywhere so one Electron-rebuilt NAN addon is used.
Do not jump to 0.20+ without rebuilding both call sites.

Native: `build/Release/fs_admin.node`. No `prebuild-install`.
