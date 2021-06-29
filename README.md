# python12
CONSTRUCTORS


1.Write a class with a default constructor, one argument constructor and two argument
constructors. Instantiate the class to call all the constructors of that class from a main
class

class  sample:

# default constructor

def __init__(self):
self.number_variable=1001

# parameterized constructor

def __init__(self ,  id , name , age , gender, doj , dob ):

self.id_value = id

self.name_value = name

self.age_value =  age

self.gender_value = gender

self.doj_value = doj

self.dob_value = dob


def print_method(self):

print(“number variable : “,self.number_variable)

obj=sample()

obj.print_method()

def print_output(self):

print(“Id value :”, self.id_value)

print(“name_value :”, self.name_value)

print(“age_value :”, self.age_value)

print(“gender_value :”, self.gender_value)

print(“doj_value :”, self.doj_value)

print(“dob_value :”, self.dob_value)
 
obj1=sample(101,’Terry’,27,’male’,10072015,10071993)

obj1.print_output()




2.Call the constructors(both default and argument constructors) of super class from a child
class
class Base1:
  def __init__():
    super(Base1, self).__init__()

class Base2:
  def __init__():
    super(Base2, self).__init__()

class Derived(Base1, Base2):
  def __init__():
    super(Derived, self).__init__()
    
 
 
 
 3.Apply private, public, protected and default access modifiers to the constructor
 
 class Super:
      
     # public data member
     var1 = None
  
     # protected data member
     _var2 = None
       
     # private data member
     __var3 = None
      
     # constructor
     def __init__(self, var1, var2, var3):  
          self.var1 = var1
          self._var2 = var2
          self.__var3 = var3
      
    # public member function   
     def displayPublicMembers(self):
   
          # accessing public data members
          print("Public Data Member: ", self.var1)
         
     # protected member function   
     def _displayProtectedMembers(self):
   
          # accessing protected data members
          print("Protected Data Member: ", self._var2)
       
     # private member function   
     def __displayPrivateMembers(self):
   
          # accessing private data members
          print("Private Data Member: ", self.__var3)
  
     # public member function
     def accessPrivateMembers(self):     
            
          # accessing private memeber function
          self.__displayPrivateMembers()
   
# derived class
class Sub(Super):
   
      # constructor 
       def __init__(self, var1, var2, var3): 
                Super.__init__(self, var1, var2, var3)
            
      # public member function 
       def accessProtectedMemebers(self):
                  
                # accessing protected member functions of super class 
                self._displayProtectedMembers()
   
# creating objects of the derived class     
obj = Sub("Geeks", 4, "Geeks !") 
  
# calling public member functions of the class
obj.displayPublicMembers()
obj.accessProtectedMemebers()
obj.accessPrivateMembers() 
  
# Object can access protected member
print("Object is accessing protected member:", obj._var2)
  
# object can not access private member, so it will generate Attribute error
#print(obj.__var3)



4.Write constructors with return type int and String


class MyClass(object):
    def __init__(self):
        pass
    def __new__(cls):
        if i_want_to_return_something_else:
            return something_other_than_object_instance
        else:
            # this should be written else the new instance will never be returned when this class is instanciated
            return super(MyClass, cls).__new__(cls)


 
 
 
 
5.Try to call the constructor multiple times with the same object


* when switching from Java to Python was multiple constructors. Python does not support them (directly), but there a may other approaches that work very similar (maybe even better).


class Student:    
    def __init__(self,name,id,age):    
        self.name = name;    
        self.id = id;    
        self.age = age    
    def display_details(self):    
        print("Name:%s, ID:%d, age:%d"%(self.name,self.id))    
s = Student("John",101,22)    
print(s.__doc__)    
print(s.__dict__)    
print(s.__module__)   

