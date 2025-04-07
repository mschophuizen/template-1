IMPORTANT to use GitHub:

First create an account at https://github.com

Before you can use GitHub on you device, have GitHub CLI installed, So do the next:
Open Terminal windows (MAC):
Check if GitHub CLI is installed (MAC): Type in terminal window:
gh --version
When this gives an ERROR then GitHub CLI is not installed, so do the next:
{
    Check is Brew is installend (MAC): Type in terminal window:
    brew -- version
    When this gives an ERROR then Brew is not installed, so do the next:
    {   
        Install brew (MAC): Type in terminal window: 
        /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

    }
    Install GitHub CLI (MAC): Type in terminal window:
    brew install gh
    Authenticate GitHub CLI (MAC): Type in terminal window:
    gh auth login
    Follow the prompts. You can log in via web browser or token, and choose GitHub.com
}


Now GitHub CLI is installed on you computer, and you can ask AI (in Cursor of Cline) to help you to use GIT and GitHub

=====================================================

Git is a version control system, so you can keep track of your development stages.

Prompts for AI to help with GIT (Apple MAc has git installed by default) and GitHub:
Prompt: I want to use git for this project. Can you help me with that?
Now the project has possibilities to have version control using git.


Prompt: I want a remote connection to github. Please help how to to this project. I want to connect it to a new repository named "template-1"

Now your project is on GitHub, so you have a backup of your project even when your PC fails.


After a change in your code, you can save this in git, and it will also be saved on GiThub with the mnext prompt (you can choose to fill in "comment" to whatever you like):
Save all files and commit this to git with comment "help.md updated"

How to create a branche in git? The main is the production, you can make a test branche and a development branch:
Prompt to make a test branche: make a branche in git named "test"
