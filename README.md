E**nrollment guide: Enroll iOS and iPadOS devices in Microsoft Intune**<br />
https://learn.microsoft.com/en-us/mem/intune/fundamentals/deployment-guide-enrollment-ios-ipados?source=recommendations.

Get an Apple automated device enrollment token<br />
https://learn.microsoft.com/en-us/mem/intune/enrollment/device-enrollment-program-enroll-ios

Corporate-owned devices purchased through Apple Business Manager or Apple School Manager can be enrolled in Intune via automated device enrollment. This enrollment option applies your organization's settings from Apple Business Manager and Apple School Manager and enrolls devices without you needing to touch them. iPhones and iPads can be shipped directly to employees and students. When they turn on their devices, the Apple Setup Assistant guides them through setup and enrollment.

Step1: Prerequisites<br />
•	Access to Apple Business Manager portal or Apple School Manager portal.<br />
Sign up for Business Manager account here https://business.apple.com/signup/<br />
You can't use an email that already has Apple ID<br />

•	An active Apple token (.p7m file).<br />
•	An Apple MDM push certificate in Intune.<br />
•	New or wiped devices purchased from Apple Business Manager or Apple School Manager.

Step 2: Authentication method
Before creating enrollment profile, decide how you want users to authenticate on their devices: via Intune Company Portal, Setup Assistant (legacy), or Setup Assistant with modern authentication. Using the Company Portal app or Setup Assistant with modern authentication is considered modern authentication and has features like multi-factor authentication.
•	Setup Assistant with modern authentication is supported on iOS/iPad 13.0 and later.

Supervised mode: Provides more management control over corporate-owned devices like blocking screen capture and so on.

Corporate-owned devices running iOS/iPadOS 11+ and enrolled via automated device enrollment should always be in supervised mode, which you can turn on in the enrollment profile.<br />

**Next**<br />
Enrollment program tokens: <br /> 
Before enrolling with ADE, you need automated device enrollment token (.p7m file)<br /> from Apple. This token lets Intune sync information about ADE devices that <br />your Organization owns. To upload enrollment profiles to Apple and to assign devices to those policies.<br />

You can use Apple Business Manager (ABM) or Apple School Manager (ASM) to create <br />a token and assign devices to Intune for management.<br />
**Step 1: Download the Intune public key certificate**<br />
1.	In the Microsoft Intune admin center, go to Devices > Enrollment.<br />
2.	Select the Apple tab.<br />
3.	Select Enrollment Program Tokens > Add.<br />
4.	On the Basics tab:<br />
a.	Select I agree

![image](https://github.com/stahir131/Apple-Automated-Device-Enrollment/assets/64047385/c67f339c-32b6-4a4e-aaa7-46cd0f403b2e)

b. **Select Download the Intune public key certificate required to create the token.** This saves the .pem file locally which will be used to request a trust-relationship from Apple Business Manager portal. <br />
c. Keep web browser tab and pages open to not invalidate the cert.

**Step 2: Go to Apple Business Manager portal to download Apple token**<br />
Sign in to https://business.apple.com/ with your Apple ID<br />

Go to Settings > Add MDM server and upload the public key cert(.pem file) downloaded in step 1.























