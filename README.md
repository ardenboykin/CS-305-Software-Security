# CS-305-Software-Security

### Briefly summarize your client, Artemis Financial, and its software requirements. Who was the client? What issue did the company want you to address?

Artemis Financial is a consulting company that develops individualized financial plans for its customers. The financial plans include savings, retirement, investments, and insurance. They wanted a filed verification step to be added to their web application to ensure secure communications and wanted this data verification in the form of a checksum. My goal was to take their existing software application and add the secure communication mechanism they were requesting. 

### What did you do well when you found your client’s software security vulnerabilities? Why is it important to code securely? What value does software security add to a company’s overall well-being?

I did well in utilizing static testing tools such as the OWASP dependency check to scan the codebase, which helped identify vulnerabilities and potential attack vectors. Coding securely is crucial to software development and security as it is extremely easy to exploit applications that have not been carefully made. A company that does not priorities the safety of their users will find themselves not only not well regarded, but most likely under legal fire, especially if they are a financial company like Artemis. The protection of users' data, especially personal and financial data, is of the utmost importance, as they are high targets for malicious actors.  

### Which part of the vulnerability assessment was challenging or helpful to you?

Learning about suppression and false positives was very helpful. As the codebase we were given to refactor was using several outdated libraries that we were not supposed to update, it initially looks as if the project is a security disaster waiting to happen. After using the dependency check and manually reviewing the vulnerabilities however, it proved that none of the methods actually being used in the project were actually risk factors.

### How did you increase layers of security? In the future, what would you use to assess vulnerabilities and decide which mitigation techniques to use?

Adding the cryptographic hash function SHA-256 to create the CheckSum, ensuring the data converted in the process was encoded with StandardCharsets.UTF_8 to prevent a silent fail if a platform used a different default encoding when running the application, and ensuring errors were handled appropriately with a custom message were all steps taken to increase the security of the application. In the future, I would use the OWASP dependency check due to it's large database to scan for vulnerabilities to ensure the project is not posing a risk to the company nor the users. I also will follow the Oracle Java Security Guidelines, as well as the OWASP Secure Coding Practices to build with security in mind from the beginning of the project. 

### How did you make certain the code and software application were functional and secure? After refactoring the code, how did you check to see whether you introduced new vulnerabilities?

By testing and running the application in Eclipse, I was able to make sure the application was functional. After refactoring, I ran the project through another dependency check to make sure the number of vulnerabilities detected had not increased. 

### What resources, tools, or coding practices did you use that might be helpful in future assignments or tasks?

The OWASP dependency check, the keytool extension in Eclipse to ensure HTTPS connections, and the Oracle and OWASP guidelines on security and secure coding practices were extremely helpful resources that I will utilize in the future. 

### Employers sometimes ask for examples of work that you have successfully completed to show your skills, knowledge, and experience. What might you show future employers from this assignment?

From the two projects uploaded to this repository, the Artemis Financial Vulnerability Assessment Report and the Artemis Financial Practices for Secure Software Report, I would be able to show my knowledge of security tools such as the OWASP dependency check and protocols like SSL security. I would also be able to demonstrate my capabilities of analyzing codebases and identifying vulnerabilities, as well as my knowledge of implementing hashing algorithms and ciphers. 
