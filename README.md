The image below shows how I work on 15-210 homework. I type 210 from terminal,
and new labs are automatically downloaded and extracted. Then I'm placed into
the directory of the newest lab.

<p align="center">
  <img src="./example.png">
</p>

This repository is a reference for anyone else who wants to do this. 

1. Clone [diderot-cli](https://github.com/diderot-edu/diderot-cli) into your
private drectory on AFS.

2. Create a file private/.diderot/credentials, and place your andrew email
address as the first line, and your diderot password as the second line. This
is detailed in the README of diderot-cli.

3. Now if you run the following command, you will get a list of the 15-210
assignmeents:

~/private/diderot-cli/diderot_student list_assignments "15210:F19"

4. Make sure your folder for 210 has the location/name "private/15210", and that
the folders inside of 15210 for labs you've already downloaded match the names
given by the command from step 3. Case matters!

6. Copy update.sh from this repository into your 210 folder, make it executable,
and run it. Note that it will delete .tgz files in the folder as part of
cleanup.

Now you can automatically download and extract labs using update. The next steps
are to automatically call update and cd into the newest directory from your
local computer.

1. Place the line in the 210 file in this repository at the end of the ~/.bashrc
file on your local machine, replacing ANDREWID with your andrew id. If you're on
a mac, you may have to put "source ~/.bashrc" at the end of ~/.bash_profile
(untested).


2. Run source ~/.bashrc, and then 210.

Now whenever you're in terminal, you should be able to run 210 and see the
magic happen.
