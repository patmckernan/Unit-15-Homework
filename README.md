## Unit 15 Submission File: Web Vulnerabilities and Hardening


### Part 1: Q&A

#### The URL Cruise Missile

The URL is the gateway to the web, providing the user with unrestricted access to all available online resources. In the wrong hands can be used as a weapon to launch attacks.

Use the graphic below to answer the following questions:

| Protocol         | Host Name                 | Path                   | Parameters               |
| ---------------- | :-----------------------: | ---------------------- | ------------------------ |
| **http://**      | **`www.buyitnow.tv`**     | **/add.asp**           | **?item=price#1999**     |


1. Which part of the URL can be manipulated by an attacker to exploit a vulnerable back-end database system? 

Answer: The parameter can be manipulated by an attacker to exploit a vulnerable back-end database system.

2. Which part of the URL can be manipulated by an attacker to cause a vulnerable web server to dump the `/etc/passwd` file? Also, name the attack used to exploit this vulnerability.

Answer: The path can be manipulated by an attacker to gain access to the /etc/passwd. The name of this attack is called Path Traversal.
   
3. Name three threat agents that can pose a risk to your organization.

Answer: Organized cybercriminals, hacktivits, insiders.

4. What kinds of sources can act as an attack vector for injection attacks?

Answer: Social engineering, web pages, email servers. 

5. Injection attacks exploit which part of the CIA triad?

Answer: Confidentialtiy, integrity, and authenticity. 

6. Which two mitigation methods can be used to thwart injection attacks?\

Answer: Input sanitization, and input validation can thwart injection attacks. 

____

#### Web Server Infrastructure

Web application infrastructure includes  sub-components and external applications that provide  efficiency, scalability, reliability, robustness, and most critically, security.

- The same advancements made in web applications that provide users these conveniences are the same components that criminal hackers use to exploit them. Prudent security administrators need to be aware of how to harden such systems.


Use the graphic below to answer the following questions:

| Stage 1        | Stage 2             | Stage 3                 | Stage 4              | Stage 5          |
| :------------: | :-----------------: | :---------------------: | :------------------: | :--------------: |
| **Client**     | **Firewall**        | **Web Server**          | **Web Application**  | **Database**     |
   
   
1. What stage is the most inner part of the web architecture where data such as, customer names, addresses, account numbers, and credit card info, is stored?

Answer: The inner most part of web architecture where the data is stored is stage 5: Database.

2. Which stage includes online forms, word processors, shopping carts, video and photo editing, spreadsheets, file scanning, file conversion, and email programs such as Gmail, Yahoo and AOL.

Answer: The stage that includes online forms, word processors, shopping carts, video and photo editing, spreadsheets, file scanning, file conversion, and email programs such as Gmail, Yahoo and AOL is stage 4: web application. 

3. What stage is the component that stores files (e.g. HTML documents, images, CSS stylesheets, and JavaScript files) that's connected to the Internet and provides support for physical data interactions between other devices connected to the web?

Answer: The stage of web server architecture that stores files such HTML documents, images, CSS stylesheets, and Javascript files is stage 3: web server. 

4. What stage is where the end user interacts with the World Wide Web through the use of a web browser?

Answer: The client side of the architecture is Stage 1: Client. 

5. Which stage is designed to prevent unauthorized access to and from protected web server resources?

Answer: The starge that is desinged to prevent unauthorized access is stage 2: Firewall. 

----


#### Server Side Attacks

In today’s globally connected cyber community, network and OS level attacks are well defended through the proper deployment of technical security controls such as, firewalls, IDS, Data Loss Prevention, EndPoint and security. However, web servers are accessible from anywhere on the web, making them vulnerable to attack.

1. What is the process called that cleans and scrubs user input in order to prevent it from exploiting security holes by proactively modifying user input.

Answer: The process that cleans and scrubs user input to prevent the exploition of security holes is input sanitization. 

2. Name the process that tests user and application-supplied input. The process is designed to prevent malformed data from entering a data information system by verifying user input meets a specific set of criteria (i.e. a string that does not contain standalone single quotation marks).

Answer: The process that tests user and application-supplied input is input validation. 

3. **Secure SDLC** is the process of ensuring security is built into web applications throughout the entire software development life cycle. Name three reasons why organization might fail at producing secure web applications.

Answer: Three reasons why organizations might fail at producing secure web applications would be lack of policy enoforcement, insecure log in forms, and insecure logout management.

4. How might an attacker exploit the `robots.txt` file on a web server?

Answer: An attacker could use a malware bot in order to find the data in the robots.txt file which contains private information that is being hidden. 

5. What steps can an organization take to obscure or obfuscate their contact information on domain registry web sites?

Answer: A company could use proxy information to obscure their contact information on domain registry. 
  
6. True or False: As a network defender, `Client-Side` validation is preferred over `Server-Side` validation because it's easier to defend against attacks.

   - Explain why you chose the answer that you did.

