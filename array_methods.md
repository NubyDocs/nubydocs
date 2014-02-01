**What is an Array anyway?**
 An array is a collection.  An array is a list.  What does this mean? 
  Say you have  numbers that you want to order.  
  Let's say prime digits
  Then you could put them into an array

  a = %w(  2      3      5      7     11     13     17     19     23     29 
     31     37     41     43     47     53     59     61     67     71 
     73     79     83     89     97    101    103    107    109    113 
    127    131    137    139    149    151    157    163    167    173 
    179    181    191    193    197    199    211    223    227    229 )
 
  
  
  What you can do with this array is endless... hence the power of Enumerables with the Array Class.  
  
  ***See the methods below!***


::[]
::new
::try_convert
# %w **Quick hand way of writing an array**
 %w allows you to create an array without commas and quotation marks.

Ex: a = ["1", "2", "3", "4"] is equivalent to a = %w( 1 2 3 4)

Used => All the time!
#&
#*
#+
#-
#<<
#<=> **Spaceship Operator: a <=> b** 
  if a < b then return -1
  
  if a = b then return  0
  
  if a > b then return  1
#==
#[]
#[]=
#assoc
#at
#bsearch
#clear
#collect
#collect!
#combination
#compact
#compact!
#concat
#count
#cycle
#delete
#delete_at
#delete_if
#drop
#drop_while
#each
#each_index
#empty?
#eql?
#fetch **:Fetch returns a designated element from a given index** 
Ex: %w(1 2 3 4).fetch(1) returns 2 (2 is at index 1 in this array)

Ex: %w(1 2 3 4).fetch(-1) returns 4 (4 is the last element in this array)

Used => Often

Use: Given an array of words, use fetch to only return a certain word based on its index. 
#fill
#find_index
#first
#flatten **:Flatten returns a new one dimensional array**
EX: ["1", "2", ["3", "4] "5"].flatten returns  ["1", "2", "3", "4", "5"]
Used => Often

#flatten!
#frozen?
#hash
#include? **:Include? returns true if a given object is present in self**
EX: a = %w(A B C D)
    a.include?("A") returns true
    a.include?("Z") returns false
#index
#initialize_copy
#insert
#inspect
#join
#keep_if
#last
#length
#map
#map!
#pack
#permutation
#pop **Remove the last element from an array**
Ex: a = %w[this is using pop]

    a.pop returns [this is using]
    
    a.pop(2) returns [this]
    
#product
#push
#rassoc
#reject
#reject!
#repeated_combination
#repeated_permutation
#replace
#reverse
#reverse!
#reverse_each
#rindex
#rotate
#rotate!
#sample
#select
#select!
#shift
#shuffle
#shuffle!
#size
#slice
#slice! **Slice is used to remove elements from an array given their index, and the removed object is also returned**
Ex: %w(A B C D E F G).slice!(1) returns "b" 

 the array is now %w(A C D E F G)

Used => Often
#sort
#sort!
#sort_by!
#take
#take_while
#to_a
#to_ary
#to_s
#transpose
#uniq
#uniq!
#unshift
#values_at
#zip
#|
