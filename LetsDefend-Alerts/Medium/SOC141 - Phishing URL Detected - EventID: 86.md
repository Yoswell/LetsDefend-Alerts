<h1>🛡️ SOC141 - Phishing URL Detected</h1>
<h2>📅 Date and Time: March 22, 2021, 09:23 PM</h2>
<h2>⚠️ Priority: High</h2>

<h3>📜 Introduction</h3>
<h4>On March 22, 2021, at 09:23 PM, a high-priority alert (SOC141) was triggered on our security monitoring systems, indicating the detection of a potential phishing URL. Phishing attacks are a prevalent threat in the cybersecurity landscape, often aiming to steal sensitive information such as login credentials, personal data, or financial details by masquerading as a trustworthy entity. This writeup will delve into the specifics of the alert, detailing the steps taken to investigate the suspicious URL, the methodologies used to confirm its malicious intent, and the subsequent actions implemented to mitigate the threat. Understanding and documenting such incidents is crucial for refining our defense strategies and preventing similar occurrences in the future.</h4>

![image(2)](https://github.com/user-attachments/assets/d8ab829b-33d0-40fa-924c-263d62200d6f)

<h3>🌐 Step 1: URL Research </h3>
<h4>Procederemos a analizar la URL adjunta a la alerta utilizando herramientas en línea como VirusTotal. Este servicio permite escanear y evaluar URLs en busca de amenazas conocidas, consultando bases de datos de múltiples proveedores de seguridad. Al someter esta URL a análisis en VirusTotal, el resultado indica que cuatro proveedores de seguridad la han clasificado específicamente como "Phishing". Este hallazgo refuerza nuestra sospecha inicial de que la URL está asociada con actividades maliciosas diseñadas para engañar a los usuarios y obtener información confidencial. Además, este resultado subraya la necesidad de tomar medidas inmediatas para mitigar el riesgo asociado a este intento de phishing..</h4>

![image(3)](https://github.com/user-attachments/assets/7c4e44c6-7e8d-414f-aff6-3e60a38bc539)

<h3>🌐 Step 2: Analyze Domain</h3>
<h4>In this alert we have a domain, which is "mogagrocol.ru", but when analyzing it in Virus Total we are not informed about whether the domain is dangerous or malicious. Therefore we must perform a more exhaustive search of this alert, let's try with the "Hybrid Analysis" tool, once the domain is inserted for analysis, a large list will be returned, in which there is a specific one that matches the URL shown in the alert. Which is point 2, where %40 corresponds to an "@". If we click on this specific result, we will be shown another list, from which the domain "mogagrocol.ru" and the IP address "91.189.114.8" stand out, classified as malicious.</h4>

![image(6)](https://github.com/user-attachments/assets/5d18ed71-6324-4e83-91d5-f410dea5dfcd)
![image(7)](https://github.com/user-attachments/assets/5c332a0f-2d2b-4447-8e99-e2f978bdb928)

<h3>📋 Conclusion</h3>
<h4>1 - Analyze URL Address: After completing extensive research using multiple sources and analysis tools, we have concluded that both the requested URL and its associated domain are malicious.</h4>

<h4>2 - Has Anyone Accessed IP/URL/Domain?: From the beginning, the alert description indicates that the user Emily consulted the URL classified as malicious. Additionally, it was noted that the device action for that request was marked as "allowed", suggesting that access to the URL was not blocked by security measures in place. The endpoint must be placed in a containment state. In the "Add Artifacts" section, all relevant elements that we consider necessary for the investigation must be included. This includes: source ip address and destination ip address, requested URL and domain involved. Each artifact must be registered with its corresponding type, ensuring that all necessary information is documented for thorough analysis and to facilitate future mitigation actions. </h4>

<h4>3 - Close Alert: Since we have verified that this alert corresponds to a real phishing attempt, we must classify it as a true positive.</h4>
