---
id: zayan_fyp
aliases:
  - Zayan fyp
tags: []
---

# Zayan fyp

## introduction
a vault for medical reports

## problem background:
so that people could have access to their medical reports whenever and wherever they need it.

## sessions

### user session
    can edit his info

### doctore session
    guest sessiont (without login)

## features

### features for user:
1. when you login for the first time, the website asks you medical questions such as: (Blood type? , Any allergies?, chronic deases?, etc)
2. user can upload documents to use later.
3. download button on every document.
4. user can add a comment on the test to reference it later.
5. secure login (using hashing).
6. request help from admin.
7. send feedback report.

## features for admin:
1. manage users for unexpected situtaions, can deactivate/activate or delete user accounts if needed. 
2. read feedback reports

---
    info attached to the document:
    
    date:
        today by default. user can change
    
    document type: 
        liver test.
        diabetes test.
        full screaning.
        other: give the user the option to write.

why webapp instead of an app?
- Accessibility Across Devices
- Lower development cost.
- Platform Independence.
- No Storage Constraints.
- instant access on all devices, no need to install anything


technologies used:

frontend: React or NextJS
backend: nodeJS, ExpressJS,
database: MongoDB
