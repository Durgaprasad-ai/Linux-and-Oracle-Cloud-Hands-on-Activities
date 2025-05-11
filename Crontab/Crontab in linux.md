## Cron 
>  cron is background daemon which executes the tasks or jobs at specified intervals.

## Crontab
> **Crontab** stands for **cron table** is a configuration file which tells cron to when to execute the tasks specified in the crontab file.

## Cronjob
> The tasks that are being scheduled are known as cronjobs.


## How Cron works 
> -- Cron daemon runs in the background and checks the crontab file every minute.

> -- When the current time matches with the specified time line in the crontab file, It will execute the associated tasks.


## Structure of the crontab entry :

    *   *   *   *   *
    |   |   |   |   |______________  Day of Week (0-7) 
    |   |   |   |__________________  Month(1-12)
    |   |   |______________________  Day of Month (1-12)
    |   |__________________________  Hour(0-24)
    |______________________________  Minute(0-59)


## Purpose of Crontab

> **System Maintenance :**
>
>        - clear logs, cache, temporary files
>
>        - Update system packages or software
>
> **Backup Automation :**
> 
>        - Scheduling the daily, weekly, monthly backups for databases or files.
>
> **Monitoring and Reporting :**
> 
>        - Running scripts to check system health and disk space
>
>        - Sending emails alerts or logs.
>
> **Running Scripts :**
> 
>        - Automating the python, bash, any other scripts at scheduled times.


## **Options for Structure :**
>
>  **'*'** - The asterisk operator means any value or always. If you have '*' in the hour field, it means the task will be executed for every hour.
 
> **','** - The comma operator will allows you to specify multiple values. If you have '1,3,5' in the hour field, it means the task will be executed at 1am, 3am and 5am.

> **'-'** - The hyphen operator will allows you to specify range of values. If you have '1-5' in the day of week filed, it means task will be executed from monday to friday.

> **'/'** - The slash operator will allows you to specify values repeated over certain interval between them. If you have '*/4' in the hour field, It means task will be executed for every 4 hours.
