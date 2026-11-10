# Changelog

All notable changes to this project will be documented in this file. See [commit-and-tag-version](https://github.com/absolute-version/commit-and-tag-version) for commit guidelines.

## [2.0.0](https://github.com/tonylea/ansible-role-raspberry-pi-baseline/compare/v1.0.1...v2.0.0) (2026-11-10)

### ⚠ BREAKING CHANGES

* raspberry_pi_baseline_journal_max_size is removed.

### Features

* stop capping the journal's size ([e5d1ae9](https://github.com/tonylea/ansible-role-raspberry-pi-baseline/commit/e5d1ae908af552e801fd1496aaa4fe42cefbf849))

### Documentation

* add a contributing guide ([4ab81d0](https://github.com/tonylea/ansible-role-raspberry-pi-baseline/commit/4ab81d05d5e134605bed9fce246de0d8bd238b28))
* put each sentence of the README on its own line ([02a6c4b](https://github.com/tonylea/ansible-role-raspberry-pi-baseline/commit/02a6c4bc7b363bd4f060f82bed204095db3dce4c))

## [1.0.1](https://github.com/tonylea/ansible-role-raspberry-pi-baseline/compare/v1.0.0...v1.0.1) (2026-11-08)

### Bug Fixes

* stage an EEPROM update once, not again on every run before reboot ([ce41eb3](https://github.com/tonylea/ansible-role-raspberry-pi-baseline/commit/ce41eb3cb4df7f03c8769d867f0450746f2922e5))

## 1.0.0 (2026-11-08)

### Features

* set up Raspberry Pi OS for wired, swap-free nodes ([dea4d50](https://github.com/tonylea/ansible-role-raspberry-pi-baseline/commit/dea4d50d652c32af717baaf063750e246b469980))

### Bug Fixes

* keep the journal on disk instead of only in RAM ([f26ec08](https://github.com/tonylea/ansible-role-raspberry-pi-baseline/commit/f26ec08722fd6e3884629bf0e788157b6088fd1d))
* move the journal onto disk straight away, not at the next boot ([54d0e2b](https://github.com/tonylea/ansible-role-raspberry-pi-baseline/commit/54d0e2b995110f69693234d8e2978341e6becb4c))

### Documentation

* describe what the role sets up and how it is tested ([05c12e7](https://github.com/tonylea/ansible-role-raspberry-pi-baseline/commit/05c12e780152bf16859e2d8b52592a38101b4f55))
