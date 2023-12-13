# Variables and Data Types in C#

### ***Variables***
Variables are used to **store** up **temporary data** to be used in our **program's runtime**.

### ***Data Types***
The **Type** of **Data** inside our variable.

|  |  |  |
| ----------- | ----------- | ----------- |
| **Characters** | *char* | Holds a Single Character
| **String** | *string* | Holds a Set of Characters/ Texts
| **Boolean** | *bool* | Holds True of False
| **Integers** | *int* | -2147483648 to 214748348
|  | *long* | -9223372036854775808 to 9223372036854775808
| **Floating Point** | *float* | 6/7 decimals
|  | *double* | 15 decimals

### ***Identifiers***
It is the **Name** of the **Variable** that the **programmer indicated** it is **used** to **read** and **write** inside the **variable**.

#### Rules of Identifiers
- You cannot use any special characters other than underscore (-)
- You cannot use whitespaces
- You cannot use numbers alone
- You cannot use numbers to be the first character of the identifier
- You cannot use numbers but with letters

### ***Declaring Variables***
#### **Syntax:** 
***datatype*** identifier;  
***datatype*** identifier = value;  
***datatype*** identifier1, identifier2;  
***datatype*** identifier1 = value, identifier2 = value;

```csharp
string name = Kkuru;
int age = 21;
char sex = 'M'      // single quote if char
bool isTall = true; // case sensitive
float ave = 1.5f;   // 'f' to indicate float
```

### ***Reassigning Variables***
#### **Syntax:**
identifier = value;

```csharp
string name;
int age;

name = "Kkuru";
age = 21;
```

### ***Console.WriteLine()***
1. Used to display something in the console.
2. We can display a variable's value by indicating its identifier inside the parentheses.

```csharp
int age = 21;
Console.WriteLne(age);
```

### ***Concatenation***
The process of joining Strings together with the plus operator. You can concatenate **INSIDE** a **Variable** or on the **WriteLine Statement**.


| Concatenation  | Not Concatenation |
| ----------- | ----------- |
| "Hello" + "World" | 2 + 3 |
| "2" + "3" | 'a' + 3 |
| 'a' + "b" |  |
| 2 + "3" |  |

# User Input in C#

### ***Console.ReadLine()***
Used for inputting a string. 

```csharp
string name;

Console.Write("Name: ");
name = Console.ReadLine();

Console.WriteLine("I am" + name);
```
### ***Console.Read()***
Used for inputting a Character by pressing Enter in the keyboard.

```csharp
char letter;

Console.Write("Letter: ");
letter = (char) Console.Read();

Console.WriteLine(letter);
```
### ***Console.ReadKey()***
Used for inputting a Character by pressing a Letter in the keyboard.

```csharp
char letter;

Console.Write("Press a letter: ");
letter = Console.ReadKey().KeyChar;

Console.WriteLine("\nYou pressed" + letter);
```

It is also used to delay printed *WriteLines*.

```csharp
Console.WriteLine("Hi!");
Console.ReadKey();
Console.WriteLine("I am Kkuru");
Console.ReadKey();
Console.WriteLine("Goodbye!");
```
# Datatype Conversion in C#

## ***Data type Conversion***
It is an act of converting one datatype to another.

### ***Type Casting***
Assigning a value of one datatype to another datatype.

#### ***Implicit Casting***
Converting a smaller type to a larger type size. This is done automatically.

    char -> int -> long -> float -> double

```csharp
int myInt = 10;
double myDouble = myInt;

char myChar = 'B';
int asciiCode = myChar;
```

#### ***Explicit Casting***
Converting a larger type to a smaller size type. It is done manually by using the parentheses with the datatype in it.

    double -> float -> long -> int -> char

```csharp
double myDouble = 236.75;
int x = (int) myDouble;
```

### ***Conversion Method***
It uses a built-in method to convert datatypes from one type to another especially strings.

| | |
| ----------- | ----------- |
| **Convert.ToInt32()** | *string* to *int* | 
| **Convert.ToInt64()** | *string* to *long* |
| **Convert.ToSingle()** | *string* to *float* |
| **Convert.ToDouble()** | *string* to *double* |
| **Convert.ToString()** | *any data type* to *string* |

# Arithmetic Operators in C#

| Symbol | Operation | Result | Usage |
| ----------- | ----------- | ----------- | ----------- |
| + | Addition | Sum | x + y
| - | Subtraction| Difference| x - y |
| * | Multiplication | Product | x * y
| / | Division | Quotient | x / y
| % | Modulus | Remainder | x % y
| ++ | Increment | Plus 1 | x++
| -- | Decrement | Minus 1 | x--


## ***Assignment Arithmetic Operators***
***x += y*** is same as ***x = x + y***

| Symbol | Operation | Result | Usage |
| ----------- | ----------- | ----------- | ----------- |
| += | Addition | Sum | x += y
| -= | Subtraction| Difference| x -= y |
| *= | Multiplication | Product | x *= y
| /= | Division | Quotient | x /= y
| %= | Modulus | Remainder | x %= y

