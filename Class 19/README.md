# Setting up Firebase

1. Go to: https://firebase.google.com/ and click the **Get Started** button.
2. Sign in with your Google Account (such as a GMail account), or follow the prompts to **Create account**.
3. Once you're signed in, click the Add Project button.
4. Give you project a name (any name you want) and click the Create project button.
5. Once the project is ready click the Continue button.
6. Click the button that reads "Add Firebase to your web app".
7. You will receive a prompt with all of the details for your app!  Copy them.
8. Open your html file and paste the details into the file.  Make sure to put them **before** jQuery.

It should look something like the following:
   ```<script>
     var config = {
       apiKey: "yoursupersecretapikey",
       authDomain: "yourprojectname.firebaseapp.com",
       databaseURL: "https://yourprojectname.firebaseio.com",
       projectId: "yourprojectid"
     };
     firebase.initializeApp(config);
   </script>
   
