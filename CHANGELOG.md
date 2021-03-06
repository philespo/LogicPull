#Changelog

##Version 0.9.0 (2015-02-18)

###Editor

- New size option for fields (small, medium, large, x-large)
- Add a "new line" option to keep fields on their own line, pushing other fields to the next line
  - this is for use when, for example, you want to use two small fields on a single line and instead of a third small field on the same line, you can place it one the next one
- Button text can now be customized instead of always displaying "Continue", "Exit", "Finish", etc.
  - This option is located in the buttons tab of the question being worked on in the editor

###Admin

 - New admin area for registered users who are not managers
   - This section is available at `/admin`. Users who register when completing an interview can view their completed documents in the `admin` area. Users who are "Managers" will automatically have access to the admin area, but admin users do not have access to the manager unless their account is upgraded by a manager user. 

###Manager

- New layout and design using Twitter Bootstrap 3.2
- Add the ability to reset user passwords
- Add the ability to update admin (non-manager) users to manager users
- Add a search bar to look for completed interviews by clients
- Show the last login date for a user on the users page
- Add the ability to update user privileges
- Add the ability to remove users
- Allow dashes and other special characters in deliverable and interview names (#19)
- Add the ability to update interview descriptions (#17)
- All bypassing email verification when creating new users
- Allow a password to be given when creating users in the manager
  - The password is only applied if "Disable email verification" is used, otherwise the user is emailed a link where they can set their own password
- Allow uploaded PDF forms to be downloaded from the manager (#18)
- Display recently completed and saved interviews on the interview page

###Viewer

- New layout and design using Twitter Bootstrap 3.2
- Keep the learn more fixed on the right side of the screen
- Use modals for tool tips
- Display the interview name and description in the sidebar
- Use answers already given to prepopulate questions being answered again (#2)

###Misc

- Remove node_modules from repository (#22)

**Release Notes**

- This release added some new privileges (`reset_user_passwords`, `view_saved_interviews`, `remove_users`), and in order to use them they need to be applied by a user who has `edit_user` and `edit_privledges` privledges. This can be done on the users page and clicking the edit user button, which is a gear icon.
- If you run into any conflict with `node_modules` when pulling in changes, the easiest way to fix this is by removing the `node_modules` directory, merging the latest code and then installing `node_modules` again.

  ```
  rm -rf node_modules/
  git pull origin master
  npm install
  ```
