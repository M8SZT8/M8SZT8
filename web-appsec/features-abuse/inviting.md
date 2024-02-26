# Inviting

* [ ] Failure to invalidate token
  1. Generate an invitation link and send it to your secondary account to join the team.
  2. Accept the invitation.
  3. Remove the secondary user from the team.
  4. Try to rejoin the organization using the same invitation link, and prepare to be amazed!
* [ ] Admin Invitation 1- Admin need to put password to deactive 2FA\
  2- Admin can invite another admin\
  3- Second admin can deactive 2FA for first admin without password
* [ ] IDOR 1- Admin invite user with specific email\
  2- User open message in email to complete registertion\
  3- After finish user intercept request before submit\
  4- Change email at email parameter\
  5- Email changed Successfully
* [ ] API Misconfiguration Leads to PrevEsc 1- Admin invite user\
  2- User login\
  3- In user login request there's parameter called role:"user"\
  4- Use match & replace to changed it to role:"admin"\
  5- Login with user, it's logout me directly\
  6- But i see all informtion with burp via api endpoints
* [ ] signup without accept invitation
  1. Send invite to [test@example.com](mailto:test@example.com)
  2. Disregard Invite, directly signup.
  3. [test@example.com](mailto:test@example.com) becomes part of the organisation.
  4. Victim organisation dashboard still shows that [test@example.com](mailto:test@example.com) hasn’t accepted the invitation sent to email.
  5. But in real time [test@example.com](mailto:test@example.com) remains part of the organisation anonymously.
* [ ] Logic Error Leads to Project Takeover
  1. User invite attacker to the project as member
  2. Attacker changes his name with bad chracters like html tags and %00 and other latina chars
  3. Victim tries to remove attacker from the team but he faces errors and the request doesn't occure