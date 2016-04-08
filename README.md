# fathym.io_ParticleDev
Download the fathym.io library folder to develop for Fathym on the Particle Photon
## About
[![Fathym logo](http://fathym.com/wp-content/uploads/2015/11/Fathym-Logo_Registered_sm-01-e1447723628628.png "Fathym Logo")](http://fathym.com) is a platform that let's you create powerful, social, front-end apps and dashboards for your IoT projects. Now with the fathym.io library native to Particle, it's incredibly easy to create dashboards and notifications, and even control your Photon from your own Fathym app! 

# Tutorial

## Getting up and running

1. **Download the [Fathym.io (fix link)](http://fathym.io) zip folder from this repo and unzip**
2. **Open the Particle Dev Desktop app and add the Fathym.io folder**
![Particle Dev](https://40.media.tumblr.com/85a6b84ac6a20005769c38cf79ea9c55/tumblr_o58dv5IR7S1qcz8h1o1_1280.jpg "Particle Dev")
  - Download the [Particle Dev Environment](https://www.particle.io/dev) if you haven't already
  - Inside Particle Dev: File -> Add Project Folder -> Find the fathym.io folder
  - For more about working with your Photon, start with the tutorials in the [Particle Guide](https://docs.particle.io/guide/getting-started/intro/photon/)
5. **Select your device, save, compile, flash**                                       
    ![Particle Icons](http://community.fathym.com/Files/Storage/18dc2dab-fd6e-4754-89ba-28e6611c1dae "Particle Icons")
  - The .ino should get random test data flowing to Fathym exactly as is, so we'll test everything before messing with the code
6. **Create a new Photon Part in your Fathym Home Space**
  ![Fathym Home](https://41.media.tumblr.com/101c284e6b4c640957cbaa86e444fe32/tumblr_o58dv5IR7S1qcz8h1o2_1280.jpg "Fathym Home")
  - Create an  account at [community.fathym.com](http.//community.fathym.com) if you haven't already
  - From your Home Space, click the plus "+" button to get to the catalog of addable parts
  - Choose the Particle Photon part
  - Add your Photon deviceID, which you can find on your [Particle Dashboard](https://dashboard.particle.io/user/devices)
8. **Enter your Photon Part on Fathym and add visualizations**
![Inspector](https://36.media.tumblr.com/e783e4d513003a6dc328c38347a4fa51/tumblr_o58dv5IR7S1qcz8h1o3_1280.jpg "Inspector")
  - From inside your Particle Photon Part, click the plus "+" button to get to the catalog of addable parts
  - Start by adding the inspector display
  - Save and watch your data flow through!

## Customizing

1. **Inside Particle Dev, open the fathym.io-photon.ino file**
![ino](https://40.media.tumblr.com/31879b26805e0ddac21e0a97e9fbe36e/tumblr_o58dv5IR7S1qcz8h1o4_1280.jpg "ino")
  - You'll see commented instructions about how and where to add code for your sensors
  - Note that fathym.set("attribute name", value, "units of measurement") formats the JSON to send to Fathym
2. **Open the Fathym.Build.h file**         
![build.h](https://40.media.tumblr.com/7ec2caa15654a3f089cb182301aefcbd/tumblr_o58dv5IR7S1qcz8h1o5_1280.jpg "build.h")
  - Edit the attributes that are automatically sent along with your payload by setting each item to true or false 
  - Note that the Fathym.io library includes support Photon battery power - enable battery support by uncommenting the code at the bottom of the FathymBuild.h file
3. **Add additional dashboard visualizations for your device in Fathym**
![Fathym Dashboard](https://36.media.tumblr.com/447b4d8abf0869768b89b0411e377eae/tumblr_o2crfxZXFf1qcz8h1o2_1280.jpg "Fathym Dashboard")
  - From inside your Particle Photon part, click the plus "+" button to get to the catalog of addable parts
  - Try an Historic Value part
    - Fill out the "Property Name" field with one of the attributes you're sending from your Photon (the attribute name must be an exact, case-sensitive match). Leave this field blank to create a generic graph with dropdown menu of the attributes you're sending so you can switch the attribute on the fly.   
4. **Create a Fathym Notification**         
![Notification Rule](http://community.fathym.com/Files/Storage/4ed0acc5-6b33-47e5-a8ae-a4bc5484b12a "Notification Rule")
  - From inside your Particle Photon part, click the config "cog wheel" button
  - Enter the "Add Ons" part
  - Enter the "Publish Subscription" part
  - Again, click the config "cog wheel" button
  - Enter the "Responses" part
  - Click the plus "+" button to get to the catalog of addable parts
  - Select the "Check" part
  - Name the Check Part and add a "Message Evaluation" 
    - Ensure that the property name you use is an exact match to one you're sending from your Photon
  - Save the Check part and then Enter into the Check part you just created
  - Click the plus "+" button to get to the catalog of addable parts
  - Add an "Email Response" and configure with your message and desired send frequency

## Collaborating and Setting Permissions
![Permissions](http://community.fathym.com/Files/Storage/06927353-54ad-4ecc-b29a-99cbc1f837da "Permissions")
1. From inside your Particle Photon part, click the edit button (pencil icon)
2. Open the "Permissions" tab
3. Here you can select which useres have read, write, delete, contributor, moderator, or full control access
  - Full control allows the user to enter the parts configure settings in addition to everything else
  - You can only give permission to existing Fathym users
  - Type "Everyone" to give the entire Fathym userbase a certain permission
4. Once you've given a user permission to work with your part, you'll need to share the part's url with them directly or place your part in a space that they already have access to, like the Community Space for example.

## Share your project with the Fathym community                 
![Community Space](http://community.fathym.com/Catalog/Image/67e28c78-af2e-4e11-9c65-52ba26e6a144?maxwidth=230 "Community Space")
1. From inside your Fathym Home Space, find and enter the "Community Space" (tree icon) 
2. Inside the Community Space,  click the plus "+" button to get to the catalog of addable parts
3. Change the selected tab in the upper right from "Create New" to "Add Exisiting
4. Search the "Existing Catalog" for your Particle Photon Device and Add!


  
