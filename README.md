# Astar3d
A simple A* 3D path-finding implementation for java

[Easy A* (star) Pathfinding](https://medium.com/@nicholas.w.swift/easy-a-star-pathfinding-7e6689c7f7b2)  
Recode from [python](https://gist.github.com/Nicholas-Swift/003e1932ef2804bebef2710527008f44#file-astar-py) to java

# Usage

```java
final SimpleWorldProvider worldProvider = new SimpleWorldProvider();
worldProvider.addWall(new Cell(6, 6, 3));
worldProvider.addWall(new Cell(6, 5, 4));

final Pathfinder pathfinder = new Pathfinder(new Cell(10, 7, 7), new Cell(1, 1, -1), Pathfinder.COMMON_NEIGHBORS, worldProvider);
final ArrayList<Cell> path = pathfinder.findPath();
for(Cell cell : path) {
    System.out.println(cell);
}
```