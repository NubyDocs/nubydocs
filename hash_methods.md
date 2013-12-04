Hashes
======

**Basic Definition**
A hash is an unordered collection of information where each stored value is accessed through a label(referred to as a 'key').


**Basic Components**
A hash has zero or more pairs of a 'key' and a 'value' contained within the open '{' and closed '}' brackets. We can express this key/value relationship in two ways: 

* We want to put our inventory (we have 3 'apples', 2 'bananas', and 1 'orange') into a hash named 'inventory':* 

1. The Rocket

inventory = {'apples' => 3, 'bananas' => 2, 'oranges' => 1}

2. Symbols
*add link to symbols page*
inventory = {apples: 3, bananas: 2, oranges: 1}

Here, 'apples', 'bananas', and 'oranges' are each a *key*, with their respective *values* '3', '2', and '1'.

**How to access a value for a key** 

For a specific *key*, we will use the following format:

> hash[*key*]

to return the assigned *value*. If no value exists, it will return *nil*.

*Using the above inventory example*

* inventory = {'apples' => 3, 'bananas' => 2, 'oranges' => 1}

> > inventory['apples'] *= 3*

> > inventory['bananas'] *= 2*

* inventory = {apples: 3, bananas: 2, oranges: 1}

> > inventory[:apples] *= 3*

> > inventory[:bananas] *= 3*

Regardless of what type of object our keys are, we can access the assigned value using the same *hash_name*[] notation.

How To Create a Hash

::[]
::new
::try_convert
#==
#[]
#[]=
#assoc
#clear
#compare_by_identity
#compare_by_identity?
#default
#default=
#default_proc
#default_proc=
#delete
#delete_if
#each
#each_key
#each_pair
#each_value
#empty?

* Returns true if there are no key/value pairs in the hash.
> > {}.empty? is *true*
> > {a => 2}.empty? is *false*

#eql?
#fetch
#flatten
#has_key?
#has_value?
#hash
#include?(*param*)

* Returns true if the hash has a *key* equal to the inputted param. Otherwise returns false.
> inventory = {'apples' => 3, 'bananas' => 2, 'oranges' => 1}
> > inventory.include?('apples') is *true*
> > inventory.include?('grapes') is *false*
> > inventory.include?(3) is *false*

#initialize_copy
#inspect
#invert
#keep_if
#key
#key?(*param*)

* Returns true if the hash has a key with the value of the inputted *param*.
> inventory = {'apples' => 3, 'bananas' => 2, 'oranges' => 1}
> > inventory.key?('apples') is *true*
> > inventory.key?('grapes') is *false*

#keys
* Returns an array of the keys in the hash
> inventory = {'apples' => 3, 'bananas' => 2, 'oranges' => 1}
> > inventory.values *returns* ['apples', 'bananas', 'oranges']

#length
* Returns an integer for the number of key/value pairs in the hash. An empty hash has length 0.

#member?
#merge
#merge!
#rassoc
#rehash
#reject
#reject!
#replace
#select
#select!
#shift
#size
#store
#to_a
* Creates an array for *each* key/value pair, where the first element is the key, and the second the value. The collection of arrays is contained in an array.
> inventory = {'apples' => 3, 'bananas' => 2, 'oranges' => 1}
> > inventory.to_a *returns* [['apples', 3], ['bananas', 2], ['oranges', 1]}
> > Notice that to_a creates a *new* array object, and that inventory is unchanged (still the original hash).

#to_h
#to_hash
#to_s
#update
#value?(*param*)
* Returns true if the hash has a *value* equal to the inputted param. Otherwise returns false.
> inventory = {'apples' => 3, 'bananas' => 2, 'oranges' => 1}
> > inventory.include?(3) is *true*
> > inventory.include?(1) is *false*
> > inventory.include?('apples') is *false*

#values
* Returns an array of the values for each key in the hash
> inventory = {'apples' => 3, 'bananas' => 2, 'oranges' => 1}
> > inventory.values *returns* [3, 2, 1]

#values_at
