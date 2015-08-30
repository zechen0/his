his: A command-line-based password management tool
==================================================

Uses a single master password to manage all your passwords.

Encrypted password data is stored locally.

Install
-------
```
pip install pycrypto && curl https://raw.githubusercontent.com/chenze/his/master/his -o /usr/bin/his
```

Command-line Options
---------------
- -d /path/to/datadir - default: ~/.his - optional
- -e terminal encoding - default: UTF-8 - optional


Examples
--------

```
# his
Type "help" for commands. Ctrl-D to exit
> help
* options: his -d ~/.his -e UTF-8
add            - Generate a password record
gen            - Generate a password without saving it
gen <n>        - Generate n-len password
gen <n> <luns> - l lowercase, u uppercase, n numbers, s special chars
g              - list groups
Ctrl-D         - exit
Type anything else to search

> add     
Please Enter Your New Master Password: 
Again: 
URL or Title: example.com
Username: chen
[g]enerate OR [e]nter: g
Your password for example.com is RzL8uviB4M6p
New Group Name: First Group
> 

> first
[0]First Group - example.com - chen / RzL8uviB4M6p
> exam
[0]First Group - example.com - chen / RzL8uviB4M6p

> g
[0]First Group
[1]Another Group

> gen
qdcTRMuh1egW
> gen 12 luns
8.VT<=6-zrdG
```
