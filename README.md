# Threat-Intelligence

## Threat Intelligence Tools
This room on TryHackMe covers the concepts of Threat Intelligence and various open-source tools that are useful.

#The learning objectives include:
- Understanding the basics of threat intelligence & its classifications.
- Using UrlScan.io to scan for malicious URLs.
- Using Abuse.ch to track malware and botnet indicators.
- Investigate phishing emails using PhishTool
- Using Cisco's Talos Intelligence platform for intel gathering.

##Tools
- UrlScan.io
- Abuse.ch
- PhishTool
- Cisco's Talos Intelligence platform

# Urlscan.io is a free service developed to assist in scanning and analysing websites. It is used to automate the process of browsing and crawling through websites to record activities and interactions.
When a URL is submitted, the information recorded includes the domains and IP addresses contacted, resources requested from the domains, a snapshot of the web page, technologies utilised and other metadata about the website.

## Task 3
* What was TryHackMe's Cisco Umbrella Rank based on the screenshot?
The Cisco Umbrella domain rank is illustrated in the attached screenshot summary, indicating that the rank for the primary domain is 345612.
<img width="943" alt="Screenshot 2024-03-10 at 14 35 49" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/76b83042-e638-4b78-9db4-2351d6c25100">

* How many domains did UrlScan.io identify on the screenshot?
The attached screenshot reveals that the website communicated with 17 IPs across 4 countries and 13 domains.
<img width="941" alt="Screenshot 2024-03-10 at 14 48 53" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/1d3c5249-7e54-4f1f-b32c-38968d468bac">

* What was the main domain registrar listed on the screenshot?
The name if the domain registrar is NAMECHEAP INC.
<img width="939" alt="Screenshot 2024-03-10 at 14 53 17" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/5289f10a-2f65-4222-8245-e2510a57f8f7">

* What was the main IP address identified for TryHackMe on the screenshot?
The main IP address identified is 2606:4700:10::ac43:1b0a.
<img width="940" alt="Screenshot 2024-03-10 at 14 57 08" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/2903e29b-a2a2-4ceb-9bc2-4689bb543864">

# Abuse.ch is a research project hosted by the Institue for Cybersecurity and Engineering at the Bern University of Applied Sciences in Switzerland. It was developed to identify and track malware and botnets through several operational platforms developed under the project. These platforms are:
- Malware Bazaar:  A resource for sharing malware samples.
- Feodo Tracker:  A resource used to track botnet command and control (C2) infrastructure linked with Emotet, Dridex and TrickBot.
- SSL Blacklist:  A resource for collecting and providing a blocklist for malicious SSL certificates and JA3/JA3s fingerprints.
- URL Haus:  A resource for sharing malware distribution sites.
- Threat Fox:  A resource for sharing indicators of compromise (IOCs).

## Task 4
* The IOC 212.192.246.30:5555 is identified under which malware alias name on ThreatFox?
Begin by selecting and highlighting the suspected IP address in the question, then navigate to ThreatFox. Once the page has loaded, proceed to click on the ThreatFox database.
<img width="1301" alt="Screenshot 2024-03-10 at 15 08 28" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/da657203-49b7-468b-bd64-537a6c958ae0">

Upon reaching the subsequent page, you may attempt to immediately search for the IP and port, but unfortunately, you won't discover any results. Therefore, prior to conducting the IP:port search, click on the Search Syntax button. This action will reveal a dropdown menu, with the first bullet point corresponding to IOC, as requested in the question.
<img width="1393" alt="Screenshot 2024-03-10 at 15 13 36" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/132f42da-c2a5-4bb6-8031-671bf245dfad">

Now we need to paste the IOC 212.192.246.30:5555 to the search box and search.
<img width="1417" alt="Screenshot 2024-03-10 at 15 18 31" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/96424dc2-02da-4fb0-a5db-5876cc5e4ba4">

In the search results, we click on the ip:port link to see the malware alias which is "Katana".
<img width="1440" alt="Screenshot 2024-03-10 at 15 23 40" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/643ba70d-57d9-4e0b-b3fd-0e63bf8f481b">

