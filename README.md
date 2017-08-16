# DM der Clubklasse 2017

Tracking-Link: <http://glidertracker.org/#nowelcome&lst=https://raw.githubusercontent.com/kerel-fs/gliding_tasks/master/2017-DM-club/tracking.csv>

# Examples
## OGN-DDB to trackingCSV
```
import csv
import sys

with open("./2017-DM-club.csv", 'r') as f:
    reader = csv.reader(f, quotechar="'")
    print("ID,CALL,CN,TYPE")
    for row in reader:
        print(",".join(["06" + row[1],row[3], row[4], row[2]]))
```

## JSON-Task
```
{"tasks": [
    {"name": "15m", "color": "0000FF", "legs": [ [47.3,1.55],[48.2,2.3],[30000],[47.5,-1.3],[50000],[47.3,1.5] ] },
    {"name": "standart","color": "FFFF00","legs": [ [47.2,1.55],[46.5,2.3],[46.5,-0.2],[47,-0.2],[47.2,1.5] ] },
    {"name": "open","color": "FFFFFF","legs": [ [47.25,1.6],[48,3],[46,3],[47.22,1.6] ],
    "wlist": ["DD1111", "DD2222", "DD3333", "DD4444"]}
]}
```
