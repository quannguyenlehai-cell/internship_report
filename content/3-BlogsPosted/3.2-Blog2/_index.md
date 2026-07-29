---
title: "Blog 2"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 3.2. </b> "
---
# WHAT I LEARNED AFTER EXPERIENCING AWS IOT CORE.

Recently, I had time to delve deeper into researching and applying AWS IOT Core to hardware and embedded systems projects. Since switching to AWS IOT Core, my mindset for building IoT systems has changed considerably. Below are some perspectives and lessons learned after the implementation process.

## MQTT protocol with low latency.

When using microcontrollers like ESP32, hardware resources and bandwidth are major obstacles. AWS IoT Core optimally supports MQTT for microcontrollers, enabling instant payload sending and actuator control (such as servos) without resource consumption.

## Strong Security with (X.509 Certificates and IAM Policy)
Each connected device has its own X.509 Cryptographic Certificate, Amazon Root CA, and Fine-granted IAM Policies to limit which devices are allowed to publish or subscribe to which topics.

## Serverless Synchronized Ecosystem
AWS IoT Core offers seamless connectivity with serverless services. With the IoT Rules Engine, data can be sent via AWS Lambda for backend logic processing without requiring a continuously running server. IoT Core can also integrate with AWS RDS to store user information and push it to AWS Amplify.

In short, AWS IoT Core is the bridge between hardware and cloud infrastructure. Although it took some time to configure the Certificate and IAM Policy, the system runs smoothly, reliably, and is ready to scale up.

https://docs.aws.amazon.com/iot/latest/developerguide/what-is-aws-iot.html


[Article Link](https://www.facebook.com/share/p/1BhrwMoQHS/)