# Arrays in C#

is a Collection of Multiple Values in a **Single  Variable** with the **Same Datatype**. They are governed by using an **index**.

### ***Elements***
The individual values in an array.

## ***Declaring Arrays***
### ***Declare with Values***

```csharp
string[] names = {"Kkuru", "Jiro", "Jin"};
```

### ***Declare without Values***

```csharp
string[] names = new string[4];
```


## ***Index***
A number that represents a position in a collection.

### ***Accessing Array***

| ***Value*** | "Kkuru" | "Jiro" | "Jin" | "Ssamu" | "Mina" |
| ----------- | ----------- | ----------- | ----------- | ----------- | ----------- |
| ***Index*** | 0 | 1 | 2 | 3 | 4 |

### ***Reading Array Element***
```csharp
names[0];
```

### ***Assigning Array Element***
```csharp
names[0] = "Sana";
```

### ***Assigning Array Element with User Input***
```csharp
names[0] = Console.ReadLine();
```

# Conditionals in C#

### ***Conditional Statements***
Allows a program to make action based on the*given condition*. It makes our program smarter. Typically it *compares two values* so that our program can decide what action should be taken.

| Label | Symbol | Syntax |
| ----------- | ----------- | ----------- |
| Equals | == | x == y
| NOT Equals | != | x != y
| Less Than | < | x < y
| Less Than or Equals | <= | x<= y
| Greater Than | > | x > y
| Greater Than or Equals | >= | x >= y

### **IF Statement**
Handles **1 Conditional Expression**, it **either** does **SOMETHING** or **NOTHING**.

```csharp
int age = 18;

if(age >= 18){
    Console.WriteLine("You can drive.")
}
```

### **IF-ELSE Statement**
Handles **2 Conditional Expressions**, it **either** does the first Code Block or the second Code Block.

```csharp
Console.Write("Population: ");

int currentPopulation = ConvertToInt32(Console.ReadLine());
int maxPopulation = 100;

if (currentPopulation == maxPopulation)
{
    Console.WriteLine("Population Stable.");
}
else
{
    Console.WriteLine("Overpopulated.");
}
```

### **IF - ELSE IF - ELSE**
Handles **3 or More Conditional Expressions**, The possibility of this Statements are limitless it will run a certain code block based on the condition.

```csharp
Console.Write("Age: ");
int age = Convert.ToInt32(Console.ReadLine);

if (age >= 24)
{
    Console.WriteLine("Adult");
}
else if (age >= 18)
{
    Console.WriteLine("Young Adult");
}
else if (age >= 13)
{
    Console.WriteLine("Teenager");
}
else if (age >= 4)
{
    Console.WriteLine("Kid");
}
else
{
    Console.WriteLine("Baby");
}
```

### **Nested Conditional Statement**
A **Conditional Statement** within a **Conditional Statement**. It can be an any type of **Conditional Statement**.

```csharp
int age = 18;
bool isRegistered = true;

if (age >= 18)
{
    if (isRegistered)
    {
        Console.WriteLine("You can vote!");
    }
    else
    {
        Console.WriteLine("You can register as a Voter!");
    }
}

else
{
    Console.WriteLine("Access Denied!");
}
```


### **Equals Method**

```csharp
Console.Write("Password: ");
string pword = Console.ReadLine();

if(pword.Equals("imcute123"))
{
    Console.WriteLine("Login Successul!");
}
else
{
    Console.WriteLine("Access Denied!");
}
```

### **Equals Method (*Ignoring Case*)**

```csharp
Console.Write("Username: ");
string user = Console.Readline();

if(user.Equals("kkuru",StringComparison.InvariantCultureIgnoreCase))
{
    Console.WriteLine("User Exist.");
}
else
{
    Console.WriteLine("User Not Found.");
}
```

## ***Logical Operators***

| Label | Symbol | Syntax | Description
| ----------- | ----------- | ----------- |----------- |
| AND | && | condition && condition | Both Conditions need to be True.
| OR | \|\| | condition \|\| condition | Either Conditions need to be True.
| NOT | ! | !condition | Inverts the Current Condition

#### *NOT*
```csharp
int age = 18;

if(!(age >= 18))
{
    Console.WriteLine("Access Denied!");
}
else
{
    Console.WriteLine("Access Granted!");
}
```

#### *AND*
```csharp
int age = 12;
bool isRegistered = true;

if (age >= 18 && isRegistered)
{
    Console.WriteLine("You can vote");
}
else
{
    Console.WriteLine("Access Denied!");
}
```
#### *OR*
```csharp
bool level = 50;
bool isVIP = true;

if(level >= 100 || isVIP)
{
    Console.WriteLine("You have obtained the legendary item!");
}
else
{
    Console.WriteLine("You don't meet the requirements");
}
```

# Switch Statements in C#

### ***Switch Statements***
it is a similar to a Conditional Statement but only checks for equality and only works with **strings**, **char**, **int**, and **enums**.

