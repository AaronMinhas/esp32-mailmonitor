# ESP32-CAM Enabled Mail Sensing IoT Device

## Inspiration
This project was proposed as a fun and somewhat silly solution to checking for mail without the need to walk to the mailbox. Why walk when technology can do it for you?

## Project Overview
This project uses an ESP32-CAM board inside a mailbox to send notifications when mail is delivered. The system captures an image of the mailbox contents and sends an email to the user with the image attached. 

## Features
- **Rechargeable / Self-Sustainable**: The device is powered via solar to ensure long-term sustainability.
- **Notifications**: A motion sensor triggers the ESP32 to capture an image and send an email when mail is delivered. The image is attached to the email for easy viewing.
- **Waterproof**: The device is housed in a **GO-PRO waterproof case** to protect it from weather conditions.

## Design Overview
1. **ESP32 Functionality**:
   - **Motion Detection**: The ESP32 wakes up from deep sleep when motion is detected in the mailbox.
    - **Image Capture**: The ESP32 captures an image 5-10 seconds after motion detection to allow for proper mail placement.
   - **Email Notification**: Once an image is captured, an email is sent to the user with the image attached.
  
2. **Email Notifications**:
   - The email contains the message: "Mail has been delivered," with the image of the mailbox contents attached.

## Initial Concerns

### False Positives
- **Issue**: The system triggering false positives, such as when the mail is collected.
- **Potential Solution**: ¯\_(ツ)_/¯ unbeknownst to me thus far, still exploring potential fixes.

### Wifi Range
- **Issue**: The ESP32 has a weak signal to home network.
- **Potential Solution**: Use an external antenna for the ESP32 to improve signal strength, or consider a Wi-Fi range extender for better coverage.
