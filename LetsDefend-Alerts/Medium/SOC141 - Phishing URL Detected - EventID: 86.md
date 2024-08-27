<h1>🛡️ SOC141 - Phishing URL Detected</h1>
<h2>📅 Date and Time: March 22, 2021, 09:23 PM</h2>
<h2>⚠️ Priority: High</h2>

<h3>📜 Introduction</h3>
<p>On March 22, 2021, at 09:23 PM, a high-priority alert (SOC141) was triggered on our security monitoring systems, indicating the detection of a potential phishing URL. Phishing attacks are a prevalent threat in the cybersecurity landscape, often aiming to steal sensitive information such as login credentials, personal data, or financial details by masquerading as a trustworthy entity. This writeup will delve into the specifics of the alert, detailing the steps taken to investigate the suspicious URL, the methodologies used to confirm its malicious intent, and the subsequent actions implemented to mitigate the threat. Understanding and documenting such incidents is crucial for refining our defense strategies and preventing similar occurrences in the future.</p>

![imagen](https://github.com/user-attachments/assets/e4a8331b-86e8-4c0a-828c-52137349de04)

<h3>🌐 Step 1: URL Research </h3>
<p><strong>Objective:</strong> Determine the nature of the URL that has been reported in the alert.<br><br>
<strong>1 - URL review in Reputation Services:</strong><br>
We will analyze the URL attached to the alert in online tools such as Virus Total. This tool, when analyzing this URL, will tell us that it is classified by 4 Security vendors as "Phishing".</p>

![2024-08-27_14-26](https://github.com/user-attachments/assets/42deb6f6-24b3-4920-bec2-6efaf030e50d)

<p><strong>2 - Domain Analysis:</strong><br>
In this alert we have a domain, which is "mogagrocol.ru", but when analyzing it in different tools they do not report anything about whether the domain is dangerous or malicious. Therefore we must perform a more exhaustive search for this alert.</p>

<p><strong>3 - Analyze the source of the alert:</strong><br>
We know that this alert comes from a user called "EmilyComp", with an IP assigned to her workstation "172.16.17.49", so let's start by going to the "Email Security" section and search for the name "Emily". This will return a result that we will click on. Once we click on this result, the email that Emily has received will open. Here we will find two things, a domain called "netflix-payments.com" and a URL "http://bit.ly/3ecXem52".</p>

![2024-08-27_14-45](https://github.com/user-attachments/assets/60985a3b-8ff2-413d-bfac-37f6916092c2)
![2024-08-27_14-51](https://github.com/user-attachments/assets/68b26068-4074-4426-8d98-6598674e5ca3)




True Positive (+5 Point)
Playbook Answers :
Has Anyone Accessed IP/URL/Domain? (+5 Point)
Analyze URL Address (+5 Point)
