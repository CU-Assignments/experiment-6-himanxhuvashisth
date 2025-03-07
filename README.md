Develop Java programs using lambda expressions and stream operations for sorting, filtering, and processing large datasets efficiently.

Easy Level:
Write a program to sort a list of Employee objects (name, age, salary) using lambda expressions.
Medium Level:
Create a program to use lambda expressions and stream operations to filter students scoring above 75%, sort them by marks, and display their names.
Hard Level:
Write a Java program to process a large dataset of products using streams. Perform operations such as grouping products by category, finding the most expensive product in each category, and calculating the average price of all products.



### code ####

import java.util.*;

class Employee {
    String name;
    int age;
    double salary;

    public Employee(String name, int age, double salary) {
        this.name = name;
        this.age = age;
        this.salary = salary;
    }

    @Override
    public String toString() {
        return name + " - Age: " + age + ", Salary: $" + salary;
    }
}

public class EmployeeSorting {
    public static void main(String[] args) {
        List<Employee> employees = Arrays.asList(
            new Employee("John", 30, 50000),
            new Employee("Alice", 25, 60000),
            new Employee("Bob", 35, 55000)
        );

        // Sorting by salary using lambda
        employees.sort((e1, e2) -> Double.compare(e1.salary, e2.salary));

        // Display sorted employees
        employees.forEach(System.out::println);
    }
}
