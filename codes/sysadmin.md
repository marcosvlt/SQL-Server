# Admin routines.

### Restore a database

```SQL
USE [master]
RESTORE DATABASE [DATABASE_NAME] FROM  DISK = N'/path/file.bak' WITH  FILE = 1, NORECOVERY,  NOUNLOAD,  REPLACE,  STATS = 5
GO
```

### Truncate a table

```SQL
USE[Nome_do_banco]
TRUNCATE TABLE tablename
```

### Undo recover status

```SQL
USE [master]
GO
ALTER DATABASE [DATABASE_NAME] SET RECOVERY SIMPLE WITH NO_WAIT
GO
```
### Shirink database

```SQL
USE [Qualitor_SebraePR]
GO
DBCC SHRINKDATABASE(N'DATABASE_NAME' )
GO
```

### DROP A USER FROM A DATABASE
```SQL
USE [DATABASE_NAME]
GO
DROP USER [username]
GO
```

### Configure permissions 
```SQL
USE [DATABASE_NAME]
GO
CREATE USER [username] FOR LOGIN [usernameloginsql] WITH DEFAULT_SCHEMA=[dbo]
GO
USE [DATABASE_NAME]
GO
ALTER ROLE [db_datareader] ADD MEMBER [username]
GO
USE [DATABASE_NAME]
GO
ALTER ROLE [db_datawriter] ADD MEMBER [username]
GO
USE [DATABASE_NAME]
GO
ALTER ROLE [db_owner] ADD MEMBER [username]
GO
```
