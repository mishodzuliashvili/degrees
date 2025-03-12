# Degrees of Separation

This program determines the "degrees of separation" between two actors by identifying movies they appeared in together.

## How It Works

I developed a breadth-first search algorithm to identify the shortest connection between actors. My approach:

1. The program imports all data regarding actors, movies, and casting information.

2. When two actors' names are entered, it finds the shortest possible connection between them through shared films.

3. The algorithm treats actors as nodes in a graph with movies serving as the connections.

4. To determine the shortest path, I implemented a queue system to track all potential connections, examining them in order of how many connections they require.

## My Implementation

I focused on creating efficient, clean code:

- Selected BFS as it guarantees finding the minimum path between actors
  
- Prevented redundancy by tracking previously examined actors

- Constructed the connection path backward after locating the target actor

- Utilized sets for quicker verification when checking if an actor has been examined

- Implemented early termination to cease searching once the target actor is found

```python
$ python degrees.py large
Loading data...
Data loaded.
Name: Emma Watson
Name: Jennifer Lawrence
3 degrees of separation.
1: Emma Watson and Brendan Gleeson starred in Harry Potter and the Order of the Phoenix
2: Brendan Gleeson and Michael Fassbender starred in Trespass Against Us
3: Michael Fassbender and Jennifer Lawrence starred in X-Men: First Class
```

