# TwilioVideoforce

Step 1: Download this repo to your computer and unzip it to a folder of your own choice.

Step 2: Open config.php and find the values needed for the following parameters in your Twilio account below:

$TWILIO_ACCOUNT_SID = 'Found in Your Twilio Dashboard: https://www.twilio.com/console ';
$TWILIO_CONFIGURATION_SID = 'Generate one here: https://www.twilio.com/console/video/profiles/create ';
$TWILIO_API_KEY = 'Generate here: https://www.twilio.com/console/video/dev-tools/api-keys/create ';
$TWILIO_API_SECRET = 'Generate here: https://www.twilio.com/console/video/dev-tools/api-keys/create ';

Step 3: Navigate to the folder you unzipped this repo to in Terminal or Command Prompt and open a localhost. Open index.html
in your browser to ensure that the localhost is live. 

  EG: php -S http 8000
  In browser: localhost:8000/index.html
  

Step 4: Open another Terminal or Command Prompt window or tab and type ngrok http (localhost port here). Open index.html to
ensure that the localhost is live. 

 EG: ngrok http 8000
 In browser: https://d8gb3ab6.ngrok.io/index.html
 
Step 4.5: If you have a web server, feel free to use it as long it is protected by HTTPS. Twilio's servers will reject an
insecure HTTP request. 

Step 5: In your Force.com developer console, copy the contents of twiliovideo.vfp into your console. Replace the url in the
$.getJSON method with the secure NGrok server you generated earlier or your own web server. 

  EG: $.getJSON('https://d8gb3ab6.ngrok.io/tokensf.php'
  or $.getJSON('https://mywebsite.com/tokensf.php'
  
Step 6: Test using Twilio's Video testing tools, including the rando.php file (included in tokensf.php), or by downloading 
a mobile sdk of Twilio Video to test the connection. 

Feel free to suggest changes, issues, and discuss. 

Have fun!
