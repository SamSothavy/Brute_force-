# Brute Force

## Objective

The objective of this lab is to understand how brute-force attacks are conducted against authentication mechanisms and to evaluate the effectiveness of password security controls. The exercise demonstrates the process of identifying login services, testing credential security, and assessing the risks associated with weak passwords in a controlled environment.

## Skills Learned

- Authentication service enumeration
- Understanding brute-force attack methodologies
- Password security assessment
- Credential testing and validation
- Identifying weak password policies
- Analyzing authentication responses
- Assessing the impact of weak credentials
- Understanding account lockout and rate-limiting controls
- Documenting security findings and remediation recommendations

## Tools Used

- Hydra
- Nmap
- Nikto
- Gobuster
- zbar
- Kali Linux Terminal
- Burp Suite (for web authentication analysis)

## Step

Please clone this lab from the following Git repository:
bash
```
https://github.com/SamSothavy/Brute_force-lab.git
```

Use **Nmap** to scan the target system and identify the open ports and exposed services.

<img width="1706" height="949" alt="Screenshot 2026-06-30 154309" src="https://github.com/user-attachments/assets/5a92d308-bb95-454b-a866-81e10b84fa36" />

The Nmap scan identified multiple open ports on the target system. For the purposes of this lab, the assessment focuses on **port 80 (HTTP)**, where the web application is hosted.

<img width="1706" height="696" alt="Screenshot 2026-06-30 154600" src="https://github.com/user-attachments/assets/31dc433d-edfb-4bf2-aba3-6ecaaebdd4d8" />

<img width="1717" height="907" alt="Screenshot 2026-06-30 154653" src="https://github.com/user-attachments/assets/c91a1fbd-e8b9-4103-b2df-628c4683082f" />

We then use **Nikto** to perform a web vulnerability scan and identify potential security issues on the target server.

<img width="1713" height="787" alt="Screenshot 2026-06-30 155750" src="https://github.com/user-attachments/assets/502acfad-03c3-46a6-bfcf-b7652b700809" />

<img width="1713" height="927" alt="Screenshot 2026-06-30 155928" src="https://github.com/user-attachments/assets/010aff50-cd7f-43d5-84f6-569fdfedacff" />

Next, we use **Hydra** to perform a brute-force attack 

**Note:** Before brute-force testing, identify the request method, required parameters, and the server’s error responses (e.g., “Invalid credentials”).

<img width="1912" height="983" alt="Screenshot 2026-06-30 171814" src="https://github.com/user-attachments/assets/b255a11f-5b5d-4d9a-92cd-1c39dd0db72a" />

<img width="1707" height="524" alt="Screenshot 2026-06-30 172453" src="https://github.com/user-attachments/assets/76ff7d0b-5764-4a23-b206-c07d4aa4cbb5" />

**Note:** Avoid brute-forcing both the username and password at the same time, as it can be very time-consuming. If possible, obtain either a valid username or a valid password first to make the testing process more efficient.

<img width="1713" height="933" alt="Screenshot 2026-06-30 172548" src="https://github.com/user-attachments/assets/ba6ec6ea-b494-4b36-9fae-e9992ad7ddc3" />

<img width="1708" height="775" alt="Screenshot 2026-06-30 172609" src="https://github.com/user-attachments/assets/05ef7f5c-62ff-40a8-9f1c-9bb451b774ea" />




