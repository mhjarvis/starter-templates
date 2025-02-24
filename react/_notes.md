# React Project Setup

## Updated Setup

```bash
npm create vite@latest
```

## Using Vite

```bash
    # replace app name as needed:
    npm create vite@latest my-first-react-app -- --template react

    # install the following packages, enter 'y'
    Ok to proceed?  (y)

    # follow the rest of setup:
    cd my-first-react-app
    npm install

    # creates live server on localhost:5173
    npm run dev
```

## Connect project to a remote (empty) repository

1. Initialize the local project with Git.

```bash
    git init
```

2. Add all files to stagin area and commit.

```bash
    git add .
    git commit -m 'Initial Commit'
```

3. Add remote repository to the local project.

```bash
    git remote add origin <repository-url>
    git remote -v   // verify if needed
```

4. Push project.

```bash
    git push -u origin main
```

c
