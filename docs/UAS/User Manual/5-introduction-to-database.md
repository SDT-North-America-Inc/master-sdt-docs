## 5. Introduction to Database/ Tree Structure

### 5.1. Database definition

UAS3 is fundamentally used as a Database to manage your collection, processing, and analysis of
data. A database is an integrated collection of logically related records or files consolidated into a
common pool that provides data for one or more multiple uses. It is used to store and organize
information in such a way as to make it easy to retrieve.
Imagine a library where you know all the books you need are located but you have no logical way of
finding them – it would be a nightmare. In the same way, many databases are created in such a way
that only their creator knows how to find information. As predictive maintenance departments are
typically comprised of team members relying on integrated data, this would not be a good database.

### 5.2. Tree structure definition

UAS3 uses hierarchical database model in which the data is organized into a tree like structure. The
content could be data collected with the SDT340, SDT270 or LUBExpert, comments, events, statuses,
or external document.

The tree structure is the way of representing the hierarchical nature of the Database. It is named a
tree structure because the representation looks like a tree. In this type of structure, The Database
name, also called the Database root, is the top of the tree structure and the Measurements, also
called the ''leaves", are at the end. A Measurement is the combination between a sensor choice and
Measurement settings. The branches between the Database name and the Measurements
Categories are called Nodes.

(^) ❶ Database Root
❷ Node
❸ Measurement

#### 5.2.1. Node

Node is a position in a tree between the database root and the Measurement. Each node has a unique
parent (their upper level) and can have multiple child (their lower levels).
UAS3 database can effectively contain a virtually unlimited number of nodes, regarding your computer
storage capacity.

#### 5.2.2. Measurement

The Measurement combines a sensor choice (by example the Needle RS1 or Parabolic dish) and a set
of specific parameters (by example Static or Dynamic measurement, the Mixer Frequency, the
bandwidth).
For each measurement point, you can decide the type of sensor you want to use. SDT340, SDT
work with a variety of different sensors like Airborne and Structure borne Ultrasound probes,
Accelerometer, Tachometer, Thermometer. LUBExpert works with one single sensor – LUBESense1.

##### ❶

##### ❷

(^) ❸


However, the notion of sensor type is not sufficient for reliable comparison of data. For example, an
RMS calculated between 10 and 1000 Hz is not comparable to an RMS calculated between 10 and
10000 Hz. This is the reason why, UAS3 adds, to the sensor type, the parameters associated to the
measurement.
Measurement is the end leave of the tree structure.
Consequently, no sub level can be assigned to a Measurement.

The Measurement name is generated automatically by UAS3, when it is created, regarding your
selection.
Measurements can be **Static** or **Dynamic**.

**Static measurement**

A static measurement is one which is purely a single numerical value - a dBμV value (RMS, maxRMS
or Peak), linear value of ratio (Crest Factor), RMS velocity, Peak acceleration ... or a temperature are
all static measurements.
Static measurements can be collected using either the SDT340, SDT270 or LUBExpert.
These values are normally logged for trending or alarm comparison.

**Dynamic measurement**

A dynamic measurement is entire event recorded during defined data acquisition time, represented
as Time domain or Frequency domain.
An example of dynamic measurement would be a recording of the ultrasonic signal from a bearing,
or a recording of the collection of close and purge phases of a steam trap.

This type of measurement would normally be analyzed by viewing and processing the time signal of
perhaps the spectrum of the signal in UAS3.

### 5.3. Structure of a good database

A considerable amount of thought should go into the structure of your database. Spending some
time in detailed consideration of nomenclature and organizational structure, will help you to develop
your database in the right way today.

##### NOTE!

_It is highly recommended to introduce several assets into your database, and work with it for day or
two, in different situations, performing different tasks. If you are not completely satisfied, edit it, try it
again. Once you are satisfied and tree structure is correctly reflecting organizational structure and it
is suitable for required tasks, continue. Do not put yourself in a position of introducing 1000 assets
and realizing then that it should be organized differently._

It may be that you have already been through this process with the development of your
computerized maintenance management software (CMMS) database in which case you are likely to
be using the same database structure in UAS3.
If you are not familiar to this topic, here are some issues to consider.
Consider when you are filling in an address form.
There can be several levels of information needed to define your address:

- Country.
- State, Province or Region
- Town or City name
- District name
- Street or road name
- House or Apartment number


