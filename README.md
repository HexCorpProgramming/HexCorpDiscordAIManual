# HexCorp Discord AI Manual
This is where we will document how the AI can be used. We use MkDocs to turn markdown into an HTML+CSS+JS site that is then hosted using GitHub Pages.

## Requirements
Follow the instructions under https://www.mkdocs.org/#installation to set up Python 3 and MkDocs.

Additionally you will need a GitHub account and git (https://git-scm.com).

Using a good markdown editor with live preview like Visual Studio Code is optional.

## Serving locally
To preview what the manual looks like without publishing it to the internet, you can run a small local server, that will show you what the manual would look like, if you published it right now. Execute `python -m mkdocs serve` in a command line terminal and wait until the message `Serving on http://127.0.0.1:8000` appears. You can minimize the terminal window now, but do not close it.

You can now open your webbrowser and put http://127.0.0.1:8000 in the adress field to see your local version of the manual. When you have made changes it may be necessary to reload the page to see them in the browser as well but in a lot of cases it will immediately show them without any additional actions.

When you are done editing you can stop the server by pressing Ctrl+C in the command line terminal.

## Publishing to the website
When you are confident that the current version of the manual should be made available to the public you can use the command `python -m mkdocs gh-deploy` to do so.

Please read https://www.mkdocs.org/user-guide/deploying-your-docs/ before attempting this and ask other people working on the documentation if they are okay with publishing now.