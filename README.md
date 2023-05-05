Download Link: https://assignmentchef.com/product/solved-cse522-assignment-2-design-patterns-and-tree-memento
<br>
<h1>Part 1: Generic Tree Iterators</h1>

The file GenericIterators.java posted under Resources → Assignments defines generic versions of AbsTree, Tree, and DupTree discussed in class.   The file also gives the

outlines of generic external iterators for these classes, called AbsTreeIterator, TreeIterator and DupTreeIterator respectively.

Considerable code-factoring can be achieved in their definitions because TreeIterator and DupTreeIterator only need to define their constructors;  the entire logic of traversal can be kept in AbsTreeIterator.

Also given in GenericIterators.java are tester methods that represent sets and bags as trees and duptrees, respectively, and carry out <em>containment</em> tests by invoking the boolean method contains, to be defined by you in this assignment.

<strong><em>What you should program: </em></strong>

<ul>

 <li>Complete the AbsTreeIterator class by writing code for its constructor and the methods next(), hasNext() and stack_tree_nodes(). Note that, for duptrees,  the next() method should return the value in a DupTree node as many times as specified by the count associated with this node.  Each invocation of next() returns only one value.</li>

</ul>

Note: Refer to Lecture 6 slide #35 for guidance on how to define the private method stack_tree_nodes().

<ul>

 <li>Complete the definition of the static boolean method contains(AbsTree&lt;T&gt; tr1, AbsTree&lt;T&gt; tr2) in class GenericIterators so that it works for sets as well as bags. For your reference:</li>

 <li>A set s1 contains set s2 if every member of s2 is also a member of s1.</li>

 <li>A bag b1 contains bag b2 if every member, x, of b2 is also a member of b1; also, the number of occurrences of x in b2 is less than or equal to the number of occurrences of x in b1.</li>

</ul>

<strong><em>Important: </em></strong> There are two key requirements for contains:

<ul>

 <li>that the test is carried out by making only one traversal through each set/bag; and</li>

 <li>that the test returns false as soon as possible, i.e., without necessarily traversing the entire set/bag.</li>

</ul>

These requirements can be met because the elements of sets and bags are Comparable and therefore can be enumerated in order.

Run the five test methods given in GenericIterators.java.    Each test should print out on the console the values that are compared during their execution in to clarify their behavior.   Check your output against the answers given in A2_Part1_output.txt.

<strong> Part 2:  Tree Memento </strong>

Lecture 9 contains a demo of a Graphical User Interface (GUI) for trees and duptrees.   A screen-shot of the GUI is shown below.  Using this GUI we can perform the four familiar operations on trees and duptrees: insert, delete, min, and max.

Most of the code for Part 2 is given at Resources → Assignments → TreeGUI.java.   You are to fill out the missing parts in the assignment.  The focus here is on the Undo operation using which you should be able to undo all changes made to the tree/duptree, restoring earlier trees/duptrees.




More specifically, you are to code the following parts:

<ul>

 <li>The clone() operation in class AbsTree;</li>

 <li>The entire class TreeMemento;</li>

 <li>The actionPerformed methods for deleteButton and UndoButton in class TreeGUI. The insertButton code is provided to you for reference.</li>

</ul>




You are permitted to add extra fields and code in class TreeGUI in order to support the above operations.




<strong><em>What can be undone</em></strong>: Only those inserts and deletes that actually change the state of a tree/duptree can be undone.   Inserts and deletes that do not change the state of the tree/delete are not eligible for being undone.  Hence, unlike A1 Part 1, the insert and delete methods here return a boolean indicating whether the state of the tree/duptree has changed – this convention is followed in the state updating methods of Java’s collection classes.     Also, unlike A1 Part 1, it is permissible to delete the last value from a tree/duptree.




Exception messages to be printed: <em>“No more undo operations are possible,” “Cannot delete from an empty tree,” “Cannot delete non-existent value n,”</em> <em>“Number format error – please re-enter value” “Cannot take min of an empty tree,” </em>and<em> “Cannot take max of an empty tree.” </em>

<strong><em> </em></strong>

<strong><em>Demos</em></strong><strong><em> and Testing.   </em></strong>Two demos, A2_Part2_Tree_demo.mp4 and A2_Part2_DupTree_demo.mp4, will be posted to clarify the expected behavior of your program for trees and duptrees.


