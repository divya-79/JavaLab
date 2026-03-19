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







