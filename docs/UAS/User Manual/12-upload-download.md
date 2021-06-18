## 12. Upload and Download between UAS3 and Instrument

Instrument (SDT340, SDT270 or LUBExpert) functions as slave (so to speak) to the UAS3 software.

That practically means that Instrument receives Database, Work orders, Alarms, and all other
information to work with, from UAS3. Instrument will work with what was uploaded. To make it
simple and practical:

- Instrument can work with one database (Tree Structure) at the time, the one uploaded
- UAS3 uploads one database (Tree Structure) to instrument at the time
- Once database (Tree Structure) uploaded, it contains all information from UAS3 database
- Uploading new database (Tree Structure) deletes existing one in the instrument
- Instrument can “serve” several UAS3 software, always downloading data to same one

In practical operation, when we decide to collect data, inspect or replenish grease, we will upload
that database (Tree Structure) and our instrument is ready to collect data using settings defined in
Tree Structure, store data in exact positions, execute work orders, react to assigned alarms.

Once instrument is connected to UAS3 via USB cable, left click on Device in top toolbar and there are
several actions you can perform:

Instrument update and upgrade functions:

- **Upload key** – when instrument is upgraded with new functionalities, purchased key needs to
    be uploaded, this function enables that
- **Update firmware** – as our users, in case of updates on instrument’s firmware, you will be
    informed to perform update, this function enables that

Database and collected data transfer:

- **Upload from PC to SDT340** – this function performs transfer of database (Tree Structure)
    from your UAS3 to you instrument. It is performed as follows:
       o Power on your instrument and connect it with you PC via USB cable
       o Left click on **Upload from PC to SDT340** and transfer window will pop up

Instrument is properly connected and recognized, and you need to press **Transfer** button.

Following message will pop up every time transfer from PC to instrument is attempted:


In case you have data from previous data collection/inspection, new upload will erase it, so make
sure that data from instrument is downloaded. If it is, press **Ok** and transfer will begin:

Once finished, data transfer confirmation will pop up:

Data is transferred and you are ready for field work (from the data standpoint).

- **Download from SDT340 to PC** – this function performs transfer of collected data from your
    instrument to UAS3. It is performed as follows:
       o Power on your instrument and connect it with you PC via USB cable
       o Left click on **Download from SDT340 to PC** and transfer window will pop up

Instrument is properly connected and recognized, and you need to press **Transfer** button.


Once finished, data transfer confirmation will pop up:

Your collected data is now in UAS3, ready to be overviewed and analyzed.

_NOTE!_ In case following window appears:

Check is instrument is powered on, check connection and click on refresh icon in top right corner.

Do not change database while instrument is collecting data in the field.

In case you are not downloading to same PC where it was uploaded from, and database will not be
recognized, UAS3 will create Rescue Node, so you will not lose your data. Copy data from Rescue
Node and paste to the right place (using backup procedure, explained later).
