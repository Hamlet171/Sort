# Sort
Профилирование
Bubblesort
Flat profile:

Each sample counts as 0.01 seconds.
 no time accumulated

| % time       | cumulative | self    | calls   |  self   |  total  | name   |
|--------------|------------|---------|---------|---------|---------|--------|
|	       |    seconds | seconds |		| Ts/call | Ts/call |        |
|--------------|-----------:|--------:|--------:|:--------|:-------:|:-------|
|      0.00    |   0.00     |  0.00   |  343    | 0.00    | 0.00    | swap   |
|      0.00    |   0.00     |  0.00   |    1    | 0.00	  | 0.00    | bubble |
|--------------|-----------:|--------:|--------:|:--------|---------|:-------|

		     Call graph 


granularity: each sample hit covers 4 byte(s) no time propagated

|index % time  | self | children |   called  | name	    |
|--------------|-----:|---------:|----------:|:-------------|
|              |  0.00|    0.00  |  343/343  | bubble [3]   |
|[2]      0.0   | 0.00 |   0.00  | 343       | swap [2]     |
|--------------|-----:|---------:|----------:|:-------------|
|              |  0.00|    0.00  |    1/1    | main [113]   |
|[3]      0.0  |  0.00|    0.00  |    1      | bubble [3]   |
|              |  0.00|    0.00  |  343/343  | swap [2]     |
|--------------|-----:|---------:|----------:|:-------------|

 
----------------------------------------------------------------------------
Insertsort
Flat profile:

Each sample counts as 0.01 seconds.
 no time accumulated

  %   cumulative   self              self     total           
 time   seconds   seconds    calls  Ts/call  Ts/call  name    
  0.00      0.00     0.00      332     0.00     0.00  swap
  0.00      0.00     0.00        1     0.00     0.00  insertSort


		     Call graph 


granularity: each sample hit covers 4 byte(s) no time propagated

index % time    self  children    called     name
                0.00    0.00     332/332         insertSort [3]
[2]      0.0    0.00    0.00     332         swap [2]
-----------------------------------------------
                0.00    0.00       1/1           main [113]
[3]      0.0    0.00    0.00       1         insertSort [3]
                0.00    0.00     332/332         swap [2]
-----------------------------------------------


----------------------------------------------------------------------------
Mergesort
Flat profile:

Each sample counts as 0.01 seconds.
 no time accumulated

  %   cumulative   self              self     total           
 time   seconds   seconds    calls  Ts/call  Ts/call  name    
  0.00      0.00     0.00       42     0.00     0.00  merge
  0.00      0.00     0.00        1     0.00     0.00  mergeSort


		     Call graph (explanation follows)


granularity: each sample hit covers 4 byte(s) no time propagated

index % time    self  children    called     name
                0.00    0.00      42/42          mergeSort [3]
[2]      0.0    0.00    0.00      42         merge [2]
-----------------------------------------------
                                  84             mergeSort [3]
                0.00    0.00       1/1           main [114]
[3]      0.0    0.00    0.00       1+84      mergeSort [3]
                0.00    0.00      42/42          merge [2]
                                  84             mergeSort [3]
-----------------------------------------------


----------------------------------------------------------------------------
Quicksort
Flat profile:

Each sample counts as 0.01 seconds.
 no time accumulated

  %   cumulative   self              self     total           
 time   seconds   seconds    calls  Ts/call  Ts/call  name    
  0.00      0.00     0.00       52     0.00     0.00  swap
  0.00      0.00     0.00        1     0.00     0.00  quicksort
  
       Call graph (explanation follows)


granularity: each sample hit covers 4 byte(s) no time propagated

index % time    self  children    called     name
                0.00    0.00      52/52          quicksort [3]
[2]      0.0    0.00    0.00      52         swap [2]
-----------------------------------------------
                                  35             quicksort [3]
                0.00    0.00       1/1           main [114]
[3]      0.0    0.00    0.00       1+35      quicksort [3]
                0.00    0.00      52/52          swap [2]
                                  35             quicksort [3]
-----------------------------------------------
