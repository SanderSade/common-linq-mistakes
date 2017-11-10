
This is a list of regular expressions which help to find LINQ mistakes ([#3](https://github.com/SanderSade/common-linq-mistakes/issues/3)).

## .Single() and .SingleOrDefault()
use: `\.Single(OrDefault)?\(.*\)`

## .First() and .FirstOrDefault()  
use: `\.First(OrDefault)?\(.*\)`

## Empty .Count()
use: `\.Count\(\)`

## Other occurences of .Count()
use: `\.Count\(.*\)`
or in this case `if.*\(.*\.Count\(.*\)\)` might help.

## .Where().First() and .Where().FirstOrDefault()
use: `\.Where\(.*\)\.First(OrDefault)?\(.*\)`

## .Where().Where()
use: `\.Where\(.*\)\.Where\(.*\)`

## .OrderBy().OrderBy()
use: `\.OrderBy\(.*\)\.OrderBy\(.*\)`

## .Select(x => x)
use: `\.Select\((\w)\s*=>\s*\1\)`