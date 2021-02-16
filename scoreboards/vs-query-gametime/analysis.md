
# Question
---
## Which is faster?
#### Query Gametime:
```mcfunction
execute store result score # value run time query gametime
```

## or
#### Scoreboard get:
```mcfunction
scoreboard players add #i value 1
execute store result score # value run scoreboard players get #i value
```

# Answer
---
### Query gametime is ~27.85% slower than scoreboard players get.

Query gametime averages out at 3889 iterations per 50ms while Scoreboard get averages around 5390 iterations per 50ms even with the extra scoreboard add command.

#### Query gametime readout:
![Missing Image!][image-a]

#### Scoreboard players get readout:
![Missing Image!][image-b]

# Extra Context
This question was brought up by Onnowhere while suggesting different, possibly more efficient, solutions to changing an area effect clouds Air tag every tick for a tool called [Animated Java](https://discord.gg/jFgY4PXZfp)

[image-a]: https://github.com/SnaveSutit/minecraft-commands-performance-analysis/blob/main/scoreboards/vs-query-gametime/images/query-game-time-a.png
[image-b]: https://github.com/SnaveSutit/minecraft-commands-performance-analysis/blob/main/scoreboards/vs-query-gametime/images/query-game-time-b.png
