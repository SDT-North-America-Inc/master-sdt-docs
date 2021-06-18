## 7. Remote access to a database on a local network

This feature is available since version 3.1862.

### 7.1. Prerequisites

- At least, 2 PC (1 host + 1 client) with distinct licenses of UAS3 V 3.1862 or more recent
    versions, are mandatory. Both are connected on the same network (local or VPN).
- PostgreSQL v13.1 or more recent is running on the host PC (windows sleep settings
    disabled)
- The TCP port 5432 is open on the host PC and static IP address are assumed to be assigned
    on the local network.

### 7.2. Principle

### 7.3. Getting synchronized

- Retrieve the host IP address:

On the host PC, in the search box on the windows taskbar, type **cmd** and press **enter**. In the new screen,
type: **ipconfig /all** and press **enter** and retain the **IP v4 address.**

When UAS3 is running on the host PC, you should see directly the default screen where the location
of the database is identified.


On the client PC, the last IP address will be used as settings to get synchronized with the distant
database.

Launch UAS3 on the client PC then go to **Options/Database settings.** By default, UAS3 is utilizing the
localhost database, assuming PostgreSQL is running.

To change the default settings, tick **advanced settings** then **type the IP address** determined at the first
step (192.168.0.17 for this example).

If the settings are correct, UAS3 will automatically restart.

You can now verify that the synchronization is well established with the distant host. In the default
screen of UAS3 Client, you can browse and open the distant tree structure (ex: test_340dB), where the
client is now synchronized.


### 7.4. Notes

- Both client and host can interact simultaneously with the same database. A pop-up
    system informs in real time about the changes and invite the passive user to refresh the
    tree structure.
- A distant client can interact with the host database while UAS3 is not running on the host
    PC. Only PostgreSQL Database server is always required to ensure the synchronization.
- Each time UAS3 is launched, the distant client and the host retrieve the last updated
    database.
- An auto-reconnection system ensures the continuity of the distant service.


```
Navigation
```
**Graph Pane** (^) **Picture Pane
Top Pane Bottom Pane**^
**Top toolbar**