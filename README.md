# Rubik's Cube(s) Solver
2 layers is done, still working on 3 layers

2 layers: applying the idea "meet in the middle." The god number for a pocket cube is 14 for quarter turns, which means in every permutation of the cube it takes an maxinum number of 14 steps to solve it. Thinking about the limited steps, if bruteforce all possible moves it would take $O(14^(12))$ which is still a massive amount; however applying the idea "meet in the middle", it shrinks the time complexity to $O(7^12))$ plus cutting edge, which is very viable. 

Basically, the idea is we separate the 14 steps into 2 parts -- 7 steps starting from the complete cube and mark the stages, and 7 steps starting from the scrambled cube. It continues searching until it encounters a stage that was mark prevously, which is the answer.

NOTE: because the code writer has a limited knowledge of this field, he(I) uses(use) STI -> map in cpp to mark visited. Note that the time complexity for seaching and setting for the STL is $O(logn)$, which significantly(a bit) increases the time complexity since it needs to operate so many times. IF could come up with a better hashing method for a stage of a cube, it could be faster. 

Currently it takes about 5 seconds to generate a solution for a scrambles cube. 
