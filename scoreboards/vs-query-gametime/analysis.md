
# Question
---
## Which is faster?
#### Query Gametime:
```
execute store result score # value run time query gametime
```

## or
#### Scoreboard get:
```
scoreboard players add #i value 1
execute store result score # value run scoreboard players get #i value
```

# Answer
---
Query gametime is ~27.85% slower than scoreboard players get.

Query gametime averages out at 3889 iterations per 50ms while Scoreboard get averages around 5390 iterations per 50ms even with the extra scoreboard add command.

![Missing Image!](https://github.com/SnaveSutit/minecraft-commands-performance-analysis/blob/main/scoreboards/vs-query-gametime/images/query-game-time-a.png?raw=true "Query Gametime performance")

![Missing Image!](https://github.com/SnaveSutit/minecraft-commands-performance-analysis/blob/main/scoreboards/vs-query-gametime/images/query-game-time-a.png?raw=true "Scoreboard get performance")
