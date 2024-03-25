[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/FgMJElkj)
# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.
  - constant factors and hidden constants typically in asymtotic analysis constant factors are ignored.
    In real life situation these factors can have a decent impact on the actual time comlexity.
  - The type of analysis you are doing. If it is big O notation then this would give you loose bounds which mean that the runtime my be 
    actually faster than the analysis is for the worst case scenario.
  - Hardware may have different instruction sets algorithms that perform well on one machine may not perform the same on another type 
    of machine. Asymtoic analysis does not take this into consideration and can lead to misleading expectations of performance.

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.
  - Given that the BST is balanced we can assume that the average case time complexity is $\ O(\log_2 n) $
  - $\(\log_2 n)$ is how we can determine the hieght of the tree with n being the amount of elements in the tree.
  - we also know that with the hieght of the tree we can determine the maximum amount of comparisons that would be made to find a
    particular element in the tree.
  - $\\log_2 1000 = 9.965$ which we can just round to 10 given the tree is balanced. So know we know the height of the tree is 10
    and the max number of comparisons made is 10 or $\\log_2 (n)$
  - So now we know a tree that has 1000 elements has a height of ten and a max number of comparisons of 10. We also know this takes 5 
    seconds so find a specific element.
  - $\\log_2 10000 = 13.287$ We can round to the nearest integer of 13 as the hieght and can get the max number of comparisons of 13.
  - Now using what we know we can estimate the amount of time it would take to find the same element in a tree with 10,000 elements and 
    a height of 13.
  - time for height of $\ 13 = \frac{5 * 13}{10} = \frac{65}{10} = 6.5 seconds $.  

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.
  - The efficiency of binary search can be significantly influenced by how effectively it utilizes the cache and memory. In scenarios where the cache is not utilized optimally, fetching elements from memory can 
    lead to increased search time.
  - The distrubution of the data within the tree could be different. By distribution of data within the binary tree I am talking about  
    the different ways the data can be arranged within the tree. So if the element we want is in the middle of the data set or close to 
    the root. But in the next set The same element could be in a different location in the tree or further away form the best case.
  - The difference of these 2 cases could be explained by a possiblity of the searches being run on different machines.
 
I recieved help from the TA.
I also reviewed  theory-vs-practice-Boomboomyoyo , theory-vs-practice-wyo-kaitlyn , and theory-vs-practice-Countmooshroom

Add your answers to this markdown file.
