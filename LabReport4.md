# Lab Report 4 - Vim

### Log into ieng6:
<img width="600" alt="image" src="https://github.com/jharasaki/cse15l-lab-reports/assets/156235690/f3b7669c-d815-4d80-adab-261203abe61d">

`ssh <space> jharasaki@ieng6-201.ucsd.edu` to log into ieng6

### Clone my fork of the repository:
<img width="728" alt="image" src="https://github.com/jharasaki/cse15l-lab-reports/assets/156235690/3ca31174-7d36-438c-a9bc-550a8d5a078d">

Forked and then cloned the lab 7 repository using the ssh URL `git <space> clone <space> git@github.com:jharasaki/lab7.git`.

### Run the tests first time:
<img width="600" alt="image" src="https://github.com/jharasaki/cse15l-lab-reports/assets/156235690/b8e61983-a733-4040-8bbe-226118a11b09">

Ran the test with `bash test.sh`. This first test demonstrates that there is one test that fails.

### Edit the cause for failing test:
<img width="600" alt="image" src="https://github.com/jharasaki/cse15l-lab-reports/assets/156235690/6344e046-d47d-4c15-84be-0e1e2c144f71">

Opened the file in vim using `vim ListExamples.java`

**Steps i took to edit the bug:** `/index1 <enter>, 9n, 5l, x, i, 2, :wq <enter>`

`/index1 <enter>` searches for and maps to the first "index1" in the file

`n` will map to the next instance of "index1", press this 9 times to get to the index1 we need to change

`l` will move the cursor to the left, press this 5 times to get to the "1" of "index1"

`x` to delete the "1" in "index1"

`i` to go into insert mode, then press '2' to insert "2" in that spot

`:wq <enter>` to save and exit from vim


### Run the tests again:
<img width="450" alt="image" src="https://github.com/jharasaki/cse15l-lab-reports/assets/156235690/467819bf-a444-4db5-9611-72da6af066de">

Ran the tests again using `bash test.sh` and now demonstrating that both tests succeed.

### Commit and push the resulting change to Github:
<img width="450" alt="image" src="https://github.com/jharasaki/cse15l-lab-reports/assets/156235690/091995d4-c822-45c4-a75b-06f164213465">

Then finally committed the changes to the git files.