The database required to manage all this data would require 6 levels in order to fully describe the
location of each house or apartment.

Notice how the structure starts at the top, with the country, and moves down becoming more
specific, or localized, with each lower level.

Consider how you might want to organize and search through this database to:

- Find a particular house on a particular street.
- Find all houses on that street
- Find all the streets in a particular district with the same name

An important function of the database then, is to organize the data into a hierarchical structure – this
is what we call a tree.
Using UAS3, you can create multiple databases. Each database is characterized by its name and has
its own tree structure. In a tree structure model, the database name is equivalent to the database
root.
The number of databases is limited only by your computer storage capacity.
You cannot open simultaneously several databases. One logical unit (process, location...) should be in
one database/tree structure. You can upload only one database at the time in the SDT340, SDT270 or
LUBExpert. This is additional reason to create your database with logical nature of work in mind.

### 5.4. Number of levels

Inside UAS3 databases, you can organize the tree with a maximum of 6 levels. This means, 6
additional levels below your tree structure name. Final level (whether it is 2nd, 3rd, ... or 6th) allows
you to define a measurement (sensor type, measurement settings). This is just to avoid confusion
that might appear when counting levels (it could look like 8 if includes tree structure name and
sensor/measurement level). This should be more than enough for most applications and will
generally be more than is used by your CMMS program.
Careful consideration should be given to the use of these levels to maximize your ability to locate and
describe a measurement point within your plant. Tree structure is there to make you do your job
easily, so it needs to be built in a way that allows you to search, filter or view asset groups and assets
in easiest way.

Whilst we have 6 levels, you do not need to use all 6 all of the time. If you can define your
measurement point location at 2nd, 3rd or 4th level, that is all you need to create. There is no
requirement to invent levels just to make it up to 6. UAS3 is flexible enough to identify
measurements wherever they may be in the tree structure which gives you tremendous flexibility in
your database design.

```
The SDT270 and LUBExpert Database is identical to that of UAS3, but its screen can display only 5
levels at the time. SDT340 will display all levels defined in UAS3.
```
### 5.5. Choice of a reliable naming

In UAS3 database, as in most databases, the use of upper, lower case and space character can be
used as a distinguishing characteristic which can be used to filter through large amounts of data
quickly:

- Pump 1 is not the same as pump1.
- Pump1 is not the same as pump 1.
- Non-driven bearing is not the same as Nd bearing or/and bearing.


Being consistent is critically important when you are creating a database. It helps you to keep track
and it helps the database search engine to find what you are looking for in future. It is important that
you develop a standardized naming system and stick to it.
Think of terms you can use within your own plant or organization which will convey meaning.
Abbreviation is often required, so make sure that the abbreviations you use are consistent and
understood by all involved.
Consistency between the maintenance department and operators is also important. If you have a
conveyor feed into a zoned oven for example, do you number the Recirc fans from the infeed end
forward or from the outfeed end backwards? Is your system consistent with what the operators call
them?

One simple naming system is to use capitals for Areas, Processes, Functions (Recirc Fan, Boiler Feed
Water Pump) and lower-case letters for components inside one of these functional units (motor,
pump, fan, gearbox, bearing).
You might want to add a suffix that might help you easily filter assets according to certain criteria (as
an example; electrical motor GL, where GL stands for Grease Lubricated, or exhaust fan OL, where OL
stands for Oil Lubricated) and extract only assets that you need for certain task.

### 5.6. Considerations for Database construction

As you add more and more information, data, and measurements to any predictive maintenance
database, the value and the cost of the database increases. That value is based upon the knowledge
locked away inside it about the reliability of components, systems and methods used in your plant.
Cost related to database represents hundreds of ours invested to populate it.
Both value and cost are high, so make sure you built it in a way that will deliver benefit.

As you build your database then, plan ahead a little bit by putting information in now which will
make it easy for you to do some digging in the future. Consider some of these real-life database
searches and their implications in the database construction. In example, show me:

- Bearings mounted next to belt pulleys.
- Drive end bearing of all 15kW motors on site.
- Pump drive end bearing.
- Conveyor roll bearings using ABC grease.

One way to build an efficient database is to:

- Regroup all identical equipment into one branch level (or Node).
- Regroup equipment from a process function into one branch level.
- Avoid regrouping machines regarding survey routines.
