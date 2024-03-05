[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/FgMJElkj)
# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.
  - constant factors and hidden constants typically in asymtotic analysis constant factors are ignored.
    In real life situation these factors can have a decent impact on the actual time comlexity.
  - The input data given in the real world can be much different then what it would be assumed to be for the asymtotic analysis.
    an algorrithm that performs well for the average and worst case senario might might not have good performance for a
    specific input that was not considered.
  - Hardware may have different instruction sets algorithms that perform well on one machine may not perform the same on another type of 
    machine. Asymtoic analysis does not take this into consideration and can lead to misleading expectations of performance.

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.
  - Given that the BST is balanced we can assume that the average case time complexity is $\ O(\log_2 n) $
  - $\(\log_2 n)$ is how we can determine the hieght of the tree with n being the amount of elements in the tree.
  - we also know that with the hieght of the tree we can determine the maximum amount of comparisons that would be made to find a
    particular element in the tree.
  - $\\log_2 1000 = 9.965$ which we can just round to 10 given the tree is balanced. So know we know the height of the tree is ten
    and the max number of comparisons made is 11 or $\\log_2 (n) + 1$
  - So now we know a tree that has 1000 elements has a height of ten and a max number of comparisons of 11. We also know this takes 5 
    seconds so find a specific element.
  - $\\log_2 10000 = 13.287$ We can round to the nearest integer of 13 as the hieght and can get the max number of comparisons of 14.
  - Now using what we know we can estimate the amount of time it would take to find the same element in a tree with 10,000 elements and a 
    height of 13.
  - time for height of $\ 13 = \frac{5 * 13}{10} = \frac{65}{10} = 6.5 seconds $.  

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

Add your answers to this markdown file.
