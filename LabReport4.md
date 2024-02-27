# Lab Report 4 - Vim

### Log into ieng6:
![image](https://github.com/jharasaki/cse15l-lab-reports/assets/156235690/f3b7669c-d815-4d80-adab-261203abe61d)

### Clone my fork of the repository (already did it in lab):
![image](https://github.com/jharasaki/cse15l-lab-reports/assets/156235690/652ec5a3-cf12-4b23-9455-3bba039fb20d)

### Run the tests, demonstrating that they fail:
![image](https://github.com/jharasaki/cse15l-lab-reports/assets/156235690/edb96e16-6e85-4a8d-acdb-fba2caaa92c7)

### Edit the cause for failing test:
<img width="581" alt="image" src="https://github.com/jharasaki/cse15l-lab-reports/assets/156235690/6344e046-d47d-4c15-84be-0e1e2c144f71">

Steps i took: `/index1 <enter>, 9n, 5l, x, i, 2, :wq <enter>`

`/index1 <enter>` searches for and maps to the first "index1" in the file

`n` will map to the next instance of "index1", press this 9 times to get to the index1 we need to change

`l` will move the cursor to the left, press this 5 times to get to the "1" of "index1"

`x` to delete the "1" in "index1"

`i` to go into insert mode, then press '2' to insert "2" in that spot

`:wq <enter>` to save and exit from vim



### Run the tests, demonstrating that they now succeed:
![image](https://github.com/jharasaki/cse15l-lab-reports/assets/156235690/467819bf-a444-4db5-9611-72da6af066de)

### Commit and push the resulting change to Github:
<img width="397" alt="image" src="https://github.com/jharasaki/cse15l-lab-reports/assets/156235690/1c12fdd3-c612-403e-a450-69afc43b6b01">
