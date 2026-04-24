[Program-1 WAP TO DEMONSTRATE COMMAND LINE ARGUMENT](#ASSI-1)

[Program-2 WAP TO DEMONSTRATE HELLO-WORLD](#ASSI-2)

[Program-3 WAP for the addition of two distances where each distance is given in meter,centimeter and millilmeter using object and classes.](#ASSI-3)

[Program-4 WAP for the addition of two times where each time is given in hour,minute and second using object and classes.](#ASSI-4)

[Program-5 WAP for the addition of two times where each time is given in hour and minute using object and classes.](#ASSI-5)

[Program-6 WAP for the addition of two distances where each distance is given in meter and centimeter using object and classes.](#ASSI-6)

[Program-7 WAP using objects and classes to do reverse of 1-D Array](#ASSI-7)

[Program-8 Write a class for implementation operation of matrix(3x3):  1.Transpose, 2.Sum, 3.Multiply, 4.Sum of Rows, 5.Sum of Column, 6.Sum of diagonal](#ASSI-8)

[Program-9  Collect the code of C language for any 5 operation ,convert the logic to java in object orented fashion](#ASSI-9)

[Program-10 Demonstrate all 3 types of inheritance 1. Single, 2. Multilevel, 3. Hierarchial](#ASSI-10)

[PROGRAM 11:Write a class that is having four method for 1-dimensional array. (Input, output 1,out2, reverse).](#ASSI-11)

[PROGRAM 12:write a class with multiple methods to perform matrix operations (transpose, addition, sum of rows, sum of columns, sum of diagonal).](#ASSI-12)

[PROGRAM 13 Write a program using three classes to print 1-100 ,1-100,1-100 with and without thread and analyse the output and repeat the same program using runnable interface.](#ASSI-13)

[PROGRAM 14  Using the concept of multithreading the output of all three threads must be synchronised (use join method).](#ASSI-14)

[PROGRAM 15 Addition of 2 numbers using swing.](#ASSI-15)

[PROGRAM 16:Make one calculator in swing.](#ASSI-16)

[PROGRAM 17:Matrix Addition using swing class.](#ASSI-17)

[PROGRAM 18:Create one jframe apply 10 buttons on that after clicking on each button a new structure is created.(Circle, oval rectangle, etc ....)](#ASSI-18)

[PROGRAM 19:Just using mouse Event create a frame like paint brush with selection of colour and width.](#ASSI-19)





## ASSI-1

```
public class cla {
    static int add(int num1, int num2) { // num1,num2 are integers to add
        return num1 + num2;
    }

    static int sub(int num1, int num2) { // num1,num2 are integers to subtract
        return num1 - num2;
    }

    static int mul(int num1, int num2) { // num1,num2 are integers to multiply
        return num1 * num2;
    }

    static int div(int num1, int num2) { // num1,num2 are integers to divide
        return num1 / num2;
    }

    public static void main(String[] args) {
        int n1 = Integer.parseInt(args[0]); // narrowing of atring arguments into integer arguments
        int n2 = Integer.parseInt(args[1]); // narrowing of atring arguments into integer arguments
        System.out.println("addition of command line arguments are " + add(n1, n2));
        System.out.println("subtraction of command line arguments are " + sub(n1, n2));
        System.out.println("multiplication of command line arguments are " + mul(n1, n2));
        System.out.println("division of command line arguments are " + div(n1, n2));

    }
}# JavaLab
```
<img width="721" height="227" alt="image" src="https://github.com/user-attachments/assets/b8210a15-565e-4345-a73c-59ba3e7a4a1c" />

## ASSI-2
```
public class greetings{
    public static void main(String[]args){
            System.out.print('hello world');
    }
}
```
<img width="721" height="227" alt="image" src="https://github.com/user-attachments/assets/93a81de8-eafc-47cb-86d1-771673e77421" />

## ASSI-3
```
public class AddDis {
    int m, cm, mm; // initialising

    AddDis(int meter, int centimeter, int millimeter) { // constructor
        m = meter;
        cm = centimeter;
        mm = millimeter;
    }

    static AddDis add(AddDis d1, AddDis d2) { // add function
        int m = d1.m + d2.m;
        int cm = d1.cm + d2.cm;
        int mm = d1.mm + d2.mm;

        // convert mm to cm
        cm = cm + (mm / 10);
        mm = mm % 10;

        // convert cm to m
        m = m + (cm / 100);
        cm = cm % 100;

        return new AddDis(m, cm, mm);
    }

    void display() {
        System.out.println(m + " m " + cm + " cm " + mm + " mm");
    }

    public static void main(String[] args) {

        AddDis d1 = new AddDis(200, 20, 50);
        AddDis d2 = new AddDis(200, 56, 87);

        AddDis result = AddDis.add(d1, d2);

        System.out.print("Total Distance: ");
        result.display();
    }
}
```
<img width="550" height="109" alt="image" src="https://github.com/user-attachments/assets/f7463c98-2bb9-46d6-910c-8154980aed00" />

## ASSI-4
```
public class AddTime {
    int hr, min, sec; // variables

    // constructor
    AddTime(int hour, int minute, int second) {
        hr = hour;
        min = minute;
        sec = second;
    }

    // add function
    static AddTime add(AddTime t1, AddTime t2) {
        int hr = t1.hr + t2.hr;
        int min = t1.min + t2.min;
        int sec = t1.sec + t2.sec;

        // convert seconds to minutes
        min = min + (sec / 60);
        sec = sec % 60;

        // convert minutes to hours
        hr = hr + (min / 60);
        min = min % 60;

        return new AddTime(hr, min, sec);
    }

    // display method
    void display() {
        System.out.println(hr + " hr " + min + " min " + sec + " sec");
    }

    public static void main(String[] args) {

        AddTime t1 = new AddTime(2, 45, 50);
        AddTime t2 = new AddTime(1, 30, 30);

        AddTime result = AddTime.add(t1, t2);

        System.out.print("Total Time: ");
        result.display();
    }
}
```
<img width="506" height="126" alt="image" src="https://github.com/user-attachments/assets/981f53be-5f0b-49b9-aa1a-30b078a6333d" />

## ASSI-5
```
public class AddTime {
    int hr, min; // variables

    // constructor
    AddTime(int hour, int minute) {
        hr = hour;
        min = minute;
    }

    // add function
    static AddTime add(AddTime t1, AddTime t2) {
        int hr = t1.hr + t2.hr;
        int min = t1.min + t2.min;

        // convert minutes to hours
        hr = hr + (min / 60);
        min = min % 60;

        return new AddTime(hr, min);
    }

    // display method
    void display() {
        System.out.println(hr + " hr " + min + " min");
    }

    public static void main(String[] args) {

        AddTime t1 = new AddTime(2, 45);
        AddTime t2 = new AddTime(1, 30);

        AddTime result = AddTime.add(t1, t2);

        System.out.print("Total Time: ");
        result.display();
    }
}
```
<img width="523" height="82" alt="image" src="https://github.com/user-attachments/assets/a997feb8-878a-4fff-b983-c9b6988fc60b" />

## ASSI-6
```
public class AddDis {
    int m, cm; // initialising

    AddDis(int meter, int centimeter) { // constructor
        m = meter;
        cm = centimeter;
    }

    static AddDis add(AddDis d1, AddDis d2) { // add function
        int m = d1.m + d2.m;
        int cm = d1.cm + d2.cm;

        // convert cm to m
        m = m + (cm / 100);
        cm = cm % 100;

        return new AddDis(m, cm);
    }

    void display() {
        System.out.println(m + " m " + cm + " cm ");
    }

    public static void main(String[] args) {

        AddDis d1 = new AddDis(200, 20);
        AddDis d2 = new AddDis(200, 56);

        AddDis result = AddDis.add(d1, d2);

        System.out.print("Total Distance: ");
        result.display();
    }
}
```
<img width="548" height="81" alt="image" src="https://github.com/user-attachments/assets/b4677f61-2a88-4f25-a84e-5c3d41f99947" />


## ASSI-7
```
// Main class
public class MainClass {
    public static void main(String[] args) {
        
        ArrayOperations obj = new ArrayOperations();
        
        System.out.println("Original Array:");
        obj.displayArray();
        
        obj.reverseArray();
        
        System.out.println("Reversed Array:");
        obj.displayArray();
    }
}
// Class containing all functions
class ArrayOperations {
    
    int[] arr = {10, 20, 30, 40, 50};  // predefined array

    // Method to reverse array
    void reverseArray() {
        int start = 0, end = arr.length - 1;
        
        while(start < end) {
            int temp = arr[start];
            arr[start] = arr[end];
            arr[end] = temp;
            
            start++;
            end--;
        }
    }

    // Method to display array
    void displayArray() {
        for(int i = 0; i < arr.length; i++) {
            System.out.print(arr[i] + " ");
        }
        System.out.println();
    }
}

```
<img width="531" height="102" alt="image" src="https://github.com/user-attachments/assets/76e80c6a-185e-4cf3-ad4a-9936c14596b9" />

## ASSI-8
```
// Class containing all matrix operations
class MatrixOperations {
    
    int[][] A = {
        {1, 2, 3},
        {4, 5, 6},
        {7, 8, 9}
    };

    int[][] B = {
        {9, 8, 7},
        {6, 5, 4},
        {3, 2, 1}
    };

    // Display matrix
    void display(int[][] M) {
        for(int i = 0; i < 3; i++) {
            for(int j = 0; j < 3; j++) {
                System.out.print(M[i][j] + " ");
            }
            System.out.println();
        }
    }

    // 1. Transpose
    void transpose() {
        int[][] T = new int[3][3];
        
        for(int i = 0; i < 3; i++) {
            for(int j = 0; j < 3; j++) {
                T[j][i] = A[i][j];
            }
        }

        System.out.println("Transpose of Matrix A ");
        display(T);
    }

    // 2. Sum of two matrices
    void sum() {
        int[][] S = new int[3][3];
        
        for(int i = 0; i < 3; i++) {
            for(int j = 0; j < 3; j++) {
                S[i][j] = A[i][j] + B[i][j];
            }
        }

        System.out.println("Sum of A and B ");
        display(S);
    }

    // 3. Multiplication
    void multiply() {
        int[][] M = new int[3][3];
        
        for(int i = 0; i < 3; i++) {
            for(int j = 0; j < 3; j++) {
                M[i][j] = 0;
                for(int k = 0; k < 3; k++) {
                    M[i][j] += A[i][k] * B[k][j];
                }
            }
        }

        System.out.println("Multiplication of A and B ");
        display(M);
    }

    // 4. Sum of rows
    void rowSum() {
        System.out.println("Row sums of Matrix A:");
        
        for(int i = 0; i < 3; i++) {
            int sum = 0;
            for(int j = 0; j < 3; j++) {
                sum += A[i][j];
            }
            System.out.println("Row " + (i+1) + " sum = " + sum);
        }
    }

    // 5. Sum of columns
    void columnSum() {
        System.out.println("Column sums of Matrix A:");
        
        for(int j = 0; j < 3; j++) {
            int sum = 0;
            for(int i = 0; i < 3; i++) {
                sum += A[i][j];
            }
            System.out.println("Column " + (j+1) + " sum = " + sum);
        }
    }
    // 6. Sum of diagonals
void diagonalSum() {
    int primary = 0, secondary = 0;
    
    for(int i = 0; i < 3; i++) {
        primary += A[i][i];           // main diagonal
        secondary += A[i][2 - i];     // secondary diagonal
    }

    System.out.println("Primary Diagonal Sum = " + primary);
    System.out.println("Secondary Diagonal Sum = " + secondary);
}
}

// Main class
public class MainClass {
    public static void main(String[] args) {
        
        MatrixOperations obj = new MatrixOperations();

        System.out.println("Matrix A:");
        obj.display(obj.A);

        System.out.println("Matrix B:");
        obj.display(obj.B);

        obj.transpose();
        obj.sum();
        obj.multiply();
        obj.rowSum();
        obj.columnSum();
        obj.diagonalSum();
    }
}
```
<img width="835" height="720" alt="image" src="https://github.com/user-attachments/assets/af64df54-1337-45a1-a997-7f0088bfe9bc" />

## ASSI-9
```
// Class containing all operations
class NumberOperations {

    int num = 5;      // for factorial & fibonacci
    int pal = 121;    // for palindrome
    int arm = 153;    // for armstrong

    // 1. Factorial
    void factorial() {
        int fact = 1;
        for(int i = 1; i <= num; i++) {
            fact *= i;
        }
        System.out.println("Factorial of " + num + " = " + fact);
    }

    // 2. Fibonacci Series
    void fibonacci() {
        int a = 0, b = 1;
        System.out.println("Fibonacci series:");
        
        for(int i = 1; i <= num; i++) {
            System.out.print(a + " ");
            int c = a + b;
            a = b;
            b = c;
        }
        System.out.println();
    }

    // 3. Palindrome Number
    void palindrome() {
        int temp = pal;
        int rev = 0;
        
        while(temp > 0) {
            int digit = temp % 10;
            rev = rev * 10 + digit;
            temp /= 10;
        }

        if(pal == rev) {
            System.out.println(pal + " is Palindrome");
        } else {
            System.out.println(pal + " is Not Palindrome");
        }
    }

    // 4. Armstrong Number
    void armstrong() {
        int temp = arm;
        int sum = 0;
        
        while(temp > 0) {
            int digit = temp % 10;
            sum += digit * digit * digit; // for 3-digit number
            temp /= 10;
        }

        if(sum == arm) {
            System.out.println(arm + " is Armstrong");
        } else {
            System.out.println(arm + " is Not Armstrong");
        }
    }

    // 5. Pattern (Right Triangle)
    void pattern() {
        System.out.println("Pattern:");
        
        for(int i = 1; i <= 5; i++) {
            for(int j = 1; j <= i; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}

// Main class
public class MainClass {
    public static void main(String[] args) {
        
        NumberOperations obj = new NumberOperations();

        obj.factorial();
        obj.fibonacci();
        obj.palindrome();
        obj.armstrong();
        obj.pattern();
    }
}
```
<img width="584" height="263" alt="image" src="https://github.com/user-attachments/assets/0f6a3ab2-206e-44bf-9f12-d263aaaf4b65" />

## ASSI-10
```
// Base class
class A {
    void showA() {
        System.out.println("Class A (Parent)");
    }
}

// Single Inheritance 
class B extends A {
    void showB() {
        System.out.println("Class B (Child of A)");
    }
}

// Multilevel Inheritance
class C extends B {
    void showC() {
        System.out.println("Class C (Child of B)");
    }
}

// Hierarchical Inheritance
class D extends A {
    void showD() {
        System.out.println("Class D (Another Child of A)");
    }
}

class E extends A {
    void showE() {
        System.out.println("Class E (Another Child of A)");
    }
}

// Main class
public class MainClass {
    public static void main(String[] args) {

        // Single Inheritance
        System.out.println("Single Inheritance:");
        B obj1 = new B();
        obj1.showA();
        obj1.showB();

        // Multilevel Inheritance
        System.out.println("\nMultilevel Inheritance:");
        C obj2 = new C();
        obj2.showA();
        obj2.showB();
        obj2.showC();

        // Hierarchical Inheritance
        System.out.println("\nHierarchical Inheritance:");
        D obj3 = new D();
        E obj4 = new E();

        obj3.showA();
        obj3.showD();

        obj4.showA();
        obj4.showE();
    }
}
```
<img width="701" height="434" alt="image" src="https://github.com/user-attachments/assets/aaab1d2c-b7e2-4a64-8352-3abfbf3c599d" />

## ASSI-11
```

import java.util.Scanner;

class ArrayOperations {
    int arr[];
    int size;

    
    void input() {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter size of array: ");
        size = sc.nextInt();

        arr = new int[size];

        System.out.println("Enter elements:");
        for (int i = 0; i < size; i++) {
            arr[i] = sc.nextInt();
        }
    }

    
    void output1() {
        System.out.println("Array elements (Output1):");
        for (int i = 0; i < size; i++) {
            System.out.print(arr[i] + " ");
        }
        System.out.println();
    }

    
    void output2() {
        System.out.println("Array elements (Output2):");
        for (int x : arr) {
            System.out.print(x + " ");
        }
        System.out.println();
    }

  
    void reverse() {
        System.out.println("Array in reverse:");
        for (int i = size - 1; i >= 0; i--) {
            System.out.print(arr[i] + " ");
        }
        System.out.println();
    }
}


public class Main {
    public static void main(String[] args) {
        ArrayOperations obj = new ArrayOperations();

        obj.input();
        obj.output1();
        obj.output2();
        obj.reverse();
    }
}
```
<img width="836" height="537" alt="image" src="https://github.com/user-attachments/assets/2693fdbf-0d3a-46cd-9b2b-5191b77141b3" />

## ASSI-12
```
import java.util.Scanner;

class MatrixOperations {
    int a[][], b[][], result[][];
    int r, c;

    // Input matrices
    void input() {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter rows and columns: ");
        r = sc.nextInt();
        c = sc.nextInt();

        a = new int[r][c];
        b = new int[r][c];
        result = new int[r][c];

        System.out.println("Enter elements of Matrix A:");
        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++) {
                a[i][j] = sc.nextInt();
            }
        }

        System.out.println("Enter elements of Matrix B:");
        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++) {
                b[i][j] = sc.nextInt();
            }
        }
    }

    // Display matrix
    void display(int m[][]) {
        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++) {
                System.out.print(m[i][j] + " ");
            }
            System.out.println();
        }
    }

    // Addition of matrices
    void addition() {
        System.out.println("Addition of matrices:");
        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++) {
                result[i][j] = a[i][j] + b[i][j];
            }
        }
        display(result);
    }

    // Transpose of matrix A
    void transpose() {
        System.out.println("Transpose of Matrix A:");
        for (int i = 0; i < c; i++) {
            for (int j = 0; j < r; j++) {
                System.out.print(a[j][i] + " ");
            }
            System.out.println();
        }
    }

    // Sum of rows (Matrix A)
    void sumRows() {
        System.out.println("Sum of rows (Matrix A):");
        for (int i = 0; i < r; i++) {
            int sum = 0;
            for (int j = 0; j < c; j++) {
                sum += a[i][j];
            }
            System.out.println("Row " + (i + 1) + " = " + sum);
        }
    }

    // Sum of columns (Matrix A)
    void sumColumns() {
        System.out.println("Sum of columns (Matrix A):");
        for (int i = 0; i < c; i++) {
            int sum = 0;
            for (int j = 0; j < r; j++) {
                sum += a[j][i];
            }
            System.out.println("Column " + (i + 1) + " = " + sum);
        }
    }

    // Sum of diagonal elements (Matrix A)
    void sumDiagonal() {
        int sum = 0;
        for (int i = 0; i < r && i < c; i++) {
            sum += a[i][i];
        }
        System.out.println("Sum of diagonal elements = " + sum);
    }
}

// Main class
public class Main {
    public static void main(String[] args) {
        MatrixOperations obj = new MatrixOperations();

        obj.input();
        System.out.println("\nMatrix A:");
        obj.display(obj.a);

        System.out.println("\nMatrix B:");
        obj.display(obj.b);

        obj.addition();
        obj.transpose();
        obj.sumRows();
        obj.sumColumns();
        obj.sumDiagonal();
    }
}
```
<img width="1177" height="590" alt="image" src="https://github.com/user-attachments/assets/ccd2a5ca-c3fb-41e7-9ef2-120fad15adc0" />
<img width="1112" height="567" alt="image" src="https://github.com/user-attachments/assets/97c01cb5-a26c-4682-93eb-04b291b813c2" />



## ASSI-13
```


class A {
    void print() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("A: " + i);
        }
    }
}

class B {
    void print() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("B: " + i);
        }
    }
}

class C {
    void print() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("C: " + i);
        }
    }
}

public class Main {
    public static void main(String[] args) {
        A a = new A();
        B b = new B();
        C c = new C();

        a.print();
        b.print();
        c.print();
    }
}
```
<img width="1172" height="779" alt="image" src="https://github.com/user-attachments/assets/f6975565-84a6-4a08-85b5-52f0b2e4e6e1" />
<img width="1176" height="753" alt="image" src="https://github.com/user-attachments/assets/069b5acf-5f11-424f-8866-9c5954aaddb3" />

<img width="1205" height="783" alt="image" src="https://github.com/user-attachments/assets/2d4775de-7a65-4a03-8869-0e09c6a36966" />
<img width="1180" height="731" alt="image" src="https://github.com/user-attachments/assets/db06c5ad-7f89-4d56-8a10-9bfcc95b5762" />
<img width="1173" height="721" alt="image" src="https://github.com/user-attachments/assets/f5dc1e1a-f685-44ce-a0b6-54e67d66158f" />
<img width="1192" height="714" alt="image" src="https://github.com/user-attachments/assets/66859fc4-2f26-4569-95b3-cd660c249d1c" />
<img width="1170" height="775" alt="image" src="https://github.com/user-attachments/assets/40af6795-5206-4552-875d-7ca6a89a18ac" />
<img width="890" height="850" alt="image" src="https://github.com/user-attachments/assets/c684cc33-2271-40dd-b946-f2665ec927fa" />

## ASSI-14
```
class MyThread extends Thread {
    String name;

    MyThread(String name) {
        this.name = name;
    }

    public void run() {
        for (int i = 1; i <= 100; i++) {
            System.out.println(name + ": " + i);
        }
    }
}

public class Main {
    public static void main(String[] args) {
        try {
            MyThread t1 = new MyThread("A");
            MyThread t2 = new MyThread("B");
            MyThread t3 = new MyThread("C");

            t1.start();
            t1.join();   // wait until t1 finishes

            t2.start();
            t2.join();   // wait until t2 finishes

            t3.start();
            t3.join();   // wait until t3 finishes

        } catch (InterruptedException e) {
            System.out.println(e);
        }
    }
}
```
<img width="1172" height="779" alt="image" src="https://github.com/user-attachments/assets/f6975565-84a6-4a08-85b5-52f0b2e4e6e1" />
<img width="1176" height="753" alt="image" src="https://github.com/user-attachments/assets/069b5acf-5f11-424f-8866-9c5954aaddb3" />

<img width="1205" height="783" alt="image" src="https://github.com/user-attachments/assets/2d4775de-7a65-4a03-8869-0e09c6a36966" />
<img width="1180" height="731" alt="image" src="https://github.com/user-attachments/assets/db06c5ad-7f89-4d56-8a10-9bfcc95b5762" />
<img width="1173" height="721" alt="image" src="https://github.com/user-attachments/assets/f5dc1e1a-f685-44ce-a0b6-54e67d66158f" />
<img width="1192" height="714" alt="image" src="https://github.com/user-attachments/assets/66859fc4-2f26-4569-95b3-cd660c249d1c" />
<img width="1170" height="775" alt="image" src="https://github.com/user-attachments/assets/40af6795-5206-4552-875d-7ca6a89a18ac" />
<img width="890" height="850" alt="image" src="https://github.com/user-attachments/assets/c684cc33-2271-40dd-b946-f2665ec927fa" />

## ASSI-15
```
import javax.swing.*;
import java.awt.event.*;

public class AddSwing {
    public static void main(String[] args) {

        // Create frame
        JFrame f = new JFrame("Addition");

        // Create components
        JLabel l1 = new JLabel("Enter first number:");
        JLabel l2 = new JLabel("Enter second number:");
        JTextField t1 = new JTextField();
        JTextField t2 = new JTextField();
        JButton b = new JButton("Add");

        // Set positions
        l1.setBounds(30, 30, 150, 30);
        t1.setBounds(180, 30, 100, 30);

        l2.setBounds(30, 80, 150, 30);
        t2.setBounds(180, 80, 100, 30);

        b.setBounds(100, 130, 80, 30);

        // Add components to frame
        f.add(l1);
        f.add(t1);
        f.add(l2);
        f.add(t2);
        f.add(b);

        // Button action
        b.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                int a = Integer.parseInt(t1.getText());
                int b1 = Integer.parseInt(t2.getText());
                int sum = a + b1;

                JOptionPane.showMessageDialog(f, "Sum = " + sum);
            }
        });

        // Frame settings
        f.setSize(350, 250);
        f.setLayout(null);
        f.setVisible(true);
        f.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
    }
}
```
<img width="578" height="413" alt="image" src="https://github.com/user-attachments/assets/d9c59517-4242-4a0e-897f-dcffe596a994" />
<img width="459" height="206" alt="image" src="https://github.com/user-attachments/assets/9247390e-7d95-46e5-a693-824025a97dae" />

## ASSI-16
```
import javax.swing.*;
import java.awt.event.*;

public class Calculator implements ActionListener {

    JFrame f;
    JTextField t;
    JButton b1,b2,b3,b4,b5,b6,b7,b8,b9,b0;
    JButton add, sub, mul, div, eq, clr;

    int num1, num2, result;
    char op;

    Calculator() {
        f = new JFrame("Calculator");

        t = new JTextField();
        t.setBounds(30, 40, 240, 30);

        b1 = new JButton("1"); b1.setBounds(30,80,50,40);
        b2 = new JButton("2"); b2.setBounds(90,80,50,40);
        b3 = new JButton("3"); b3.setBounds(150,80,50,40);

        b4 = new JButton("4"); b4.setBounds(30,130,50,40);
        b5 = new JButton("5"); b5.setBounds(90,130,50,40);
        b6 = new JButton("6"); b6.setBounds(150,130,50,40);

        b7 = new JButton("7"); b7.setBounds(30,180,50,40);
        b8 = new JButton("8"); b8.setBounds(90,180,50,40);
        b9 = new JButton("9"); b9.setBounds(150,180,50,40);

        b0 = new JButton("0"); b0.setBounds(90,230,50,40);

        add = new JButton("+"); add.setBounds(210,80,50,40);
        sub = new JButton("-"); sub.setBounds(210,130,50,40);
        mul = new JButton("*"); mul.setBounds(210,180,50,40);
        div = new JButton("/"); div.setBounds(210,230,50,40);

        eq = new JButton("="); eq.setBounds(30,230,50,40);
        clr = new JButton("C"); clr.setBounds(150,230,50,40);

        JButton[] buttons = {b1,b2,b3,b4,b5,b6,b7,b8,b9,b0,add,sub,mul,div,eq,clr};

        for (JButton b : buttons) {
            f.add(b);
            b.addActionListener(this);
        }

        f.add(t);
        f.setSize(320,350);
        f.setLayout(null);
        f.setVisible(true);
        f.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
    }

    public void actionPerformed(ActionEvent e) {
        String s = e.getActionCommand();

        if (s.matches("[0-9]")) {
            t.setText(t.getText() + s);
        }
        else if (s.equals("+") || s.equals("-") || s.equals("*") || s.equals("/")) {
            num1 = Integer.parseInt(t.getText());
            op = s.charAt(0);
            t.setText("");
        }
        else if (s.equals("=")) {
            num2 = Integer.parseInt(t.getText());

            switch(op) {
                case '+': result = num1 + num2; break;
                case '-': result = num1 - num2; break;
                case '*': result = num1 * num2; break;
                case '/': result = num1 / num2; break;
            }

            t.setText("" + result);
        }
        else if (s.equals("C")) {
            t.setText("");
        }
    }

    public static void main(String[] args) {
        new Calculator();
    }
}
```
<img width="522" height="569" alt="image" src="https://github.com/user-attachments/assets/7ae59c9c-6951-4a50-9dbf-1001543363bb" />

## ASSI-17
```
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

public class MatrixAdditionUI extends JFrame implements ActionListener {

    JTextField[][] m1 = new JTextField[2][2];
    JTextField[][] m2 = new JTextField[2][2];
    JTextField[][] result = new JTextField[2][2];
    JButton addBtn;

    public MatrixAdditionUI() {

        setTitle("Matrix Addition");
        setSize(420, 250);
        setLocationRelativeTo(null);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        // Main panel
        JPanel mainPanel = new JPanel(new GridLayout(1, 3, 15, 10));

        // Matrix Panels
        mainPanel.add(createMatrixPanel("Matrix A", m1));
        mainPanel.add(createMatrixPanel("Matrix B", m2));
        mainPanel.add(createMatrixPanel("Result", result));

        // Button panel
        JPanel btnPanel = new JPanel();
        addBtn = new JButton("Add Matrices");
        addBtn.setFocusPainted(false);
        addBtn.setBackground(new Color(70, 130, 180));
        addBtn.setForeground(Color.WHITE);
        addBtn.setFont(new Font("Arial", Font.BOLD, 12));
        addBtn.addActionListener(this);
        btnPanel.add(addBtn);

        // Layout set
        setLayout(new BorderLayout(10, 10));
        add(mainPanel, BorderLayout.CENTER);
        add(btnPanel, BorderLayout.SOUTH);

        setVisible(true);
    }

    // Method to create matrix panel
    private JPanel createMatrixPanel(String title, JTextField[][] matrix) {
        JPanel panel = new JPanel();
        panel.setBorder(BorderFactory.createTitledBorder(title));
        panel.setLayout(new GridLayout(2, 2, 5, 5));

        for (int i = 0; i < 2; i++) {
            for (int j = 0; j < 2; j++) {
                matrix[i][j] = new JTextField(2); // smaller box
                matrix[i][j].setHorizontalAlignment(JTextField.CENTER);
                matrix[i][j].setFont(new Font("Arial", Font.BOLD, 14));
                panel.add(matrix[i][j]);
            }
        }
        return panel;
    }

    public void actionPerformed(ActionEvent e) {
        try {
            for (int i = 0; i < 2; i++) {
                for (int j = 0; j < 2; j++) {
                    int a = Integer.parseInt(m1[i][j].getText());
                    int b = Integer.parseInt(m2[i][j].getText());
                    result[i][j].setText(String.valueOf(a + b));
                }
            }
        } catch (Exception ex) {
            JOptionPane.showMessageDialog(this, "Enter valid numbers!");
        }
    }

    public static void main(String[] args) {
        new MatrixAdditionUI();
    }
}
```
<img width="702" height="421" alt="image" src="https://github.com/user-attachments/assets/a5718f44-3738-4ccd-a58b-99922e3d247b" />

## ASSI-18
```
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

public class ShapeDrawer extends JFrame implements ActionListener {

    String shape = "";
    DrawPanel panel;

    public ShapeDrawer() {
        setTitle("Shape Drawer");
        setSize(500, 400);
        setLocationRelativeTo(null);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        // Panel for buttons
        JPanel btnPanel = new JPanel(new GridLayout(2, 5, 8, 8));

        String[] shapes = {
            "Circle", "Oval", "Rectangle", "Square", "Line",
            "Triangle", "Arc", "RoundRect", "3DRect", "Ellipse"
        };

        for (String s : shapes) {
            JButton btn = new JButton(s);
            btn.setFocusPainted(false);
            btn.setBackground(new Color(60, 120, 180));
            btn.setForeground(Color.WHITE);
            btn.addActionListener(this);
            btnPanel.add(btn);
        }

        // Drawing panel
        panel = new DrawPanel();
        panel.setBackground(Color.WHITE);

        setLayout(new BorderLayout(10, 10));
        add(btnPanel, BorderLayout.NORTH);
        add(panel, BorderLayout.CENTER);

        setVisible(true);
    }

    public void actionPerformed(ActionEvent e) {
        shape = e.getActionCommand();
        panel.repaint();
    }

    // Custom panel for drawing
    class DrawPanel extends JPanel {
        protected void paintComponent(Graphics g) {
            super.paintComponent(g);
            g.setColor(Color.BLACK);

            switch (shape) {
                case "Circle":
                    g.drawOval(150, 80, 100, 100);
                    break;

                case "Oval":
                    g.drawOval(120, 80, 160, 100);
                    break;

                case "Rectangle":
                    g.drawRect(120, 80, 160, 100);
                    break;

                case "Square":
                    g.drawRect(150, 80, 100, 100);
                    break;

                case "Line":
                    g.drawLine(100, 50, 300, 200);
                    break;

                case "Triangle":
                    int x[] = {150, 250, 200};
                    int y[] = {150, 150, 50};
                    g.drawPolygon(x, y, 3);
                    break;

                case "Arc":
                    g.drawArc(120, 80, 160, 100, 0, 180);
                    break;

                case "RoundRect":
                    g.drawRoundRect(120, 80, 160, 100, 30, 30);
                    break;

                case "3DRect":
                    g.draw3DRect(120, 80, 160, 100, true);
                    break;

                case "Ellipse":
                    g.drawOval(130, 70, 140, 120);
                    break;
            }
        }
    }

    public static void main(String[] args) {
        new ShapeDrawer();
    }
}
```
<img width="851" height="676" alt="image" src="https://github.com/user-attachments/assets/5c13ea73-8622-4680-ab95-b07319394ea0" />

## ASSI-19
```
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

public class PaintBrushApp extends JFrame {

    Color currentColor = Color.BLACK;
    int brushSize = 5;

    DrawArea drawArea;

    public PaintBrushApp() {

        setTitle("Mini Paint Brush");
        setSize(600, 450);
        setLocationRelativeTo(null);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        // Top panel (controls)
        JPanel topPanel = new JPanel();

        // Color Button
        JButton colorBtn = new JButton("Choose Color");
        colorBtn.addActionListener(e -> {
            Color newColor = JColorChooser.showDialog(this, "Select Color", currentColor);
            if (newColor != null) currentColor = newColor;
        });

        // Brush size selector
        String sizes[] = {"2", "5", "10", "15", "20"};
        JComboBox<String> sizeBox = new JComboBox<>(sizes);
        sizeBox.setSelectedIndex(1);
        sizeBox.addActionListener(e -> {
            brushSize = Integer.parseInt((String) sizeBox.getSelectedItem());
        });

        // Clear button
        JButton clearBtn = new JButton("Clear");
        clearBtn.addActionListener(e -> drawArea.clear());

        topPanel.add(colorBtn);
        topPanel.add(new JLabel("Brush Size:"));
        topPanel.add(sizeBox);
        topPanel.add(clearBtn);

        // Drawing area
        drawArea = new DrawArea();
        drawArea.setBackground(Color.WHITE);

        add(topPanel, BorderLayout.NORTH);
        add(drawArea, BorderLayout.CENTER);

        setVisible(true);
    }

    // Drawing Panel
    class DrawArea extends JPanel implements MouseMotionListener {

        Image image;
        Graphics2D g2;

        public DrawArea() {
            addMouseMotionListener(this);
        }

        protected void paintComponent(Graphics g) {
            super.paintComponent(g);

            if (image == null) {
                image = createImage(getWidth(), getHeight());
                g2 = (Graphics2D) image.getGraphics();
                g2.setRenderingHint(RenderingHints.KEY_ANTIALIASING,
                                    RenderingHints.VALUE_ANTIALIAS_ON);
                clear();
            }

            g.drawImage(image, 0, 0, null);
        }

        public void clear() {
            if (g2 != null) {
                g2.setPaint(Color.WHITE);
                g2.fillRect(0, 0, getWidth(), getHeight());
                g2.setPaint(currentColor);
                repaint();
            }
        }

        public void mouseDragged(MouseEvent e) {
            if (g2 != null) {
                g2.setPaint(currentColor);
                g2.setStroke(new BasicStroke(brushSize,
                        BasicStroke.CAP_ROUND,
                        BasicStroke.JOIN_ROUND));

                g2.drawLine(e.getX(), e.getY(), e.getX(), e.getY());
                repaint();
            }
        }

        public void mouseMoved(MouseEvent e) {}
    }

    public static void main(String[] args) {
        new PaintBrushApp();
    }
}
```
<img width="1026" height="758" alt="image" src="https://github.com/user-attachments/assets/d808218c-fe25-43f7-a8cb-7e3b26ba37f7" />




















