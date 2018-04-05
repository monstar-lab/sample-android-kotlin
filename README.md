# Sample for Android (Kotlin)

[![CircleCI](https://circleci.com/gh/noboru-i/sample-android-kotlin.svg?style=svg)](https://circleci.com/gh/noboru-i/sample-android-kotlin)

This is the sample continuous integrated project for Android (Kotlin).

## What is this repository?

- **Lint**
  - **ktlint**
  - **detekt**
  - **Android Lint**
- **Build**: Configured build setting. e.g. `signingConfigs`, `buildTypes`
- **CircleCI**: Lint, Test, and Build in [CircleCI](https://circleci.com/).
- **PR Comment by Danger**: [Danger](http://danger.systems/ruby/) configuration is included. Lint error comes as PR comment.


## How to setup

1. Setup CircleCI build.
    - Turn "On" "Only build pull requests".
2. Copy or refer to below files. [diff](https://github.com/noboru-i/sample-android-kotlin/compare/6e14739b8d26c11b66d3e0c11478fbe84b479ebc...master)
    - `.circleci/config.yml`
    - `Dangerfile`
    - `Gemfile`
    - `Gemfile.lock` : If you want newer version, please exec `bundle update`.
    - `build.gradle`
    - `detekt.yml` : Please create default config by `./gradlew detektGenerateConfig`
    - `app/build.gradle`
    - `app/keystores/debug.keystore` : Please get from local.
    - `app/keystores/release.jks` : Please get or create.
2. Set environment variable.
    - `DANGER_GITHUB_API_TOKEN` : token for check bot
    - `ANDROID_KEYSTORE_PASSWORD` : password for release keystore
    - `ANDROID_KEYSTORE_ALIAS` : alias for release keystore
    - `ANDROID_KEYSTORE_PRIVATE_KEY_PASSWORD` : alias's password for release keystore

## Customize

This repository is targeting for very simple project.

But in real world, we need to work for complex project.

We have some advice for customizing configuration in [Wiki](https://github.com/noboru-i/sample-android-kotlin/wiki).
Please refer to it.