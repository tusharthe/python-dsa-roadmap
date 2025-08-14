# Intensive 6-Week Python DSA Roadmap
*From Basic Python to DS/AI Ready*

## Overview
**Timeline**: 6 weeks (can be compressed to 4-5 weeks with extra dedication)
**Daily Commitment**: 3-4 hours
**Goal**: Master core DSA concepts for Data Science & AI interviews

---

## Week 1: Foundation + Arrays & Strings

### Day 1-2: Complexity Analysis & Python DSA Essentials
**Theory (1 hour)**
- Big O notation deep dive
- Python-specific optimizations for DSA
- Essential Python libraries: `collections`, `heapq`, `bisect`, `itertools`

**Python DSA Setup**
```python
# Essential imports to master
from collections import defaultdict, Counter, deque
import heapq
import bisect
from itertools import permutations, combinations
```

**Resources**
- **Video**: [Big O Notation - CS Dojo](https://www.youtube.com/watch?v=D6xkbGLQesk)
- **Practice**: [Python Collections Module](https://docs.python.org/3/library/collections.html)

### Day 3-4: Arrays & Two Pointers
**Core Problems (15+ problems)**
- Two Sum, Three Sum, Four Sum
- Container With Most Water
- Trapping Rain Water
- Remove Duplicates from Sorted Array
- Move Zeros

**Python-Specific Techniques**
- List comprehensions for filtering
- `enumerate()` for index tracking
- Slicing tricks: `arr[::-1]`, `arr[::2]`

**GitHub Resource**: [Python Array Algorithms](https://github.com/TheAlgorithms/Python/tree/master/sorts)

### Day 5-7: String Manipulation & Sliding Window
**Core Problems**
- Longest Substring Without Repeating Characters
- Minimum Window Substring
- Valid Anagram
- Group Anagrams
- Palindromic Substrings

**Python String Mastery**
- `str.join()` vs `+=` performance
- `ord()` and `chr()` for character manipulation
- String slicing and indexing tricks

---

## Week 2: Linked Lists + Stacks & Queues

### Day 8-10: Linked Lists
**Implementation Focus**
```python
class ListNode:
    def __init__(self, val=0, next=None):
        self.val = val
        self.next = next
```

**Core Problems (12+ problems)**
- Reverse Linked List (iterative & recursive)
- Merge Two Sorted Lists
- Remove Nth Node From End
- Linked List Cycle I & II
- Intersection of Two Linked Lists

**Advanced**: Doubly Linked List for LRU Cache

### Day 11-14: Stacks & Queues + Hash Tables
**Stack Problems**
- Valid Parentheses
- Daily Temperatures
- Largest Rectangle in Histogram
- Evaluate Reverse Polish Notation

**Queue Problems**
- Implement Stack using Queues
- Moving Average from Data Stream

**Python Collections Deep Dive**
```python
from collections import deque, defaultdict, Counter
# deque for O(1) operations on both ends
# defaultdict for cleaner code
# Counter for frequency counting
```

**Hash Table Problems**
- Design HashMap
- Subarray Sum Equals K
- Longest Consecutive Sequence
- Word Pattern

---

## Week 3: Trees (Critical for ML)

### Day 15-17: Binary Trees Fundamentals
**Implementation**
```python
class TreeNode:
    def __init__(self, val=0, left=None, right=None):
        self.val = val
        self.left = left
        self.right = right
```

**Core Problems (15+ problems)**
- Tree Traversals (Preorder, Inorder, Postorder, Level Order)
- Maximum Depth of Binary Tree
- Validate Binary Search Tree
- Lowest Common Ancestor
- Binary Tree Right Side View
- Serialize and Deserialize Binary Tree

**Python Tree Techniques**
- Recursive vs iterative approaches
- Using `deque` for level-order traversal
- Stack simulation for iterative traversals

### Day 18-21: Advanced Trees
**Binary Search Trees**
- Insert into BST
- Delete Node in BST
- Kth Smallest Element in BST

**Tries (Important for NLP)**
```python
class TrieNode:
    def __init__(self):
        self.children = {}
        self.is_end_word = False
```
- Implement Trie
- Word Search II
- Design Add and Search Words Data Structure

**Why Trees Matter for AI**: Decision trees, parsing, hierarchical data in ML

---

## Week 4: Graphs + Recursion/Backtracking

### Day 22-24: Graph Algorithms
**Implementation**
```python
# Adjacency List representation
graph = defaultdict(list)

# BFS Template
def bfs(start):
    queue = deque([start])
    visited = set([start])
    
# DFS Template  
def dfs(node, visited):
    if node in visited:
        return
    visited.add(node)
```

**Core Problems (12+ problems)**
- Number of Islands
- Clone Graph
- Course Schedule I & II
- Word Ladder
- Network Delay Time
- Minimum Spanning Tree (Kruskal's/Prim's)

### Day 25-28: Recursion & Backtracking
**Core Problems**
- Generate Parentheses
- Letter Combinations of Phone Number
- N-Queens
- Sudoku Solver
- Permutations & Combinations
- Word Search

**Python Recursion Optimization**
- `sys.setrecursionlimit(10000)` when needed
- Memoization with `functools.lru_cache`

---

## Week 5: Dynamic Programming (Essential for ML)

### Day 29-31: 1D DP
**Core Problems (10+ problems)**
- Fibonacci Numbers
- Climbing Stairs
- House Robber I, II, III
- Coin Change
- Longest Increasing Subsequence
- Decode Ways

**Python DP Patterns**
```python
# Bottom-up approach
dp = [0] * (n + 1)

# Top-down with memoization
@lru_cache(maxsize=None)
def solve(n):
    # recursive solution
```

### Day 32-35: 2D DP
**Core Problems**
- Unique Paths I & II
- Minimum Path Sum
- Edit Distance
- Longest Common Subsequence
- 0/1 Knapsack
- Maximum Square

**Why DP Matters for AI**: Optimization problems, reinforcement learning, sequence modeling

---

## Week 6: Advanced Topics + Interview Prep

### Day 36-38: Heaps & Advanced Data Structures
**Heap Problems**
- Kth Largest Element
- Top K Frequent Elements
- Merge K Sorted Lists
- Find Median from Data Stream

**Python Heapq Mastery**
```python
import heapq
# Min heap by default
# For max heap: use negative values
```

**Union-Find**
- Number of Connected Components
- Redundant Connection

### Day 39-42: Final Sprint + Mock Interviews
**Daily Practice**
- 5-7 problems per day
- Mix of all topics covered
- Timed practice (30-45 min per problem)
- Mock interview problems

---

## Python-Specific DSA Libraries & Tricks

### Essential Imports
```python
from collections import defaultdict, Counter, deque, namedtuple
from functools import lru_cache
import heapq
import bisect
from itertools import permutations, combinations, accumulate
import sys
```

### Performance Tips
```python
# Fast input for competitive programming
input = sys.stdin.readline

# Increase recursion limit
sys.setrecursionlimit(10000)

# Use list comprehension over loops
result = [x*2 for x in nums if x > 0]

# Use enumerate for index tracking
for i, val in enumerate(arr):

# Binary search with bisect
bisect.bisect_left(arr, target)
```

---

## Daily 3-4 Hour Schedule

### Morning Session (1.5-2 hours)
- **30 min**: Theory/concept learning (videos/reading)
- **60-90 min**: Implement new data structure/algorithm from scratch
- **15 min**: Quick review of previous day

### Evening Session (1.5-2 hours)
- **60-90 min**: Solve 3-5 practice problems
- **30 min**: Review solutions, optimize code
- **15 min**: Plan next day's topics

### Weekend Intensive
- **Project day**: Build something substantial
- **Mock interview**: Practice explaining solutions
- **Weak topic review**: Revisit challenging concepts

---

## Curated Resource List

### Primary Video Resources
1. **[NeetCode](https://www.youtube.com/c/NeetCode)** - Best LeetCode explanations (Python)
2. **[Back to Back SWE](https://www.youtube.com/channel/UCmJz2DV1a3yfgrR7GqRtUUA)** - Interview focused
3. **[Tushar Roy](https://www.youtube.com/user/tusharroy2525)** - DP and graph algorithms

### GitHub Resources
1. **[TheAlgorithms/Python](https://github.com/TheAlgorithms/Python)** - Clean Python implementations
2. **[keon/algorithms](https://github.com/keon/algorithms)** - Minimal, clean Python code
3. **[donnemartin/interactive-coding-challenges](https://github.com/donnemartin/interactive-coding-challenges)** - Jupyter notebooks

### Practice Platforms (Priority Order)
1. **LeetCode** - Primary platform (aim for 200+ problems)
2. **HackerRank** - Good for basic concepts
3. **CodeSignal** - Interview simulation

---

## Weekly Milestones

### Week 1: ✅ Foundation Strong
- Master Big O analysis
- Comfortable with arrays/strings
- Python collections library fluency

### Week 2: ✅ Linear Data Structures
- Implement all basic structures from scratch
- Solve 50+ easy-medium problems
- Hash table patterns mastered

### Week 3: ✅ Tree Mastery
- All tree traversals memorized
- BST operations fluent
- Trie implementation solid

### Week 4: ✅ Graph & Backtracking
- BFS/DFS templates memorized
- Graph problems confidence
- Backtracking patterns understood

### Week 5: ✅ DP Proficiency
- 1D and 2D DP patterns clear
- Optimization thinking developed
- Memoization vs tabulation mastered

### Week 6: ✅ Interview Ready
- Mixed problem solving fluency
- Advanced data structures comfort
- Explanation skills polished

---

## Projects for Portfolio (DS/AI Relevant)

### Week 2: **Data Structure Visualizer**
- Build web app visualizing arrays, linked lists, stacks, queues
- Use Python backend with simple frontend

### Week 3: **Tree-based Decision System**
- Implement decision tree from scratch
- Visualize decision paths

### Week 4: **Graph-based Recommendation System**
- Build simple recommendation engine using graphs
- Implement collaborative filtering basics

### Week 6: **Algorithm Performance Analyzer**
- Compare sorting algorithms performance
- Visualize Big O complexities
- Prepare for ML algorithm complexity understanding

---

## Success Metrics

### Daily Targets
- **Problems solved**: 3-5 per day
- **New concepts**: 1-2 per day
- **Code written**: 200-300 lines per day

### Weekly Targets
- **Total problems**: 25-35 per week
- **Implementation projects**: 1 per week
- **Mock interviews**: 2 per week (weeks 4-6)

### Final Target (Week 6)
- **Total problems solved**: 200+ (LeetCode equivalent)
- **Medium problems comfort**: 70%+ success rate
- **Interview readiness**: Can solve medium problem in 30 minutes
- **DS/AI foundation**: Ready for pandas, numpy, scikit-learn

---

## Transition to DS/AI After DSA

### Immediate Next Steps
1. **NumPy**: Arrays manipulation (your DSA arrays knowledge applies directly)
2. **Pandas**: DataFrames (hash tables and indexing concepts)
3. **Algorithm Complexity in ML**: Understanding training time complexity
4. **Tree-based ML**: Decision trees, random forests
5. **Graph-based ML**: Network analysis, recommendation systems

### Why This DSA Foundation Helps
- **Algorithm thinking**: Critical for ML algorithm selection
- **Optimization mindset**: Essential for model tuning
- **Data structure knowledge**: Crucial for efficient data preprocessing
- **Problem decomposition**: Key skill in ML pipeline design

Start Week 1 immediately - the intensive nature means momentum is crucial. You've got this! 🚀
