# HexAI
Hex game with artificial intelligence using Monte Carlo simulation.  
Author: 
 Romain Garnier <rom1{dot}garnier{at}yahoo{dot}fr>.    
Licensing provisions:    
 Apache 2.0 license.  

Compile with  
$ g++ -Wall -Wextra -Wpedantic -Wconversion HexAI.cpp -o HexAI  
Execute as  
$ ./HexAI dimension HumanVsHuman  

Human can play against human if second argument > 0.  
Machine chooses positions in the hex table and computes best move from  
a chosen number of Monte Carlo simulations (minimum 100, default 1000).  
Hex table is showed on terminal with played positions.  
Positions are numbered as a grid.  
 
For Hex board description see https://en.wikipedia.org/wiki/Hex_(board_game)   

X should take left<->right path to win.  
O should take up<->down path to win.  

The human might want to play in first or take machine position.  
Machine might want to take human position if the latest plays first.  

Player should hit (row number enter button, then column enter).  

The algorithm finds shortest paths from src to all other vertices  
with union-find data structure  
(see https://en.wikipedia.org/wiki/Disjoint-set_data_structure)   