* Which malware is associated with the JA3 Fingerprint 51c64c77e60f3980eea90869b68c58a8 on SSL Blacklist?
We begin by copying the JA# Fingerprint and navigating to the SSL blacklist website. On the website we select view details under SSL blacklist.
<img width="1267" alt="Screenshot 2024-03-10 at 15 41 23" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/7652dc85-f6ad-4346-aaec-94590d198fb6">

After the new window opens, paste the JA3 Fingerprint 51c64c77e60f3980eea90869b68c58a8 into the search box and click on the search button.
<img width="1248" alt="Screenshot 2024-03-10 at 15 43 07" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/d16c5ac2-ae8e-4210-8ee2-40074e15191d">

Now, proceed to click on the link associated with the JA3 Fingerprint. The name of the malware, "Dridex," can be located within the table displayed in the open window.
<img width="1419" alt="Screenshot 2024-03-10 at 15 50 31" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/8f81335d-5b41-4a8c-8851-585340240393">

* From the statistics page on URLHaus, what malware-hosting network has the ASN number AS14061?
We begin by copying the ASN number and then navigate to the URLhaus website. Within the website, we visit the statistics page and search for the ASN number AS14061 to locate the malware-hosting network.
<img width="1382" alt="Screenshot 2024-03-10 at 16 02 43" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/2169782c-a029-4bf3-962e-4647b905d8c9">

* Which country is the botnet IP address 178.134.47.166 associated with according to FeodoTracker?
We start by copying the IP address 178.134.47.166 and proceed to the FeodoTracker website. Within the website, we select "browse" and paste the IP address into the search box to view the results. The search outcomes reveal that the country associated with the botnet IP address is "Georgia."
<img width="1440" alt="Screenshot 2024-03-10 at 16 11 36" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/2761e303-9f26-47db-8da6-b8e750103686">

## Task 5
PhishTool seeks to elevate the perception of phishing as a severe form of attack and provide a responsive means of email security. Through email analysis, security analysts can uncover email IOCs, prevent breaches and provide forensic reports that could be used in phishing containment and training engagements.

#The core features include:
- Perform email analysis: PhishTool retrieves metadata from phishing emails and provides analysts with the relevant explanations and capabilities to follow the email’s actions, attachments, and URLs to triage the situation.
- Heuristic intelligence: OSINT is baked into the tool to provide analysts with the intelligence needed to stay ahead of persistent attacks and understand what TTPs were used to evade security controls and allow the adversary to social engineer a target.
- Classification and reporting: Phishing email classifications are conducted to allow analysts to take action quickly. Additionally, reports can be generated to provide a forensic record that can be shared.

#Additional features are available on the Enterprise version:
- Manage user-reported phishing events.
- Report phishing email findings back to users and keep them engaged in the process.
- Email stack integration with Microsoft 365 and Google Workspace.

* What social media platform is the attacker trying to pose as in the email?
To uncover the organization the attacker is attempting to impersonate, we must enable the attack box in TryHackMe and access the initial email using Pluma. By scrolling attentively through the content, we'll recognize the familiar social media platform "LinkedIn," which is the website the attacker is mimicking.
<img width="794" alt="Screenshot 2024-03-10 at 17 19 02" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/aa474ebc-4b8f-4070-b8d7-b38216acb56d">

* What is the senders email address?
To locate the sender's email address, simply hold (Ctrl + F) and search for "sender" in the search box.
<img width="665" alt="Screenshot 2024-03-10 at 18 13 18" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/6b93dc95-6a4d-47fc-a221-df1fd57d1c67">

* What is the recipient's email address?
To locate the receiver's email address, simply hold (Ctrl + F) and search for "receive ot to" in the search box.
<img width="668" alt="Screenshot 2024-03-10 at 18 16 43" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/03576e69-5be5-448f-9074-1af8a0022b87">

* What is the Originating IP address? Defang the IP address.
To neutralize the originating IP, locate the sender's IP address and navigate to CyberChef. Next, search for "Defang IP address" and drag it to the Recipe section. We will now see the Defanged IP Address in the output section which is "204[.]93[.]183[.]11"
<img width="1183" alt="Screenshot 2024-03-10 at 18 24 20" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/34ed6797-e9dd-4032-9549-a151d1662968">
<img width="940" alt="Screenshot 2024-03-10 at 18 24 57" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/b39ed78f-85eb-4f68-89e8-6f37a123484e">

