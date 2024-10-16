# Direct-Request-OWASP-Challenge

## Objective 
Specifically, my goal was to see how easily valuable information, such as the company's financial reports, could be accessed by directly requesting files.
## Planform: rangeforce
## Scenario
ou work as a security specialist for ComTech, a mid-sized, publicly-traded keyboard manufacturing company. Recently, the U.S. Securities and Exchange Commission (SEC) launched an investigation against a small Eastern European investment bank suspected of insider trading after making millions of dollars by trading in ComTech stocks shortly before public announcements.

ComTech has started an internal investigation into the matter — and you have been tasked with evaluating the security of the company's digital assets.

In this module, you will discover how valuable information can be stolen by directly requesting it. 

## Steps

![image](https://github.com/user-attachments/assets/03a7d073-3222-47df-abbc-c522913edf4b)

I began by thoroughly inspecting ComTech's public website to locate any sections that contained or referenced financial reports. While there was a page listing previous financial reports, there wasn’t any direct link to the most recent report.

<img width="519" alt="image" src="https://github.com/user-attachments/assets/b17166b9-802d-4601-8059-5cec3bf85a05">

By examining the URLs of previous financial reports, I noticed a consistent file-naming pattern. For example, one of the URLs for a past report was structured like this:

http://news.commensuratetechnology.com/assets/20221108-annual-financial-report.pdf

The pattern included the date followed by -annual-financial-report.pdf. I inferred that the latest financial report might follow this same structure.

Even though the new financial report hadn’t been published on the website yet, I modified the URL based on the previous pattern to check if the latest report had been uploaded but not linked.
I tried a URL with the expected 2024 report date:

<img width="553" alt="image" src="https://github.com/user-attachments/assets/470851b6-e9a9-45a6-8397-47b8a2794dc3">

This attempt was successful, and I was able to access and open the PDF file containing ComTech’s latest financial report.

<img width="515" alt="image" src="https://github.com/user-attachments/assets/9bf074b0-5ddd-4f83-a9b3-1f9dbdb60589">


## How I think this vulnerability can be prevented:

**Improve Access Control:** Implement stronger access controls for digital assets, ensuring that files cannot be accessed without proper authorization, even if they are uploaded to the server.

**Review File Naming Conventions:** Consider using randomized or non-predictable file names for sensitive documents to prevent unauthorized access through URL manipulation.

**Conduct Regular Security Audits:** Regularly audit the company’s digital assets to ensure that sensitive files are not exposed inadvertently.

