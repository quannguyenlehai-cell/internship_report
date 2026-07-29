---
title: "Blog 3"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 3.3. </b> "
---
2-Month Internship Project: Facial Recognition Door Access Control System

This is an intelligent access control system combining inexpensive AI hardware (Edge-AI) and cloud infrastructure (AWS Serverless).
1. Idea
In reality, current door locking methods all have their own drawbacks:
- Mechanical keys & magnetic cards: Easily lost, forgotten, or copied.

- PIN passwords: Easily spied on.

- Cloud-based facial scanning locks: Often expensive and prone to delays.

Objective: To create a super-affordable facial scanning door access control system (hardware cost less than 400,000 VND), with administrators managing access remotely via web.

2. How the System Works
The model is divided into two main parts:
- At the door (ESP32-CAM)
All facial recognition is processed directly on the ESP32-CAM chip.
Standing in front of the camera -> Chip scans face -> Data matching -> Unlocking (latency less than 0.5 s).

- In the cloud (AWS infrastructure)
AWS IoT Core: receives data from the device.
AWS Lambda: Automatically "wakes up" to receive data.

AWS Amplify & API Gateway: Creates a webpage for administrators to see who has entered and exited, add new users, or remotely open and close the door.

3. Project Highlights
Super affordable price: the hardware cost for one door unit is only about 400k VND - nearly 90% cheaper than commercial smart lock systems.
Cloud cost optimization: Thanks to the serverless backend, the system automatically scales when users are present and incurs virtually no costs when idle.
Ultra-low latency: AI processing at the end device enables instant activation.
Conclusion:
In just two months, from a student who was still unfamiliar with the concept of cloud, building a project combining IoT and Serverless has helped me understand much more about practical system knowledge.

— with Lehaiquan Nguyen.

[Facebook Link](https://www.facebook.com/groups/awsstudygroupfcj/permalink/2225859081512385/?rdid=edl9gIuvqI9LEabB#)