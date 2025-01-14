<!-- DISCLIB -->
# DISCLib
<!-- based on the repo from 
https://github.com/othneildrew/Best-README-Template

<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->

<!-- PROJECT SHIELDS -->
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![License][license-shield]][license-url]

## Nombre y código
Nombre: Laura Valentina Lara Diaz
Código: 201912967

[View Demo and Examples][demo-url] · [Report Bug][bugs-url] · [Request Feature][issues-url]

<!-- PROJECT CONTENT -->
**Table of Contents (up to date)**
<!-- autogenerated by plugin -->

1. [DISCLib](#DISCLib)
    1. [About The Project](#About-The-Project)
        1. [Structure](#Structure)
        1. [Implementation](#Implementation)
    1. [Getting Started](#Getting-Started)
        1. [Prerequisites](#Prerequisites)
        1. [Installation](#Installation)
    1. [Usage](#Usage)
    1. [Contact and support](#Contact-and-support)
    1. [Roadmap](#Roadmap)
    1. [Contributing](#Contributing)
    1. [License](#License)
    1. [Authors and acknowledgment](#Authors-and-acknowledgment)

<!-- ABOUT THE PROJECT -->

## About The Project

This project was created as a pedagogical library to teach the undergraduate students in the Systems and Computer Engineer program at Universidad de los Andes and others in the faculty to use and understand data structures and its related algorithm. This includes Arrays, Lists, Maps, Ordered Maps, Binary Search Trees (BST), Red Black Trees (RBT) and Graphs.

**IMPORTANT** This is a work in progress. The project is mainly focused as a teaching tool for undergraduate college students and is not intended to be used as a full-functional library.

[Back to top](#disclib)

<!-- STRUCTURE -->
### Structure

The project has four main parts:
1. [DISClib](./DISClib) Root folder with the library implementation.
    1. [ADT](./DISClib/ADT) Folder with the main Abstract Data Types (ADT) implemented in the library.
        1. [List](./DISClib/ADT/list.py) Script implementing the ADT Lists in the library, configurable by Array List, Single Linked List and Double Linked List structures.
        1. [Queue](./DISClib/ADT/queue.py) Script implementing the ADT queue based in the ADT List.
        1. [Stack](./DISClib/ADT/stack.py) Script implementing the ADT stack based in the ADT List.
        1. [Map](./DISClib/ADT/map.py) Script implementing the ADT Map using Hash Tables as data structures, configurable by collision handling method to Linear Probing and Separate Chaining.
        1. [Ordered Map](./DISClib/ADT/orderedmap.py) Script implementing the ADT Ordered Maps using binary trees as data structures, configurable to Binary Search Trees (BST) and Red Black Tree (RBT).
        1. [MinPQ](./DISClib/ADT/minpq.py) Script implementing the ADT Min Priority Queue using heap data structures.
        1. [Indexed MinPQ](./DISClib/ADT/indexminpq.py) Script implementing the ADT Indexed Min Priority Queue using the indexed heap data structure.
        1. [Graph](./DISClib/ADT/graph.py) Script implementing the ADT Graph using adjacency lists as data structures.

    1. [Algorithms](./DISClib/Algorithms) Folder with the main algorithms implemented to manage the ADTs.
        1. [Graphs](./DISClib/Algorithms/Graphs) Folder with the algorithms to manage the ADT Graph.
            1. [DFS](./DISClib/Algorithms/Graphs/dfs.py) Script implementing the Depth First Search (DFS) algorithm.
            1. [BFS](./DISClib/Algorithms/Graphs/bfs.py) Script implementing the Breath First Search (BFS) algorithm.
            1. [DFO](./DISClib/Algorithms/Graphs/dfo.py) Script implementing the Depth First Order (DFO) topological sorting algorithm.
            1. [Cycles](./DISClib/Algorithms/Graphs/cycles.py) Script implementing the Cycle Detection algorithm.
            1. [SCC](./DISClib/Algorithms/Graphs/scc.py) Script implementing the Strongly Connected Components (SCC) algorithm.
            1. [Prim](./DISClib/Algorithms/Graphs/prim.py) Script implementing the Prim's algorithm.
            1. [Dijkstra](./DISClib/Algorithms/Graphs/dijkstra.py) Script implementing the Dijkstra's algorithm.
            1. [Bellman-Ford](./DISClib/Algorithms/Graphs/bellmanford.py) Script implementing the Bellman-Ford algorithm.
        1. [Sorting](./DISClib/Algorithms/Sorting) Folder with the algorithms implementing sorting for the ADT List.
            1. [Selection Sort](./DISClib/Algorithms/Sorting/selectionsort.py) Script implementing the Selection Sort algorithm.
            1. [Insertion Sort](./DISClib/Algorithms/Sorting/insertionsort.py) Script implementing the Insertion Sort algorithm.
            1. [Shell Sort](./DISClib/Algorithms/Sorting/shellsort.py) Script implementing the Shell Sort algorithm.
            1. [Merge Sort](./DISClib/Algorithms/Sorting/mergesort.py) Script implementing the Merge Sort algorithm.
            1. [Quick Sort](./DISClib/Algorithms/Sorting/quicksort.py) Script implementing the Quick Sort algorithm.
        1. [Trees](./DISClib/Algorithms/Trees) Folder with the algorithms to manage the ADT Trees.
            1. [Traversal](./DISClib/Algorithms/Trees/traversal.py) Script implementing the Transversal algorithm for binary trees, it includes the preorder, inorder and postorder structure walkthrough.

    1. [Data Structures](./DISClib/DataStructures) Folder with the main data structures implemented to support the ADTs in the library.
        1. [Array List](./DISClib/DataStructures/arraylist.py) Script implementing the Array List data structure.
        1. [Single Linked List](./DISClib/DataStructures/singlelinkedlist.py) Script implementing the Single Linked List data structure.
        1. [Double Linked List](./DISClib/DataStructures/doublelinkedlist.py) Script implementing the Double Linked List data structure.
        1. [Heap](./DISClib/DataStructures/heap.py) Script implementing the Heap data structure.
        1. [Indexed Heap](./DISClib/DataStructures/indexheap.py) Script implementing the Indexed Heap data structure.
        1. [Indexed MinPQ Node](./DISClib/DataStructures/iminpqnode.py) Script implementing the Indexed MinPQ Node data structure to support the Indexed Heap implementation.
        1. [Separate Chaining Hash Table](./DISClib/DataStructures/chaininghashtable.py) Script implementing the Separate Chaining Hash Table data structure.
        1. [Linear Probing Hash Table](./DISClib/DataStructures/probehashtable.py) Script implementing the Linear Probing Hash Table data structure.
        1. [Map Entry](./DISClib/DataStructures/mapentry.py) Script implementing the Map Entry/Value data structure to support the Hash Table implementation.
        1. [Binary Search Tree (BST)](./DISClib/DataStructures/bst.py) Script implementing the Binary Search Tree (BST) data structure for the ADT Ordered Map.
        1. [BST Node](./DISClib/DataStructures/bstnode.py) Script implementing the BST Node data structure to support the Binary Search Tree (BST) data structure.
        1. [Red Black Tree (RBT)](./DISClib/DataStructures/rbt.py) Script implementing the Red Black Tree (RBT) data structure for the ADT Ordered Map.
        1. [RBT Node](./DISClib/DataStructures/rbtnode.py) Script implementing the RBT Node data structure to support the Red Black Tree (RBT) data structure.
        1. [Adjacency List](./DISClib/DataStructures/adjlist.py) Script implementing the Adjacency List data structure for ADT Graph.
        1. [Edge](./DISClib/DataStructures/edge.py) Script implementing the Edge data structure to support the Graph's Adjacency List implementation.

    1. [Utils](./DISClib/Utils) Folder with the main utilities implemented to support the ADTs in the library.
        1. [Error Handling](./DISClib/Utils/error.py) Script implementing the Error Handling utility for all the libraries.

1. [Test](./Test) Folder with the tests for the library.
    1. [List](./Test/list) Scripts to evaluate the ADT Lists.
    1. [Queue](./Test/queue) Scripts to evaluate the ADT Queue.
    1. [Stack](./Test/stack) Scripts to evaluate the ADT Stack.
    1. [Map](./Test/map) Scripts to evaluate the ADT Map.
    1. [Ordered Map](./Test/orderedmap) Scripts to evaluate the ADT Ordered Map.
    1. [Binary Search Tree](./Test/bst) Scripts to evaluate the ADT Binary Search Tree.
    1. [MinPQ](./Test/minpq) Scripts to evaluate the ADT Min Priority Queue.
    1. [Graph](./Test/graph) Scripts to evaluate the ADT Graph.

**NOTE:** `DISClib` uses the  the `config.py` scripts to configure the library's build path and allows the Python interpreter to find the relative path in any OS condition.

[Back to top](#disclib)

<!-- BUILT WITH -->
### Implementation

This library was built with the following technologies:
  * `Mac OS` and `Windows 10` for operating system.
  * `VS code` for the IDE.
  * `Python 3.6` for the programming language.
  * `Pytest` for the testing framework.

As a design principle **DISClib** minimize the use of Python external libraries in its implementation.

Finally, **DISClib** works between `Python 3.6` and `Python 3.9` versions.

[Back to top](#disclib)

<!-- GETTING STARTED -->
## Getting Started

This section contains the steps to get started with the library. As is the case with any other library, you need to install the library and then import it in your project.

As the library is not Object Oriented, you need to import the library in your project as a module using the following steps in [Installation](#installation).

[Back to top](#disclib)

<!-- PREREQUISITES -->
### Prerequisites

As a design principle **DISClib** minimize the use of Python external libraries in its implementation.

To execute the tests in the `Test` folder, you need to install the `Pytest` package.

  ```bash
  pip install pytest
  ```

[Back to top](#disclib)

<!-- INSTALLATION -->
### Installation

For the moment the **DISClib** is available as a local dependency in your project. To install it you can follow the next steps:

1. Create a new project folder.
1. Clone the repo with the command:

   ```sh
   git clone https://github.com/ISIS1225DEVS/ISIS1225-Lib.git
   ```

1. Move the **DISClib** folder to the project folder.
1. Create a new Python file in the project folder.
1. Import the necessary **DISClib** ADT modules into your project with the command:

   ```python
    from DISClib.ADT import list as lt
    from DISClib.ADT import map as mp
   ```

1. Start coding!

[Back to top](#disclib)

<!-- USAGE EXAMPLES -->
## Usage

**DISCLib** is a library that provides a set of ADT's to support the development and use of algorithms. Its intended as a teaching tool in the course [ISIS1225-Estructuras de Datos y Algoritmos][uniandes-url].

To check the laboratories repositories, go to the following links:

* [ISIS1225-SampleMVC][sample-mvc-url] MVC pattern introduction laboratory.
* [ISIS1225-SampleConflicts][sample-conflicts-url] GitHub conflicts solution laboratory.
* [ISIS1225-SampleList][sample-list-url] ADT List laboratory.
* [ISIS1225-SampleSorts][sample-sort-url] ADT List sorting algorithms laboratory.
* [ISIS1225-sampleMap][sample-map-url] ADT Map laboratory.
* [ISIS1225-SampleCollision][sample-collision-url] ADT Map collision method laboratory.
* [ISIS1225-SampleTree][sample-tree-url] ADT Ordered Map (BST and RBT) laboratory.
* [ISIS1225-sampleGraph][sample-graph-url] ADT Graph laboratory.
* [ISIS1225-SampleAlgorithm][sample-algorithm-url] ADT Graph algorithms laboratory.
* [ISIS1225-Reto1][challenge1-url] First Challenge repository.
* [ISIS1225-Reto2][challenge2-url] Second Challenge repository.
* [ISIS1225-Reto3][challenge3-url] Third Challenge repository.
* [ISIS1225-Reto4][challenge4-url] Fourth Challenge repository.

[Back to top](#disclib)

<!-- CONTACT -->
## Contact and support

For further information and contact, use the following links:

* Official Repository [DISClib][disclib-url].
* Repository for [Demo and Examples][demo-url].
  
If you require further information, please contact us [via this email](mailto:isis1225@uniandes.edu.co)

[Back to top](#disclib)

<!-- ROADMAP -->
## Roadmap
The Road so far led us to complete the following features:

* [ ] To include examples for all modules in the repository [Demo and Examples][demo-url].
* [ ] To clean some code and make it more readable.
* [ ] To standardize the functions and variables names throughout the library.
* [ ] To improve the library the documentation.
* [ ] To implement the Adjacency Matrix data structure for the ADT Graph.

See the [open issues][issues-url] for a full list of proposed features (and known issues).

[Back to top](#disclib)

<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this project better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project.
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`).
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the Branch (`git push origin feature/AmazingFeature`).
5. Open a Pull Request.

[Back to top](#disclib)

<!-- LICENSE -->
## License

Copyright 2020, Departamento de sistemas y Computación, Universidad de Los Andes.
Developed for the class _"ISIS1225 - Estructuras de Datos y Algoritmos"_ or _"ISIS1225 - Data Structure and Algorithms"_ in english.

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the [GNU General Public License](LICENSE) for more information go to [GNU ORG][gnu-url].

[Back to top](#disclib)

<!-- ACKNOWLEDGMENTS -->
## Authors and acknowledgment

* [Dario Correal][dariocorreal-url] is the original author and main developer of the library.
* [Santiago Arteaga][phillipus85-url] is a contributor and repository administrator. 
* [Luis Florez][le99-url] is a contributor and developed examples and tutorials for the library.

[Back to top](#disclib)

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
<!-- links for DISClib -->
[contributors-shield]: https://img.shields.io/github/contributors/ISIS1225DEVS/ISIS1225-Lib.svg?style=for-the-badge
[contributors-url]: https://github.com/ISIS1225DEVS/ISIS1225-Lib/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/ISIS1225DEVS/ISIS1225-Lib.svg?style=for-the-badge
[forks-url]: https://github.com/ISIS1225DEVS/ISIS1225-Lib/network/members
[stars-shield]: https://img.shields.io/github/stars/ISIS1225DEVS/ISIS1225-Lib.svg?style=for-the-badge
[stars-url]: https://github.com/ISIS1225DEVS/ISIS1225-Lib/stargazers
[issues-shield]: https://img.shields.io/github/issues/ISIS1225DEVS/ISIS1225-Lib.svg?style=for-the-badge
[issues-url]: https://github.com/ISIS1225DEVS/ISIS1225-Lib/issues
[license-shield]: https://img.shields.io/badge/License-GPLv3-blue.svg?style=for-the-badge
[license-url]: https://github.com/ISIS1225DEVS/ISIS1225-Lib/blob/master/LICENSE
<!-- [linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/linkedin_username
[product-screenshot]: images/screenshot.png -->
[uniandes-url]: https://cursos.virtual.uniandes.edu.co/isis1225/
[organization-url]: https://github.com/ISIS1225DEVS/
[disclib-url]: https://github.com/ISIS1225DEVS/ISIS1225-Lib
[demo-url]: https://github.com/ISIS1225DEVS/ISIS1225-Examples
[bugs-url]: https://github.com/ISIS1225DEVS/ISIS1225-Lib/issues
[issues-url]: https://github.com/ISIS1225DEVS/ISIS1225-Lib/issues
[gnu-url]: http://www.gnu.org/licenses/
<!-- contributors  -->
[dariocorreal-url]: https://github.com/dariocorreal
[phillipus85-url]: https://github.com/phillipus85
[le99-url]: https://github.com/le99
<!-- EDA lab + challenges repository -->
[sample-mvc-url]: https://github.com/ISIS1225DEVS/ISIS1225-SampleMVC
[sample-conflicts-url]: https://github.com/ISIS1225DEVS/ISIS1225-SampleConflicts
[sample-list-url]: https://github.com/ISIS1225DEVS/ISIS1225-SampleList
[sample-sort-url]: https://github.com/ISIS1225DEVS/ISIS1225-SampleSorts
[sample-map-url]: https://github.com/ISIS1225DEVS/ISIS1225-SampleMap
[sample-collision-url]: https://github.com/ISIS1225DEVS/ISIS1225-SampleCollision
[sample-tree-url]: https://github.com/ISIS1225DEVS/ISIS1225-SampleTree
[sample-graph-url]: https://github.com/ISIS1225DEVS/ISIS1225-SampleGraph
[sample-algorithm-url]: https://github.com/ISIS1225DEVS/ISIS1225-SampleAlgorithm
[challenge1-url]: https://github.com/ISIS1225DEVS/Reto1-Template
[challenge2-url]: https://github.com/ISIS1225DEVS/Reto2-Template
[challenge3-url]: https://github.com/ISIS1225DEVS/Reto3-Template
[challenge4-url]: https://github.com/ISIS1225DEVS/Reto4-Template