# Bench
Benchmark class to measure the amount of time , memory   that elapses between two  or more checkpoints.
 ### Usage 

 As Simple as Possible

```
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
 ### Display 
more details
```
Bench::printTimers(true);
```
keep it simple
```
Bench::printTimers();
``` 
 ### Get timers 

```
Bench::getTimers();
Bench::getTimers(null);
Bench::getTimers(true);
// 4 is the decimal precision
Bench::getTimers(null,4);
Bench::getTimers(true,9);
``` 
``` 
 ### Stop the timer 

```
Bench::stop('first_point');
```
// will get server  load
```
Bench::stop('first_point',true);

``` 
