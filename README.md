# How to get Google Assistant on your Windows, Mac, or Linux Machine
# My-Device
Google Assistant on Windows using Python 


# Creating Google Account on Google Cloud 


Google Assistant is Google’s answer to Amazon’s Alexa smart home assistant. Initially only available with limited functionality in the Google Allo application, Google Assistant later rolled out with the Google Home and Pixel smartphones to bring the full power of Google’s assistant to consumers.

# Get Google Assistant on Windows/Mac/Linux Machines

Requirements:

  Python 3
  Built Tools for Microsoft Visual Studio 2017 if on Windows
  
You’ll need to have Python installed no matter whether or not you are using Windows, macOS, or a GNU/Linux distribution. Installation is fairly simple and already well-documented by the Python wiki, so we won’t go into many details about getting Python up and running on your machine.

Once you’ve got Python working on your machine (you can confirm it is working by opening up a terminal/command prompt and then simply typing python.) If you see the terminal/command prompt return the current Python version on your computer, then you’re golden.



# Configure the Google Assistant API

What follows are step-by-step instructions walking you through the process to enable the Google Assistant API in the Cloud Platform Console so you can access Google Assistant through the Python program. All of these steps are platform independent, meaning that the steps are the same for Windows, macOS, and GNU/Linux users.

1. Go to the Projects page in the Google Cloud Platform Console.
2. Click on “Create Project” up top.
3. Name the Project “My Google Assistant” and click “Create.”
4. Wait a few seconds for the Console to create your new Project. You should see a spinning progress icon in the top right. After it is    done creating your Project, you will be brought to your Project’s configuration page.
5. Click this link to go straight to the Google Assistant API page. Up top, click “Enable.”
6. Google will warn you that you need to create credentials to use this API. Click “Create credentials” in the top right. This will take    you to a setup wizard page where Google helps you figure out what kind of credentials you need to use this API.
7. Under “where will you be calling the API from”, select “Other UI (e.g. Windows, CLI tool)“. For “what data will you be accessing”        select the “User data” circle. Now tap “what credentials do I need?”
8. Google should recommend that you create an OAuth 2.0 client ID. Name the Client ID anything you want, for example, your name +          Desktop. Once done picking a name, click “create client ID.”
9. Under “product name shown to users” enter “My Google Assistant.” Click continue.
10. Click “done.” There’s no need to click download here as we only need the client secret, which we will download next.
11. Now under the list of OAuth 2.0 client IDs, you should see the client ID you just made. All the way to the right, click on the           download icon to download the client_secret_XXX.json file, where ‘XXX’ is your client ID. Save this file anywhere on your computer,     ideally in a new folder called “googleassistant.”
12. Go to the Activity controls page for your Google account and make sure that “Web & App Activity”, “Location History”, “Device           Information”, and “Voice & Audio Activity” are enabled. This is so Google Assistant can actually read you personalized information.



We have now created a mechanism for a client, in this case our Windows/Mac/Linux machine, to access the Google Assistant API under our Google account. Next we need to set up the client that will access the Google Assistant API.


# Install the Google Assistant Sample Python Project


1. Open cmd
2. write,   It will take little time.
  i).  py -m pip install google-assistant-sdk[samples]
  ii). google-oauthlib-tool --client-secrets File_location\xxxxxx.json --scope https://www.googleapis.com/auth/assistant-sdk-prototype -        -save --headless
           Note: File Location = location of json file 
           xxxxxx.json = name_of_ur_json_file.json
           
  iii). python -m googlesamples.assistant.grpc.audio_helpers
  iv).  python -m googlesamples.assistant.grpc.pushtotalk
  
        
        
  
