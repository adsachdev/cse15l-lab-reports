# Lab Report - 4
May 20, 2024

## 1) Login to ieng6
[login image]()

- Keys pressed: `ssh<space>adsachdev@ieng6.ucsd.edu<enter>`
- Summary: Typed `ssh` and my username to log into `ieng6`

## 2) Cloning the repository
[git clone image]()

- Keys pressed: `git<space>clo<tab><command>V<enter>`
- Summary: Wrote `git` and `clo` with `<tab>` to complete the command, then `<command>V` to paste the ssh url

## 3) Showing tests fail
[test run-1 image]()

- Keys pressed: `cd<space>l<tab><enter>` and `bash<space>t<tab><enter>`
- Summary: Typed `cd` and `l` with `<tab>` which prompted it to complete the name of the directory, this allowed me to enter into directory `lab7/`. Then typed `bash<space>t` with `<tab>` to complete the name of the file, this allowed me to run the tests through `test.sh`.  

## 4) Edit code 
[edit code image]()

- Keys pressed: `vim<space>L<tab>.<tab><enter>` and `44Glllllxi2<esc>:wq<enter>`
- Summary: Typed `vim<space>L` with `<tab>` to complete the name of directory `ListExamples` then typed `.` with `<tab>` to complete `.java` this allowed me to edit the file `ListExamples.java` through vim. 
  Then typed `44G` which took my cursor directly to line 44 where the change was supposed to be made. 
  Then `lllll` which took me right 5 spaces on the same line. 
  Then `x` while the cursor was on `1` and removed it. 
  Then `i` which took me into insert mode followed by `2` which added `2` at that spot and `<esc>` to exit insert mode.
  Then `:wq` which quit vim after saving the changes. 

## 5) Showing test pass
[test run-2 image]()

- Keys pressed: `<up><up><enter>`
- Summary: Running the test command was 2 places up, so that is how I accessed and ran it. 

## 6) Commit and push
[git push image]()

- Keys pressed: `git<space>add<space>.<enter>` and `git<space>com<tab><space>-m<space>"index<space>changed<space>to<space>pass<space>test"<enter>` and `git<space>push<tab><tab>main<enter>`
- Summary: First typed `git<space>add<space>.<enter>` which ensures we want to include all changes in the commit.
  Then `git<space>com<tab>` that completed `git commit` followed by `-m` and a message describing the changes made.
  Then `git<space>push<tab><tab>main`which completed the command `git push origin main` which pushed my changes to the git repo. 
