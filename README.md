# n8n-docker-compose
Simple N8N install using docker compose please update the .env file with the various variables N8N needs.
This compose use MySQL as it's data base.

#### securing(basic auth only)
Change the username and password please create a very complex password

N8N_BASIC_AUTH_ACTIVE=true  
N8N_BASIC_AUTH_USER=user  
N8N_BASIC_AUTH_PASSWORD=password

#### MySQL
The location of the MySQL server, MySQL Should be on Private Subnet

DB_TYPE=mysqldb  
DB_MYSQLDB_DATABASE=n8n  
DB_MYSQLDB_HOST=mysql  
DB_MYSQLDB_PORT=3306  
DB_MYSQLDB_USER=user  
DB_MYSQLDB_PASSWORD=password  

#### timezone
GENERIC_TIMEZONE="Africa/Johannesburg"  
TZ="Africa/Johannesburg"

#### smtp
N8N_EMAIL_MODE=smtp  
N8N_SMTP_HOST=smtp.mail.com  
N8N_SMTP_PORT=587 #default port 465  
N8N_SMTP_SSL=false #or true  
N8N_SMTP_USER=mail@mail.com  
N8N_SMTP_PASS=email_password  
N8N_SMTP_SENDER=sender_mail@mail.com  
N8N_EDITOR_BASE_URL=http://n8n_url:5678

#### logging
N8N_LOG_LEVEL=error  
N8N_LOG_OUTPUT=console #console or file

## Start docker-compose#

n8n can now be started via:

``sudo docker-compose up -d``

To stop the container:

``sudo docker-compose stop``