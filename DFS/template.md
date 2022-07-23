## DFS template
```
def dfs():
    # check
    1. ending condition
    2. previously visited or not
    // OUT: out of index
    if (!inArea(image, x, y)) return;
    // CLASH: meet other colors, beyond the area of origColor
    if (image[x][y] != origColor) return;
    // VISITED: don't visit a coordinate twice
    if (visited[x][y]) return;
    visited[x][y] = true;
    image[x][y] = newColor;
    ##DFS to other paths
    dfs(x - 1, y); // up
    dfs(x + 1, y); // down
    dfs(x, y - 1); // left
    dfs(x, y + 1); // right
```