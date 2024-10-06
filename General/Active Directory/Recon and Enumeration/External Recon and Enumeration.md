### What Should We Look For?

During our external reconnaissance, several critical pieces of information need to be identified. While some of this data may not be readily available, it is still worthwhile to explore what can be uncovered. If we encounter obstacles during a penetration test, revisiting the insights gathered from passive reconnaissance can provide the boost needed to progress. For instance, breach data might reveal credentials that allow access to a VPN or other external services. Below is a summary of key data points to focus on during this phase of the engagement:

| **Data Point**        | **Description**                                                                                                                                                          |
| --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **IP Space**          | Identifying valid ASNs for the target, public netblocks, cloud infrastructure, DNS records, and hosting providers.                                                         |
| **Domain Information**| Using IP and DNS data, uncover domain administrators, subdomains, publicly accessible services (e.g., mail servers, VPN portals), and the defenses in place (SIEM, IPS/IDS).|
| **Schema Format**     | Discovering email formats, AD usernames, and password policies to generate username lists for testing external-facing services.                                             |
| **Data Disclosures**  | Searching for publicly available files (e.g., PDFs, DOCs) that may contain sensitive metadata, intranet links, or credentials.                                              |
| **Breach Data**       | Looking for publicly leaked usernames, passwords, or other information that could provide an entry point for an attacker.                                                 |

We’ve outlined the "what" and "why" of external reconnaissance; next, let's explore the "where" and "how."

### Where Should We Look?

The data points mentioned above can be collected using various methods and resources. Numerous websites and tools can provide valuable information for conducting our assessment. Below is a list of potential resources and examples to help gather the necessary data:

| **Resource**                       | **Examples**                                                                                                                                                     |
| ---------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **ASN / IP Registrars**            | IANA, ARIN (for the Americas), RIPE (for Europe), and tools like BGP Toolkit.                                                                                     |
| **Domain Registrars & DNS**        | DomainTools, PTRArchive, ICANN, manual DNS lookups, or querying well-known DNS servers (e.g., 8.8.8.8).                                                          |
| **Social Media**                   | LinkedIn, Twitter, Facebook, regional social media, and news articles for organizational insights.                                                               |
| **Public-Facing Company Websites** | Company websites often have useful information in news articles, embedded documents, and pages like "About Us" or "Contact Us."                                   |
| **Cloud & Dev Storage Spaces**     | GitHub, AWS S3 buckets, Azure Blob storage, and using Google Dorks to find public repositories or exposed assets.                                                 |
| **Breach Data Sources**            | Tools like HaveIBeenPwned and Dehashed to check for corporate emails or passwords in breach databases, which can be tested against exposed login portals.          |
https://www.iana.org/
https://www.arin.net/
https://www.ripe.net/
https://bgp.he.net/
https://www.domaintools.com/
http://ptrarchive.com/
https://lookup.icann.org/en
https://haveibeenpwned.com/
https://www.dehashed.com/
https://whois.domaintools.com/
https://viewdns.info/

breadcrumbs:
https://github.com/trufflesecurity/truffleHog
https://buckets.grayhatwarfare.com/

https://github.com/initstring/linkedin2username