Answer: False, you would want both client-side and server-side to have validation. Server-side is easier to mitigate than client-side attacks. 

____

#### Web Application Firewalls

WAFs are designed to defend against different types of HTTP attacks and various query types such as SQLi and XSS.

WAFs are typically present on web sites that use strict transport security mechanisms such as online banking or e-commerce websites.

1. Which layer of the OSI model do WAFs operate at?

Answer: WAF's operate at layer 7: application of the OSI model. 

2. A WAF helps protect web applications by filtering and monitoring what?

Answer: WAF helps protect web applications by monitoring and filtering HTTP traffic. 

3. True or False: A WAF based on the negative security model (Blacklisting) protects against known attacks, and a WAF based on the positive security model (Whitelisting) allows pre-approved traffic to pass.

Answer: True
____

#### Authentication and Access Controls

Security enhancements designed to require users to present two or more pieces of evidence or credentials when logging into an account is called multi-factor authentication.

- Legislation and regulations such as The Payment Card Industry (PCI) Data Security Standard requires the use of MFAs for all network access to a Card Data Environment (CDE).

- Security administrators should have a comprehensive understanding of the basic underlying principles of how MFA works.

1. Define all four factors of multifactor authentication and give examples of each:

   - Factor 1: Knowledge factor. An example of this would be a login input such as a password, or PIN.

   
   - Factor 2: Possession factor. An example of possession factor would be a software token, or smart card.
   
   
   - Factor 3: Inherent factor. An example of an inherent factor would be biometric identification. (finger pring/retina scan)

   
   - Factor 4: Location factor. An example of a location factor would be GPS detection, or a callback to a phone number. 

   
2. True or False: A password and pin is an example of 2-factor authentication.

Answer: False
   
3. True or False: A password and `google authenticator app` is an example of 2-factor authentication.

Answer: True
   
4. What is a constrained user interface? 

Answer: A constrained user interface is a security practice that will limit the user access to sensitive information, and the use of programs based on permissions. 

----
____

### Part 2: The Challenge 

In this activity, you will assume the role of a pen tester hired by a bank to test the security of the bank’s authentication scheme, sensitive financial data, and website interface.


#### Lab Environment   

We'll use the **Web Vulns** lab environment. To access it: 
  - Log in to the Azure Classroom Labs dashboard. 
  - Find the card with the title **Web Vulns** or **Web Vulnerability and Hardening**.
  - Click the monitor icon in the bottom-right. 
  - Select **Connect with RDP**.
  - Use Credentials (azadmin:p4ssw0rd*)

- The lab should already be started, so you should be able to connect immediately. 

- Refer to the [lab setup instructions](https://cyberxsecurity.gitlab.io/documentation/using-classroom-labs/post/2019-01-09-first-access/) for details on setting up the RDP connection.

Once the lab environment is running, open the HyperV manager and make sure that the OWASPBWA and Kali box is running.

- Then, login to the Kali VM and navigate to the IP address of the OWASPBWA machine.

- Click the option for 'WebGoat' and start the WebGoat app.

- Use the credentials: `guest`:`guest`

On the bottom of the left side of the screen, click on `Challenge` and then choose `The Challenge`.

**Note:** A common issue with this lab is the Challange activity failing to start successfully. Hit the `Restart the Lesson` button in the top right if you get an error starting the activity.

### The Challenge Instructions

#### Challenge #1

Your first mission is to break the authentication scheme. There are a number of ways to accomplish this task.

 ![Hidden Java Script username and password](https://github.com/patmckernan/Unit-15-Homework/blob/main/images/Hidden%20java%20script%20user%20name%20and%20password.png)


After completing the first challenge, you will be provided with an option to continue to the next challenge.

#### Challenge #2

Next, steal all of the credit card numbers from the database. 

![All user CC information](https://github.com/patmckernan/Unit-15-Homework/blob/main/images/All%20user%20CC%20information.png)
 

After completing the second challenge, you will be provided with an option to continue to the next challenge.


#### Challenge #3

Your final act is to deface the website using command injection. Follow the walkthrough below to help you get started. 

- After completing the second challenge, you will be provided with an option to continue to the next challenge.
  

- Now that we know where the webpage is, your task will be to deface the website. Keep in mind the following:
  * Use **WebScarab** to perform command injection.
  * When performing command injection, you will need to select a field that WebScarab can return commands to. These fields are typically located in a drop down. 
  * You will also need to locate and edit the the webpage's source code: `webgoat_challenge_guest.jsp`
  * Your final command will:
    * Change to the location of the `webgoat_challenge_guest.jsp` file.
    * **and** echo `You've been hacked by...` followed by your name, to the `webgoat_challenge_guest.jsp` file.

![Website Defaced](https://github.com/patmckernan/Unit-15-Homework/blob/main/images/Website%20defaced.png)

![Website Defaced-1](https://github.com/patmckernan/Unit-15-Homework/blob/main/images/Website%20defaced-1.png)


---
© 2020 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.  