```csharp
char grades = 'A';

switch(grades)
{
    case 'A':
        Console.WriteLine("Outstanding!");
        break;
        
    case 'B':
        Console.WriteLine("Excellent!");
        break;

    case 'C':
        Console.WriteLine("Satisfactory");
        break;
        
    case 'D':
        Console.WriteLine("Good");
        break;

    case 'E':
        Console.WriteLine("Needs Improvement");
        break;

    case 'F':
        Console.WriteLine("Failed");
        break;

```

### ***Case Keyword***
Used to define a "*Case*" in switch statement.

### ***Default Keyword***
Often used to **handle values** that are **NOT** on the **Case**. It is recommended that this keyword is used on the **END** of a **switch statement**.

```csharp
    default:
        Console.WriteLine("Invalid Grade");
        break;
}
```

### ***Break Keyword***
used to **Break Out** of a **switch statement** or **loop statements** without executing the whole block of code inside it.

# While and Do While Loop in C#

### ***WHILE Loop***
It is used when you want a Code Block to run repeatedly **WHILE** a **CONDITION** is met.

```csharp
int 0;

while (i < 5)
{
    Console.WriteLine(i);
    i++;
}
```

#
    0
    1
    2
    3
    4

### ***ITERATING Arrays***
It means, reads every element inside an array and do something with it.

```csharp
int i = 0;
string[] names = {"Kkuru", "Jin", "Jiro", "Sana", "Mina"};

while (i < 5)
{
    Console.WriteLine(names[i]);
    i++;
}
```

#
    Kkuru
    Jin
    Jiro
    Sana
    Mina

### ***Array LENGTH***
You can find out the size of an array by calling their length variable(built in variable in an array)

```csharp
int i = 0;
string[] names = {"Kkuru", "Jin", "Jiro", "Sana", "Mina"};
    
while(i <= names.length);
{
    Console.WriteLine(names[i]);
    i++;
}
```
#
    Kkuru
    Jin
    Jiro
    Sana
    Mina


### ***DO - WHILE Loop***
Same as the While Loop but it **EXECUTES** the Code Block first before checking the **CONDITION**.

```csharp
int j = 0;

do
{
    Console.WriteLine(j);
    j++;
}
while (j < 5);
```
#
    0
    1
    2
    3
    4

### ***BREAK Keyword***
Used to **BREAK Out** of a **LOOP** Statement **earlier** than it is **expected** to end.

```csharp
int i = 0;

string[] names = {"Kkuru", "Jin", "Jiro", "Sana", "Mina"};

while (i < 5)
{
    Console.WriteLine(names[i]);
    i++;
    break;
}
```
#
    Kkuru

### ***Conditions in WHILE Loop***

You can use Conditions inside a while loop for different reasons like, searching inside an array.

```csharp
string[] names = {"Kkuru", "Jin", "Jiro", "Sana", "Mina"};
int i = 0;

while (i < 5)
{
    if(names[i].Equals("Jiro"))
    {
        Console.WriteLine("We found " + names[i]);
        break;
    }
    else
    {
        Console.WriteLine(names[i]);
    }
    i++;
}
```
#
    Kkuru
    Jin
    Jiro

    # FOR Loop in C#

### ***For Loop***
It is used when you want a Code Block to run repeatedly **WHILE** the **Condition is Met.**  
Its a **more compact format** but **more complicated** version of a **WHILE loop**. **FOR Loops** are commonly used to **iterate** through **Collections** and **Arrays**.

```csharp
for(int i = 0; i < 5; i++)
{
    Console.WriteLine(i);
}
```

    0
    1
    2
    3
    4

### ***ITERATING Arrays***
It means to read every element inside an array and do something with it.

```csharp
string[] names = {"Kkuru","Jin","Jiro","Sana","Mina"};

for(int i; i < 5; i++)
{
    Console.WriteLine(names[i]);
}
```


    Kkuru
    Jin
    Jiro
    Sana
    Mina


### ***Array LENGTH***
You can find out the size of an array by calling their length variable (built-in variable in an array).

```csharp
string[] names = {"Kkuru","Jin","Jiro","Sana","Mina","IU","Ssamu"};

for (int i = 0; i < names.Length; i++)
{
    Console.WriteLine(names[i]);
}
```

    Kkuru
    Jin
    Jiro
    Sana
    Mina
    IU
    Ssamu

*Other Example*

```csharp
string[] names = {"Kkuru","Jin","Jiro","Sana","Mina","IU","Ssamu"};

for (int i = names.Length - 1; i >= 0; i--)
{
    Console.WriteLine(names[i]);
}
```

    Ssamu
    IU
    Mina
    Sana
    Jiro
    Jin
    Kkuru


### ***BREAK Keyword***
Used to **BREAK Out** of a **LOOP** statement **earlier** than it is **expected** to end.

### ***CONDITIONS in For Loop***
You can use Conditions inside a for loop for different reasons like, searching inside an array.

