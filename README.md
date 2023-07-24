# v4_project
Advent Hymnals Version 4 Project Management helpers

## Todo
- [ ] Migrating hymnals from csycms to v4.
- [ ] From github(.md) to .docx. to google docs
- [ ] From google docs back to .md
- [ ] New webapp
- [ ] New mobile app
- [ ] Add midi players
- [ ] Add mp3 players
- [ ] Add links to youtube videos
- [ ] Add sheet music viewers
- [ ] Add song comparisons


*Note:* These notes are to be put in the AH_v4 blog

For the automation we are going to use:
- colab
- google docs & sheets
- github actions

Rq:: mermaid illustration

## Creating the google workspace
We want to have access to google drive and some of the apps in its independent account. We want a means of creating the account without a phone number to keep our phones safe.
Creating workspace (without gmail) for free
https://workspace.google.com/essentials/ (from: https://www.reddit.com/r/gsuite/comments/d80f55/using_g_suite_without_gmail/
)

Create AH email
We want to create the email `adventhymnals@gospelsounders.org`
```bash
set +H # if the password as an exclamation mark
curl -s -X POST "https://mail.mailserver.example/admin/mail/users/add" -d "email=adventhymnals@gospelsounders.org" -d "****=" -u "admin@email:****"
```

Follow steps to Invite `adventhymnals@gospelsounders.org` to workspace created in step 1.

After `adventhymnals@gospelsounders.org` has joined google using the invite, remove the account from the google workspace so that it can be used to access colab. The free workspace accounts do not have access to colab. If successful, google account should be created without telephone verification.

## Structure of the drive
- private
- public
