1. Configure the ssh key. This will be used later when connecting our local repository to our remote one

```
git config --global user.name your_name
git config --global user.email your_email@example.com

git config --global core.editor your_text_editor # optional

git config --global -e

git config --global core.autocrlf true / input

git config --help
git config -h
```

Ohh shit, git [Oh Shit, Git!?!](https://ohshitgit.com/)
git config [Git - Git Configuration](https://git-scm.com/book/en/v2/Customizing-Git-Git-Configuration)

```
cd project_name
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/your-username/your-repo.git
git push -u origin main

```

Hunks?
```
mkdir new_directrory
cd new_directory
touch new_file.html
code .
```