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

> > inventory['apples'] #=> 3*

> > inventory['bananas'] #=> 2*

* inventory = {apples: 3, bananas: 2, oranges: 1}

> > inventory[:apples] #=> 3*

> > inventory[:bananas] #=> 3*

Regardless of what type of object our keys are, we can access the assigned value using the same *hash_name*[] notation.

How To Create a Hash

*Calling the *new* method: Hash.new # => {}

> Note: Hash.new can take optional arguments which will define specific values within the hash. 

> > inventory = Hash.new(apples: 3, bananas: 2) #=> inventory = {apples: 2, bananas: 3}

*Setting a variable equal to an empty hash: inventory = {}

Editing and Adding a key/value Pair

*We can manually define a key/value pair using the hash[*key*] format, which will alter the original hash.

* This process will either override a value for an existing key, or add a new key/value pair with the information provided.

> inventory = {apples: 2, bananas: 1}

> inventory[:bananas] = 2

> > inventory #=> {apples: 3, bananas: 2}

*Now we will add the key 'oranges' with a value of 1*

> inventory[:oranges] = 1

*Now looking at our inventory hash:

> > inventory #=> {apples: 3, bananas: 2, oranges: 1}


::[]
::new
::try_convert(*param*)

* Tries to convert the specified *param* to a hash. If successful, it will return a converted hash and returns nil otherwise.

> Hash.try_convert([1, 2, 3]) #=> nil

> Hash.try_convert({1 => 2, 3 => 4}) #=> {1 => 2, 3 => 4}

#==

* Compares equality as a boolean. For two hashes to be equal, each key/value pair must be equal (according to their class's object equality) as well as the same number of keys. 

> {1 => 2, 3 => 4} == {3 => 4, 1 => 2} #=> true

> {1 => 2, 3 => 4} == {1 => 3, 3 => 4} #=> false

> {1 => 2, 3 => 4} == {2 => 2, 3 => 4} #=> false

#!=

* Compares inequality as a boolean. 

#[*key*]

* Find the value in the hash for the specified key. If no value exists, it will return *nil*.

> inventory = {'apples' => 3, 'bananas' => 2, 'oranges' => 1}

> > inventory['apples'] #=> 3

> > inventory['grapes'] #=> *nil*

#[*key*]=(*param*)

* Sets the value of the specified key as *param*. If the hash does not have the *key*, a new key/value pair is added with the values of *key*/*param*

> inventory = {'apples' => 3 }

> > inventory['apples'] = 10 #=> inventory = {'apples' => 10}

> > inventory['grapes'] = 4 #=> inventory = {'apples' => 3, 'grapes' => 4}

#assoc
#clear

* Removes all key/value pairs from a hash.

> inventory = {'apples' => 3, 'bananas' => 2, 'oranges' => 1}

> > inventory.clear #=> {}

#compare_by_identity
#compare_by_identity?
#default
#default=
#default_proc
#default_proc=
#delete
#delete_if
#each {|key,value| *block* }

* Calls the block once on each key in the hash, with the *key* and *value* as parameters.

> inventory = {'apples' => 3, 'bananas' => 2, 'oranges' => 1}

> > inventory.each { |fruit, quantity| inventory[fruit.upcase] = (quantity * 2) }

> > #=> {'APPLES' => 6, 'BANANAS' => 4, 'ORANGES' => 2}

#each_key
#each_pair
#each_value
#empty?

* Returns true if there are no key/value pairs in the hash.

> > {}.empty? #=> *true*

> > {a => 2}.empty? #=> *false*

#eql?

* Returns *true* if two hashes are equal by the hash equality method. Otherwise *false*.

> {'apples' => 3, 'bananas' => 2}.eql?({'apples' => 3, 'bananas' => 2}) #=> *true*

> {'apples' => 3, 'bananas' => 2}.eql?({'apples' => 3, 'bananas' => 4}) #=> *false*

#fetch
#flatten
#has_key?
#has_value?
#hash
#include?(*param*)

* Returns true if the hash has a *key* equal to the inputted param. Otherwise returns false.

> inventory = {'apples' => 3, 'bananas' => 2, 'oranges' => 1}

> > inventory.include?('apples') #=> *true*

> > inventory.include?('grapes') #=> *false*

> > inventory.include?(3) #=> *false*

#initialize_copy
#inspect
#invert

* Returns a new hash by applying the original hash's values as keys, and keys as values. 

> inventory = {'apples' => 3, 'bananas' => 2, 'oranges' => 1}

> > inventory.invert #=> {3 => "apples", 2 => "bananas", 1 => "oranges"}

#keep_if
#key
#key?(*param*)

* Returns true if the hash has a key with the value of the inputted *param*.

> inventory = {'apples' => 3, 'bananas' => 2, 'oranges' => 1}

> > inventory.key?('apples') #=> *true*

> > inventory.key?('grapes') #=> *false*

#keys

* Returns an array of the keys in the hash

> inventory = {'apples' => 3, 'bananas' => 2, 'oranges' => 1}

> > inventory.values *returns* ['apples', 'bananas', 'oranges']

#length

* Returns an integer for the number of key/value pairs in the hash. An empty hash has length 0.

#member?(*key*)

* Returns *true* if the specified key is in the hash. Otherwise, returns *false*.

> inventory = {'apples' => 3, 'bananas' => 2, 'oranges' => 1}

> > inventory.member?('apples') #=> *true*

> > inventory.member?('kiwi') #=> *false*

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

* Returns an integer for the number of key/value pairs in the hash

> inventory = {'apples' => 3, 'bananas' => 2, 'oranges' => 1}

> > inventory.size #=> 3

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

> > inventory.include?(3) #=> *true*

> > inventory.include?(1) #=> *false*

> > inventory.include?('apples') #=> *false*

#values
* Returns an array of the values for each key in the hash

> inventory = {'apples' => 3, 'bananas' => 2, 'oranges' => 1}

> > inventory.values #=> [3, 2, 1]

#values_at(*key*)
* Returns an array of the values for specified keys, and can take multiple keys as arguments.

> inventory = {'apples' => 3, 'bananas' => 2, 'oranges' => 1}

> > inventory.values_at('apples') #=> [3]

> > inventory.values_at('apples', 'bananas') #=> [3,2]
