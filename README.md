# Generate Git Commits on macOS, Each Time you Start your Mac.

## Introduction

This repository contains a script that allows you to generate daily Git commits automatically on macOS. By following the steps below, you can create an application that will push empty commits to your GitHub or GitLab repository, giving the appearance of daily activity on your commit graph.

<img src="https://i.ibb.co/q5w7RmD/Capture-d-cran-2023-06-02-23-15-34.png" alt="How it works" />

## How to Use 🧑‍💻

1. Prerequisites: Make sure you have [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) and [Ruby](https://www.ruby-lang.org/en/documentation/installation/) installed on your machine.

2. Clone this repository to your macOS machine:
   ```shell
   gh repo clone DjDc31/auto-repo
   ```

3. Create [a private repository](https://github.com/new) called `auto-repo` in your GitHub or GitLab account.

4. Open the `exc.rb` file and update the code:
   - Set the appropriate directory path in the script.
   - Add your GitHub username and personal access token to authorize the automatic push. You can generate a token in your GitHub account settings: [https://github.com/settings/tokens](https://github.com/settings/tokens).

5. Open the `script.applescript` file using a text editor. In this file, you'll find the line:
   ```shell script
   do shell script "/usr/bin/ruby /path/to/your/script.rb"
    ```
  Replace /path/to/your/script.rb with the absolute path to your Ruby script.


6. Compile the AppleScript script into an application. Open Terminal and run the following command:
    ```shell script
    osacompile -o /path/to/your/application.app /path/to/your/script.applescript
    ```
  Replace /path/to/your/application.app with the desired absolute path for the application.

7. Configure the application for automatic startup:
- Go to System Preferences on your MacBook.
- Select "Users & Groups" or "Accounts".
- Choose your username from the left column.
- Go to the "Login Items" tab.
- Click the "+" button to add your application to the list of startup applications.



Done! Now by configuring your application this way, it will automatically launch every time you start up your MacBook and do a push of an empty file 😉

## Support This Project

If you find this tool useful or interesting, please consider supporting the project by giving it a star. Maintaining an open-source project requires time and effort. ⭐️

## DISCLAIMER

This tool was created as a playful experiment and should not be taken seriously. While it can generate fake commits, it's not meant to encourage dishonesty or misrepresentation of one's activity. While cheating with fake push is never encouraged, if someone is judging your professional skills based on your GitHub activity graph, they deserve to see a rich activity graph 🤓
