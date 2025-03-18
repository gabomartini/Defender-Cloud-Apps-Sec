<p align="center">
  <img src="https://github.com/user-attachments/assets/d75e3b18-178a-43ec-b5e5-1dd6c584675b" width="150" height="auto">
  <h1 align="center">Securing Enterprise Applications with Defender for Cloud Apps</h1>
</p>

#### *In this tutorial we will:*
*- Discover and analyze Shadow IT applications using Microsoft Defender for Cloud Apps.*

*- Block unsafe applications by tagging them as unsanctioned to prevent their usage.*

*- Automate the blocking of risky applications by creating a custom app discovery policy.*

#### Tasks:
1.  Configuring Defender for Endpoint for Cloud App Security.
2.  Analyzing Shadow IT Risks and Usage.
3.  Restrict Unauthorized & Risky Applications.
4.  Automating Shadow IT Management with Policies.

## Task 1: Configuring Defender for Endpoint for Cloud App Security.

In this task, we will enable Microsoft Defender for Cloud Apps by integrating it with Defender for Endpoint, allowing visibility and control over unauthorized applications.

1.  In the Microsoft Defender portal, https://security.microsoft.com, expand "Investigation & response" then expand "Hunting" and select "Advanced Hunting". Wait for the completion of the new spaces preparation. 

<p align="center">
<img src="https://github.com/user-attachments/assets/cef4469c-da78-426c-a47e-ddc0c4fb3141">
</p>

2.	In the Microsoft Defender portal, in the left navigation page expand System then select Settings.
3.	On the Settings page select Microsoft Defender XDR.

<p align="center">
<img src="https://github.com/user-attachments/assets/b8616627-9415-451e-b4e4-2c6a2d6a4398">
</p>

4.	Under Microsoft Defender XDR, select "Preview features" and Enable Microsoft Defender for Cloud Apps.
5.	At the bottom of the page, select "Save". With this set-up all signals coming from Microsoft Defender for Endpoints are forwarded to Defender for Cloud Apps giving you the ability to block unsecure applications. All applications tagged as Unsanctoned will now be blocked.

## Task 2: Analyzing Shadow IT Risks and Usage.

In this task, we will analyze discovered applications within the organization, assess their risk levels, and identify potentially unsafe software.

1.  In the Microsoft Defender portal, in the left navigation page expand Cloud apps and select Cloud discovery.

<p align="center">
<img src="https://github.com/user-attachments/assets/201d29f9-a990-4e1e-8276-70b99e9a49f6">
</p>

2.	On the Cloud Discovery page select Discovered apps.

<p align="center">
<img src="https://github.com/user-attachments/assets/91b658e3-1f70-4710-b1ec-edca5e38441c">
</p>

3.	The Discovered apps blade displays all applications currently utilized within your organization. Explore multiple applications and their associated risk scores by selecting each respective application. Defender for Cloud Apps assesses risks by evaluating regulatory certification, industry standards, and best practices. The score reflects the maturity of the app's suitability for enterprise use. It calculates a total score for each app by averaging weighted subscores across various risk categories that include considerations for reliability.

## Task 3: Restrict Unauthorized & Risky Applications.

In this task, we will block high-risk applications by marking them as unsanctioned, preventing employees from using them.

1.  In the Microsoft Defender portal, in the left navigation page expand Cloud apps and select Cloud discovery.
2.	On the Cloud Discovery page select Discovered apps.
3.	Set the filter for Risk score to 0 - 4.

<p align="center">
<img src="https://github.com/user-attachments/assets/ef5f9923-ae57-47ea-80c1-651b97c7b88d">
</p>
 
4.	Select "Bulk selection" then select "All".
5.	Select the three dots (...) for More actions.
6.	Select Tag as unsanctioned.

<p align="center">
<img src="https://github.com/user-attachments/assets/f439a590-3b50-453e-a542-14a69dd4d17d">
</p>
 
7.	Select "Save". You have successfully blocked vulnerable applications from being used by users.

<p align="center">
<img src="https://github.com/user-attachments/assets/96702f1f-01d7-46b5-a702-12a3ab6ca8f2">
</p>

<p align="center">
<img src="https://github.com/user-attachments/assets/33abff9c-47c4-47b9-96e5-bff68f780d08">
</p>

## Task 4: Automating Shadow IT Management with Policies.

In this task, we will create an automated policy to tag and block unsafe applications based on risk scores, ensuring continuous security enforcement.

1.  In the Microsoft Defender portal, in the left navigation page expand Cloud apps and select Cloud discovery.
2.	On the Discovered apps page select "+ New policy from search".

<p align="center">
<img src="https://github.com/user-attachments/assets/34a1fa2a-7335-43fc-ba5c-ecd435625cdc">
</p>

3.	Enter the following information: Policy Name: Tag unsafe apps as unsanctioned, Policy severity: Medium, Description for users: Applications with a risk score of 4 or lower will be unsanctioned and blocked automatically.
4.	Under Apps matching all of the following add a filter and set it to Risk score equals 0-4.
5.	Under Alerts select Create an alert for each matching event with the policy's severity and set the value for Daily alert limit per policy to 5.
6.	Under Governance actions select Tag app as unsanctioned.

<p align="center">
<img src="https://github.com/user-attachments/assets/c5c176a6-9141-42e7-957e-173858965313">
</p> 

7.	Select "Create". You have successfully created a policy to tag applications with a risk score of 5 or lower as unsanctioned.

<p align="center">
<img src="https://github.com/user-attachments/assets/30d0f270-233c-4757-8c4e-af97c3ce91f0">
</p>
