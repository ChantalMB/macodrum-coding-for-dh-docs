# Connecting Git and GitHub

> Steps for connecting Git (local to your device) to GitHub (on the web)

To connect to GitHub from your computer, you first must generate a personal access token (PAT) and connect via HTTPS (**H**yper**t**ext **T**ransfer **P**rotocol **S**ecure). As you may have guessed by the name, this is a secure way to transfer files to your GitHub account by letting GitHub know that your personal device can be trusted through a unique and elaborate "key", much like a password.

!!! info "For Windows Users"

    To configure Git and perform the initial set up of GitHub on your device, you must use Git Bash which is located under the <q>Git</q> folder that can be accessed from the Start menu. After this step is done you may continue to use the Anaconda Powershell Prompt!

## Configuring Git

These commands modify the configuration file (aka Settings) for Git, hence calling `git config`. The flag `--global` means that these configurations will only be applied to the user account you're logged into, rather than to every account on your device (assuming there's multiple).

- To add a username associated with your device's Git profile (tip: use your Github username so this is easy to remember):
  ```
  git config --global user.name "Your GitHub name here"
  ```
- To add an email associated with your device's Git profile (use the same email you used for Github):
  ```
  git config --global user.email "your_email@example.com"
  ```
- To make Git output use colour (easier to read):
  ```
  git config --global color.ui true
  ```

## Using a PAT

- On the GitHub website, go to your profile settings which can be accessed by selecting your profile picture in the upper right corner of the page.
- In the left hand menu, scroll down to the bottom and open "Developer settings"
- Select "Personal access tokens", then hit the button which says "Generate new token"

Once on the **"New personal access token"** page you will:

- Set the expiry date for your PAT- this is the interval at which you will have to generate a new PAT. Choose however long you feel comfortable keeping this "password" active for!
- Grant access permissions for this PAT- since you are the admin user of your device that is connecting to your GitHub account, we suggest ticking every checkbox to make sure you do not miss any permissions you may need.

Once your PAT is generated, save it with the rest of your passwords and treat it like one! If you accidentally push it to GitHub in a note file, the PAT will automatically be disabled and you will have to create a new one.

**In the next step of this workshop,** when you enter the `git push` command:

- **On MacOS**: You will be prompted in the command line to enter your GitHub username and password. Enter your username as expected, but **enter your PAT as the password** to connect your account.
- **On Windows**: A login box will open giving you ways to connect to GitHub; select the option which asks to use a PAT and proceed as instructed. 

Should you ever need to remove your PAT to set a new one, you can use the follow command to remove the PAT:
```
git config --global --unset credential.helper
```
And you will be prompted to enter your new PAT the next time you `git push`!



