---
id: Notizen
aliases: []
tags: []
---

---

17:29, Thu 25 September 2025

---

# Machine Learning

1. Get Live market data using APIs
2. Find external Datasets.
3. Build a prediction Model.
4. Backtest
5. Package

**Quant Developer**

Math - 3
Coding - 5
    Python/C++
Finance - 2

### Method 2

1. Form a hypothesis
2. Find Data
3. Reshape the data
4. Clean the Data
5. Error Metric
6. Split Data
7. Train the data

### Important
Problem
Quality of data
Accuracy of the model


# Mama Mboga

Stalls
from local farmers
delivery to mama mboga

# Mama Fua

Uber but for mama fuas

Mobile Phone Login
Mobile first UI/UX
Kenyan Trust worthy color palette


# useEffect

Use Effect's callback function cannot be an async function, so if you need an async function you have to define another function inside of the callback, for example;

```tsx
// This is Right!
useEffect(() => {
	const someFunction = async () => {
		...
	}
})
```

Not;

```tsx
// This is wrong
useEffect(async() => {
	...
})
```


# Oh My Zsh

[Home · ohmyzsh/ohmyzsh Wiki · GitHub](https://github.com/ohmyzsh/ohmyzsh/wiki)

https://dominikrys.com/posts/zsh-in-git-bash-on-windows/


# Git Sketch

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

# To-do

- [ ] Obsidian Follow link function
