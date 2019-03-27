
# Polymorphism & Composition Homework - Quiz

# Polymorphism

1. What does the ___word___ 'polymorphism' mean?

From the Greek meaning "having multiple forms"


2. What does it mean when we apply polymorphism to OO design? Give a simple Java example.

Polymorphism describes a pattern in object oriented programming in which classes have different functionality while sharing a common interface.
In others words, is the ability to process objects of various types and classes through a single, uniform interface.
For example, in Java:

class Vehicle {


    public String move(){

    return "Vehicles can move!";

    }

}

class MotorBike extends Vehicle {

    public String move() {

    return “MotorBike can move and accelerate too!”;

    }

}

class Tractor extends Vehicle {

public String move() {

return "Tractor can move, accelerate and plow the ground as well."
}

}

When we apply a method to different classes that have the same behaviour. 


3. What can we use to implement polymorphism in Java?

We can use inheritance, abstract methods (overriding) and interfaces.


4. How many 'forms' can an object take when using polymorphism?
Many, as many as it needs.


5. Give an example of when you could use polymorphism.

You can use polymorphism when you have a football team (coach, player and massage therapist) and each one has an 'action on the field' but implement in a different way.
The coach "lead the game", the player "play the game" and the therapist "give massage to the players". In this case, you can create an Interface called 'IAction' to be implemented
in the class Coach, Player and Massage Therapist.


# Composition

6. What do we mean by 'composition' in reference to object-oriented programming?

Composition describes a class that references one or more objects of other classes in instance variables. This allows you to model a has-a association between objects rather
than inheritance from a parent classes


7. When would you use composition? Provide a simple example in Java.

This is an example when you have a car class that has-a engine and has-a tyre but a car is not an engine or a tyre, and a tyre or engine are not a car.

class Engine {

 private int horsePower;

 public Engine(int horsePower){
 this.horsePower = horsePower;
 }

public String turnOn(){
return "VROOOOOM";
}

}

class Tyre {

private String colour;

public Tyre(String colour){
this.colour = colour;
}

}

class Car{

private String colour;
private String brand;
private ArrayList<Tyre> tyres;
private Engine engine;

public Car(String colour, String brand){
this.colour = colour;
this.brand = brand;
this.engine = engine;
tyres = new ArrayList<Tyre>();
}

}


8. What is/are the advantage(s) of using composition?

8.1. Reuses existing code
8.2. Design clean APIs
8.3. Change the implementation of a class used in a composition without adapting any external clients

9. When an object is destroyed, what happens to all the objects it is composed of?

The behaviours are destroyed as well.
