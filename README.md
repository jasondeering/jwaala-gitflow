jwaala-gitflow
==============

Additional ```git``` commands for quickly starting and finishing new features/fixes.

These commands are based on the following principles for Jwaala git repositories

* git repo is on client's "test" system at `../Install/Instance/.git`
* git repo branching protocol is as follows
	* `master` - current production code, tags are used to mark code at a point when something is moved to production
    * `test` - all feature/fix code in development and available for a client to test
    * feature/fix branches - created from `test` to house feature specific code
    
Conventions
--------------
Branch naming

	master
    stage     # for staging/testing before move to production
    test      # for testing multiple in-development items without losing current dev code
    feature-* # for developing new features
    fix-*     # for developing bugfixes present in current production code


Commands
--------------
`git start`

Starts a new feature/bugfix branch off of the `test` branch.

`git finish`

Closes the current feature/bugfix branch and merges it back into the `test` branch.


Examples
-------------
Create a new feature branch for adding Skip Pay to client, where 9999 refers to Zoho/Zendesk ticket number
	
    # git start feature skip-pay-9999
    
Move Skip Pay feature branch into `test`

	# git finish feature skip-pay-9999
    
Create new bugfix branch

	# git start bugfix update-text-0000
    
Move 
