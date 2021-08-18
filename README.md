# Git-CheatSheet
Git-CheatSheet

# GIT 
- version Control System (VCS)
- Source Code management Tools
- Rolling Back
- Distributed Version Control System
- Different users each maintain their own repository
- No central repository
- Changes are stored as change sets
- No single master repository
- Many working copies
**We can have two or more master repositories, it’s not must that the master repository to be one ===> No single point of failure
- Encourages participation and forking of projects
- All repositories are considered equal by Git
- Git's strengths lie in its ability to allow multiple users to contribute to a repository, and the repo owner can easily evaluate proposed changes with Git's tools.
- Git  is fast, can handle large code bases, and is distributed.


# Git configuration
1.System
- git config --system
2. User
- git config --global
3. Project
- git config
- Git config with no options will access the project-level config file.

- dir => lists folder contents
- dir -la => List all folder contents, even the hidden ones
- cat file-path/name => display contents of the file

- **NB: - Best practises for git commit messages:**
- Short single line (less than 50 characters)
- Write commit messages, present tense, not past tense
- “Fix for a bug” or “Fixes a bug” , not “fixed a bug”
                     -   Bullet points are usually asterisk or hyphens
          -  Can add “tracking numbers”  from bugs or supports requests
          - Should be CLEAR AND DESCRIPTIVE
    -
    - Bad: “fix typo”
    - Good: “Add missing hyphen in project section of HTML”
    
    - Bad: “Update login code”
    - Good: “Change user authentication to use Blowfish”
    - Bad: “Updates member report, we should discuss  if this is right next week”
    - Good: “ghi2345 - Fixes bug in admin logout”


# Git logs 
- git  log : displays the commits made
- git log -n 5: displays the five recent commits
- git log --since=2019-01-01 : limit the commits to log by time
- git log --until=2019-01-01
- git log --author=”Melvin” : Limits commits by the author
- git log --grep=”Init”: returns any commit with the String “Init”
- git log --grep=”bug fixes”: logs any commits with the phrase “bug fixes”


# Git Three Tree  Architecture
-  Most of VCS, use the Two Tree Architecture consisting of :
  - Repository (on Github)
  - Working directory
-  Git Three Architecture consists of :
 - Repository
 - Staging index
 - Working directory
                                - git add .            - git commit -m ”message”
- **Working directory =========> staging index ==================== >  Repository**

# Hash Values(SHA-1):
- Refers to the way git labels and refers to it’s commits
- git generates a checksum for each change set
- Checksum algorithms convert data into  a simple number
- Same data always equals same checksum
- The checksum is used to guarantee data integrity
- Data integrity is fundamental to git
- Changing data would change checksum
- git uses SHA-1 algorithm to create checksum
- Number generated is a 40-character hexa-decima (0-9, a-f)l string

    
# The HEAD Pointer 
- “The HEAD” ⇒ This is the reference variable maintained by git
- Place where we were last at in our repository in our last commit
- Parent of the next commit that we will make
- Points to the last commit that we made

# NB: 
- To view the changes made in a file, type :
git  diff
- Compares the working directory and the staging tree
- To view only staged differences: 
git diff --staged or git diff --cached or  git diff --color-words
- (staged is an alias for cached)


# Delete, move and rename files 
- To delete a file
git rm “filename”
- To rename a file
git mv “original filename” “new filename”

# NB: 
- To stage and commit at the same time: 
- git commit -a or git commit -all 
 - git commit -am "message"
- (does not include untracked files; does not add the new files)



# How to review / Inspect a Commit 
- git show “SHA-1” --color-words
    
- How to Compare two commits 
         -  git diff “name of the oldest commit”..“name of the other commit”
- NB: 
HEAD refers to the latest commit

-How to make multi-line commit messages 
Atomic commits => Small commits - have them affect only a single aspect ⇒ Easier to understand, to work with and to find bugs

