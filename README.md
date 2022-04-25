# CS-305 Software Security
## SNHU CS-305 Software Security Final Project

### Briefly summarize your client, Artemis Financial, and their software requirements. Who was the client? What issue did they want you to address?
Artemis Financial is upgrading their customer experience by providing a web interface for them to access their bank information. In order to provide that service to the customer, it is imperative that the system be secure and robust against attacks. The client wanted me to address security vulnerabilities in the third-party libraries being used, as well as review the code that has already been written to ensure it was written with security in mind, updating it as needed, and also to implement encryption for data (in a limited sense) using an appropriate encryption algorithm.

### What did you do particularly well in identifying their software security vulnerabilities? Why is it important to code securely? What value does software security add to a company’s overall wellbeing?
I did not do anything particularly impressive in this project. Updating the Spring Boot version to the latest fixed all of the critical and high impact vulnerabilities of the system, and most everything else was spoon-fed. Maybe some of the research I did regarding encryption could be interesting, but hardly impressive to a software security professional.

### What about the process of working through the vulnerability assessment did you find challenging or helpful?
The most challenging thing was to suppress "false positives" in the report. By the time I silenced all of the vulnerabilities in the report, the file I had to silence vulnerabilities was longer than the rest of the code for the entire project. I'm not sure why it seemed that I had to silence the same things over and over, but they were still in the report, so I kept silencing things, and eventually got rid of all the warnings. Obviously in real life, not all of those are false positives, so perhaps this is just because it's a good idea to have the suppression be extremely specific so you don't accidentally silence a warning about a vulnerability that gets exploited against you.

### How did you approach the need to increase layers of security? What techniques or strategies would you use in the future to assess vulnerabilities and determine mitigation techniques?
My number one feedback for the hypothetical client was to implement an authorization service and add role based authorization to the controllers, overriding them as needed on specific endpoints. Once a base level of authorization is in place, then they have the opportunity to decide if they want to get fancy by adding attribute based authorization or not.

### How did you ensure the code and software application were functional and secure? After refactoring code, how did you check to see whether you introduced new vulnerabilities?
I applied a heuristic approach to determining if the application was functional and secure. Unfortunately, my experience in this area is quite limited, so my heuristic model is suspect. As far as functionality, that was simple to test by running the application and making sure that the expected functionality was reflected in the actual functionality. I used the same tool to recheck the solution for vulnerabilities as before refactoring - the dependency-check package.

### What resources, tools, or coding practices did you employ that you might find helpful in future assignments or tasks?
Having an assignment in Java each week helped me become more familiar with Java, Spring, Maven, and Eclipse. The team I am on for my day job has 2 Java projects that we are responsible for in addition to the bulk of our work in C#/.NET. One of my coworkers has Java with Maven running in Visual Studio Code, so the next time I have a project to do in Java, I am going to try doing it there instead of Eclipse.

### Employers sometimes ask for examples of work that you have successfully completed to demonstrate your skills, knowledge, and experience. What from this particular assignment might you want to showcase to a future employer?
There is some interesting information about the history of encryption in my report to Artemis Financial if they are curious about that. Otherwise I would not direct a future employer to this repository.
