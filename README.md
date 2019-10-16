# SC2 Replay Renamer
A feature-rich StarCraft II replay renamer, inspired by [Burny's SC2 Replay Renamer](https://github.com/BurnySc2/SC2-Replay-Renamer)

## Windows Installation
1. Download the latest version from [Releases](https://github.com/derickboss1/sc2-replay-renamer/releases)
1. Alternatively, you can build from the source by running `build.bat`. With the default configurations, the executable will be located in `dist/`

## Python
1. Download the required modules by running `pip install -r requirements.txt`
1. run `python run.py`

## Features
* Batch renaming of many replays
* Automatic renaming of new replays
* You can also filter by:
  * Custom games
  * Team games
  * Games against AI
  * Games in subfolder that you do not wish to be renamed

## Documentation
`Template` is a string that represents the pattern you wish to name your replay files after. It should contain variables and should make sure every file has a unique name (usually, this can be quickly solved by putting `$uniqueID` somewhere in your `Template` string)

`team` refers to all of the players on a given side. This also applies to 1v1/ladder games

`ladder` refers to all `1v1` games that are not custom. Unranked games are considered `ladder`

### Template Variables
Variable | Explanation | Requires Player ID
---------|---------------|:-----------------:
$myraces |  Races on your team | :heavy_check_mark:
$myrace | same as `$myraces` | :heavy_check_mark:
$WL |  `W` if you won; `L` if you lost (UPPERCASE) | :heavy_check_mark:
$wl |  `w` if you won; `l` if you lost (lowercase) | :heavy_check_mark:
$myteam | Names of players on your team | :heavy_check_mark:
$mymmr | average MMR of your team | :heavy_check_mark:
$oppteam | Names of players on opponent team | :heavy_check_mark:
$oppraces | Races on opponent team | :heavy_check_mark:
$opprace | same as `$oppraces` | :heavy_check_mark:
$oppmmr | average MMR of opponents | :heavy_check_mark:
$t1 | Names of players on team 1 | :x:
$t2 | Names of players on team 2 | :x:
$t1races | Races on team 1 | :x:
$t2races | Races on team 2 | :x:
$t1mmr | Average MMR of team 1 | :x:
$t2mmr | Average MMR of team 2 | :x:
$durationmins | number of minutes of replay (excludes remaining seconds) | :x:
$durationsecs | number of remaining seconds of replay (between 0 and 59) | :x:
$month | Month you played the game (01 to 12) | :x:
$day | Day of month you played the game | :x:
$year | Year you played the game | :x:
$hour | Hour you played the game (00 to 23) | :x:
$min | Minute you played the game (00 to 59) | :x:
$sec | Second you played the game (00 to 59) | :x:
$map | Map you played on (Excludes the LE at the end) | :x:
$mapLE | Map you played on (Includes the LE at the end) | :x:
$gametype | Type of the game (1v1, 2v2, FFA) | :x:
$expansion | WoL, HotS, or LotV | :x:
$uniqueID | unique identifier for your replay to prevent renaming to the same name | :x:


#### Examples
```
$myracesv$oppraces $WL $map $mynames($mymmr) v $oppnames($oppmmr) - $durationminsmins [$month-$day-$year $hour-$min-$sec]
----------------------------------------------------------------------------------------------------------------------------------

Ladder Games = PvT L Thunderbird LE CannonRusher(3500) v TerranPlayer(3535) - 5mins [10-16-2019 10-30-25].SC2Replay
Games with Random = R(T)vT W Acropolis LE RandomTerran(5533) v SaltyTerran(5500) - 15mins [10-16-2019 10-30-25].SC2Replay
Team Games = PTvTZ W Efflorescence LE CannonRusher+SaltyTerran(4500) v TerranPlayer+ZergPlayer(4000) - 20mins [10-16-2019 10-30-25].SC2Replay
```

## Screenshots

## Contributors
* Derick Tseng (derickboss1@gmail.com)