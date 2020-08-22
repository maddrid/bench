# Bench
( Benchmarking / Profiling / Timing ) class to measure the amount of time , memory (server load)  that elapses between two  (or more) points.

## Usage

As Simple as Possible
```php
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
```
Bench::printTimers(true);
```
keep it simple
```
Bench::printTimers();
```
## Get timers
```
Bench::getTimers();
Bench::getTimers(null);
Bench::getTimers(true);
Bench::getTimers(null,5);
Bench::getTimers(true,5);
```
## Stop the timer 
```
Bench::stop('first_point'); 
```
// will get server load
```
Bench::stop('first_point',true);
```
