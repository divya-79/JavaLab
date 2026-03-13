[Program-1 WAP TO DEMONSTRATE COMMAND LINE ARGUMENT](#ASSI-1)

[Program-2 WAP TO DEMONSTRATE HELLO-WORLD](#ASSI-2)

[Program-3 WAP for the addition of two distances where each distance is given in meter,centimeter and millilmeter using object and classes.](#ASSI-3)

[Program-4 WAP for the addition of two times where each time is given in hour,minute and second using object and classes.](#ASSI-4)

[Program-5 WAP for the addition of two times where each time is given in hour and minute using object and classes.](#ASSI-5)


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



