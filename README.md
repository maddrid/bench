# Bench
( Benchmarking / Profiling / Timing ) class to measure the amount of time , memory (server load)  that elapses between two  (or more) points.
## Install
```
"require": {
   "maddrid/bench": "dev-master"
  }
```
## Usage

As Simple as Possible
```php
use Maddrid\Bench as Bench ;

Bench::start('first_point');
  do_some_math
    Bench::start('second_point');
      do_more_math
    Bench::stop('second_point');
    Bench::start('third_point');
      do_more_math
    Bench::stop('third_point');
Bench::stop('first_point');
 ```

## Display

//more details
```php
Bench::printTimers(true);
```
keep it simple
```php
Bench::printTimers();
```
## Get timers
```php
Bench::getTimers();
Bench::getTimers(null);
Bench::getTimers(true);
Bench::getTimers(null,5);
Bench::getTimers(true,5);
```
## Stop the timer 
```php
Bench::stop('first_point'); 
```
// will get server load
```php
Bench::stop('first_point',true);
```
## Known facts
When getting server load 
```php
Bench::stop('first_point',true);
```
 Will add aditional 2 seconds on the checkpoint . If  checkpoint is nested , "the Parent/s " checkpoints will inherit those 2 seconds .
