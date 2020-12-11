# How to run the completed project

## Prerequisites

To run the completed project in this folder, you need the following:

- [Java SE Development Kit (JDK)](https://java.com/en/download/faq/develop.xml) and [Gradle](https://gradle.org/) installed on your development machine. If you do not have the JDK or Gradle, visit the previous links for download options. (**Note:** This tutorial was written with OpenJDK version 14.0.0.36 and Gradle 6.7.1. The steps in this guide may work with other versions, but that has not been tested.)
- A Microsoft work or school account.

If you don't have a Microsoft account, you can [sign up for the Office 365 Developer Program](https://developer.microsoft.com/office/dev-program) to get a free Office 365 subscription.

## Register a web application with the Azure Active Directory admin center

1. Open a browser and navigate to the [Azure Active Directory admin center](https://aad.portal.azure.com). Login using a **personal account** (aka: Microsoft Account) or **Work or School Account**.

1. Select **Azure Active Directory** in the left-hand navigation, then select **App registrations** under **Manage**.

    ![A screenshot of the App registrations ](/tutorial/images/aad-portal-app-registrations.png)

1. Select **New registration**. On the **Register an application** page, set the values as follows.

    - Set **Name** to `Java Graph Tutorial`.
    - Set **Supported account types** to **Accounts in any organizational directory**.
    - Leave **Redirect URI** empty.

    ![A screenshot of the Register an application page](/tutorial/images/aad-register-an-app.png)

1. Choose **Register**. On the **Java Graph Tutorial** page, copy the value of the **Application (client) ID** and save it, you will need it in the next step.

    ![A screenshot of the application ID of the new app registration](/tutorial/images/aad-application-id.png)

1. Select the **Add a Redirect URI** link. On the **Redirect URIs** page, locate the **Suggested Redirect URIs for public clients (mobile, desktop)** section. Select the `https://login.microsoftonline.com/common/oauth2/nativeclient` URI.

    ![A screenshot of the Redirect URIs page](/tutorial/images/aad-redirect-uris.png)

1. Locate the **Default client type** section and change the **Treat application as a public client** toggle to **Yes**, then choose **Save**.

    ![A screenshot of the Default client type section](/tutorial/images/aad-default-client-type.png)

## Configure the sample

1. Rename the `oAuth.properties.example` file to `oAuth.properties`.
1. Edit the `oAuth.properties` file and make the following changes.
    1. Replace `YOUR_APP_ID_HERE` with the **Application Id** you got from the App Registration Portal.

## Build and run the sample

In your command-line interface (CLI), navigate to the project directory and run the following commands.

```Shell
./gradlew --console plain run
```
