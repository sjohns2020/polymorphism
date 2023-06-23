Abstraction - cleaner code by abstracting common properties and methods 
using inheritance

Polymorphism - a way to get an ArrayList of things that don't inherit, but share a 
common behaviour (like flying)



Here are 3 classes that share some 
behaviours.


![Alt text](<Screenshot 2023-06-23 at 11.12.34.png>)



Sparrow and Penguin are both birds
and inherit from the abstract Bird class.
There is a common behaviour in Birds that
they can eat() - if this is shared by all instances
of bird class it should be abstracted away in to
the parent class. 


![Alt text](<Screenshot 2023-06-23 at 11.14.05.png>)



If we wanted an ArrayList of:
Birds: ArrayList<Bird>
Sparrows: ArrayList<Sparrow>
Penguins: ArrayListPenguin?>

But How can we get an array list of 
flying things.  

Penguin can't fly.
Aeroplanes don't inherit from Bird.

Answer - flying things have shared behaviour fly()
If we use an Interface for fly() and then implement this
in to each class that can fly we can now get:

flythingThings ArrayList<IFly>

![Alt text](<Screenshot 2023-06-23 at 11.14.35.png>)



TYPE MATTERS

We can now get these collections:
Birds: ArrayList<Bird>
Sparrows: ArrayList<Sparrow>
Penguins: ArrayListPenguin?>
flythingThings ArrayList<IFly>

A sparrow can be many types now:

Sparrow sparrow1 = new Sparrow().  - This sparrow has access to all the things a Bird has and a sparrow has

Bird sparrow2 = new Bird() - This sparrow wont be able to access the fly method.  You can't sparrow.fly()

IFly Sparrow3 = new IFly() - this sparrow can only sparrow.fly(), but wont have access to wingspan.


To get around this problem of limited access to properties and methods we use CASTING

CASTING - turning on type in to another as JAVA knows a sparrow can be treated as many different types.



