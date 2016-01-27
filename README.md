# AnyBlog

## Overview

This app showcases [dynamic websites](https://parse.com/docs/cloudcode/guide#hosting-dynamic-websites) using Parse Hosting. It's a simple blog that lets you create posts and your readers to leave comments.

You can check out the official hosted version at [www.anyblog.co](http://www.anyblog.co).

## Setup

1. Get the Parse command line tool for your OS if you have not done so yet. You can find instructions specific to your platform in the [Cloud Code QuickStart Guide](https://parse.com/apps/quickstart#cloud_code). Make sure you go through the steps to configure the Parse tool with your account key as well.

2. Open your favorite command line terminal and kick off the Parse tool's setup process by typing `parse new` then hitting ENTER.

3. Choose (n)ew app when prompted, and create a new Parse app to host your blog. For purposes of this tutorial, we will choose "my-blog", but feel free to use whichever name you prefer.

4. The tool will prompt you for the name of the directory where your Cloud Code will be hosted. We'll use the same name as the Parse app, "my-blog".

5. Hit ENTER to set up a sample Cloud Code project. This will populate your `my-blog` directory with the bare minimum necessary to host a simple Cloud Code app.

## Customization

Your `my-blog` folder should now contain two sub-folders, `cloud`, and `public`. The first contains the actual JavaScript code that will be loaded and executed in Cloud Code, while the latter contains static assets that will be served whenever someone visits your Parse app's subdomain name. You can learn more about these by visiting the [Cloud Code Guide](https://parse.com/docs/cloudcode/guide).

1. We won't be using the default template that was generated earlier by the Parse tool, so go ahead and delete both `cloud/main.js` and `public/index.html`.

2. Now copy over all the files in `cloud` and `public` from this repository over to the `cloud` and `public` sub-folders in your local `my-blog` folder.

3. Edit `cloud/app.js` and specify your `userEmail`, `userDisplayName` and `userDescription`. This will be used to attribute any posts. For extra points, you may want to come back to this later and set up your code to handle multiple users.

4. Also in `cloud/app.js`, replace YOUR_USERNAME and YOUR_PASSWORD with a username/password combination that will be used to access admin functionality later on.

## Deploying your new site

We're almost ready to start serving your site!

1. Go back to your command line terminal. Type `parse deploy`. This deploys your app to Parse.

2. Now, we'll need to configure the url where you can reach your app. Go to your App Settings page in the [Dashboard](https://dashboard.parse.com) and select "Hosting and Emails". Here you can set a unique subdomain name to host your blog.

3. Go to http://YOUR_SUBDOMAIN.parseapp.com and view your copy of AnyBlog!

## Writing your first blog post

Now that your blog is up and running, you can write your first post.

1. Visit your blog's admin console. It is available at http://YOUR_SUBDOMAIN.parseapp.com/admin.

2. Log in using the same username and password that you set up in `app.js` earlier.

3. Click on `new post` and type away! Your blog post will be available as soon as you hit "Publish".

## Next steps

* Use a custom domain name to host your blog. After registering your domain name with your favorite registrar, visit your App Settings in the Dashboard and set up your custom domain name under "Hosting and Emails".
* Modify the code to allow multiple users to log in and author their own blog posts.
* Update your blog's layout by editing the EJS templates in the `cloud/views` directory.
* Change your blog's look and feel. Stylesheets are hosted in the `public/stylesheets` directory.
