#Setting Up Dropbox Backups

We always recommend customers to maintain backup of their data in ERPNext. he database backup is downloaded in the form of an SQL file. If needed, this SQL file of backup can be restored in the another ERPNext account as well.

You can automate database backup download of your ERPNext account into your Dropbox account.

####Step 1: Go to Setup

`Explore > Setup > Integrations > Dropbox Backup`

####Step 2: Activate

In the Dropbox Backup, check "Send Backups to Dropbox" to active this feature. On checking this field, you will find field to set Frequency and notification Email.

####Step 3: Set Frequency

Set Frequency to download backup in your Dropbox account.

<img class="screenshot" alt="set frequency" src="{{docs_base_url}}/assets/img/setup/dropbox-1.png">

####Step 4: Allow Dropbox Access

After setting frequency and updating notification email, click on `Allow Dropbox access`. On clicking this button, the Dropbox login page will open in the new tab. This might require you to allow pop-up for your ERPNext account.

####Step 5: Login to Dropbox

Login to your Dropbox account by entering login credentials.

<img class="screenshot" alt="Login" src="{{docs_base_url}}/assets/img/setup/dropbox-2.png">

####Step 6: Allow

On successfull login, you will find a confirmation message as following. Click on "Allow" to let your ERPNext account have access to your Dropbox account.

<img class="screenshot" alt="Allow" src="{{docs_base_url}}/assets/img/setup/dropbox-3.png">

With this, a folder called "ERPNext" will be created in your Dropbox account, and database backup will start to auto-download in it.

##Open Source Users

####Step 1: Go to

<a href="https://www.dropbox.com/developers/apps" target="_blank" style="line-height: 1.42857143;">https://www.dropbox.com/developers/apps</a>

####Step 2:Create a new app

<img class="screenshot" alt="Create new" src="{{docs_base_url}}/assets/img/setup/dropbox-open-3.png">

####Step 3: Fill in details for the app

<img class="screenshot" alt="Create new" src="{{docs_base_url}}/assets/img/setup/dropbox-open-1.png">

-
<img class="screenshot" alt="Create new" src="{{docs_base_url}}/assets/img/setup/dropbox-open-2.png">

####Step 4: Settings in Site Config

After the app is created, note the app key and app secret and enter in `sites/{sitename}/site_config.json` as follows,

<div>
	<pre>
		<code>{ 
 "db_name": "demo", 
 "db_password": "DZ1Idd55xJ9qvkHvUH", 
 "dropbox_access_key": "ACCESSKEY", 
 "dropbox_secret_key": "SECRECTKEY" 
} 		
		</code>
	</pre>
</div>

####Step 5: Complete Backup

Setup dropbox backups from the backup manager as shown in previous section.