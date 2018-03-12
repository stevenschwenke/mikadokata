# Mikado Method
## Problem
![](images/mikado_1.png)

Problem: a simple refactoring ...

![](images/mikado_2.png)

... leads to another necessary refactoring

![](images/mikado_3.png)

That way, a tree of dependent refactorings is created 

Solution: only handle one issue at a time

## Algorithm
1. attempt refactoring
2. run into some issue
3. write down information about issue in a graph (first refactoring = parent, new issue = child)
4. revert all changes
5. begin refactoring issue => 1. step 
6. repeat until all issues are doable (= leaves of the graph)
7. refactor issues from leaves to the root of the graph

![](images/mikado_4.png)

With this algorithm, the tree will be resolved by doing one tiny refactoring after the other, ...

![](images/mikado_5.png)

... until the first refactoring can be implemented without problems. 

## Exercises
Taken from [Mikado method examples and exercises](https://github.com/mikadomethod), [here](spaceExercise/README.md) are three exercises for the method, including a sample codebase. 

## Tipps
- Use simple, digital means to "draw" the graph, for example plain text with indentation as levels. Paper doesn't scale well.
- task notation: [ ] for open tasks, [X] for closed tasks 
- (huge) Mikado graph can be processed over time instead of in one huge leap. Attention: Too much time = possible changes in graph due to changed codebase 

## Application
- common trap: thinking to complicated, doing multiple tasks "in parallel" (not possible!)
- method very useful for error tracking, debugging and explorative testing
- very useful for longer analysis
- "I know that I forgot something, but I don't know what ..." - bad feeling!
- Guy that does your code reviews will be happy about smaller commits!
- Drawing forces different thinking processes.

## Sources
- Stefan Lieser "Die Mikado Methode" ([youtube](https://www.youtube.com/watch?v=qtIGDc6LTls))
- [Mikado method examples and exercises](https://github.com/mikadomethod)
- [Home of the Mikado Method](https://mikadomethod.wordpress.com)