* How many hops did the email go through to get to the recipient?
Commencing from the file's beginning, observe the initial location. Counting the occurrences of "Received" determines the answer to this question.
<img width="666" alt="Screenshot 2024-03-10 at 18 56 52" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/67ae235f-edc4-449e-88bb-5d69aa193895">

## Task 6
IT and Cybersecurity companies collect massive amounts of information that could be used for threat analysis and intelligence. Being one of those companies, Cisco assembled a large team of security practitioners called Cisco Talos to provide actionable intelligence, visibility on indicators, and protection against emerging threats through data collected from their products. The solution is accessible as Talos Intelligence.

Cisco Talos encompasses six key teams:
- Threat Intelligence & Interdiction: Quick correlation and tracking of threats provide a means to turn simple IOCs into context-rich intel.
- Detection Research: Vulnerability and malware analysis is performed to create rules and content for threat detection.
- Engineering & Development: Provides the maintenance support for the inspection engines and keeps them up-to-date to identify and triage emerging threats.
- Vulnerability Research & Discovery: Working with service and software vendors to develop repeatable means of identifying and reporting security vulnerabilities.
- Communities: Maintains the image of the team and the open-source solutions.
- Global Outreach: Disseminates intelligence to customers and the security community through publications.

* What is the listed domain of the IP address from the previous task?
Initially, access Talos, where you'll find a search box named Reputation Lookup. Enter the defanged IP address from the preceding task into this search box, and either press enter or click the search icon. Subsequently, you'll find information regarding this IP address, including the Domain name, located under Owner Details, which provides the answer to the question.
<img width="1402" alt="Screenshot 2024-03-10 at 19 17 05" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/4b6ad668-20ea-4eec-af81-241952b0572a">

* What is the customer name of the IP address?
While remaining on the current Talos page, scroll down until you reach the section labeled Additional Information. Then, click on the WHOIS tab. Continue scrolling down until you locate the Second # start section, where the customer information is contained. Scan through this section until you find either "Customer:" or "CustName," which provides the answer to the question.
<img width="1225" alt="Screenshot 2024-03-10 at 19 24 51" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/d8ca701b-410a-498f-9ff4-dfe0ac6ea81e">
<img width="530" alt="Screenshot 2024-03-10 at 19 25 39" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/0521a54e-cbb3-4a33-ab60-3d99fb9bb5e9">

## Task 7
Scenario: You are a SOC Analyst. Several suspicious emails have been forwarded to you from other coworkers. You must obtain details from each email to triage the incidents reported. 

Task: Use the tools and knowledge discussed throughout this room (or use your resources) to help you analyze Email2.eml found on the VM attached to Task 5 and use the information to answer the questions.

* According to Email2.eml, what is the recipient's email address?
We can retrieve this answer from earlier when we examined the email in our text editor; it was specified on line 7. Additionally, Phish tool provides this information in the header details.
<img width="833" alt="Screenshot 2024-03-10 at 19 46 24" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/95dfa3d7-276c-43fb-8f11-537ecbcb7f8d">
<img width="469" alt="Screenshot 2024-03-10 at 19 43 32" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/356c9b77-86aa-4759-84f0-3328a27f3e68">

* From Talos Intelligence, the attached file can also be identified by the Detection Alias that starts with an H...
By identifying the detection alias in Talos we can find that the alias is "HIDDENEXT/Worm.Gen"
<img width="800" alt="Screenshot 2024-03-10 at 19 51 00" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/b314c90e-e58a-44ef-a9e6-e78e9687e015">

## Task 8
Scenario: You are a SOC Analyst. Several suspicious emails have been forwarded to you from other coworkers. You must obtain details from each email to triage the incidents reported. 

Task: Use the tools and knowledge discussed throughout this room (or use your resources) to help you analyze Email3.eml found on the VM attached to Task 5 and use the information to answer the questions.

* What is the name of the attachment on Email3.eml?
Inspecting line 79 in the text editor will reveal the name of the attachment. Similarly, on Phish tool, navigating to the attachment tab displays the file name.
<img width="590" alt="Screenshot 2024-03-10 at 20 06 48" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/86f85b32-f4f7-4e57-93f1-91b2bc39a491">
<img width="590" alt="Screenshot 2024-03-10 at 20 07 57" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/981e6c4c-7054-4f81-aa13-60405eee73ca">

