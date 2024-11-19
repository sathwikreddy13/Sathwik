import sys

def printMST(parent, graph):
    print("Edge \tWeight")
    for i in range(1, len(parent)):
        print(parent[i], "-", i, "\t", graph[i][parent[i]])


def primMST(graph):
    V = len(graph)
    key = [sys.maxsize] * V
    parent = [None] * V
    key[0] = 0
    mstSet = [False] * V
    parent[0] = -1

    for _ in range(V):
        u = min((key[v], v) for v in range(V) if not mstSet[v])[1]
        mstSet[u] = True

        for v in range(V):
            if graph[u][v] > 0 and not mstSet[v] and key[v] > graph[u][v]:
                key[v] = graph[u][v]
                parent[v] = u

    printMST(parent, graph)


if __name__ == "__main__":
    graph = [
        [0, 2, 0, 6, 0],
        [2, 0, 3, 8, 5],
        [0, 3, 0, 0, 7],
        [6, 8, 0, 0, 9],
        [0, 5, 7, 9, 0],
    ]

    primMST(graph)
