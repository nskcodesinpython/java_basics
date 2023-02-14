Object Oriented Programming - basics

Object - Realtime entity. instance of a class used to refer a variabel or call a function from a instanciated class.
          Can be initialised by 3 methods:
          - Using new keyword or default constructor  --->             A a  = new A()
          - Using Class.forName() method              --->             A a  = (A)Class.forName("A").newInstance();
          - Using clone method                        --->             A a1 = a.clone()
          
Class - Logical entity. group of objects which have common properties. It's kind of template/blueprint.
        class can contain following entities:
          - Fields --> Variable of specific datatype (int, char, String, boolean etc..,)
          - Methods --> Function with access specifiers, return type and positional arguments associated with the datatypes
          - Constructors --> function with the class name with no return 
          - Blocks --> 
          - Nested class and interface --> class inside class
          
Inheritance - method to create a hierarchy between classes by inheriting from other classes (Parent-Child relationship)
            public class A{
              public fn1(){
                //does some task
              }
            }
            public class B extends A{
              public fn2(){
                A.fn1();
                //does some extra task
              }
            }

          - 4 types of inheritance 
              1. Single inheritance
              2. Multi-level inheritance
              3. Heirarchial inheritance
              4. Multiple inheritance
              
          1. Single inheritance
                class A{
                
                }
                class B extends A{
                
                }
          2. Multi-level inheritance
                class A{
                
                }
                class B extends A{
                
                }
                class C extends B{
                
                }
                
           3. Heirarchial Inheritance
                class A{
                
                }
                class B extends A{
                
                }
                class C extends A{
                
                }
           4. Multiple inheritance 
                interface A{
                
                }
                interface B{
                
                }
                class C implements A,B{
                
                }

Interaface - Interace cannot implement an interface (no possibility that we can write a definition of a method inside an implemented interface inside an interface)
             In Java, an interface is an abstract type that contains a collection of methods and constant variables. It is one of the core concepts in Java and is used to achieve abstraction, polymorphism and multiple inheritances.
           public interface A {

              // Constant variable
              String var = "VAR";

              // Abstract method
              int somefunction();

              // Static method
              static boolean isEnergyEfficient(String electtronicType) {
                  if (electtronicType.equals(LED)) {
                      return true;
                  }
                  return false;
              }

              //Default method
              default void printDescription() {
                  System.out.println("Electronic Description");
             }
          }
          
 Polymorphism - entities that take diferent forms
              - Function Overloading (Compile time polymorphism)
                Method overloading is the process that can create multiple methods of the same name in the same class, and all the methods work in different ways. Method overloading occurs when there is more than one method of the same name in the class.

                    class A{
                       a(int x){
                       
                       }
                       a(int x, int y){
                       
                       }
                    }
              - Function Overriding (runtime polymorphism) - super keyword can be used to call parent method
                Method overriding is the process when the subclass or a child class has the same method as declared in the parent class.
                    
                    class A{
                      a(){
                      
                      }
                    }
                    class B extends A{
                      a(){
                      
                      }
                    }

Encapsulation - Encapsulation in Java is a mechanism of wrapping the data (variables) and code acting on the data (methods) together as a single unit. In encapsulation, the variables of a class will be hidden from other classes, and can be accessed only through the methods of their current class.

              - private variables and public methods
              
              class A{
                 private int a;
                 
                 public setA(int a){
                    this.a = a;
                 }
                 public getA(){
                    return this.a;
                 }
              }
              class B{
                   //main method and set and get A
              }
              
              
Abstraction - concept of creating a class with method definition and implementing the method definition in the child class

            public abstract class A{
               
               public abstract int a();
            
            }
            
            class B extends A{
               
               public int a(){
                    //functionality goes here
               }
            
            }