* What malware family is associated with the attachment on Email3.eml?
When examining additional details on the file hash in MalwareBazaar, you'll notice a prominent red box containing the answer. Furthermore, in the table, the name can be found in the Signature row. Additionally, within the VirusTotal Security Vendor Analysis, the name appears three times.
<img width="1061" alt="Screenshot 2024-03-10 at 20 23 41" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/dac14d48-af9e-4eec-8cb8-dbb5c5135a81">
<img width="1133" alt="Screenshot 2024-03-10 at 20 25 14" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/8d9e1aeb-622d-488f-8c0a-2b69b99e1a09">



## Task 1
# MISP
MISP - MALWARE INFORMATION SHARING PLATFORM
This room explores the MISP Malware & Threat Sharing Platform through its core objective to foster sharing of structured threat information among security analysts, malware researchers and IT professionals.

Room Objectives
- Introduction to MISP and why it was developed.
- Use cases MISP can be applied to
- Core features and terminologies.
- Dashboard Navigation.
- Event Creation and Management.
- Feeds and Taxonomies.

## Task 2
What is MISP?
MISP (Malware Information Sharing Platform) is an open-source threat information platform that facilitates the collection, storage and distribution of threat intelligence and Indicators of Compromise (IOCs) related to malware, cyber attacks, financial fraud or any intelligence within a community of trusted members. 

Information sharing follows a distributed model, with supported closed, semi-private, and open communities (public). Additionally, the threat information can be distributed and consumed by Network Intrusion Detection Systems (NIDS), log analysis tools and Security Information and Event Management Systems (SIEM).

MISP is effectively useful for the following use cases:

- Malware Reverse Engineering: Sharing of malware indicators to understand how different malware families function.
- Security Investigations: Searching, validating and using indicators in investigating security breaches.
- Intelligence Analysis: Gathering information about adversary groups and their capabilities.
- Law Enforcement: Using Indicators to support forensic investigations.
- Risk Analysis: Researching new threats, their likelihood and occurrences.
- Fraud Analysis: Sharing of financial indicators to detect financial fraud.

What does MISP support? 
MISP provides the following core functionalities:
- IOC database: This allows for the storage of technical and non-technical information about malware samples, incidents, attackers and intelligence.
- Automatic Correlation: Identification of relationships between attributes and indicators from malware, attack campaigns or analysis.
- Data Sharing: This allows for sharing of information using different models of distributions and among different MISP instances.
- Import & Export Features: This allows the import and export of events in different formats to integrate other systems such as NIDS, HIDS, and OpenIOC.
- Event Graph: Showcases the relationships between objects and attributes identified from events.
- API support: Supports integration with own systems to fetch and export events and intelligence.

The following terms are commonly used within MISP and are related to the functionalities described above and the general usage of the platform:
- Events: Collection of contextually linked information.
- Attributes: Individual data points associated with an event, such as network or system indicators.
- Objects: Custom attribute compositions.
- Object References: Relationships between different objects.
- Sightings: Time-specific occurrences of a given data point or attribute detected to provide more credibility.
- Tags: Labels attached to events/attributes.
- Taxonomies: Classification libraries are used to tag, classify and organise information.
- Galaxies: Knowledge base items used to label events/attributes.
- Indicators: Pieces of information that can detect suspicious or malicious cyber activity.

## Task 3
Dashboard
The analyst's view of MISP provides you with the functionalities to track, share and correlate events and IOCs identified during your investigation. The dashboard's menu contains the following options, and we shall look into them further:

