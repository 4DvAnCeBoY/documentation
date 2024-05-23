---
id: app-settings
title: App Settings in Real Device Cloud
hide_title: true
sidebar_label: App Settings
description: With LambdaTest, perform live interactive testing of mobile applications on Android emulators and iOS simulators and ensure your apps work seamlessly across multiple versions of Android emulators and iOS simulators.
keywords:
- app settings 
url: https://www.lambdatest.com/support/docs/app-settings/
site_name: LambdaTest
slug: app-settings/
---

<script type="application/ld+json"
      dangerouslySetInnerHTML={{ __html: JSON.stringify({
       "@context": "https://schema.org",
        "@type": "BreadcrumbList",
        "itemListElement": [{
          "@type": "ListItem",
          "position": 1,
          "name": "LambdaTest",
          "item": "https://www.lambdatest.com"
        },{
          "@type": "ListItem",
          "position": 2,
          "name": "Support",
          "item": "https://www.lambdatest.com/support/docs/"
        },{
          "@type": "ListItem",
          "position": 3,
          "name": "Native Mobile App Testing",
          "item": "https://www.lambdatest.com/support/docs/app-settings/"
        }]
      })
    }}
></script>

# App Settings

App settings play a crucial role in testing the environment for mobile applications. These settings, provided by LambdaTest, offer developers a range of capabilities to enhance testing procedures and ensure comprehensive validation of their apps functionality.

<img loading="lazy" src={require('../assets/images/mobile-app-testing/app-settings.webp').default} alt="Real "  className="doc_img" width="1366" height="629"/>

## Image Injection

Enable the Image Injection feature to capture images, QR codes, and barcode scans seamlessly within your app using LambdaTest devices. Our approach utilizes Sensor Instrumentation to seamlessly integrate your app with various mobile sensors, such as the camera. By enabling Image Injection for a specific session, LambdaTest seamlessly injects camera code modules into your app, effectively mocking or overriding the Android or iOS SDK used in your app.

Check out our detailed [support documentation](https://www.lambdatest.com/support/docs/camera-image-injection/) to learn in detail about the image injection feature.

## Biometric Authentication

Enable this setting to effortlessly test your biometric authentication-reliant applications on designated remote Lambdatest devices. This functionality enables the emulation of diverse biometric authentication techniques such as fingerprint scanning, facial recognition and others. Leveraging this feature ensures thorough validation of your applications' security and functionality across a spectrum of realistic usage scenarios.

Check out our detailed [support documentation](https://www.lambdatest.com/support/docs/biometric-authentication/) to learn in detail about the Biometric supported APIs and much more.

## Disable App Resigning (only iOS)

When users upload an iOS application to Lambdatest servers, Lambdatest will re-sign the app with a self-provisioning profile for installation on their devices during testing. This re-signing process may lead to the removal of entitlements from your iOS app. However, if the app is already signed using the Apple Developer Enterprise Program, users have this setting to opt out of this behavior. This enables you to thoroughly test functionalities like push notifications and universal links on Lambdatest devices without any hindrance.

## Disable Screenshot Unblock (only Android)

Enable this setting to conduct uninterrupted testing of your application's performance, even when screenshot capture is restricted within your app. This tool facilitates testing in both app-live and app automation scenarios, ensuring seamless evaluation of your applications.

Check out our detailed [support documentation](https://www.lambdatest.com/support/docs/disable-screenshot-block/) to learn in detail about the Network logs feature.

## Default Network Logs

Enable this feature to seamlessly initiate network log capturing at the beginning of each session within your application. By enabling this setting at the app level, you prioritize the logging of network activities over device logs, ensuring comprehensive monitoring of network interactions right from the start. 


<nav aria-label="breadcrumbs">
  <ul className="breadcrumbs">
    <li className="breadcrumbs__item">
      <a className="breadcrumbs__link" href="https://www.lambdatest.com">
        Home
      </a>
    </li>
    <li className="breadcrumbs__item">
      <a className="breadcrumbs__link" target="_self" href="https://www.lambdatest.com/support/docs/">
        Support
      </a>
    </li>
    <li className="breadcrumbs__item breadcrumbs__item--active">
      <span className="breadcrumbs__link">
        Real Device App Testing
      </span>
    </li>
  </ul>
</nav>