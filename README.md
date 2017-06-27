#GoCD Demo

A simple setup to bring up a GoCD server with 2 agents. 
This includes a config file which has a typical value stream configured which would help explain some of the concepts in GoCD.
Some users with varied roles and permissions are setup, check `<roles>` section in the config file for the exact details. All login users are using the default password badger. 

Just run a `vagrant up` from the checked out folder. This will bring up a VM with the server and agents running. Once the machine is up, you will be able to access the server from your browser using : http://localhost:8153

There are a few repositories setup under `/home/vagrant/repos` which are used by the pre-configured pipelines. You should be able to add new commits to them to trigger new builds in Go.  For the demo purposes we added two shell scripts pass.sh and fail.sh under the root folder (vagrant). After running the appropriate scripts the build will trigger automatically and see the results accordingly.  First run the ‘sh fail.sh’.

This doesn't include data setup, which basically means on first time startup, you will have to let all the pipelines run atleast once.
