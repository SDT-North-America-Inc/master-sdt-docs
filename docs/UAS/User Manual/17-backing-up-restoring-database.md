# 17. Backing up and Restoring Database

Data contained in UAS3 can be backed up and restored, for two main purposes. First is to save a backup of your data in case of mishap. Second reason is to share data with another user, whether a colleague in your team or a consultant for support.

## Backing up Full UAS Database

UAS3 is creating a backup of database with all its details. Entire Tree Structure, all Settings, all Alarms, all Measurements.

UAS3 is backing up a Data Folder as a minimum unit of backup, with its entire content.

Click on **Utilities/Database/Backup/Full UAS Database** in top toolbar, as shown below:

![image](images/missing.png)

Following window will pop up:

![image](images/missing.png)

!!! note
    In case that **Backup All Data Folders** is checked, all data folders (entire content of your UAS3) will be backed up. This is very useful to do on regular basis and preserve your data in case of mishap.

If you want to backup only one Data Folder, for purpose of sharing with you colleagues or with consultant/support, uncheck this field, as below:

![image](images/missing.png)

Now, only displayed Data Folder will be backed up [test 340 (450177119) (SDT340)]. By clicking on arrow next to the Data Folder name, drop down menu will enable you to choose any other folder.

In next step, choose destination and name for your backup file, by pressing , and press **Backup**

![image](images/missing.png)

Your backup has been created.

***Note***

If you want to create a backup of a Tree Structure that is within a Data Folder containing other different Tree Structures, or you want to backup only a part of the Tree Structure, you can do following:

- Create a new Tree Structure in new Data Folder
- Copy nodes from Tree Structure you want to backup (Structure only, or with Data, depending what you want to backup and share)
- Paste Nodes in newly created Tree Structure in new Data Folder
- Backup new Data Folder

As shown below:

![image](images/missing.png)

Copied Node is now in new Tree Structure within new Data Folder. Now you can backup the new Data Folder and it contains only what you intended to share.

Your backup file is ready to be sent:

![image](images/missing.png)

## Restoring Full UAS Database

When you need to restore backup in your UAS3, click on **Utilities/Database/Backup/Full UAS Database in top toolbar** , as shown below:

![image](images/missing.png)

Warning window will pop up, and it is always good to make a backup of your data first, of course

![image](images/missing.png)

Once you confirm, Restore Database window will pop up:

![image](images/missing.png)

By pressing '...', locate the backup file and select it. Then press **Restore**.

![image](images/missing.png)

Open your Data Folders and look for restored folder.

## Export XML, Tree Structure or Tree Structure & Measurements

This function enables you to export tree structure only or export it with selected measurement data.
This becomes very useful when operation is running on several different locations and regular refreshment of data in supervisor’s or analysts’ database is needed, as well as in all cases when data needs to be shared on regular basis without need to send large files.

Click on **Utilities/Database/Backup/Export XML** in top toolbar, as shown below:

![image](images/missing.png)

And choose if you want to export Tree Structure only, or Tree Structure + Measurement data

Exporting Tree Structure will do exactly that, export only tree structure, without any measurement data, and it can be restored in any UAS3 software:

![image](images/missing.png)

Select a File path and backup your data.

Exporting Tree Structure + Measurement data will export Tree Structure, but it will also include measurement data that you select to export.

Various tools are available to help you select data you need to export and backup.

You can select option to backup selected measurements and select them individually or using filter.

You can also select to export, and backup measurements filtered by date.

Once you export and backup your data, it is ready to be sent and restored in another UAS3 software.

!!! note
    In case that exported tree structure and import target tree structure are not identical (target tree structure was altered), difference will be overwritten by import or additional nodes will be added, and measurement data will be inserted. To make sure that everything runs smoothly, and any possible confusion is avoided, use “login users” function and assign rights to each user in regard to administrate, write or read only. That way, you can be sure that tree structures in multiple locations will be the same, and data will be easily updated with simple export/import.
