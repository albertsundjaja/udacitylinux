IP address: http://52.32.222.3/
SSH port: 2200
URL to hosted app: http://52.32.222.3/

I did all the required changes in the project detail:
Create a new user named grader
Give the grader the permission to sudo
Update all currently installed packages
Change the SSH port from 22 to 2200
Configure the Uncomplicated Firewall (UFW) to only allow incoming connections for SSH (port 2200), HTTP (port 80), and NTP (port 123)
Configure the local timezone to UTC
Install and configure Apache to serve a Python mod_wsgi application
Install and configure PostgreSQL:
Do not allow remote connections
Create a new user named catalog that has limited permissions to your catalog application database
Install git, clone and setup your Catalog App project (from your GitHub repository from earlier in the Nanodegree program) so that it functions correctly when visiting your server’s IP address in a browser. Remember to set this up appropriately so that your .git directory is not publicly accessible via a browser

Additional setting:
disable root ssh
require password for every sudo command 

the rubric require strong password for every user
but hey you dont want to type kskjjen0281jf201 as password when testing :)
so for simplicity in testing:
	password for grader is grader 
	password for root is root


Additional installation:
1. flask-sqlalchemy
2. pip
3. git

Note:
google dev disallow me to use OAuth when it originated from IP address
so the catalog app doesnt run as it supposed to be
the error said referral must come from .com or .org
if this is a requirement to pass the project, I would need to refactor the code
to use manual login instead of OAuth
