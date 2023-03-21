# google-cloude-deployment-with-nextjs
Step 1: Create a Google Cloud account

If you don't already have one, create a Google Cloud account. You will need to provide your billing information to use the platform.

Step 2: Create a new project

Once you have created an account, navigate to the Google Cloud Console and create a new project.

Step 3: Set up the Cloud SDK

To use the Google Cloud SDK, you'll need to install it on your local machine. Follow the instructions for your operating system on the Google Cloud SDK documentation page.

Step 4: Install Node.js and npm

You will need Node.js and npm installed on your local machine to build and run your Next.js app.

Step 5: Create a new Next.js app

Create a new Next.js app using the following command:

```
npx create-next-app
```
This will create a new Next.js app with some basic boilerplate code.

Step 6: Configure your app for deployment

In order to deploy your app on Google Cloud, you'll need to create a configuration file. Create a new file called app.yaml in the root directory of your project, and add the following code:

makefile
```
runtime: nodejs
env: flex
```
Step 7: Initialize a new Git repository

Initialize a new Git repository in the root directory of your project, and commit all the files to the repository.

Step 8: Create a new Cloud Storage bucket

Create a new Cloud Storage bucket to store your app's files. You can do this using the Google Cloud Console.

Step 9: Build your app

Build your app by running the following command:

```
npm run build
```
This will create a new out directory in your project's root directory.

Step 10: Upload your app to the Cloud Storage bucket

Upload the contents of the out directory to the Cloud Storage bucket you created in step 8. You can use the gsutil command to do this:

```
gsutil cp -r out gs://your-bucket-name
```
Step 11: Deploy your app

Deploy your app to Google Cloud by running the following command:
```
gcloud app deploy
```
This will deploy your app to Google Cloud, and you should be able to access it by visiting the URL provided by the command.

That's it! You have successfully deployed your Next.js app on Google Cloud.
