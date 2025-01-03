Follow this Steps : 

# **Creator’s Steps** (Initial Setup):
1. **Create a local folder and initialize it with Git**:
   ```bash
   mkdir project-folder
   cd project-folder
   git init
   ```

2. **Make some initial commit ( readme create kar lo )** (you need at least one file to commit):
   ```bash
   echo "# Initial commit" > README.md
   git add README.md
   git commit -m "Initial commit"
   ```

3. **Also rename master branch to main humko complexity nahi chhaiye**: 
   ```bash
   git branch -m "main"
   ```

3. **Create four branches (`sahil`, `yogesh`, `chaitanya`, `ritesh`)**:
   ```bash
   git checkout -b sahil
   git checkout -b yogesh
   git checkout -b chaitanya
   git checkout -b ritesh
   ```

4. **Add remote repository** (known as `origin`):
   ```bash
   git remote add origin https://github.com/username/repository-name.git
   ```

5. **IMP : Push all branches to the remote**:
   ```bash
   git push --all origin
   ```

   This will push all local branches to the remote repository.

---

# **Collaborators' Steps** (What you will do):
1. **Clone the repository**:
   ```bash
   git clone https://github.com/username/repository-name.git
   cd repository-name
   ```

2. **IMP : Fetch all branches**:
   ```bash
   git fetch --all
   ```

3. **View all branches** (local and remote):
   Use `git branch --all` to list both local and remote branches. This will show branches under `remotes/origin/`, e.g., `origin/sahil`, `origin/yogesh`, etc.

4. **Switch to all remote branches** (create a local branch that tracks the remote branch):
   To switch to the `sahil` branch from remote, you run:
   ```bash
   git checkout -b sahil origin/sahil
   git checkout -b yogesh origin/yogesh
   git checkout -b ritesh origin/ritesh
   git checkout -b chaitanya origin/chaitanya
   ```
   This command creates a local branch named `sahil` and links it to the remote branch `origin/sahil`.

5. **Add, commit, and push changes to the `your` branch**:
   - Add changes:
     ```bash
     git add .
     ```   

   - Commit the changes:
     ```bash
     git commit -m "Made some changes on sahil branch"
     ```

   - Push the changes to the remote `sahil` branch:
     ```bash
     git push origin sahil
     ```
6. **After this , Create PR to merge ur branch to main branch and sahil will merge the PR**:
   - Add changes:
     ```bash
     git add .
     ```

   - Commit the changes:
     ```bash
     git commit -m "Made some changes on sahil branch"
     ```

   - Push the changes to the remote `sahil` branch:
     ```bash
     git push origin sahil
     ```

---

### Some Points to remember : 
- ## (Suppose u are visiting for second time onwards : then whenever u come back to start working on) project do pull ur branch using command git pull origin <your_name> so that u get recent changes made by anyone.##

- `git branch --all` is used to list **both** local and remote branches.
- When you create a local branch, it won’t show under `remotes/origin/` until you push it to the remote repository.
- you can also set upstream your remote branch but hum ye nhi karenge to avoid complexities.
