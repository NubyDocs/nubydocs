::[]
::new
::try_convert
# %w **Quick hand way of writing an array**
 %w allows you to create an array without commas and quotation marks.

Ex: a = ["1", "2", "3", "4"] is equivalent to a = %w[ 1 2 3 4]

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
Ex: %w[1 2 3 4].fetch(1) returns 2 (2 is the at index 1 in this array)

Ex: %w[1 2 3 4].fetch(-1) returns 4 (4 is the last element in this array)

Used => Often

Use: Given an array of words, use fetch to only return a certain word based on its index. 
#fill
#find_index
#first
#flatten
#flatten!
#frozen?
#hash
#include?
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
#pop
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
#slice! **Slice is used to removed elements from an array given their index, and the removed object is also returned**
Ex: %w[A B C D E F G].slice!(1) returns "b" and the array is now %w[A C D E F G]

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
