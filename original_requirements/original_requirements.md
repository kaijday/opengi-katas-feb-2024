# Terms of References (ToR) for developing an SSS Exam Management and Proctoring System
 
## Background
 
SSS GmbH (SSS), based in Germany, operates as an independent certification body, conducting approximately 30,000 exams annually across diverse fields such as IT and Software Industry, Healthcare, Project Management, and Marketing Management.

Our offerings include FLEX EXAMS, allowing individuals to take exams from the convenience of their homes based on their schedules. Candidates have the option to undergo training with our esteemed partners or pursue self-study for the exams. Additionally, we collaborate with Pearson VUE for Test Center Exams, providing candidates access to multiple-choice exams at any of the 5,200 Pearson test centers spanning over 175 countries.

Currently, our exam delivery system is managed through a third-party provider. While the system offers most of the required functionalities, we face challenges in terms of support. The existing provider lacks adequate responsiveness, leading to scheduled maintenance downtime of almost a day each month. Furthermore, we encounter instances where the system becomes temporarily unavailable, particularly during peak hours. The support response time is slower than desired, and the implementation of new features or improvements often experiences significant delays, sometimes stretching for months.

Given our commitment to delivering a seamless and reliable examination experience to our candidates, we are seeking a new solution that not only encompasses the necessary functionalities but also provides responsive and timely support, minimal downtime, and quicker implementation of updates. We are open to exploring proposals that align with our goals of enhancing the efficiency and reliability of our exam and proctoring system.

## Objective
The primary goal of this Terms of Reference (ToR) is for SSS to identify a supplier capable of implementing and delivering a comprehensive online exam management and proctoring system in accordance with SSS requirements. Our objective is to establish an in-house system that grants us the autonomy to maintain, develop, and enhance its functionalities. We aim to expand our business with opportunities for white labeling and ensure accessibility across all locations where our services are offered. The selected supplier should align with our vision for robust, scalable, and customizable solutions that will contribute to the growth and diversification of our business.

## Scope of the work
The overall purpose of the work described by the ToR hereinafter is to design, develop and deliver a fully operational online exam management and proctoring system. The new online exam management and proctoring system should be a cloud based exam software solution that completely supports the entire examining process through an easy to use user interface. The system should be able to provide secure examination via Lockdown Browser and Webcam Video Recording, exam management, questions type templates, time limits, progress bars, question library, certificates, email notifications & the ability to add logos, images, videos or audio. The system should be composed of two main modules: Exam Management Module and Online Proctoring Module.
 
## Management Module
The aim of the Management Module (Administration Module) is to administrate and manage the questions type templates, exam templates, email templates, users administration, maintain questions library, exam creation and scheduling, exam monitoring, certification templates and reporting. This Module should be integrated with an internal SSS Database System and with Online Proctoring Module. This module should be available and accessible only for specific users and from specific locations
 
### User Management
The system should enable dynamic management of roles as a group of permissions where certain data or features can be restricted for certain users. For examples, not all admin users can create questions or exams.
 
### Audit Trail
The audit trail will list the trail of all actions in the database with the following information: Action (created, edited, deleted), Title, Modified By, Modified On. The trail will be available for searching by each of the columns.
 
### Managing the exams
The Exam Management Module should enable preparation of custom exams with highly advanced settings like: Exams with multiple sections, time limitations, shuffling, random question selection, in-exam navigation restrictions, weighted scores, scores in multiple categories and dimensions and so on.
 
- Within managing the exams, we should be able to:
- Categorise the exams in different categories.
- Group questions in different sections;
- Define time limits for different sections, pages, questions, or the entire exam;
- Set the rules for the user to go back and forth during the exam separately for each section;
- Automatically randomize question or answer options;
- Choose questions from the existing questions library or add new;
- You can weigh the scores of exam questions;
- Define score milestones (pass/no pass) per exam or section;
- Exam Preview;
- Possibility for customization according to the Boards Requirements;
- Generating pin code for accessing the exam;
- Categorising the prepared exams in different stages (draft, review, live, off);
- Managing the start and end date of the exam;
- Adding online Proctoring or not;
- Managing the email templates that should be send when passing or not passing the exam.
 
### Managing the questions
Within managing the questions, we should be able to:

- Choose from different questions types including single answer, multiple answers, choice matrix questions, free format, picture choice;
- Add rich content such as pictures, audio and video to the questions;
- Each question in the exam may have its own score. For example, you can give 1 point to one question and 2 points to another question. Question points are used to calculate total exam - score or total section score;
- Partial Score -The person taking the exam may earn full, half or certain percentage of score according to the answers given to the question. For example, in a question where 2 of the 5 options are correct, if the participant selects only 1 correct option, then he/she can earn half point from that question;
- Negative Score - You can reduce the score (negative score) if the participant answers the questions in the exam incorrectly. For example, if a participant gives the correct answer to a question, he/she can earn 1 point but if he/she gives incorrect answer, then the participant may lose 0.25 points;
- Setting up the maximum and the minimum scores - In the case when the requirement is that if the overall score from the candidate is negative than the candidate is receiving 0 points, we should set up 0 as a minimum score;
- Easily upgrade when new question requirements should be fulfilled - The system should be established in the way to make it possible easily to be upgraded in the case that new requirements should be fulfilled for example need for filling in the blanks, code snippets or code execution or different logic in calculating the overall score of the question.
 
## Online Proctoring Module
The aim of the Online Proctoring Module is to make modern, easy, secure and quality proctoring of candidates during the exam. It should be developed one interface for the candidates and one interface for the proctor.
 
### Participant Registration
To registrate the participant in the system, the proctoring system should be integrated with our internal client management software to make sure that the participant is registered and able to take the exam.
 
### Identity Verification during the exam
Once the user is registered and logged in the system to start the exam, he will need to be identified. Appropriate protocol should be established, through which the user will go through. 
- **ID documents:** Appropriate document for identification should be photographed or scanned from the system.
- **Video Recording:** Video of the candidate is recorded during the exam with candidate’s camera and microphone. Video recordings record both image and sound. These records can be watched live or at the end of the exam.
- **Photographing:** Candidates can be photographed periodically during the exam. These photos can be viewed live or at the end of the exam.

Videos and Photos should be automatically delete after 3 months.
 
Following things should be possible during the exam:
- Webcam proctoring
- Live monitoring
- Lockdown browser
- Multiple timers
- Event logs
 
### Functionality Verification during the exam
Following functionalities should be checked before starting the exam:
- Camera Functionality
- Microphone Functionality
- Connection with the appropriate Mobile application for Proctoring
 
### Mobile Proctoring application
Developing an Android and iOS mobile proctoring application should establish possibility to connect the mobile phone from the candidate and use the camera from the candidate as an additional security during the exam.
 
### Conducting the exam
Once the exam starts, the system should guarantee that the participant couldn’t change the exam content or manipulate the answers. The answers should be recorded and stored in real time. The participant should be able to review the answers at any time, and should easily navigate to the non-answered questions, or mark the questions that want to come back on. The exams should be live followed: who can start the exam, who is on which section and page, who answered how many questions.
 
Proctor could select between video recording and photo shooting as a surveillance method and see current videos and photos of the candidates that want to see and watch them instantly.
 
Chat support between the proctor and the candidates should be also implemented.  
 
When the exam is finished by the participant or the time passed, the assessment has to be automatic. Final score should be shown on the screen and automatic email with the results should be sent to the candidate.
 
### 3rd party Integrations
The system should be integrated with the Internal Management System, JIRA Support System and Salesforce. 
 
## Non-functional requirements

### Usability
- **Localization** - The system should be easily localized in multiple languages, the interface and the content. The testing should be performed on at least 2 languages (English and German).
- **User Experience** - An effort must be made for the user interface to be intuitive, easy to use and to administer. The users should not need any extensive IT experience to use the application. They should only require web browser. The web application must comply with W3C standards, function and appear identical with the latest versions of all major browsers: Chrome, Mozilla, Safari, Edge. The system should be supported for work only on PC and Tablet.
- **Branding** - The look and feel of the system should be customized according to SSS brand guidelines. For the SSS as a Service the branding should be customized according to Customer's brand guidelines.
- **Responsiveness** - ideally page load time should be under 2 seconds. Page load time up to 5seconds will be considered acceptable.
 
### Performance metrics
The system should be based on scalable architecture where large increase of load should be handled only by manipulation of infrastructure parameters without additional investments in the solution offered.

The system should support at any time up to 1000 consecutive users. 

The system should have near zero downtime.
 
### Modularity, adaptability, and extensibility
The system should be based on modular architecture enabling easy future upgrading of various parts of the system with minimal investment.
 
### Security Requirements
The system access should be restricted and available only for authenticated and authorized users. The permissions within the system should be controlled by a user-defined role. It should provide confidentiality and data integrity.
 
### GDPR
The system should be fully compliant with GDPR. 
  
### Support & Maintenance
Support for SSS from the supplier should be on 1st level and available 24/7. Supporting the SSS customers should be 24/7. Whether the SSS or the supplier should be the first level support for the customer should be decide later on. Nevertheless, we would like the supplier to include in the offer 1st level support (24/7) for SSS customers from the side of supplier 

Service level agreement (SLA), should be signed between SSS and the supplier. 