- Home button: Returns you to the application's start screen, the event index page or the page set as a custom home page using the star in the top bar.
- Event Actions: All the malware data entered into MISP comprises an event object described by its connected attributes. The Event actions menu gives access to all the functionality related to the creation, modification, deletion, publishing, searching and listing of events and attributes.
- Dashboard: This allows you to create a custom dashboard using widgets.
Galaxies: Shortcut to the list of MISP Galaxies on the MISP instance. More on these on the Feeds & Taxonomies Task.
- Input Filters: Input filters alter how users enter data into this instance. Apart from the basic validation of attribute entry by type, the site administrators can define regular expression replacements and blocklists for specific values and block certain values from being exportable. Users can view these replacement and blocklist rules here, while an administrator can alter them.
- Global Actions: Access to information about MISP and this instance. You can view and edit your profile, view the manual, read the news or the terms of use again, see a list of the active organisations on this instance and a histogram of their contributions by an attribute type.
- MISP: Simple link to your baseurl.
- Name: Name (Auto-generated from Mail address) of currently logged in user.
- Envelope: Link to User Dashboard to consult some of your notifications and changes since the last visit. Like some of the proposals received for your organisation.
- Log out: The Log out button to end your session immediately.
<img width="1234" alt="Screenshot 2024-03-11 at 18 47 33" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/9006ec74-d415-4cae-aacb-0c3ea622cf69">

Event Management
The Event Actions tab is where you, as an analyst, will create all malware investigation correlations by providing descriptions and attributes associated with the investigation. Splitting the process into three significant phases, we have: 

- Event Creation.
- Populating events with attributes and attachments.
- Publishing.
We shall follow this process to create an event based on an investigation of Emotet Epoch 4 infection with Cobalt Strike and Spambot from malware-traffic-analysis.net. Follow along with the examples provided below.

Event Creation
In the beginning, events are a storage of general information about an incident or investigation. We add the description, time, and risk level deemed appropriate for the incident by clicking the Add Event button. Additionally, we specify the distribution level we would like our event to have on the MISP network and community. According to MISP, the following distribution options are available:

- Your organisation only: This only allows members of your organisation to see the event.
- This Community-only: Users that are part of your MISP community will be able to see the event. This includes your organisation, organisations on this MISP server and organisations running MISP servers that synchronise with this server.
- Connected communities: Users who are part of your MISP community will see the event, including all organisations on this MISP server, all organisations on MISP servers synchronising with this server, and the hosting organisations of servers that are two hops away from this one.
- All communities: This will share the event with all MISP communities, allowing the event to be freely propagated from one server to the next.
Additionally, MISP provides a means to add a sharing group, where an analyst can define a predefined list of organisations to share events.

Event details can also be populated by filling out predefined fields on a defined template, including adding attributes to the event. We can use the email details of the CobaltStrike investigation to populate details of our event. We will be using the Phishing E-mail category from the templates.

Attributes & Attachments
Attributes can be added manually or imported through other formats such as OpenIOC and ThreatConnect. To add them manually, click the Add Attribute and populate the form fields.

Some essential options to note are: 