```csharp
string[] names = {"Kkuru","Jin","Jiro","Sana","Mina"};

for(int i = 0; i < names.Length; i++)
{
    if (names[i].Equals("Sana"))
    {
        Console.WriteLine($"We found {names[i]}");
        break;
    }
    else
    {
        Console.WriteLine(names[i]);
    }
}
```

    Kkuru
    Jin
    Jiro
    We found Sana

    # FOR EACH Loop in C#

### ***For Each Loop***
Used to iterate through collections like arrays easily without knowing the size of the collection.

### ***Iterating Arrays***
It means to read every element inside an array and do something with it.

```csharp
string[] names = {"Kkuru", "Jiro", "Jin","Ssamu", "Wonchae"};

foreach(string name in names)
{
    Console.WriteLine(name);
}
```
    Kkuru
    Jiro
    Jin
    Ssamu
    Wonchae

### ***Break Keyword***
Used to **BREAK Out** of a **LOOP** statemant **earlier** than it is **expected** to end.

```csharp
string[] names = {"Kkuru", "Jiro", "Jin", "Ssamu", "Wonchae"};

foreach(string name in names)
{
    Console.WriteLine(name);
    break;
}
```

    Kkuru

### ***Conditions in FOR-EACH Loop***
You can use Conditions inside a for-each loop for different reasons like, searching inside an array.

```csharp
string[] names = {"Kkuru", "Jiro", "Jin", "Ssamu", "Wonchae"};

foreach(string name in names)
{
    if (name = "Jin")
    {
        Console.WriteLine($"I found {name}");
        break;
    }
}
```
    Kkuru
    Jiro
    I found Jin

    # 2D Array and Nested For Loops in C#

### ***2D Array***
It's **arrays within** an **array**, it basically looks like a table with rows and columns.

Like **1D Arrays**, it can only store **one datatype** at a time.

### ***Declaring 2D Arrays***
#### ***Declare with values***

    datatype[,] identifiers = {  
        {val1, val2},
        {val1, val2},
        {val1, val2}
    };
___
###### ***Example***

```csharp
string[,] users =
{
    {"Kkuru", "Kkuru123"},
    {"Jiro", "Jiro123"},
    {"Jin", "Jin123"},
    {"Ssamu", "Ssamu123"},
    {"Wonchae", "Wonchae123"}
};
```
#### ***Declaring without values***

    datatype[,] identifiers = new datatype [rows, cols];

___
###### ***Example***
```csharp
string[,] users = new string [4, 2];
```

### ***Accessing 2D Arrays***

```csharp
string[,] users =
{
    {"Kkuru", "Kkuru123"},
    {"Jiro", "Jiro123"},
    {"Jin", "Jin123"},
    {"Ssamu", "Ssamu123"},
    {"Wonchae", "Wonchae123"}
};
```
| INDEX | 0 | 1 
| ----------- | ----------- | -----------
| 0 | "Kkuru" **[0,0]** | "Kkuru123" **[0,1]**
| 1 | "Jiro" **[1,0]** | "Jiro123" **[1,1]**
| 2 | "Jin" **[2,0]** | "Jin123" **[2,1]**
| 3 | "Ssamu" **[3,0]** | "Ssamu123" **[3,1]**
| 4 | "Wonchae" **[4,0]** | "Wonchae123" **[4,1]**

___

#### ***Read Values***

    Console.WriteLine(identifier[row,col]);

___
###### ***Example***
```csharp
Console.WriteLine(users[0,1]);
```
___

#### ***Write Values***
    identifier[row,col] = value;
___
###### ***Example***
```csharp
users[0,0] = "Aeri";
```
___



### ***NESTED FOR Loop***
it is a **for loop** inside a **for loop**.

```csharp
for(int i = 0; i < 5; i++)
{
    Console.WriteLine("Loop " + i);

    for(int x = 0; x > 5; x++)
    {
        Console.WriteLine(x);
    }
    Console.WriteLine();
}
```
    Loop 0
    0
    1
    2
    3
    4

    Loop 1
    0
    1
    2
    3
    4

    Loop 2
    0
    1
    2
    3
    4

    Loop 3
    0
    1
    2
    3
    4

    Loop 4
    0
    1
    2
    3
    4

___

### ***Iterating 2D Arrays using Nested FOR Loops***
We can use Nested For Loops or For Each Loops to iterate through 2D Array.

```csharp
string[,] users =
{
    {"Kkuru", "Kkuru123"},
    {"Jiro", "Jiro123"},
    {"Jin", "Jin123"},
    {"Ssamu", "Ssamu123"},
    {"Wonchae", "Wonchae123"}
};

for(int row = 0; row < users.GetLength[0]; row++)
{
    for(int col = 0; col < users.GetLength[1]; col++)
    {
        Console.WriteLine(users[row,col]);
    }

    Console.WriteLine();
}
```
    Kkuru
    Kkuru123

    Jiro
    Jiro123

    Jin
    Jin123

    Ssamu
    Ssamu123

    Wonchae
    Wonchae123

___

### ***Iterating 2D Arrays using For-Each Loop***

