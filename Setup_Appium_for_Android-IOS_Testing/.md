# Appium Setup and Mobile Automation Guide 🚀

This guide walks you through setting up mobile app automation using Appium. It covers installing software, writing scripts, and running tests on Android and iOS devices. If, at any point, you find that a required tool or package is missing, we provide installation steps. Follow this guide to begin automating your mobile applications!

---

## **Step 1: Installation of IntelliJ IDEA** 🛠️

Download and install **IntelliJ IDEA** from the official website.

- **Verify**: Open IntelliJ and confirm that the installation was successful.
- **Install**: If not installed, download it from [IntelliJ IDEA](https://www.jetbrains.com/idea/).

---

## **Step 2: Verify Java Installation** ☕

Ensure that **Java** is installed on your local machine.

- **Verify**: Run `java -version` in your terminal.
- **Install**: If not installed, download the **JDK** from [Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html). After installation, set the environment variables:
  - **JAVA_HOME**: Point this to your JDK directory.
  - Add this directory to your `PATH`.

- **Command**: To add in Windows, go to System Properties > Environment Variables. For macOS/Linux, add this to your `.bash_profile` or `.zshrc`.

---

## **Step 3: Verify Maven Installation** 🔧

Maven is needed for managing dependencies.

- **Verify**: Run `mvn -version`.
- **Install**: If Maven is not installed, follow these steps:
  - Download from [Maven Apache](https://maven.apache.org/download.cgi).
  - Extract it and set the `MAVEN_HOME` environment variable.
  - Add the Maven `bin` directory to your `PATH`.
  - Verify again by running `mvn -version`.

---

## **Step 4: Install Node.js** 📦

Node.js and npm (Node Package Manager) are required for Appium.

- **Verify**: Run `node -v` and `npm -v`.
- **Install**: If missing, download from [Node.js](https://nodejs.org/), install, and then verify again.
  - **Command**: For macOS/Linux, you can also use a package manager like `brew install node`.

---

## **Step 5: Install Appium** 📲

Appium is installed using npm.

- **Verify**: Run `appium -v` to check the version.
- **Install**: If Appium is not installed, run the following command:
  - `npm install -g appium`
  - Start the Appium server by typing `appium`.

---

## **Step 6: Install Android SDK** 🤖

The **Android SDK** is required for Android automation.

- **Verify**: Open **Android Studio** > SDK Manager > check if the required SDK platforms are installed.
- **Install**: If Android SDK is missing:
  - Download Android Studio from [here](https://developer.android.com/studio).
  - In Android Studio, go to **SDK Manager** and install the required Android platforms.
  - Set `ANDROID_HOME` as an environment variable in your system, pointing it to the SDK directory.
  - Add the SDK tools directory to your `PATH`.

---

## **Step 7: Installation of Vysor** 📱

Install **Vysor** to mirror your Android device's screen on your desktop.

- **Verify**: Ensure you can see your Android screen mirrored on your machine.
- **Install**: If not installed, download Vysor from [here](https://www.vysor.io/), and follow the setup instructions.

---

## **Step 8: Connect Android Phone** 🔗

To connect an Android device for testing, enable **Developer Options** and **USB Debugging** on the phone.

- **Verify**: Run `adb devices` to see if the phone is recognized.
- **Fix**: If the device isn't detected:
  - Ensure **USB Debugging** is enabled in **Developer Options**.
  - Install the required **ADB drivers** on your computer.

---

## **Step 9: Define Mobile Device Capabilities** 🔍

Appium needs specific **capabilities** for your mobile phone to interact with the device.

- **Verify**: Double-check the accuracy of your desired capabilities (e.g., `platformName`, `deviceName`, `app`).
- **Fix**: If any issue arises, ensure you have captured correct values using `adb shell` for Android or **Xcode** for iOS.

---

## **Step 10: Create a Java Project for Appium Tests** 💻

In **IntelliJ IDEA**, create a new Java project.

- **Verify**: Ensure Maven dependencies are added and resolve without issues.
- **Fix**: If Maven is not resolving dependencies, check your `pom.xml` file and ensure the Appium and Selenium dependencies are added correctly.

---

## **Step 11: Install Appium Drivers** 🛠️

Appium requires platform-specific drivers for Android and iOS.

- **Verify**: If tests are not running, ensure the drivers are installed correctly.
- **Install**: To install drivers manually:
  - **Android**: `appium --driver install uiautomator2`
  - **iOS**: `appium --driver install xcuitest`
  - **Verify**: Run `appium driver --list` to ensure they are installed.

---

## **Step 12: Review Appium Documentation** 📚

Review the official Appium documentation to better understand commands and setup for both Android and iOS automation.

- **Link**: [Appium Documentation](https://appium.io/docs/en/about-appium/intro/)

---

## **Step 13: Installation of Android SDK Platform Tools** 🔧

Make sure **Android SDK Platform Tools** are installed.

- **Verify**: Open Android Studio > SDK Manager, and check if "Platform Tools" are installed.
- **Install**: If not installed, open the SDK Manager and install the required platform tools.

---

## **Step 14: Add `ANDROID_HOME` to Environment Variables** 🌍

Set the `ANDROID_HOME` environment variable to point to your Android SDK directory.

- **Verify**: Run `echo $ANDROID_HOME` (Linux/macOS) or `echo %ANDROID_HOME%` (Windows).
- **Fix**: If not set, add it manually by:
  - **Windows**: System Properties > Environment Variables
  - **macOS/Linux**: Add `export ANDROID_HOME=path_to_sdk` in your shell profile (`.bashrc` or `.zshrc`).

---

## **Step 15: Launch Mobile App with Appium Scripts** 📜

Write and run your Appium scripts to launch mobile apps.

- **Verify**: Ensure that the desired capabilities are correct and the app launches without issues.
- **Fix**: If the app doesn't launch, check your device connection, capabilities, and Appium server logs for errors.

---

## **Step 16: Download and Install Appium Inspector** 🔍

**Appium Inspector** is used for inspecting elements in your mobile app.

- **Verify**: If Inspector is not opening, ensure the correct Appium server and session are configured.
- **Install**: If not installed, download Appium Inspector from [here](https://github.com/appium/appium-inspector).

---

## **Step 17: Locator Strategies and Selectors** 🎯

Appium supports different locator strategies like XPath, ID, Class Name, and Accessibility ID.

- **Verify**: If elements are not being found, try different locator strategies.
- **Fix**: Use **Appium Inspector** to double-check the selectors and try more efficient locator methods like **Accessibility ID**.

---

## **Step 18: Start Session with Appium Inspector** 🖥️

Start a session in **Appium Inspector** to inspect the app elements.

- **Verify**: Make sure Appium Inspector connects to the running Appium server and starts a session.
- **Fix**: If issues occur, check the Appium server logs for errors and ensure the correct desired capabilities are being used.

---

## **Step 19: Capture Selectors for Mobile Apps** 📱

Use **Appium Inspector** to capture element selectors (e.g., XPath, ID) for Android or iOS apps.

- **Verify**: Inspect elements and capture their locators to use them in your scripts.
- **Fix**: If you're unable to capture, verify the Appium Inspector session and ensure the app is running correctly on the connected device.

---

## **Step 20: Writing Appium Scripts** 📝

Write Appium scripts using captured selectors.

- **Verify**: Ensure that the scripts are correctly interacting with the app’s UI elements.
- **Fix**: If interactions fail, double-check the selectors and re-inspect the elements using Appium Inspector.

---

## **Step 21: iOS Setup for Testing** 🍏

Set up your environment to test iOS apps.

- **Verify**: Use **Xcode** to simulate or connect a real iOS device and ensure everything is working.
- **Install**: If Xcode or required tools are missing, download [Xcode](https://developer.apple.com/xcode/) and install.
  - **iOS Simulator**: Launch from Xcode to simulate a real iPhone.
  - **Install iOS Drivers**: Run `appium --driver install xcuitest` for iOS automation.

---

## **Step 22: Writing Appium Scripts for iOS** 🍎

Write Appium scripts for iOS apps using captured selectors like **Accessibility ID**, **XPath**, or **Class Name**.

- **Verify**: Test scripts on the iOS simulator or connected iOS device.
- **Fix**: If issues arise, check **Xcode logs**, Appium server logs, or use **Appium Inspector** to capture accurate selectors.

---

By following this guide, you'll be able to set up and automate tests for both Android and iOS apps using Appium. If any step is missing or doesn't work as expected, you have the respective installation steps to troubleshoot and fix the issue! 🚀
