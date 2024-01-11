# Setup for Android development with VS Code

source: <https://stackoverflow.com/questions/76763954/android-app-development-with-visual-studio-code>

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
sdkmanager "platform-tools" "platforms;android-30" "build-tools;30.0.3"
```