```csharp
string[,] users =
{
    {"Kkuru", "Kkuru123"},
    {"Jiro", "Jiro123"},
    {"Jin", "Jin123"},
    {"Ssamu", "Ssamu123"},
    {"Wonchae", "Wonchae123"}
};

int i = 1;

foreach(string info in users)
{
    Console.WriteLine(info);
    if (i % 2 == 0)
    {
        Console.WriteLine();
        i++;
    }
}
```
    Kkuru
    Kkuru123

    Jiro
    Jiro123

    Jin
    Jin123

    Ssamu
    Ssamu123

    Wonchae
    Wonchae123

    # Methods in C#

### ***Methods / Functions***
They are used to divide and sort Functionalities within a class so that the code will be readable even if its long.


#### ***CREATING Methods***
    modifiers returntype methodName()
    {
        // Do anything here.
    }

###### ***Example***
```csharp
static void sayHello()
{
    Console.WriteLine("Hello!");
}
```

#### ***CALLING Methods***
    static void Main(string[] args)
    {
        methodName();
    }

###### ***Example***
```csharp
static void Main(string[] args)
{
    sayHello();
}

static void sayHello()
{
    Console.WriteLine("Hello!");
}
```

    Hello!

___

### ***Comments***
```csharp
// This is a single-line comment.

/* This is a multi-line comment
    You can comment here too! */
```

### ***VARIABLE Scoping***

#### ***Global Variables***
Are **variables declared within** a **class**, it can be accessed within a whole class.

#### ***Local Variables***
Are **variables declared inside** a **method, conditions, loops** and **any other block of code**, it can only be **accessible within** that **block of code**.

___
```csharp
class Program
{
    //GLOBAL Variables

    static string name = "Kkuru";
    static int age = 21;

    static void Main(string[] args)
    {
        introduce();
    }

    static void introduce()
    {
        // LOCAL Variables

        string name = "Ssamu";
        int age = 18;

        Console.WriteLine($"Hi, my name is {name}.");
        Console.WriteLine($"My age is {age}.");
    }
}
```

### ***Parameters / Arguments***
A **value** that needs to be **passed** on a **Method** so that the **method** can use the **value** and **perform various operations** on it.

You can hane as many Arguments / Parameters as you want. They act as a Local Variable inside a method / function.

    modifiers returntype methodName(parameters)
    {
        // Do Anything Here
    }

###### ***Example***

```csharp
static void Main(string[] args)
{
    say("Kkuru")
    say("Ssamu")
}

static void say(string word)
{
    Console.WriteLine(word);
}
```
    Kkuru
    Ssamu


### ***RETURN Keyword***
Used to **return** a **value** from the method. It is used when a method has a result.

Example:  
A method that performs Math Equations.  
A method that Concatenates Strings.

### ***RETURN Type***
The **type** of the **value** that will be **returned, return type** are the same as **datatypes**.

**void** returns **nothing**.  
**int** returns **integers**.  
**string** returns **strings**.  
and so on...

### ***Methods with RETURNS***
    modifiers returntype methodName(arguments)
    {
        // Do anything here
        return value;
    }

___

###### ***Example***
```csharp
static void Main(string[] args)
{
    int x = add(5, 19);
    Console.WriteLine(x)
}

static int add(int num1, int num2)
{
    int sum = num1 + num2;
    return sum
}
```
    24
___

### ***OVERLOADING Methods***
you can use the same method name but different parameters so that you can cater every possibility of a method.

```csharp
static void Main(string[] args)
{
    Console.WriteLine(add(5,19));
    Console.WriteLine(add(5,19,2));
    Console.WriteLine(add(1.25f, 9.15f));
}

static int add(int num1, int num2)
{
    int sum = num1 + num2;
    return sum
}

static int add(int num1, int num2, num3)
{
    int sum = num1 + num2 + num3;
    return sum
}

static float add(float num1, float num2)
{
    float sum = num1 + num2;
    return sum
}
```
    24
    26
    10.4

# Classes and Modifiers in C#

### ***Classes***
It is **created** by the programmer, it will act as a **blueprint** of an **object** that you want to **implement** in your **program**.

They **contain** all the **attributes** and **methods** that your desired **object** should have.

### ***CREATING Classes***
We can create classes inside our current file or create another file in the solution explorer.

```csharp 

class Arithmetic
{
    public int add(int num1, int num2)
    {
        return num1 + num2;
    }

    public int subtract(int num1, int num2)
    {
        return num1 - num2;
    }

    public int multiply(int num1, int num2)
    {
        return num1 * num2;
    }

    public int divide(int num1, int num2)
    {
        retun num1 / num2;
    }
}

```
___

### ***CLASS Instantiation***
The process of creating an **Instance** of a class so we can use it on our program. These can also be called **objects**.

    ClassName identifier = new ClassName();

###### ***Example***

```csharp

Arithmetic a = new Arithmetic();

a.add(5,2);

```
___

### ***ACCESS Modifiers***
Used to modify where classes, variables, and methods are accessible.

| Modifier | Description |
| ----------- | ----------- |
| default or **private** | It can only be accessed inside its own class. |
| **public** | The class can be accessed in all classes. |
| **internal** | The methods and variables can only be accessed in the same assembly not other assemblies. |
| **protected** | It can only be accessed in the same class or in a class that is inherited from that class |


