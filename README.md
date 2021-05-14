# Drupal Developer Code Exercises
These exercises are designed to assess your Drupal knowledge and see how you solve problems.

# Instructions
* Read the exercises below.
* Push your work up in a new private repository in your own GitHub account.
* Export your local databses and push in project's root folder.
* Give the user [hardikpatel1990](https://github.com/hardikpatel1990) read access to your repository.

# Exercises

Note: All below 3 exercises should be implement in Drupal 7 latest stable version.

* Exercise 1: Multisite setup
* Exercise 2:  Display a list of users using custom form on the homepage
* Exercise 3: Create a paywall effect for the article content type

# Exercise 1:
1. Install a Drupal 7 latest stable verison that will act as the root site for our multisite instance. For example, the root site will be called d7multisite, will be reachable at d7multisite.com
2. Set up a site within the multisite called site1 which is reachable at site1.d7multisite.com

# Exercise 2:
1. Create exercise2 custom module.
2. Create custom form which has following fields
   * FullName
   * Email
   * Age
3. On form submit store form values into custom table called "user_info", form can be submitted by any user like authenticate, anonumous or admin user.
4. Create view's block to show all records of "user_info" table and show in table format and place this block on home page in content section, this block only visible to user who has administrator role.

# Exercise 3:
We want to institute a paywall for some article nodes that we are publishing.
--
1. Create exercise3 custom module.
2. Our requirements are:

* Creat a new role: premium. This new premium role will need a new permission: view full premium content.
* We do not want to paywall all of the article content on our site. We have added a new field to the article content type (field_is_premium). Only articles that have field checked should have the paywall active.
* If a node has field_is_premium checked, then users without this new permission should see the summary even when they are viewing a full node display. If they do have this new permission, then they should not see the summary, they should see the full body content.
* Users who do not get to see the full premium content should get notice on the page that says that the full content is only available with a premium account.

For testing:
--
Create two users:
--
A standard user who does not have this new role/permission exists with these credentials:
* username: standard_user
* password: standard_user

A premium user who does have this new role exists with these credentials:
* username: premium_user
* password: premium_user


We also have sample article content created:
--

Two standard articles that should not have a paywall:
* d7multisite.com/no-paywall-1
* d7multisite.com/no-paywall-2


Two premium articles that should have a paywall:
* d7multisite.com/paywall-1
* d7multisite.com/paywall-2

