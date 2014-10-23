# Hello World PHP

New users should check out the resources available at [HP Helion Docs](http://docs.hpcloud.com/helion/devplatform/workbook/helloworld/php/). 
The site includes more detail and has instructions on how to create an HP
Helion Development Platform Application Lifecycle Services Cluster.

To create an app in PHP, the only mandatory files are the index.php
and manifest.yml files. The blank composer.json file here is included to get rid 
of any potential warnings about not having a composer.json file during deployment.

Manifest.yml is a config file used to specify settings that would otherwise be
specified by a command-line tool. For PHP, only the name and buildpack fields are
required. The buildpack field is a URL for the buildpack that supports the 
necessary language and/or framework.

## Deploy to HP Helion
You can deploy this app automatically with the button below or with the manual 
instructions further down. In either case, you will need to have take care of the
prerequisites.

<a href="https://deploynow.hpcloud.com/?repoUrl=https://github.com/HelionDevPlatform/helion-hello-world-php">
![Helion  Logo](https://a248.e.akamai.net/cdn.hpcloudsvc.com/g0bc199ab57e65f093a48d069effc0c3b/prodae1//button.png?id=6)
</a>

## Prerequisites
- If you do not have an HP Helion Development Platform Application Lifecycle 
  Services Cluster available, please create one before continuing. You will also
  need to install the Helion CLI, which can be installed from the cluster's
  Management Console. Please refer to [HP Helion Docs](http://docs.hpcloud.com/helion/devplatform/workbook/helloworld/php/)
  for further details.  
- Composer is not necessary for this sample. While there is an empty composer.json
  file in this sample app, it's included to get rid of any potential warnings
  due to a missing composer.json file.
    
## Deploy the Application

To deploy the application, make sure you have the Helion CLI/client installed. 
Execute the following commands:

- Open the terminal
- If you are not already there, *cd* to the root directory of the sample. The 
  root directory contains the manifest.yml file which helps automate deployment. 
- If you have not logged in to your target environment yet, execute the following:

    `helion target https://api.example.com`
    
    `helion login`
    
    Enter your Management Console credentials
    
    `helion push`

    Hit enter to accept any default values that you may be prompted for. 
    Note: By default, ALS clusters are configured with two domains (private and
    public). In some situations, the Helion CLI may prompt you to select a target
    domain. If prompted, select the public domain from the given list (e.g. https://api.example.com)

## View and run the app
- Go to the management console (e.g. https://api.example.com)
- Check the applications link to see a list of your apps.
- Click on the name of the app you just deployed. The app name is specified in 
  manifest.yml.
- Click "View App" to see your app in action.

The result when visiting the application page and clicking 'View App' should be
a page with the text "Hello World".
