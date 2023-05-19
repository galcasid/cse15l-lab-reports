# Lab Report 4
### Step 4: Log into ieng6
![Image](step4.png)
* keys pressed: ```ssh<space>cs15lsp23bu<shift>2ieng6.ucsd.edu<enter>```.
### Step 5: Clone your fork of the repository from your Github account
![Image](cloningDirectory.png)
* keys pressed: ```git<space>clone<space><command>v<enter>```
* ```<command>v``` is pasting git@github.com:galcasid/lab7.git which was copied from GitHub.
### Step 6: Run the tests, demonstrating that they fail
![Image](testFailure.png)
* keys pressed: ```cd<space>lab7<enter>bash<space>test.sh<enter>```
* ```cd<space>lab7<enter>``` is to change directory to lab7
* ```bash<space>test.sh<enter>``` is to run the tests
### Step 7: Edit the code file to fix the failing test
![Image](vimNoEdit.png)
* keys pressed: ```vim<space><shift>list<shift>examples.java<enter>```
* This sequence of keys opens vim for ListExamples.java
![Image](vimColonWQ.png)
* keys pressed: ```xi2<esc>:wq```
* ```<enter>``` not yet pressed in this screenshot to show edits made in vim
![Image](vimExits.png)
* key pressed: ```<enter>```
* exits out of vim
### Step 8: Run the tests, demonstrating that they now succeed
![Image](step8.png)
* keys pressed: ```bash<space>test.sh<enter>```
### Step 9: Commit and push the resulting change to your Github account (you can pick any commit message!)
![Image](step9.png)
* keys pressed: ```git<space>add<space>.<enter>git<space>commit<space>-m<space><shift>'index2<shift>'<enter>git<space>push<enter>```
* ```git<space>add<space>.<enter>``` adds changes
* ```git<space>commit<space>-m<space><shift>'index2<shift>'<enter>``` commits changes to repository
* ```git<space>push<enter>``` pushes changes to repository
