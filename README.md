# mysql-wsl-ubuntu
This repo use to documenting how to connect and use mysql in wsl in ubuntu machine


## Install Mysql 

To install MySQL on WSL (ie. Ubuntu):

1. Open your WSL terminal (ie. Ubuntu).
2. Update your Ubuntu packages: `sudo apt update`
3. Once the packages have updated, install MySQL with: `sudo apt install mysql-server`
4. Confirm installation and get the version number: `mysql --version`

You may also want to run the included security script. This changes some of the less secure default options for things like remote root logins and sample users. To run the security script:

1. Start a MySQL server: `sudo /etc/init.d/mysql start`
2. Start the security script prompts: `sudo mysql_secure_installation`
3. The first prompt will ask whether you’d like to set up the Validate Password Plugin, which can be used to test the strength of your MySQL password. You will then set a password for the MySQL root user, decide whether or not to remove anonymous users, decide whether to allow the root user to login both locally and remotely, decide whether to remove the test database, and, lastly, decide whether to reload the privilege tables immediately.
To open the MySQL prompt, enter: sudo mysql

To see what databases you have available, in the MySQL prompt, enter: `SHOW DATABASES;`

To create a new database, enter: `CREATE DATABASE database_name;`

To delete a database, enter: `DROP DATABASE database_name;`

For more about working with MySQL databases, see the MySQL docs.

To work with with MySQL databases in VS Code, try the MySQL extension.


> Reference: https://docs.microsoft.com/en-us/windows/wsl/tutorials/wsl-database
