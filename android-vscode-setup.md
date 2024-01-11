# Setup for Android development with VS Code

## Install Java

```bash
sudo apt install default-jre
sudo apt install default-jdk
sudo apt install openjdk-21-jdk
```

## Install Android Studio command line tools

```bash
curl -LO https://dl.google.com/android/repository/commandlinetools-linux-11076708_latest.zip
mkdir -p ~/Android/cmdline-tools/latest
unzip commandlinetools-linux-*.zip -d ~/Android/cmdline-tools/latest
rm commandlinetools-linux-*.zip
```

## Configure environment variables

```bash
export ANDROID_HOME=$HOME/android
export PATH=$ANDROID_HOME/cmdline-tools/latest/bin:$PATH
export PATH=$ANDROID_HOME/emulator:$PATH
export PATH=$ANDROID_HOME/platform-tools:$PATH
export PATH=$ANDROID_HOME/tools:$PATH
```

## Install Android SDK

```bash
sdkmanager list # list available packages
sdkmanager "platform-tools" "platforms;android-28" "platforms;android-29" "platforms;android-30" "platforms;android-31" "platforms;android-32" "platforms;android-33" "platforms;android-34" "build-tools;34.0.0" "build-tools;33.0.2" "emulator" "sources;android-34" "sources;android-33" "system-images;android-34;google_apis;x86_64"
```

## Install SDKMAn

```bash
curl -s "https://get.sdkman.io" | bash
sdk version
```

Note: For creating Android projects, we still need to install Android Studio for project template.

[Source](https://stackoverflow.com/questions/76763954/android-app-development-with-visual-studio-code)

Stackoverflow notes: [Command-Line based Development Environments for Building and Debugging Android Applications](https://stackoverflow.com/a/76150499)
