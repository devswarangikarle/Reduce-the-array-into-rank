# Reduce-the-array-into-rank

class ReduceArray:
    def __init__(self, size, elements):
        self.n = size
        self.arr = elements
        self.ranks = [0] * size

    def reduce_to_rank(self):
        indices = list(range(self.n))
        indices.sort(key=lambda i: self.arr[i])

        
        for i in range(self.n):
            self.ranks[indices[i]] = i

    def print_reduced_array(self):
        print(*self.ranks)


n = int(input())
arr = list(map(int, input().split()))


reducer = ReduceArray(n, arr)
reducer.reduce_to_rank()
reducer.print_reduced_array()
