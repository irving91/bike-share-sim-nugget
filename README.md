# bike-share-sim-nugget

This project is all about simulation and optimization. Here we're pulling data for over 1.5 million journeys accross 700+ docking stations in London's bike share network and asking two simple questions: 
1) How can we estimate the number of bad experiences occuring for customers?
2) How can we optimize this system?

In order to answer these questions, we first need to define what we mean by bad experiences. Bad experiences here come in two forms - either a customer tries to rent a bike at a station which is empty, or tries to return a bike at a station which is full. Whether either one of these things happens is in turn a function of docking station inventory,     capacity, and random demand at each station over a given period of time. In more formal terms, we need to model the random variables of customers arriving and departing from stations with fixed capacity (a constriant of this problem) for the purpose of estimating the expected values for bad experiences. This is possible using a stochastic simulation method (i.e. simulating interactions many thousands of times). Bike inventory levels at the start of each defined period of time for each station here represent our decision variable. By iterating over all the possibilities, we can determine what the optimal inventory levels are for each station at the start of each defined period of time.
