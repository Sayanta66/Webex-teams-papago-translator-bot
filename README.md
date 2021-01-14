Creating a AWS EC2 Instance :

- Create a free account in Amazon Web Services
- In the initial page of the console, go to the EC2 instance page
- Click on Launch Instance
- Pick a linux OS( which will be your virtual OS in the VM engine)
- select the free tire 
- Give a unique name to the publisher key and download it
- Review and launch the instance

Creating a Security Group and connecting the EC2 instance:

- From the left panel click on security group and create new
- Name it and add a description
- Add rules with ports 22 and 7777 with location 0.0.0.0/0 as both are open ports
- Create the security group
- Right click on the EC2 Instance and click change security group
- Remove the launch wizard security group and add the new one just created
- Click on connect and in the dialog box click on SSH
- Connect the EC2 instance with the server as instructed.(IMP : Publisher Pair key must be in valid format)
- Open terminal and after connecting, Install python and flask
- Test with a .py file so that you can see the server up and running

Creating a Bot in Webex and posting a webhook

- Go to dveloper.webex.com
- Sign up/Sign in and click on build apps
- Click on bot and fill up the necessary things and save it
- Copy the generated token, the Bot ID and the Bot email
- Go to documentation and under API Reference click on webhooks and then click on post(Which makes a new webhook)
- Fill the details and in the url section give the url of the EC2 instance from the dashboard with adding ":7777" as it determines the open port in which the server will be running
- ok 200 message will come which will tell that the webhook has been posted successfully

Testing the bot

- If the server is up and running, go to webex.com and sign in
- Create a team and under invite, type your bot name and it will appear
- Send message to the bot to check if it's working fine.
