# Hello World PHP

To create an app in PHP, the only mandatory files are the index.php
and manifest.yml files. The blank composer.json file here is included to get rid 
of any potential warnings about not having a composer.json file during deployment.

Manifest.yml is a config file used to specify settings that would otherwise be
specified by a command-line tool. For PHP, only the name and buildpack fields are
required. The buildpack field is a URL for the buildpack that supports the 
necessary language and/or framework.

## Prerequisites
- If you do not have an HP Helion Development Platform Application Lifecycle 
  Services Cluster available, please create one before continuing. You will also
  need to install the Helion CLI. 
- If you do not have the MySQL service enabled on your cluster, you can take the
  following steps to enable it:
    - Go to the management console (e.g. https://api.example.com)
    - Admin --> Cluster --> Settings (gear icon on right corner) --> Check off 
      MySQL --> Save
- Composer is not necessary for this sample. While there is an empty composer.json
  file in this sample app, it's included to get rid of any potential warnings
  due to a missing composer.json file.
    
## Deploy the Application

To deploy the application, make sure you have the Helion CLI/client installed. 
Execute the following commands:

- Open the terminal
- If you are not already there, *cd* to the root directory of the sample. The root directory contains the manifest.yml file which helps automate deployment. 
- If you have not logged in to your target environment yet, execute the following:

    `helion target https://api.example.com`
    
    `helion login`
    
    Enter your Management Console credentials
    
    `helion push -n`

## View and run the app
- Go to the management console (e.g. https://api.example.com)
- Check the applications link to see a list of your apps.
- Click on the name of the app you just deployed. The app name is specified in manifest.yml.
- Click "View App" to see your app in action.

The result when visiting the application page and clicking 'View App' should be
a page with the text "Hello World".
