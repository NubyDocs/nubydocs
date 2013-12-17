I. Running a Program

There are two ways to run ruby code.  You can run the program you wrote in the console or you could run it in IRB.  Here is how you run it from the program in the console.  
class Sample
    def hello
      puts "Hello, World!"
    end
end

 s = Sample.new
 s.hello

You would then run it in the console like this.  

$ ruby my_program.rb
   Hello, World!

IRB is used mostly to experiment and see what what you are producing so that you can better find out what is happening in your code. in IRB you can spit out code and have it show you the steps of what it's producing not just spit out the final answer or error. 

2. Variables
A variable is just a name for a piece of data.  They are flexible and can be changed at any time.  Variables are assigned using the equal sign.  a = 5, is an example of a variable.  Variables can store words("strings") and numbers like b = "hello" or c =12.  Variables must be lowercase and if they are a string, cannot be have a number at the front of the string

3. Objects, Attributes and Methods
in ruby everything is an object.  objects know information called attributes and these attributes can do actions called methods. 
Object = Personal Chef
Attributes = Height, Weight, Eye Color
Method  = Walk, Run, Climb 

Here is how we would write this class in ruby:
class PersonalChef
  def make_toast(color)
    puts "Making your toast #{color}!"
    return self
  end
end     
return brings the program back to the beggining

make it work in rib by:
load 'personal_chef.rb'
frank = PersonalChef.new
frank.make_toast(burned)
=> "Making your toast burned!"

4. Strings
A string is defined as anything between two "" marks.  A string can be as short as "hello" or much longer like a sentence or paragraph.  Here are some common string methods that are used often in ruby.

length - finds the length of the sting.  the method call              
"hello".length returns 5
delete - delete lets you specify what should be deleted.          
"hello".delete("l") returns "heo"
gsub - replaces a letters within a string with other letters.        
"hello".gsub("ll",y to") returns "hey too"
split - breaks up a string along any parameters that you set, comma's, spaces, letters ect
"Welcome to ruby".split(" ") returns ["Welcome", "to", "ruby"]
substring - sometimes we want to return a part of a string.      
"Hello Everyone"[0..4] returns "hello"
"Hello Everyone"[6..-2] returns "hello" returns "very"

you an combine strings and variables:
today = saturday
puts "happy " + today + "!" returns "happy saturday!"

string interpolation - string interpolation is when you put data in the middle of a string, this #{} is an interpolation marker.  Inside those bracket you can put any variables, or ruby code which can be evaluated.
puts "Happy #{today}! It is the #{day_of_year} day of the year."

5. Symbols
symbols are used for passing information around inside the program.  Symbols are characterized by a colon and and then a word after it like :flag or :entry_form

6. Numbers
there are two basic kinds of numbers: integers, which are whole numbers like 1,2,3 and floats which have a decimal, like 5.6. generally avoid floats if you can because whole numbers are easier for you and and your computer to work with.  you can also do regular math operations with integers and floats.  numbers have a bunch of methods which you can see for yourself if you type in any number.methods in your IRB console. for example 5.methods

7. Arrays
An array is a number indexed list.  [car, bike, house].  when counting objects inside of an array, always start with zero.  

object = ["car", "bike", "house"]
object[2] returns "bike"
object.first returns "car"
object.last returns "house"

important array methods
sort - rearrange the order of the elements
each - iterate through each element
join - mash them all together in one string
index - you find the address of the a specified element
shovel << - add another object to an array by shoveling (<<) that object on the end
meal  = ["breakfast", "lunch", "dinner"]
meal <<  "desert" 
returns meal = ["breakfast", "lunch", "dinner", "dessert"]
include? checks to see if an object is contained in the array.  returns true or false

8. Hashes
A hash is an unordered collection where the data is organized into key/value pairs. 
produce = {"apples => 3, "oranges" => 5, "lemons" => 2}
puts "there are #{produce[:oranges]} oranges in the fridge"

def inventory
  produce = {apples: 3, oranges: 1, carrots: 12}
  produce.each do |item, quantity|
    puts "There are #{quantity} #{item} in the fridge."
  end
end

"There are 3 apples in the fridge."
"There are 1 oranges in the fridge."
"There are 12 carrots in the fridge."


9. Conditionals
conditional statements evaluate to true or false.  The most common conditional operators are equal (==), greater than (>), greater than or to equal to(>=) less than (<), and less than or equal to(<=). statements which return true or false, should have a ? mark after them.  

Conditional Statements
in this statement, a time is passes through the minutes variable and the evaluated
def water_status(minutes)
  if minutes < 7
    puts "The water is not boiling yet."
  elsif minutes == 7
    puts "It's just barely boiling"
  elsif minutes == 8
    puts "It's boiling!"
  else
    puts "Hot! Hot! Hot!"
  end
  return self
end

Conditional Looping
def countdown(counter)
  while counter > 0
    puts "The counter is #{counter}"
    counter = counter - 1
  end
  return self
end


10. Equality vs Assignment
Assignment (=): means that you are assigning the value of one thing to another thing.  like assigning a variable or array or hash
Equality (==): means you are asking if two objects are equal to each other. 