### ***STATIC***
#### ***classes***
Are classes that cannot be instantiated and it shall only contain static methods and variables.

#### ***methods and variables***
Are methods and variables tat belongs to the class itself and not the instance.

```csharp

class Arithmetic
{
    public static int add(int num1, int num2)
    {
        return num1 + num2;
    }

    public static int subtract(int num1, int num2)
    {
        return num1 - num2;
    }

    public static int multiply(int num1, int num2)
    {
        return num1 * num2;
    }

    public static int divide(int num1, int num2)
    {
        retun num1 / num2;
    }
}

class Program
{
    static void Main(string[] args)
    {
        Arithmetic.add(5,2);
    }
}

```
___

### ***READONLY Keyword***
A keyword used so that a variable cannot be reassigned to a new value.

    public static readonly float PI = 3.14


# Classes and Objects in C#

## ***Object - Oriented Programming***
It focuses on implementing real world objects using **Classes** to create variation of **Objects**, that has attributes and purpose.

It helps us create much **flexible** and **efficient** code than **procedural programming**.

## ***Classes***
It is **created** by the programmer, it will act as a **blueprint** of an **object** that you want to **implement** in your **program**.

They **contain** all the **attributes** and **methods** that your desired **object** should have.

## ***Objects***
It is **created** by instantiating a **Class**.

It is anything that has an **attribute** and a **purpose.**

## ***Attributes***
These are the **global variables** declared inside the **class** of our **object**.

it is used to **create variations** of an **object** using only one class.

---

### ***CLASS Creation***
**Person**
- First Name
- Last Name
- Sex
- Age

```csharp
public Person class{
    // Attributes
    public string firstName;
    public string lastName;
    public char sex;
    public int age;

    // Methods or Purpose
}
```
---

### ***CLASS Instantiation***
The process of creating an **Object** using a **class** so we can use it on our program.

```csharp
Person p1 = new Person();
Person p2 = new Person();
Person p3 = new Person();
```
---

### ***ACCESSING Attributes***

#### ***WRITING Attributes***
    identifier.attribute = value;

#### ***READING Attributes***
    Console.WriteLine(identifier.attribute);

---
```csharp
p1.firstName = "Kkuru";
p1.lastName = "Lee";
p1.sex = 'M';
p1.age = 18;

p2.firstName = "Jiro";
p2.lastName = "Pasco";
p2.sex = 'M';
p2.age = 21;

p3.firstName = "Wonchae";
p3.lastName = "Aeri";
p3.sex = 'F';
p3.age = 25;


Console.WriteLine(p1.firstName + " " + p1.lastName);
Console.WriteLine(p2.firstName + " " + p2.lastName);
Console.WriteLine(p3.firstName + " " + p3.lastName);
```

# Constructors in C#

### ***Constructors***
Is a **method** called when you **instantiate a class / create an object**.

It is used to **initialized** the **attributes** of an **object** or **run** a **block of code** when an **object is created**.

### ***CREATING Constructors***
**Constructor method** are **named** after their **Class Name**.

    modifiers className class{
        modifiers className(){
            //Constructor
        }
    }

```csharp
class Product
{
    public Product()
    {
        Console.WriteLine("Product Created!")
    }
}
```
---

### ***THIS keyword***
The **this** keyword refers to the **class** itself.

The **this keyword** will **enables** you to **access global variables** inside the **class** if you have the **same variable names** in a **parameter**.

```csharp
class Product
{
    public string name;
    public float price;

    public Product(string name, float price)
    {
        this.name = name;
        this.price = price;
    }
}

class Program
{
    static void Main(string[] args)
    {
        Product p1 = new Product("Milk", 150);
        Product p2 = new Product("Coke", 75);
        Product p3 = new Product("Bread", 25);
    }
}
```

# Object Methods in C#

### ***OBJECT METHODS***
Are **methods** declared inside an **Object Class.**  
**Object Methods** are **considered** as the **Object's purpose.**

### ***CREATING Object Methods***
**Object Methods** are same as the **Methods** that tackled.

    modifiers className class{
        modifiers returntype methodName(arguments){
            // Do anything here;
        }
    }

```csharp
class Character
{
    public string name, dialog;
    public int hp, mp, lvl;

    public Character(string name, string dialog, int hp, int mp, int lvl)
    {
        this.name = name;
        this.dialog = dialog;
        this.hp = hp;
        this.mp = mp;
        this.lvl = lvl;
    }

    public void introduce()
    {
        Console.WriteLine("I am " + name);
    }

    public void sayDialog()
    {
        Console.WriteLine(name + " : " + dialog);
    }

    public void checkStats()
    {
        Console.WriteLine("Name  : " + name);
        Console.WriteLine();
        Console.WriteLine("Level : " + lvl);
        Console.WriteLine("HP    : " + hp);
        Console.WriteLine("MP    : " + mp);
    }
}
```

---

