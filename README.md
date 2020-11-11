# Programming Project #2 URL: https://github.com/yisheng9/Project2-master
### By Yisheng Huang (PID yisheng9)
This blog will record some of my problems and solutions about the second project. This project consists of two major parts:

  - Process input data in to ListMap
  - Select the best data and output

# Part I Process data

  - I adopted ListMap as my data type.

A few benefits:
  - Can store any data type, mainly string and int
  - "Immutable!"
  - Has all the functions of the list

I first processed the initial data using two string methods and saved them, well, I can also implement all functions with just one line of code, but this is not good for debugging. This step can also delete all non-Chain data for later operations.

# Part II Select the best data
It is mainly divided into two parts, with and without intersection. In theory, they are almost the same except that one line is different. When extracting different cuisine scores and saving them to the map, I think my method is more cumbersome and not suitable for this project, probably because I am not familiar with scala.

### How to Run

Just need to pass the Input to Recommender.scala and the program will work properly:
For example,
```sh
$ scala Recommender Nearby_Restaurants1.csv USER1_Res_His.csv USER2_Res_His.csv USER3_Res_His.csv
Your party should go to: Veil

$ scala Recommender Nearby_Restaurants1.csv USER3_Res_His.csv USER4_Res_His.csv USER5_Res_His.csv
Your party should go to: The Mountainview Grill

$ scala Recommender Nearby_Restaurants4.csv USER4_Res_His.csv USER5_Res_His.csv USER6_Res_His.csv
Your party should go to: The Summer Blossom

$ scala Recommender Nearby_Restaurants1.csv USER1_Res_His.csv USER2_Res_His.csv USER3_Res_His.csv USER4_Res_His.csv USER6_Res_His.csv  USER7_Res_His.csv
Your party should go to: The Mountainview Grill

$ scala Recommender Nearby_Restaurants2.csv USER1_Res_His.csv USER2_Res_His.csv USER3_Res_His.csv USER4_Res_His.csv USER5_Res_His.csv USER6_Res_His.csv
Your party should go to: The Copper Diner
```

# Answer some questions

### Why is * your * functional code cleaner than equivalent procedural/imperative code?
Functional programming uses a lot of functions to reduce code duplication, so the program is shorter and the development speed is faster.
### What are some potential side effects and bugs that are avoided by your functional code?
Functional programming does not depend on and does not change the state of the outside world. As long as the input parameters are given, the returned results must be the same. Therefore, each function can be regarded as an independent unit, which is very conducive to unit testing and debugging, and modular combination.
### Why may functional programming be a good paradigm for data processing in general?
Processing data often requires a lot of CPU time, functional programming can well perform parallel programming.
### What functions/techniques could be used to code a more thorough restaurant recommender?
Big data can be used to recommend and predict new restaurants to users.
### Would you be inclined to learn more functional programming outside of this course if given the chance? Why or why not? Be honest.
Fundamentalistic functional programming cannot even be written in ordinary loops (because the loop has a variable idx or conditional variables), it must be implemented recursively. The result of this is to eliminate all "states". Any "state" is the final result obtained by processing a certain set of functions through a certain input. I think this is a good idea that can help me learn programming languages from a different perspective. So I will definitely learn this way of programming outside of this course.

License
----

MIT
