# Passive

{% hint style="info" %}
OSINT (Open Source Intelligence) techniques involve gathering information from publicly available sources to gather intelligence about individuals, organizations, or other targets of interest.
{% endhint %}

### Techniques

#### Google Dorking

1. Site Search: By using the "site:" operator followed by a specific domain, you can limit your search to a particular website. For example, "site:example.com" will only display search results from the example.com domain.
2. File Type Search: Using the "filetype:" operator, you can search for specific file types. For instance, "filetype:pdf" will retrieve search results that only include PDF files.
3. Intitle/Allintitle: The "intitle:" operator allows you to search for pages with specific words in the title. For example, "intitle:password reset" will show pages with "password reset" in the title. The "allintitle:" operator searches for multiple terms in the title.
4. Inurl/Allinurl: The "inurl:" operator is used to find pages with specific words in the URL. For instance, "inurl:admin" will display pages with "admin" in the URL. The "allinurl:" operator searches for multiple terms in the URL.
5. Cache Search: Using the "cache:" operator followed by a URL, you can view the cached version of a web page as stored by Google.
6. Related Search: The "related:" operator shows websites that are similar to the specified domain. For example, "related:example.com" will display sites related to example.com.
7. Link Search: By using the "link:" operator followed by a URL, you can find pages that link to the specified URL. For instance, "link:example.com" will show pages linking to example.com.
8. Combination and Advanced Operators: You can combine various operators to create more complex search queries. For example, using "intitle:" and "site:" together, like "intitle:login site:example.com," will search for login pages within the example.com domain.

[https://www.exploit-db.com/google-hacking-database](https://www.exploit-db.com/google-hacking-database)

#### Social Media Analysis&#x20;

Social media platforms like Facebook, Twitter, LinkedIn, and Instagram provide a wealth of information. By analyzing profiles, posts, comments, and connections, you can gather insights about individuals, their interests, affiliations, and even potential security vulnerabilities. HashTag searches, geolocation, and image searches can also be useful in extracting relevant information.

#### Public Records and Government Databases&#x20;

1. Property Records: These records include information about property ownership, tax assessments, sale history, and property details. They are usually maintained by local government agencies, such as county assessor's offices or land registries.
2. Business Registrations: Government databases maintain records of registered businesses, including information about the company's name, address, directors, shareholders, and registration status. These records are typically managed by agencies like the Secretary of State or Companies House, depending on the country.
3. Court Records: Court records contain information about legal cases, including criminal proceedings, civil suits, judgments, and other legal actions. These records can be accessed through online court portals or by visiting the respective courthouse.
4. Professional Licenses: Many professions require licenses, such as doctors, lawyers, real estate agents, or contractors. Government databases maintain records of licensed professionals, including their qualifications, certifications, and any disciplinary actions taken against them.
5. Voter Registration: Voter registration databases provide information about registered voters, including their names, addresses, and sometimes political affiliations. These databases are maintained by government election authorities and are often accessible for public viewing.
6. Freedom of Information Act (FOIA) Requests: Governments have provisions like the FOIA that allow citizens to request access to specific government records, documents, or information. FOIA requests can be made to various government agencies, providing access to a wide range of information.
7. Environmental Databases: Government agencies track and maintain data on environmental aspects such as air quality, water quality, hazardous waste, and contaminated sites. These databases often provide public access to environmental monitoring reports and related information.
8. Criminal Records: Law enforcement agencies and court systems maintain criminal records, including arrest records, convictions, and charges. These records may be accessible through online databases or by contacting the appropriate law enforcement agencies.
9. Government Spending and Contracts: Some governments provide public access to databases that track government spending, contracts awarded, and vendors associated with these contracts. These databases can provide insights into how public funds are allocated and utilized.
10. Health and Safety Violations: Government agencies responsible for health and safety regulations maintain databases that document violations, inspections, and enforcement actions against businesses and individuals. These records can reveal information about safety violations, health code compliance, and related issues.

#### WHOIS Lookup

WHOIS databases provide information about domain name registrations. By performing a WHOIS lookup, you can find details about the domain owner, their contact information, registration dates, and sometimes even the hosting provider. This information can help you gain insights into the organization behind a website or identify potential attack vectors.

* [https://www.whois.com/whois](https://www.whois.com/whois)
* [https://lookup.icann.org/en](https://lookup.icann.org/en)
* [https://who.is/](https://who.is/)
* [https://dnsdumpster.com/](https://dnsdumpster.com/)
* [https://mxtoolbox.com/CERT.aspx](https://mxtoolbox.com/CERT.aspx)
* [https://www.sslchecker.com/sslchecker](https://www.sslchecker.com/sslchecker)

#### Online Forums and Communities

Participating in or monitoring online forums and communities relevant to your target can provide valuable information. People often discuss various topics, share experiences, and seek advice, which can provide insights into their activities, challenges, and potential vulnerabilities.

#### Publicly Available Exploit Databases

There are databases that catalog known software vulnerabilities and associated exploits. By searching these databases, you can identify vulnerabilities in target systems or applications and obtain information about exploit techniques and available patches.

* [https://www.exploit-db.com/](https://www.exploit-db.com/)
* [https://vulners.com/](https://vulners.com/)
* [https://nvd.nist.gov/vuln](https://nvd.nist.gov/vuln)
* [https://security.snyk.io/](https://security.snyk.io/)

#### Reverse Image Search

Reverse image search tools allow you to upload an image or provide its URL to find similar or identical images across the web. This can help in identifying the original source of an image, verifying the authenticity of a profile picture, or locating other instances where the image has been used.

* [https://tineye.com/](https://tineye.com/)
* [https://www.reverseimagesearch.com/](https://www.reverseimagesearch.com/)
* [https://www.bing.com/visualsearch](https://www.bing.com/visualsearch)
* [https://images.google.com/](https://images.google.com/)

#### Metadata Analysis

Metadata embedded within files (such as documents, images, or videos) can contain valuable information. Extracting and analyzing metadata can reveal details like author names, timestamps, geolocation, device information, or editing history, providing additional context to the information.

* [https://exiftool.org/](https://exiftool.org/)
* [https://gchq.github.io/CyberChef/](https://gchq.github.io/CyberChef/)