### ***CALLING Object Methods***
**Object Methods** are same as the **Methods** that tackled.

    ClassName cn = new ClassName(constructor);
    cn.methodName(arguments);

```csharp
class Program
{
    static void Main(string[] args)
    {
        Character c = new Character("Kkuru", "Hello World", 100, 50, 1);
        c.introduce;
        // I am Kkuru
        c.sayDialog;
        // Kkuru : Hello World
        c.checkStats;
        /* Name  : Kkuru
        
           Level : 1
           HP    : 100
           MP    : 50
         */
    }
}
```

# Encapsulation in C#

### ***Encapsulation***
An **OOP** technique used to **hide** data from direct access.

### ***Encapsulation Advantages***
1. It **hides direct access** to our **variables**, it also **hides** our **implementation** of how we **get** and **set** a certain value.
2. We can **decide** whether we want to **make** a **variable read - only** or **write - only**.

### ***USING Encapsulation***
**Declare Attributes** as **PRIVATE**.

    modifiers className class{

        //Private Attributes

    }

```csharp
class User
{
    //private fields
    private int userID;
    private string userName;
    private string firstName, lastName;
}
```

---

### ***Getter and Setters***
Used to **get** and **set** encapsulated variables.

    //field
    private int userID;

    //property
    public int UserID{
        get{
            return userID;
        }
        set{
            userID = value;
        }
    }

```csharp
class User
{
    //private fields
    private int userID;
    private string userName;
    private string firstName, lastName;

    //properties
    public int UserID
    {
        get {return userID;}
        set
        { 
            if (value >=1000) userID = value;
            else Console.WriteLine("Error, User ID must not be below 1000.");
        }
    }

    public string UserName
    {
        get{return userName;}
        set{
            userName = value;}
    }

    public string FirstName
    {
        get{return firstName;}
        set{firstName = value;}
    }

    public string LastName
    {
        get{return lastName;}
        set{lastName = value;}
    }

    public string FullName
    {
        get{return firstName + " " + lastName;}
    }
    
    public User(int userID, string userName, string firstName, string lastName)
    {
        UserID = userID;
        UserName = userName;
        Firstname = firstName;
        LastName = lastName;
    }
}
```
---

### ***USING Getter and Setter***

```csharp
class Program
{
    static void Main(string[] args)
    {
        User user = new User(202080094, "HelloWorld","Kkuru", "Lee");

        Console.WriteLine(user.FullName);
        // Kkuru Lee
    }
}
```

--- 

### ***Getter and Setter (shortcut)***

    // Automatic Property
    public int userID{
        get;
        set;
    }

```csharp
class User
{
    // Automatic Properties
    public int userID
    {
        get;
        set;
    }

    public string userName
    {
        get;
        set;
    }

    public string firstName
    {
        get;
        set;
    }

    public string lastName
    {
        get;
        set;
    }

    public User(int userID, string userName, string firstname, string lastname)
    {
        this.userID = userID;
        this.userName = userName;
        this.firstName = firstName;
        this.lastName = lastName;
    }
}

class Program
{
    static void Main(string[] args)
    {
        User user = new User(202080094, "HelloWorld", "Kkuru", "Lee");

        user.firstName = "Jiro";
    }
}
```

# Overloading Constructors in C#

### ***OVERLOADING Constructors***
An **OOP** technique used to **create** multiple constructors with different arguments. It is used to cope up with the needs of a certain instance of an object.

*Same as Method Overloading*

**Create Multiple Constructoes with Different Arguments**


    modifiers class className{
        // Declare Attributes Here
        className(arguments){

        }

        className(arguments){

        }
    }

```csharp
class Product
{
    public int productID
    {
        get;
        set;
    }

    public string productName
    {
        get;
        set;
    }

    public string productDescription
    {
        get;
        set;
    }

    public int productStock
    {
        get;
        set;
    }

    public int productPrice
    {
        get;
        set;
    }

    public Product(int productID, string productName, string productDescription, int productStock, int productPrice)
    {
        this.productID = productID;
        this.productName = productName;
        this.productDescription = productDescription;
        this.productStock = productStock;
        this.productPrice = productPrice;
    }

    public Product(int productID, string productName, int productStock, int productPrice)
    {
        this.productID = productID;
        this.productName = productName;
        this.productStock = productStock;
        this.productPrice = productPrice;
    }
}

class Program
{
    static void Main(string[] args)
    {
        Product p = new Product(1, "Milk", 5, 150);
        Product p1 = new Product(2, "Coffee", "to make you awake", 5, 100)
    }
}
```

# Inheritance in C#

### ***Inheritance***
An **OOP technique** used to **inherit attributes, properties,** and **methods** from one **class** to **another**.

### ***Base Class***
The class where we will inherit the attributes and methods.

### ***Derived Class***
The class who will inherit attributes annd methods from a base class.

### ***USING Inheritance***
**':' after Derived Class Name**

    modifiers class derivedClassName: baseClassName{
        // Attributes and Methods
    }

