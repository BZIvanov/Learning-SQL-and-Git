# Installation process for Linux

1. Run in the terminal:

```bash
sudo apt update && upgrade
sudo apt install mysql-server
exit
```

2. Reopen the terminal and type:

```bash
sudo mysql
```

in the mysql terminal enter the following commands:

```sql
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
FLUSH PRIVILEGES;
exit
```

3. Now in the terminal type

```bash
mysql -u root -p
```

You will be asked for password, which is the password you have used when typing the ALTER USER command after BY.

4. Now in the sql terminal to check if everything is done correctly type:

```sql
show databases;
```

and you should see something like:

```sql
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| sys                |
+--------------------+
```

# Installation process for Windows

## download in installator

1. Go to [mysql]('https://www.mysql.com/') website and click _Downloads_
2. click _MySQL Community (GPL) Downloads_ link then _MySQL Community Server_
3. Click _Go to Download Page_ for the recommended download option
4. Click _Download_ the web MSI installer (the smaller in MBs version)
5. Skip the login steps by clicking _No thanks_ link

## run the installator

Note: White installing if you don't see _Product configuration_ option in the wizard on the left side menu go back to the website and click _Looking for previous GA versions_ and select some previous version and download that installing file. If you don't do this you will not see setting password and other options. Run again the installer, without uninstalling if you installed with the other installer.

1. Proceed with _Full_ option
2. If you are asked for python or other connector just click _Next_ and agree with _Yes_
3. Execute and install the dependencies on the next page

## using workbench

1. Click the plus sign to setup a connection

- give it some _Connection name_
