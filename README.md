[README_SESSION14.md](https://github.com/user-attachments/files/32087121/README_SESSION14.md)
# Session 14

## Example 1

```python
file = open("my_playlist.txt", "w")

file.write("Kesariya\n")
file.write("Apna Bana Le\n")
file.write("Heeriye\n")
file.write("Tum Hi Ho\n")
file.write("Chaleya\n")

file.close()

print("Songs successfully saved.")```

### Output

```text
Songs successfully saved.
```

## Example 2

```python
file = open("my_playlist.txt", "r")

for song in file:
    print(song.upper(), end="")

file.close()```

### Output

```text
KESARIYA
APNA BANA LE
HEERIYE
TUM HI HO
CHALEYA
```

## Example 3

```python
import csv

data = [
    ["match", "Team1","Team2","winner"],
    ["match 1","india","australia","india"],
    ["match 2","mumbai","chennai","mumbai"],
    ["match 3","dehli","punjab","punjab"]
]

file = open("ipl_matches.csv","w",newline="")
writer = csv.writer(file)
writer.writerows(data)

file.close()```

## Example 4

```python
import json
data = {

    "username":"ziyan",
    "followers":500
}

file = open("user_profile.json", "w")

json.dump(data,file)

print(data["username"])
print(data["followers"])

file.close()```

### Output

```text
ziyan
500
```

## Example 5

```python
from pathlib import Path

file = Path("zomato_orders.json")

if file.exists():
    print("zomato_orders.json file found.")
else:
    print("zomato_orders.json file not found.")```

### Output

```text
zomato_orders.json file not found.
```
