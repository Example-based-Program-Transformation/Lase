# Lase

## Publication

> Meng, N., Kim, M., & McKinley, K. S. (2013, May). LASE: locating and applying systematic edits by learning from examples. In 2013 35th International Conference on Software Engineering (ICSE) (pp. 502-511). IEEE.


## Description

Similar to [Sydit](https://github.com/Example-based-Program-Transformation/Sydit), Lase also generalizes and applies program transformation based on code change examples. However, it requires developers to provide two or more examples to enable its feature of automatically searching for candidate locations to change. In scenarios when identifying edit locations is more challenging than making the edits, this feature is very important because it can help developers avoid errors of omission. When developers provide multiple code change examples, Lase infers an edit script for each example, extracts the common edit shared between them and regards that as the systematic edit demonstrated by all examples. In this way, Lase can filter out any edit operation specific to some of the examples. When generalizing a program transformation out of the exemplar edits, Lase abstracts both identifiers and context when necessary. With identifier abstraction, Lase only abstracts identifiers which are used differently while keeping the other ones concrete. With context abstraction, Lase extracts context in each example and then identifies the common context shared between them. The context alignment and commonality extraction are done using a combination of three techniques: clone detection with [CCFinder](http://www.ccfinder.net), program dependence analysis, and a subtree isomorphism algorithm. After deriving a program transformation, Lase leverages the transformation to both search for code to change and make changes accordingly.

## Code Source
[http://people.cs.vt.edu/nm8247/program_transformation.html](http://people.cs.vt.edu/nm8247/program_transformation.html)