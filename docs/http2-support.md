---
id: http2-support
title: HTTP/2 Support in LambdaTest Tunnel
hide_title: false
sidebar_label: HTTP/2 Support
description: Learn how LambdaTest Tunnel supports HTTP/2 for modern, high-performance web application testing.
keywords:
  - http2
  - lambdatest tunnel
  - performance testing
  - web protocol
  - automatic proxy
image: /assets/images/og-images/Sharing-Lambda-Tunnel.jpg
url: https://www.lambdatest.com/support/docs/http2-support/
site_name: LambdaTest
slug: http2-support/
---

# HTTP/2 Support in LambdaTest Tunnel

## Overview

LambdaTest Tunnel provides out-of-the-box support for HTTP/2, enabling users to test their web applications using the latest web protocol without any additional configuration. HTTP/2 support is essential for performance testing, as it includes improvements such as multiplexing, server push, and header compression. This document provides an overview of HTTP/2 support within LambdaTest Tunnel and its benefits.

## Key Features

- **Automatic HTTP/2 Proxying:** LambdaTest Tunnel automatically proxies both HTTP/1 and HTTP/2 traffic, simplifying the testing process for applications that use the latest web protocols.
- **Improved Performance Testing:** With HTTP/2 support, users can test their applications' performance characteristics, such as load times and response behavior, under conditions that mirror modern browser-server communication.
- **Seamless Integration:** No additional flags or configurations are required to enable HTTP/2 support, ensuring a smooth integration into existing testing workflows.

## Usage

Using HTTP/2 with LambdaTest Tunnel does not require any special configuration or flags. The tunnel automatically detects and proxies HTTP/2 traffic alongside HTTP/1, ensuring that your tests accurately reflect the behavior of web applications under real-world conditions.

To start using LambdaTest Tunnel with HTTP/2 support, simply initiate the tunnel as you normally would:

```sh
./LambdaTestTunnel --user YourLambdaTestUsername --key YourLambdaTestAccessKey
```

With the tunnel running, any HTTP/2 traffic between your local development environment and the LambdaTest cloud platform will be automatically proxied, allowing you to conduct thorough performance and functionality testing on your web applications.

## Conclusion

The inherent support for HTTP/2 in LambdaTest Tunnel is a testament to LambdaTest's commitment to providing developers and QA professionals with cutting-edge tools for web application testing. By automating the proxying of HTTP/2 traffic, LambdaTest Tunnel ensures that users can effortlessly test their applications in environments that utilize the latest web protocols, leading to faster, more reliable web applications.

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
        HTTP/2 Protocol
      </span>
    </li>
  </ul>
</nav>