<p align="center">
  <img src="https://github.com/user-attachments/assets/d75e3b18-178a-43ec-b5e5-1dd6c584675b" width="150" height="auto">
  <h1 align="center">Securing Enterprise Applications with Defender for Cloud Apps</h1>
</p>

#### *In this tutorial we will:*
*•	Discover and analyze Shadow IT (unauthorized applications used within an organization) with Microsoft Defender for Cloud Apps.*

*•	Block unsafe applications by tagging them as unsanctioned to prevent usage.*

*•	Automate the blocking of risky applications with a custom app discovery policy.*

#### Tasks:
1.  Configuring Defender for Endpoint for Cloud App Security.
2.  Analyzing Shadow IT Risks and Usage.
3.  Restrict Unauthorized & Risky Applications.
4.  Automating Shadow IT Management with Policies.

## Task 1: Configuring Defender for Endpoint for Cloud App Security.

Enable Microsoft Defender for Cloud Apps by integrating it with Defender for Endpoint to gain visibility and control over unauthorized applications.

1.	Open the Microsoft Defender portal at https://security.microsoft.com.
2.	In the left navigation menu, expand "Investigation & response", then expand "Hunting" and select "Advanced Hunting". (Wait for the new spaces preparation to complete.)

<p align="center">
<img src="https://github.com/user-attachments/assets/cef4469c-da78-426c-a47e-ddc0c4fb3141">
</p>

3.	In the left navigation menu, expand "System", then select "Settings".
4.	On the "Settings" page, click "Microsoft Defender XDR".

<p align="center">
<img src="https://github.com/user-attachments/assets/b8616627-9415-451e-b4e4-2c6a2d6a4398">
</p>

5.	Under "Microsoft Defender XDR", select "Preview features".
6.	Enable "Microsoft Defender for Cloud Apps" by checking its box. (This forwards signals from Defender for Endpoint to Defender for Cloud Apps, enabling app blocking.)
7.	Scroll to the bottom of the page and click "Save". (All applications tagged as "Unsanctioned" will now be blocked across monitored devices.)

## Task 2: Analyzing Shadow IT Risks and Usage.

Analyze discovered applications within your organization to assess their risk levels and identify potentially unsafe software.

1.	In the Microsoft Defender portal, from the left navigation menu, expand "Cloud apps" and select "Cloud discovery".

<p align="center">
<img src="https://github.com/user-attachments/assets/201d29f9-a990-4e1e-8276-70b99e9a49f6">
</p>

2.	On the "Cloud Discovery" page, click "Discovered apps".

<p align="center">
<img src="https://github.com/user-attachments/assets/91b658e3-1f70-4710-b1ec-edca5e38441c">
</p>

3.	Review the "Discovered apps" blade, which lists all applications currently used in your organization.
4.	Explore multiple applications by clicking each one to view its risk score and details. (Defender for Cloud Apps assigns risk scores based on regulatory certifications, industry standards, and best practices, averaging weighted subscores across categories like reliability and security to determine enterprise suitability.)

## Task 3: Restrict Unauthorized & Risky Applications.

Block high-risk applications by tagging them as unsanctioned, preventing employees from using them.

1.	In the Microsoft Defender portal, from the left navigation menu, expand "Cloud apps" and select "Cloud discovery".
2.	On the "Cloud Discovery" page, click "Discovered apps".
3.	Set the "Risk score" filter to "0 - 4" to display applications with low safety ratings.

<p align="center">
<img src="https://github.com/user-attachments/assets/ef5f9923-ae57-47ea-80c1-651b97c7b88d">
</p>
 
4.	Click "Bulk selection", then select "All".
5.	Click the three dots (...) for "More actions".
6.	Select "Tag as unsanctioned".

<p align="center">
<img src="https://github.com/user-attachments/assets/f439a590-3b50-453e-a542-14a69dd4d17d">
</p>
 
7.	Click "Save". (This blocks all selected vulnerable applications from use by users.)

<p align="center">
<img src="https://github.com/user-attachments/assets/96702f1f-01d7-46b5-a702-12a3ab6ca8f2">
</p>

<p align="center">
<img src="https://github.com/user-attachments/assets/33abff9c-47c4-47b9-96e5-bff68f780d08">
</p>

## Task 4: Automating Shadow IT Management with Policies.

Create an automated policy to tag and block unsafe applications based on risk scores, ensuring continuous security enforcement.

1.	In the Microsoft Defender portal, from the left navigation menu, expand "Cloud apps" and select "Cloud discovery".
2.	On the "Discovered apps" page, click "+ New policy from search".

<p align="center">
<img src="https://github.com/user-attachments/assets/34a1fa2a-7335-43fc-ba5c-ecd435625cdc">
</p>

3.	Enter the following details:
    -  Policy Name: "Tag unsafe apps as unsanctioned".
    -  Policy severity: "Medium".
    -  Description for users: "Applications with a risk score of 4 or lower will be unsanctioned and blocked automatically".
4.	Under "Apps matching all of the following", add a filter and set it to "Risk score equals 0-4".
5.	Under "Alerts", check "Create an alert for each matching event with the policy's severity" and set "Daily alert limit per policy" to "5".
6.	Under "Governance actions", select "Tag app as unsanctioned".

<p align="center">
<img src="https://github.com/user-attachments/assets/c5c176a6-9141-42e7-957e-173858965313">
</p> 

7.	Click "Create". (This policy automatically tags and blocks applications with a risk score of 4 or lower.)

<p align="center">
<img src="https://github.com/user-attachments/assets/30d0f270-233c-4757-8c4e-af97c3ce91f0">
</p>
