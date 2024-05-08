# Starting with Object-Oriented Programming 

## Understanding Classes and Objects

* Definition of a class

```cpp
class Car {
public:
    string make;
    string model;
    int year;
};
```

* Definition of an object

```cpp
Car myCar;
myCar.make = "Toyota";
myCar.model = "Camry";
myCar.year = 2022;
```


## Encapsulation

Access specifiers: public, private, protected

```cpp
class BankAccount {
private:
    double balance;
    string accountNumber;

public:
    void deposit(double amount) {
        balance += amount;
    }

    double getBalance() {
        return balance;
    }
};
```
## Inheritance

```cpp
class Animal {
public:
    void makeSound() {
        cout << "Animal makes a sound" << endl;
    }
};

class Dog : public Animal {
public:
    void wagTail() {
        cout << "Dog wags its tail" << endl;
    }
};
```

## Polymorphism

```cpp
class Shape {
public:
    virtual double area() {
        return 0;
    }
};

class Rectangle : public Shape {
private:
    double length;
    double width;

public:
    double area() override {
        return length * width;
    }
};
```