```csharp
class Program
{
    static void Main(string[] args)
    {
        Person p = new Person();
        p.name = "Kkuru";
        p.sex = "Male";
        p.age = 21;
        p.introduceSelf();

        Toddler t = new Toddler();
        t.name = "Wonchae";
        t.sex = "Female";
        t.age = 1;
        t.introduceSelf();
        t.cry();
    }
}

class Person
{
    public string name 
    {
        get;
        set;
    }

    public string sex
    {
        get;
        set;
    }

    public int age
    {
        get;
        set;
    }

    public void introduceSelf()
    {
        Console.WriteLine("Name : " + name);
        Console.WriteLine("Sex  : " + sex);
        Console.WriteLine("Age  : " + age);

    }
}

class Toddler : Person
{
    public void cry()
    {
        Console.WriteLine(name + " is crying.");
    }
}
```

### ***OVERRIDING Constructors***
**You are required to call the constructor of the superclass**

### ***BASE Keyword***
can only be used by **derived class** and it is **used** to **call** their **base class** so we can access their constructions, attributes, and methods.

```csharp
class Program
{
    Person p = new Person("Kkuru", "Male", 21);
    p.introduceSelf();

    Toddler t = new Toddler("Wonchae", "Female", 1, "Peek-a-Boo");
    t.faveGame();
    t.introduceSelf();
    t.cry();

    Child c = new Child("Ssamu", "Female", 5, "Valorant", "Sleeping");
    c.introduceSelf();
    c.cry();
    c.doHobby();
}

class Person
{
    public string name 
    {
        get;
        set;
    }

    public string sex
    {
        get;
        set;
    }

    public int age
    {
        get;
        set;
    }

    public Person(string name, string sex, int age)
    {
        this.name = name;
        this.sex = sex;
        this.age = age;
    }

    public void introduceSelf()
    {
        Console.WriteLine("Name : " + name);
        Console.WriteLine("Sex  : " + sex);
        Console.WriteLine("Age  : " + age);

    }
}

class Toddler : Person
{
    public string faveGame
    {
        get;
        set;
    }

    public Toddler(string name, string sex, int age, string faveGame) : base(name, sex, age)
    {
        this.faveGame = faveGame;
    }

    public void cry()
    {
        Console.WriteLine(name + " is crying.");
    }
}

class Child : Toddler
{
    public string hobby
    {
        get;
        set;
    }

    public Child(string name, string sex, int age, string faveGame, string hobby) : base(name, sex, age, faveGame)
    {
        this.hobby = hobby;
    }

    public void doHobby()
    {
        Console.WriteLine(name + " is " + hobby);
    }
}
```

### ***OVERRIDING Methods***
**To retain the Functionality from the Base Class use the Base Keyword to call the Method**

```csharp
class Program
{
    Person p = new Person("Kkuru", "Male", 21);
    Toddler t = new Toddler("Wonchae", "Female", 1, "Peek-a-Boo");
}

class Person
{
    public string name 
    {
        get;
        set;
    }

    public string sex
    {
        get;
        set;
    }

    public int age
    {
        get;
        set;
    }

    public Person(string name, string sex, int age)
    {
        this.name = name;
        this.sex = sex;
        this.age = age;
    }
}

class Toddler : Person
{
    public string faveGame
    {
        get;
        set;
    }

    public Toddler(string name, string sex, int age, string faveGame) : base(name, sex, age)
    {
        this.faveGame = faveGame;
    }
}
```

# Start Your Quotebook

## To Do:

>First I locate ng Files Directory

>1. Create the MyQuoteBook folder

    mkdir MyQuoteBook

>2. Create a file called “happiness.txt” and add a few quotes about happiness to it
    
    touch happiness.txt
    add
>3. Initialize your git repository and make your first commit
    
    git init
    git commit -m ""
>4. Add another file called “humor.txt” and add a few quotes to it
    
    touch humor.txt
    Add
>5. Make your second commit

    git init
    git commit -m""

>6. Make changes to both files and make a third commit

    Change something in the file
    git commit -m "Change Files"
>7. Revert your third commit

    git revert HEAD
    ctrl + c
    :q!
>8. Run “git revert -n HEAD” to see how you can “Revert the revert” and then make a commit

    git revert -n HEAD
>9.  Reset to the commit before you had reverted (Step 7)

    git reset --hard HEAD^
>10. Create a new branch in your “MyQuoteBook” project

    git branch Motivational
>11. On this new branch create a separate file for your motivational quotes, add a file motivation_quotes.txt

        git checkout motivational
        touch motivation_quotes.txt
>12. Add some content to the motivational quotes file and then make a commit

    touch motivation_quote.txt
    git commit -m""
>13. Checkout the master branch

    git checkout master
>14. Merge the branch you made in the previous assignment (for motivational quotes) into your master branch

git merge motivational
>15. Solve any merge conflicts that arise


>16. Check your git history

    git log
>17. Delete the motivational quotes branch (hint: you will add a modifier to the git branch command and then
specify the branch to delete)

git branch -d motivational-quotes
>18.  create a repository in Github, and push your project there.

    git remote add origin (link)
    git push -u -f origin master