# Restore SQL database in AWS RDS SQL instance

## Setting Up for Native Backup and Restore

AWS RDS SQL instance doesn't support backups from file system. So, you need to create an S3 bucket to place your SQL backups.

Secondly, you need to have an AWS IAM role to access the bucket.

Finally, SQLSERVER_BACKUP_RESTORE option should be added to an option group on your DB instance.

## Restore backup command

```t-sql
exec msdb.dbo.rds_restore_database
        @restore_db_name='AdventureWorks',
        @s3_arn_to_restore_from='arn:aws:s3:::contoso-database-backups/staging/AdventureWorks.bak';
```

## Database backup status command

```t-sql
exec msdb.dbo.rds_task_status
```