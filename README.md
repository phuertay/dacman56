# dacman56 ZMK Module

This repository contains the shield files for a Dactyl Manufold 5×6 to allow users to build firmware. This can be done by adding the module to the west.yml found in your zmk-config's config directory. There is a full guide available for this here: [ZMK Modules Doc](https://zmk.dev/docs/features/modules)

## Usage

Edit your west.yml file found in your zmk-config's config directory to add the dacman56 module. Example:

```
manifest:
  remotes:
    - name: ph
      url-base: https://github.com/phuertay
  projects:
    - name: zmk
      remote: ph
      revision: main
      import: app/west.yml
    - name: zmk-keyboard-dacman56
      remote: ph
      revision: main
  self:
    path: config
```
Once you have the module added to your west.yml you can then build firmware as if it was in your config's shield directory or in ZMK main.
