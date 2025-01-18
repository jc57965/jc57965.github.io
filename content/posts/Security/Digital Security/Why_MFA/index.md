---
title: "why MFA is an absolute must"
date: 2025-01-17T08:06:25+06:00
description: SMS MFA also is as bad as the cybersecurity industry says it is.
menu:
  sidebar:
    name: Why MFA
    identifier: Why_MFA
    parent: Digital-Security
    weight: 10
author:
  name: Jeff Carstensen
  image: /images/author/jeff.png
math: true
---

## Introduction

MFA is a must in this this day and age. I not naive in that it is a foolproof way to secure your account. However, MFA adds just more more layer of security to your account and many times an hacker will move on to a less secure account to comprise.  There are many ways and opinions on how to implement MFA. This article will cover the most common ways with pros and cons of each way to implement MFA.

## SMS MFA

SMS MFA is the most common form of MFA. It is a simple and easist way to implement MFA as most people have a cell phone these days. We all gotten the text message with a six digit code we have to enter after successfully logging into one of our accounts. SMS MFA is also the least secure form of MFA. in the age of social engineering and sim jacking one can easily find thier cell phone number compromised. it for this reason that the telecom industry is trying to make it harder to port your cell phone number.  the Telecoms each have introduced protection to prevent this from happening however many of these are opt in programs. if you rely on SMS MFA i would make sure your provider has enabled all protections to prevent sim jacking from happening on your account.

## Email MFA

Email MFA is a second most common form of MFA much like SMS this is not very secure as social engineering and phishing can compromise your email account. Email based MFA works much like SMS MFA in providing a code or a login link to confirm your identity. one again this relies on being able to access the email account tied to your service account for a given service.  Also if a hacker is able to access your email account and begin to move laterally to try and compromise other accounts email based MFA will not prevent this from happening unlike the following solutions cover in the next sections.

## App Based MFA

App based MFA is the best mix of security and usability. It is a very secure way to implement MFA. App based MFA brings the best of requiring something you know and something you have.  App Based MFA relies on the user using an mobile application where after scanning an QR code the application will generate a Time Based One Time Password (TOTP) code in the form of a six or digit code.  The user will then enter the code into the application to confirm their identity. This is the most secure form of MFA as it requires the user to have a secondary devic in the form of a mobile phone to be able to access an account..  This is also a highly secure form of MFA as attackers must not only gain access to the username and password but also gain access to the TOTP code which changes every 30 seconds or so. These apps also provide an extra layer of protection as many of these apps are also protected by the biometrics protection options on the device. These apps also provide a better user experience in the event you no longer have access to your phone when using app based MFA many services will provide you a list of backups code to use in case you lose access to your device.

## iOS MFA Recommendations

In the app store there is no shortage of apps that provide a wallet to store your 2FA codes.  The most popular wallets are Google Authenticator and Microsoft Authenticator. Twilo Authy is also another popular option.  However I would recommend against using any of the big name wallets as they are required to either provide a phone number to setup an account or use your google or microsoft account to setup. my Recommendation for a MFA app for iOS and the one I personally use is 2FAS Auth. It is a free app that is open source and has a very simple interface. it is also very secure as it uses the device hardware to generate the codes and can pair with face id or require a pin to unlock. it also has a great feature as of late where upon opening the app all codes are automatically hidden making an shoulder surfing attack very difficult. Also it makes cloud backups to your iCloud account an option but not an requirement.


## Android MFA Recommendations

Android has a similar problem to iOS in that there is no shortage of apps that provide a wallet to store your 2FA codes.  Andriod has many of the same options as iOS. Much like my iOS recommendations again I will recommmend the lesser known app 2FAS Auth. I will also recommend an Android only app in Aegis Authenticator.  This app is also open source and doesn't rely on a needing an account to setup and like 2FAS Auth it can also use the biometrics protection of your device to add an extra layer of security. It also has the same feature as 2FAS Auth that it will hide all codes upon opening the app.  Aegis Authenticator is also a mature app compared to 2FAS Auth as it has been around for a whie and has a large community of users.

## Hardware based MFA

Hawrdware based MFA is the most secure form of MFA it is also the most difficult to implement in my opinion. One thing we haven't talked about yet is the price to implement the above solutions all the other options are nearly free to implement. you using the phone service you already have the email account tied to your account is likely free. and both app recommendations are free as well. Hardware based MFA uses NFC and USB devices to authenicate your identity. the issue with this is you must carry around this USB device wit you if you access your protected account on the go. for this reason it is always advise to have a complete secondary device that you keep secure in a safe or other secure location. These devices range from $30 to $60 USD depending on the brand and features. given this number it costs nearly $100 to to implement hardware based MFA.  there are also limited options for hardware based MFA devices with Yubico and Google being the main two. in my opinion again I would look at Yubico over Google to keep you secured keys away from big tech. Yubico however is not without it's issues. In 2024 Security researches found a flaw with the Yubikey 5 and Security Key Series prior to firmware 5.7 are  vulnerable to a high-level cloning attack in which Yubico has stated a fix can not be released. It should be mentioned that this flaw would not affect most end users as it requires a highly techical know how and a expensive setup to complete the exploit. furthermore the flaw requires an attacker to have access to the device for over a day to complete the attack.

Yubikey is still the leader in hardware based MFA. it is my opinion unless you have a specific reason such as working for governments or have properity company information that you wan't to protect at all costs than hardware base MFA is the way to go.

## Conclusion

Finally in conclusion with the rise of cybercrime and data breaches I would recommend that you take the time to implement MFA on your accounts. Most people should use App based MFA if the service allows for it as it is the easist to implement and provides the balence of usability and security. SMS and Email based MFA is better than nothing but with social engineering and phishing attacks and sim jacking an constant threat. it is important to be mindful of the risks.
