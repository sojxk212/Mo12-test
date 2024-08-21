# Mo12-test
# 967778239092
# import requests
from random import randrange,choice
from time import sleep
import os
try:
    from fake_email import Email
except:
    os.system('pip install fake_email')
    from fake_email import Email
acc1=0
os.system('cls' if os.name == 'nt' else 'clear')
ID=input('Enter Your ID : ')
os.system('cls' if os.name == 'nt' else 'clear')
token=input('Enter Your Token : ')
os.system('cls' if os.name == 'nt' else 'clear')
def acc():
    global acc1
    try:
        year=str(randrange(1997,2008))
        day=str(randrange(1,28))
        month=str(randrange(1,12))
        name=''.join(choice('azertyuiopmlkjhgfdsqwxcvbn')for i in range(randrange(3,7)))+' '+''.join(choice('azertyuiopmlkjhgfdsqwxcvbn')for i in range(randrange(2,5)))
        username=''.join(choice('azertyuiopmlkjhgfdsqwxcvbn1234567890_.')for i in range(randrange(9,15)))
        mail=Email().Mail()
        email=mail['mail']
        def q():
            try:
                headers = {
    'accept': 'text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.7',
    'accept-language': 'en-US,en;q=0.9',
    'cache-control': 'max-age=0',
    'dnt': '1',
    'dpr': '0.8',
    'priority': 'u=0, i',
    'sec-ch-prefers-color-scheme': 'dark',
    'sec-ch-ua': '"Chromium";v="124", "Microsoft Edge";v="124", "Not-A.Brand";v="99"',
    'sec-ch-ua-full-version-list': '"Chromium";v="124.0.6367.118", "Microsoft Edge";v="124.0.2478.80", "Not-A.Brand";v="99.0.0.0"',
    'sec-ch-ua-mobile': '?0',
    'sec-ch-ua-model': '""',
    'sec-ch-ua-platform': '"Windows"',
    'sec-ch-ua-platform-version': '"10.0.0"',
    'sec-fetch-dest': 'document',
    'sec-fetch-mode': 'navigate',
    'sec-fetch-site': 'same-origin',
    'sec-fetch-user': '?1',
    'upgrade-insecure-requests': '1',
    'user-agent': 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/124.0.0.0 Safari/537.36 Edg/124.0.0.0',
    'viewport-width': '914',
}
                response = requests.get('https://www.instagram.com/accounts/emailsignup/', headers=headers)
                csrftoken=response.cookies.get_dict()['csrftoken']
                client_id=response.text.split('"machine_id":"')[1].split('"')[0]
                return csrftoken,client_id
            except:
                print('error get csrftoken and client_id')
                q()
        for i in range(999999):
            try:
                csrftoken,client_id=q()
                break
            except:''
        os.system('cls' if os.name == 'nt' else 'clear')
        print(f'''
email : {email}
username : {username}
name : {name}
csrftoken : {csrftoken}
client_id : {client_id}
number accounts : {str(acc1)}
''')
        print('')
        sleep(0.5)
        cookies = {
    'csrftoken': csrftoken,
}
        headers = {
    'accept': '*/*',
    'accept-language': 'en-US,en;q=0.9',
    'content-type': 'application/x-www-form-urlencoded',
    'dnt': '1',
    'origin': 'https://www.instagram.com',
    'priority': 'u=1, i',
    'referer': 'https://www.instagram.com/accounts/emailsignup/',
    'sec-ch-prefers-color-scheme': 'dark',
    'sec-fetch-dest': 'empty',
    'sec-fetch-mode': 'cors',
    'sec-fetch-site': 'same-origin',
    'user-agent': 'Mozilla/5.0 (iPhone; CPU iPhone OS 16_6 like Mac OS X) AppleWebKit/605.1.15 (KHTML, like Gecko) Version/16.6 Mobile/15E148 Safari/604.1 Edg/124.0.0.0',
    'x-asbd-id': '129477',
    'x-csrftoken': csrftoken,
    'x-ig-app-id': '936619743392459',
    'x-ig-www-claim': '0',
    'x-instagram-ajax': '1013449353',
    'x-requested-with': 'XMLHttpRequest',
}
        data = {
    'enc_password': '#PWD_INSTAGRAM_BROWSER:10:1715438070:AUpQAM+Apdtte/OpskJiLcYuBE9XZv/6singMGa8xpUhxj8kmX19qpmerT8s2o+sacfGaSeBCNq5rTV97Bz4JqoJrVgLgfiJFmq6NZ0aih5skSEIWXaPr8HFJ5Ilf/jVFRhYnWJqJWPJixACCA==',
    'email': email,
    'first_name': name,
    'username': username,
    'client_id': client_id,
    'seamless_login_enabled': '1',
    'opt_into_one_tap': 'false',
}
        response = requests.post(
    'https://www.instagram.com/api/v1/web/accounts/web_create_ajax/attempt/',
    cookies=cookies,
    headers=headers,
    data=data,
)
        sleep(0.5)
        cookies = {
    'csrftoken': csrftoken,
}
        headers = {
    'accept': '*/*',
    'accept-language': 'en-US,en;q=0.9',
    'content-type': 'application/x-www-form-urlencoded',
    'dnt': '1',
    'origin': 'https://www.instagram.com',
    'priority': 'u=1, i',
    'referer': 'https://www.instagram.com/accounts/emailsignup/',
    'sec-ch-prefers-color-scheme': 'dark',
    'sec-fetch-dest': 'empty',
    'sec-fetch-mode': 'cors',
    'sec-fetch-site': 'same-origin',
    'user-agent': 'Mozilla/5.0 (iPhone; CPU iPhone OS 16_6 like Mac OS X) AppleWebKit/605.1.15 (KHTML, like Gecko) Version/16.6 Mobile/15E148 Safari/604.1 Edg/124.0.0.0',
    'x-asbd-id': '129477',
    'x-csrftoken': csrftoken,
    'x-ig-app-id': '936619743392459',
    'x-ig-www-claim': '0',
    'x-instagram-ajax': '1013449353',
    'x-requested-with': 'XMLHttpRequest',
}
        data = {
    'day': day,
    'month': month,
    'year': year,
}
        sleep(0.5)
        response = requests.post(
    'https://www.instagram.com/api/v1/web/consent/check_age_eligibility/',
    cookies=cookies,
    headers=headers,
    data=data,
)
        cookies = {
    'csrftoken': csrftoken,
}
        headers = {
    'accept': '*/*',
    'accept-language': 'en-US,en;q=0.9',
    'content-type': 'application/x-www-form-urlencoded',
    'dnt': '1',
    'origin': 'https://www.instagram.com',
    'priority': 'u=1, i',
    'referer': 'https://www.instagram.com/accounts/emailsignup/',
    'sec-ch-prefers-color-scheme': 'dark',
    'sec-fetch-dest': 'empty',
    'sec-fetch-mode': 'cors',
    'sec-fetch-site': 'same-origin',
    'user-agent': 'Mozilla/5.0 (iPhone; CPU iPhone OS 16_6 like Mac OS X) AppleWebKit/605.1.15 (KHTML, like Gecko) Version/16.6 Mobile/15E148 Safari/604.1 Edg/124.0.0.0',
    'x-asbd-id': '129477',
    'x-csrftoken': csrftoken,
    'x-ig-app-id': '936619743392459',
    'x-ig-www-claim': '0',
    'x-instagram-ajax': '1013449353',
    'x-requested-with': 'XMLHttpRequest',
}
        data = {
    'device_id': client_id,
    'email': email,
}
        response = requests.post(
    'https://www.instagram.com/api/v1/accounts/send_verify_email/',
    cookies=cookies,
    headers=headers,
    data=data,
)
        if '"email_sent":true' in response.text:
            print('done send code')
        else:
            print('error send code')
            acc()
        print('')
        sleep(0.5)
        cookies = {
    'csrftoken': csrftoken,
}
        headers = {
    'accept': '*/*',
    'accept-language': 'en-US,en;q=0.9',
    'content-type': 'application/x-www-form-urlencoded',
    'dnt': '1',
    'origin': 'https://www.instagram.com',
    'priority': 'u=1, i',
    'referer': 'https://www.instagram.com/accounts/emailsignup/',
    'sec-ch-prefers-color-scheme': 'dark',
    'sec-fetch-dest': 'empty',
    'sec-fetch-mode': 'cors',
    'sec-fetch-site': 'same-origin',
    'user-agent': 'Mozilla/5.0 (iPhone; CPU iPhone OS 16_6 like Mac OS X) AppleWebKit/605.1.15 (KHTML, like Gecko) Version/16.6 Mobile/15E148 Safari/604.1 Edg/124.0.0.0',
    'x-asbd-id': '129477',
    'x-csrftoken': csrftoken,
    'x-ig-app-id': '936619743392459',
    'x-ig-www-claim': '0',
    'x-instagram-ajax': '1013449353',
    'x-requested-with': 'XMLHttpRequest',
}
        while True:
            sleep(0.5)
            mass=Email(mail["session"]).inbox()
            if mass:
                print('done get otp code')
                print('')
                break
        code=str(mass).split("'topic': '")[1].split(' is your Instagram code')[0]
        print('otp code : '+code)
        print('')
        data = {
    'code': code,
    'device_id': client_id,
    'email': email,
}
        response = requests.post(
    'https://www.instagram.com/api/v1/accounts/check_confirmation_code/',
    cookies=cookies,
    headers=headers,
    data=data,
)
        sleep(0.5)
        if 'signup_code' in str(response.text):
            signup_code=response.json()['signup_code']
        else:
            print('error get signup_code')
            acc()
        print('signup code : '+signup_code)
        cookies = {
    'csrftoken': csrftoken,
}
        headers = {
    'accept': '*/*',
    'accept-language': 'en-US,en;q=0.9',
    'content-type': 'application/x-www-form-urlencoded',
    'dnt': '1',
    'origin': 'https://www.instagram.com',
    'priority': 'u=1, i',
    'referer': 'https://www.instagram.com/accounts/emailsignup/',
    'sec-ch-prefers-color-scheme': 'dark',
    'sec-fetch-dest': 'empty',
    'sec-fetch-mode': 'cors',
    'sec-fetch-site': 'same-origin',
    'user-agent': 'Mozilla/5.0 (iPhone; CPU iPhone OS 16_6 like Mac OS X) AppleWebKit/605.1.15 (KHTML, like Gecko) Version/16.6 Mobile/15E148 Safari/604.1 Edg/124.0.0.0',
    'x-asbd-id': '129477',
    'x-csrftoken': csrftoken,
    'x-ig-app-id': '936619743392459',
    'x-ig-www-claim': '0',
    'x-instagram-ajax': '1013449353',
    'x-requested-with': 'XMLHttpRequest',
}
        data = {
    'enc_password': '#PWD_INSTAGRAM_BROWSER:10:1715438382:AUpQAG8uH+FPt7g0UGQtScEEm9ATngQaKSmhYGwTO7BOsOBc3/nc/EZ5pgSXOo7FSpQfzLvDcKAeAUsK8+j7qPRb5Sv0i8Q/XVI44ATZqRrqIYzD3cXr6u8GZwk1Aq5UmE+srufEDSbFMiIVYA==',
    'day': day,
    'email': email,
    'first_name': name,
    'month': month,
    'username': username,
    'year': year,
    'client_id': client_id,
    'seamless_login_enabled': '1',
    'tos_version': 'row',
    'force_sign_up_code': signup_code,
}
        response = requests.post(
    'https://www.instagram.com/api/v1/web/accounts/web_create_ajax/',
    cookies=cookies,
    headers=headers,
    data=data,
)
        print(response.text)
        if 'username_is_taken' in str(response.text):
            print('username is taken')
            acc()
        elif 'email_is_taken' in str(response.text):
            print('email is taken')
            acc()
        elif '"account_created":true' in str(response.text):
            acc1+=1
            sessionid=response.cookies.get_dict()['sessionid']
            info=f'''
new instgram acc
acc num {str(acc1)}
name : {name}
username : {username}
email : {email}
password : qredes123
sessionid : {sessionid}
birthdate : {day}/{month}/{year}

By : @Qredes
'''
            print(info)
            requests.get(f'https://api.telegram.org/bot{token}/sendMessage?chat_id={ID}&text={info}')
            acc()
        else:
            print('انت محظور شغل vpn ادا كنت مشغله غير دولة')
            sleep(9)
            acc()

    except:
        print('انت محظور شغل vpn ادا كنت مشغله غير دولة')
        sleep(9)
        acc()

acc()
