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

## Template Documentation
`Template` is a string that represents the pattern you wish to name your replay files after. It should contain variables and should make sure every file has a unique name (usually, this can be quickly solved by putting `$uniqueID` somewhere in your `Template` string)

### Variables
* #### Variables that require Player ID
  |    Variable    |    Output         |
  :---------------:|:------------------:
  |    $myteam     |CannonZ+SaltyTerran|
  |    $myraces    |      PT           |

* #### Variables that do not require Player ID
  |    Variable    |   Output          |
  :---------------:|:------------------:
  


#### Examples
```
$myracesv$oppraces $WL $mapname $mynames($mymmr) v $oppnames($oppmmr) - $durationminsmins [$month-$day-$year $hour-$min-$sec]
----------------------------------------------------------------------------------------------------------------------------------

Ladder Games = PvT L Thunderbird LE CannonRusher(3500) v TerranPlayer(3535) - 5mins [10-16-2019 10-30-25].SC2Replay
Games with Random = R(T)vT W Acropolis LE RandomTerran(5533) v SaltyTerran(5500) - 15mins [10-16-2019 10-30-25].SC2Replay
Team Games = PTvTZ W Efflorescence LE CannonRusher+SaltyTerran(4500) v TerranPlayer+ZergPlayer(4000) - 20mins [10-16-2019 10-30-25].SC2Replay
```

## Screenshots

## Contributors
* Derick Tseng (derickboss1@gmail.com)