- For Intrusion Detection System: This allows the attribute to be used as an IDS signature when exporting the NIDS data unless it overrides the permitted list. If not set, the attribute is considered contextual information and not used for automatic detection.
- Batch import: If there are several attributes of the same type to enter (such as a list of IP addresses, it is possible to join them all into the same value field, separated by a line break between each line. This will allow the system to create separate lines for each attribute.

The analyst can also add file attachments to the event. These may include malware, report files from external analysis or simply artefacts dropped by the malware. We have added the Cobalt Strike EXE binary file to our event in our example. You also have to check the Malware checkbox to mark the file as malware. This will ensure that it is zipped and passworded to protect users from accidentally downloading and executing the file.

Publish Event

Once the analysts have created events, the organisation admin will review and publish those events to add them to the pool of events. This will also share the events to the distribution channels set during the creation of the events.

# Questions
How many distribution options does MISP provide to share threat information?
There aree 4 distribution options provided by MISP.
<img width="1225" alt="Screenshot 2024-03-11 at 22 12 11" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/af42d0a3-cdde-4024-9a55-23c6f59819f8">

Which user has the role to publish events?
Organisation admin.
<img width="1324" alt="Screenshot 2024-03-11 at 22 13 59" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/ff946474-56f9-4177-9410-03cd48bdc266">

## Task 4
# Feeds
Feeds are resources that contain indicators that can be imported into MISP and provide attributed information about security events. These feeds provide analysts and organisations with continuously updated information on threats and adversaries and aid in their proactive defence against attacks.

MISP Feeds provide a way to:

- Exchange threat information.
- Preview events along with associated attributes and objects.
- Select and import events to your instance.
- Correlate attributes identified between events and feeds.
Feeds are enabled and managed by the Site Admin for the analysts to obtain information on events and indicators.

#Taxonomies
A taxonomy is a means of classifying information based on standard features or attributes. On MISP, taxonomies are used to categorise events, indicators and threat actors based on tags that identify them.

Analysts can use taxonomies to:

- Set events for further processing by external tools such as VirusTotal.
- Ensure events are classified appropriately before the Organisation Admin publishes them.
- Enrich intrusion detection systems' export values with tags that fit specific deployments.

Taxonomies are expressed in machine tags, which comprise three vital parts:

- Namespace: Defines the tag's property to be used.
- Predicate: Specifies the property attached to the data.
- Value: Numerical or text details to map the property.
<img width="862" alt="Screenshot 2024-03-11 at 22 21 47" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/8209dbed-079b-4457-b4c9-2fcbeae63f35">

# Tagging
Information from feeds and taxonomies, tags can be placed on events and attributes to identify them based on the indicators or threats identified correctly. Tagging allows for effective sharing of threat information between users, communities and other organisations using MISP to identify various threats.

In our CobaltStrike event example, we can add tags by clicking on the buttons in the Tags section and searching from the available options appropriate to the case. The buttons represent global tags and local tags, respectively. It is also important to note that you can add your unique tags to your MISP instance as an analyst or organisation that would allow you to ingest, navigate through and share information quickly within the organisation.

## Task 5
Scenario Event
CIRCL (Computer Incident Respons Center Luxembourg) published an event associated with PupyRAT infection. Your organisation is on alert for remote access trojans and malware in the wild, and you have been tasked to investigate this event and correlate the details with your SIEM. Use what you have learned from the room to identify the event and complete this task.

* What event ID has been assigned to the PupyRAT event?
To get the event ID of th pupyRAT, you navigate to the Event list page and locate the filter bar positioned above the Event list on the right side. Enter "PupyRat" in the designated field and proceed to click on "Filter."
<img width="661" alt="Screenshot 2024-03-13 at 20 42 27" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/72c9462d-c7d3-45c3-ac79-360bbb652180">
Upon loading the page, the answer can be found in the topmost column labeled "Event ID."
<img width="1440" alt="Screenshot 2024-03-13 at 20 58 18" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/49d960cf-fec8-4f66-aaa8-fa88a3b1000c">

* The event is associated with the adversary gaining ______ into organisations.
Based on the phrasing of the question, it seems we're in search of a specific kind of organizational access. Return to the PupyRAT MISP page and this time, pay close attention to the tags. Among these tags, you'll notice several references to a form of access termed as "Remote Access."
<img width="713" alt="Screenshot 2024-03-13 at 21 06 27" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/d124b62a-eceb-426b-94cc-3137000f93c2">

* What IP address has been mapped as the PupyRAT C2 Server.
Understanding that C2 represents a command and control server, we utilize the search box to search for the term "command" to streamline our search. Within this specific row, you will find an IP address, which is associated with the PupyRat command and control server. The IP address can be see on the left side of the row.
<img width="721" alt="Screenshot 2024-03-13 at 21 16 53" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/7a98e10f-5c11-4565-8e20-c423eeb3d918">

* From the Intrusion Set Galaxy, what attack group is known to use this form of attack?
Returning to the PupyRAT MISP page, the answer can be discovered within the tag section. Observing the first tag, it references both a galaxy and an intrusion set. By examining the tag's end, "Magic Hound" is revealed as the answer.
<img width="711" alt="Screenshot 2024-03-13 at 21 28 32" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/985080a0-50dc-4f5a-8adf-967349d348bc">

* There is a taxonomy tag set with a Certainty level of 50. Which one is it?
Revisiting the PupyRAT MISP page one last time, and focusing on the tags again. Seek out the blue tag located on the bottom row, which indicates certainty = "50". The term "OSINT" mentioned at the beginning is the solution to this query.
<img width="719" alt="Screenshot 2024-03-13 at 21 38 41" src="https://github.com/AlCybx/Threat-Intelligence/assets/161755166/201ebec6-5b8f-49f2-9eab-4f07f19771a0">





