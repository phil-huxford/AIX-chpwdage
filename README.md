# AIX-chpwdage


[![LinkedIn][linkedin-shield]][linkedin-url]




<!-- ABOUT THE PROJECT -->
## About The Project

This script is used to add a `ADMCHG` flag to users in the `/etc/security/passwd` file. This flag does not change a users password, but the user will be prompt to change their password next time they log in. This can apply to all users immediately, if there is a cybersecurity event for example, or you can specify a UNIX timestamp and any password that was changed before that timestamp will be flagged to be reset.

You can choose to exclude system users (if you maintain a list of them).


The `files` folder contains both the script and the man page.



### Built With

* ksh93 (KornShell) for AIX (UNIX).



### Prerequisites

If you wish to exclude system users, you must place a list of them somewhere on the system and add the path to the script (line 3) and preferably to the man page.

### Flags

This script will run as normal if it is run without any flags *unless* you maintain a list of system users. If you maintain a list of system users and do not specify a flag, you will be asked if you want to include them in the list of users to be flagged.

The `-h` flag will display the help file (the man page).

The `-i` flag is used to `include` system users in the list of users to be flagged. If you use this flag and do not have a list of system users, you will get the following error:
*"No system user list found, please see the man page."*

The `-e` flag is used to `exclude` system users from the list of users to be flagged. If you use this flag and do not have a list of system users, you will get the following error:
*"No system user list found, please see the man page."*



 
## Contact

Phil Huxford - [![LinkedIn][linkedin-shield]][linkedin-url]

Project Link: [https://github.com/phil-huxford/AIX-chpwdage](https://github.com/phil-huxford/AIX-chpwdage)


[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/in/phillip-huxford/
