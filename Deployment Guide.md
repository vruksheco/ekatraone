**Twilio Credentials**
1. SignIn to your Twilio Account:
	- You will get your ACCOUNT_SID & AUTH_TOKEN from your Daskboard.
2. For MESSAGING_SERVICE_SID:
	- Search for 'Messaging Services' in the search bar
	- Select any of your Messaging Services SID
3. For from_whatsapp_number:
	- Search for 'Whatsapp Senders' in the search bar
	- Copy the number from here.

**Twilio App Setup**
1. Go to https://github.com/vruksheco/ekatraone-twilio and clone/download the repo.
2. SignIn to your github -> Create new a repo(By Clicking on 'New') -> Enter Repo name -> Give Description -> Choose Public/Private -> Create Repo.
3. SignIn to your Heroku Account -> Click on New -> Create a new app -> Go to your cloned repo -> Open a terminal in that directory
4. Then enter the following commands:
	1. heroku login (then press any key, then you would be prompted to login to your heroku account)
	2. git init
	3. heroku git:remote -a {PROJECT_NAME}
	4. git add .
	5. git commit -a "{COMMIT_MESSAGE}
	6. git push heroku master
5. In your Overview tab -> Click on Configure Add-ons -> Search for 'Advanced Scheduler' in the Add-Ons search bar -> Select Advanced Scheduler -> Slect a plan -> Click on Submit Order Form.
6. After the Advanced Scheduler in your Installed add-ons section -> Click on the Advanced Scheduler add-on -> Click on Create Trigger then:
	1. Enter name for the trigger
	2. Command: python app.py
	3. Select your timezone
	4. Leave the default state
	5. Select Type
	6. Set time by following prompts, according to your select Type
	7. Click Save

**Backend**
1. Go to https://github.com/vruksheco/ekatraone-backend and clone/download the repo.
2. SignIn to your github -> Create new a repo(By Clicking on 'New') -> Enter Repo name -> Give Description -> Choose Public/Private -> Create Repo.
3. SignIn to your Heroku Account -> Click on New -> Create a new app -> Go to your cloned repo -> Open a terminal in that directory
4. Then enter the following commands:
	1. heroku login (then press any key, then you would be prompted to login to your heroku account)
	2. git init
	3. heroku git:remote -a {PROJECT_NAME}
	4. git add .
	5. git commit -a "{COMMIT_MESSAGE}
	6. git push heroku master
5. Now go to the settings tab on your heroku account -> Click on Reveal Config Var -> Here insert the following variables
	JWT_SECRET_KEY='{YOUR_JWT_SECRET_KEY}'\
	CORS_HEADER='Content-Type'\
	JWT_HEADER_NAME='Authorization'\
	JWT_HEADER_TYPE='Bearer'\
	SECRET_KEY='{YOUR_SECRET_KEY}'\
	MAIL_SERVER='{YOUR_MAIL_SERVER}'\
	MAIL_USERNAME='{YOUR_MAIL_USERNAME}'\
	MAIL_PASSWORD='{YOUR_MAIL_PASSWORD}'\
	MAIL_PORT=465\
	MAIL_DEFAULT_SENDER='{YOUR_MAIL_DEFAULT_SENDER}'\
	ACCOUNT_SID='{YOUR_TWILIO_ACCOUNT_SID}'\
	AUTH_TOKEN='{YOUR_TWILIO_AUTH_TOKEN}'\
	MESSAGING_SERVICE_SID='{YOUR_TWILIO_MESSAGING_SERVICE_SID}'\
	ACCESS_CONTROL_ALLOW_ORIGIN='*'\
	AWS_BUCKET='{YOUR_AWS_BUCKET}'\
	AWS_ACCESS_KEY='{YOUR_AWS_ACCESS_KEY}'\
	AWS_SECRET_ACCESS_KEY='{YOUR_AWS_SECRET_ACCESS_KEY}'\
	AWS_DEFAULT_REGION='{YOUR_AWS_DEFAULT_REGION}'
	from_whatsapp_number = '{YOUR_TWILIO_WHATSAPP_NUMBER} (Example:whatsapp:+12546553377')
6. Then Go to your Overview tab -> Click on Configure Add-ons -> Search for 'Postgres' in the Add-Ons search bar -> Select Heroku Postgres -> Slect a plan -> Click on Submit Order Form


**Frontend**
1. Go to https://github.com/vruksheco/ekatraone-frontend and clone/download the repo.
2. SignIn to your github -> Create new a repo(By Clicking on 'New') -> Enter Repo name -> Give Description -> Choose Public/Private -> Create Repo.
3. Then go to your downloaded repo -> Open a terminal in that directory -> then enter the following commands
	- git init
	- git add .
	- git commit -am "{COMMIT_MESSAGE}"
	- git branch -M main
	- git remote add origin {LINK_OF_YOUR_REPO} (this line will be mentioned on the page after you click on 'Create a Repository' on github)
	- git push -u origin main
2. SignIn to https://vercel.com.
3. Click on New Project -> Import your repo by clicking on import -> \
	Then enter your Project Name, \
	Framework Preset: Other, \
	ROOT DIRECTORY: ./ ,\
	Build and Output Settings
    - BUILD COMMAND: quasar build
    - OUTPUT DIRECTORY: /dist/spa
    - INSTALL COMMAND:  npm install\
	Environment Variables: In here you would need to enter the following variables:\
		SQLALCHEMY_DATABASE_URI={YOUR_DATABASE_URL}\
		JWT_SECRET_KEY='{YOUR_JWT_SECRET_KEY}'\
		CORS_HEADER='Content-Type'\
		JWT_HEADER_NAME='Authorization'\
		JWT_HEADER_TYPE='Bearer'\
		SECRET_KEY='{YOUR_SECRET_KEY}'\
		MAIL_SERVER='{YOUR_MAIL_SERVER}'\
		MAIL_USERNAME='{YOUR_MAIL_USERNAME}'\
		MAIL_PASSWORD='{YOUR_MAIL_PASSWORD}'\
		MAIL_PORT=465\
		MAIL_DEFAULT_SENDER='{YOUR_MAIL_DEFAULT_SENDER}'\
		ACCOUNT_SID='{YOUR_TWILIO_ACCOUNT_SID}'\
		AUTH_TOKEN='{YOUR_TWILIO_AUTH_TOKEN}'\
		MESSAGING_SERVICE_SID='{YOUR_TWILIO_MESSAGING_SERVICE_SID}'
4. Then Click on Deploy.
