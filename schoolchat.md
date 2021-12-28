# DIDComm and SSI using Aries Framework JavaScript on Node.js with Aries Mobile Agent React Native
## The goal of the project is to design a messaging application called "School Chat" that allows students who are considering applying to a school to chat with other students who currently attend that school so that they can ask questions and get information that might help them decide if they want to apply.

### Organizational Structure

- Multiple schools will participate in this program and all of the participating schools belong to an organization called "The School Group".
- The School Group is the authority for whether or not a school is a member of its organization.
- The School Group is also the authority for which students currently attend which schools in the organization.
- All of the colleges in The School Group are provided with an account that allows them to log in to The School Group administrative website and make changes to the profiles of students that attend their college.

### Entities Involved in this example scenario

>**The School Group**<br/>
>An organization consisting of a group of schools that all agree to operate under the same policies. The organization can add new schools at any time.
>
>**Popular College**<br/>
>A college that is a member of The School Group. A college can add new students at any time.
>
>**Alice**<br/>
>A student who is considering attending Popular College.
>
>**Bob**<br/>
>A student who currently attends Popular College.
>
>**Employee**<br/>
>An employee of Popular College with the ability to log in to The School Group administrative website and make changes to the profiles of students that attend Popular College.

## Desired real-world behavior
1. Alice is contemplating applying to Popular College.

2. While browsing the Popular College website on her mobile device she taps a link to download the "School Chat" app that was created by The School Group. This app will allow her to chat with students who currently attend Popular College (or any other school that is a member of The School Group).

3. Alice installs the School Chat app on her mobile device and then opens it for the first time.

4. The app shows Alice a list of all of the colleges that are members of The School Group.

5. Alice taps on Popular College.

6. The app shows Alice a list of students who attend Popular College that have also volunteered to answer questions from potential applicants like Alice.

7. Bob is one of the students at Popular College who has volunteered to answer questions and his name appears in the list.

8. Alice decides that she would like to chat with Bob and taps his name on the list.

9. A chat window appears for Alice with a message that says "Waiting for Bob..."

10. Bob receives a notification on his mobile device that Alice wants to chat with him.

11. Bob taps "Accept" on the chat notification.

12. A chat window appears for Bob with a message that says "Ready to chat with Alice."

13. The message on Alice's chat window changes to "Ready to chat with Bob."

14. Alice and Bob may now type messages that are sent back and forth between them.

## Privacy, security, and connectivity requirements

- These messages must not be able to be read by anyone but Alice or Bob, including the administrators of "School Chat" app and servers, members of The School Group, or other students.

 - If Alice makes her initial request to chat with Bob while he does not have the School Chat app open then he will receive the request to chat the next time he opens the School Chat app.

- If Alice or Bob sends a message while the other person does not have the School Chat app open then the other person will still receive the message later when they open the School Chat app.

- Bob needs to be issued a credential that proves that he is a student at Popular College. This credential is issued by The School Group.

- After both Alice and Bob's chat window show the message "Ready to chat with..." the School Chat app on Alice's mobile device needs to request proof from Bob that he is a student at Popular College.
- The School Chat app on Bob's mobile device needs to prove to Alice's School Chat app that he has been issued a credential by The School Group that proves that he is a student at Popular College.
- The School Chat app on Alice's device will verify the proof that Bob shares with her as having been issued by The School Group.
- After the School Chat app on Alice's device verifies that Bob's credential is valid then a "Verified Student at Popular College" badge appears under Bob's name in the chat window on Alice's School Chat app.

## Verification of Bob as a student of Popular College

1. When Bob first enrolled in Popular College through their official website he received an email at the end of the process asking him to verify his identity in person with an employee of Popular College.

2. Bob visited the registration office on the Popular College campus and showed his physical driver’s license to an employee of Popular College.

3. The employee first verified Bob’s identity using his driver’s license and then logged into The School Group’s administrative website using the Popular College account.

4. The employee used The School Group’s administrative website to update Bob’s profile in The School Group’s database to reflect that he was a verified student at Popular College.

5. After the employee verified Bob’s identity using his driver’s license and updated his profile they asked Bob if he would like to download the School Chat app and volunteer to answer questions from other potential students.

6. Bob agreed and downloaded the School Chat app on his mobile device.

7. The employee at Popular College then tapped on the “Invite Student To Answer Questions” button on Bob’s newly updated profile and a QR code appeared on the employee’s screen.

8. The employee at Popular College then presented Bob with the QR code to scan.

9. Bob scanned the QR code in his School Chat app and a connection with The School Group was established.

10. After the connection was established Bob immediately received a credential from The School Group that verifies that he is a student at Popular College.

11. That credential was stored in Bob’s School Chat app and can later be sent to Alice when her School Chat app requests proof that Bob is a student at Popular College.