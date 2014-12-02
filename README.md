diaspora-notifications-extractor
================================

Python script which log a user on a diaspora*'s pod, get the new notifications and put them in a JSON file.

# Use

To run the script you need to give 3 parameters : 

1. URL of the diaspora's POD
2. Login of the user
3. Password of the user
 
Example : 
```bash
$ python3 diaspora_get_notifs.py https://mondiaspora.net userLogin userPassword
```
With: 
- userLogin : the login used to log on the diaspora* pod
- userPassword : the password used to log on the diaspora* pod

It will create a file ```notifs.json``` containing the notifications such as : 
```json
[{"text": "Notification example.", "time": "2014-11-27T20:47:32Z"}]
```

If the script encounter a problem, the ```notifs.json``` file will contain something like : 
```json
{"error": "Error when trying to login : Invalid username or password."}
```

# Requirement

To run the script you need to have python3 installed on your system. Furthermore, the script use the library [lxml](http://lxml.de/) so you need to have it.

