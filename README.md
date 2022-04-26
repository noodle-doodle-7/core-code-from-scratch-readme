<h1 align="center"> Core Code Software Development from scratch </h1>

<h2 align="center"> Week # 1 </h2>

<details><summary> Tuesday April 5th </summary>
<p>
            
### Compiled vs Interpreted programming languages

#### Compiled Languages

These are instructions that our processor can handle and understand, and have to be manually compiled. These are faster and efficent to handle and provide better control over hardware. 

> There are 3 elements used on compiled codes: source code, compiler & machine code (executable).
            
| Pros ✅ | Cons ❌ |
| ---- | ---- |
| Ready to run | Not cross-platform |
| Open faster | Not flexible |
| Source Code stays private/secured | Too much steps |

#### Interpreted Languages

These are processed on a line-by-line format, this makes them slower than compiled languages but they're some simpler to code. Also this types of languages can be changed on-the-go and display real-time changes as well.

> This code is not compiled, that means that everybody will need a interpreter to execute the code.

| Pros ✅ | Cons ❌ |
| ---- | ---- |
| Cross-platform | Interpreter required |
| Simpler to test | Ofter Slower |
| Easier to debug | Source Code is public |

<hr>

> *JavaScript is considered a hybrid, due to it has characteristics of both compiled and interpreted languages.*

<hr>

### Pseudocode for currency converter
            
> *Pseudocode* is defined as simple or plain description of the steps contained in an algorithm.

```javascript
### num1 = USD amount to covert
### num2 = updated BTC value
### Total = USD amount coverted to BTC

START
PRINT Hello, please enter the amount to USD to covert!
num1 <-- GET
PRINT Thank you, please wait a moment.
num2 <-- GET(https://valuta.exchange/es/usd-to-btc)
Total <-- num1 / num2
PRINT Your total in BTC is
PRINT Total
END
```

### Low-Level vs High-Level Programming Languages

> The level of a coding languages represents the amount of abstraction between *Programming Languages* and *Machine Languages.*

| Low-Level 📉 | High-Level 📈 |
| ---- | ---- |
| Little or no distortion of programming concepts | Rely on functions, objects or other abstractions |
| Close to hardware | Simpler to use |
| No complier or interpreter needed | Independent of architecture |
| Very efficient | Not as efficent due to line-by-line operation |
| Great for OS or firmware applications | Easier to develop |
| Difficult to use & takes longer to develop | Mainly used on Web applications |
            
</p>
</details>     
            
<details><summary> Wednesday April 6th </summary>
<p>   

### Date of birth in Matrix (binary code)
> This was calculated using the method of *the powers of 2*, demonstrated in [this](https://www.youtube.com/watch?v=rsxT4FfRBaM&ab_channel=TheOrganicChemistryTutor) video.
            
If my bithday year is 1999, we need to find how to translate it into binary code.
            
**STEP 1** > First we get the year that we want to convert --> 1999
            
**STEP 2** > Then we need the powers of 2 to find a big enought power that equal or the closest to "1999" but not bigger than "1999"

            2^1 = 2
            2^2 = 4
            2^3 = 8
            2^4 = 16
            2^5 = 32
            2^6 = 64
            2^7 = 128
            2^8 = 256
            2^9 = 512
            2^10 = 1024 <<
            2^11 = 2048
            2^12 = 4096
            
We stop at "1024" due to is less than "1999" (the number that we are converting) and "2048" is more than "1999" too. 
            
**STEP 3** > We need to keep track that we used one (1) 2^10 = 1024 and we substract "1024" from "1999".
            
            1999 - 1024 = 975
            
Then we repeat the previous step (STEP 2) making sure to keep track tha we used one "1024". Now we search for a number equal or lower than "975"
            
            2^1 = 2
            2^2 = 4
            2^3 = 8
            2^4 = 16
            2^5 = 32
            2^6 = 64
            2^7 = 128
            2^8 = 256
            2^9 = 512 <<
            2^10 = 1024 (1)
            2^11 = 2048
            
Notate that we used one "512" and substract it from "975"
            
            975 - 512 = 463
            
We apply STEP 2 and STEP 3 again.
            
            2^1 = 2
            2^2 = 4
            2^3 = 8
            2^4 = 16
            2^5 = 32
            2^6 = 64
            2^7 = 128
            2^8 = 256 <<
            2^9 = 512 (1)
            2^10 = 1024 (1)
            2^11 = 2048
            2^12 = 4096
            
            463 - 256 = 207
            
**STEP 4** > After substracting all the powers of 2 until we get "0", fill up the spaces between the numbers that we did not used with a "0" and organize it.
            
            2^0 = 1 (1)
            2^1 = 2 (1)
            2^2 = 4 (1)
            2^3 = 8 (1)
            2^4 = 16 (0)
            2^5 = 32 (0)
            2^6 = 64 (1)
            2^7 = 128 (1)
            2^8 = 256 (1)
            2^9 = 512 (1)
            2^10 = 1024 (1)
            2^11 = 2048
            2^12 = 4096
            
> You organize it from the biggest number that we used (1024) to the smallest number (1). You only notate the counters of the numbers that we used.
            
            That would look something like this: 
            
            1024 (1), 512 (1), 256 (1), 128 (1), 64 (1), 32 (0), 16 (0), 8 (1), 4 (1), 2 (1), 1 (1)
            
We remove the powers of 2 and the commas from the list & then you are left with this:
            
            11111001111

This collection of 1's and 0's is the equivalent to "1999" in binary code. Input this solution on [this](https://www.binaryhexconverter.com/binary-to-decimal-converter) calculator to check the result.
           
### Program that adds any two given numbers provided by the user
> This _assembly_ code was created on the MIPS platform.
            
```assembly
  .data
	      num1: .asciiz "\nIngrese el primer numero: "
	      num2: .asciiz "\nIngrese el segundo numero: "
	      resultado: .asciiz "\nEl resultado es: "
  .text
	      main:
	      li $v0, 4
	      la $a0, num1
	      syscall
	      
	      li $v0, 5
	      syscall
	      
	      move $t0, $v0
	      
	      li $v0, 4
	      la $a0, num2
	      syscall
	      
	      li $v0, 5
	      syscall
	      
	      move $t1, $v0
	      
	      add $t2, $t0, $t1
	     
	      li $v0, 4
	      la $a0, resultado
	      syscall
	      
	      li $v0, 1
              move $a0, $t2
              syscall
```

### Program that prints my name
> This _assembly_ code was created on the MIPS platform.

```assembly
.data
	      name: .asciiz "\n\n > Fernando Maldonado :D < \n\n "
  .text
	      main:
	      li $v0, 4
	      la $a0, name
	      syscall
```
            
</p>
</details>

<details><summary> Thrusday April 7th </summary>
<p>

### How to Print Special Numbers? 

```javascript

// Let's print just the even numbers from 0 to 100

for (var i = 0; i <= 100; i++) {
    if (i % 2 == 0) console.log (i);
}    

/*

var i = 0 indicates that we start with 0
i <= 100 indicates the limit of the count
i++ indicates increment (+1)
if (i % 2 == 0) validates of the number is even

*/

```

### Bad Code pt I

The code shown below is not working on the desired way, after checking some loggical operators, we can notice that the other developer wrote the wrong logical test operation in the first part of the code.

```javascript
var cond = false;

if ((cond = true)) {
  console.log('The cond variable is true');
} else {
  console.log('The cond variable is false');
}
```

Now that we recognize the error, we can correct it by simply changing one logical operator. We swapped the ```if ((cond = true))``` for ```if (cond == true)```.

```javascript
var cond = false;

if (cond == true) {
  console.log('The cond variable is true');
} else {
  console.log('The cond variable is false');
}
```
> You can the explanation about the _==_ logical operator on this [link](https://learn.onemonth.com/difference-between-equal-signs-javascript/#:~:text=In%20JavaScript%2C%20the%20%E2%80%9C%3D%3D%E2%80%9D,return%20either%20true%20or%20false.)

### Bad Code pt II

We need to correct the following code to be compliant with the following requirements:
- If the number is 100, display the message "This is a special number!"
- If the number is less than 1000 but a multiple of 10, display the message "This number is almost special."
- If none of the above are true display the message "Just a regular number"

```javascript
var n = 100;

if (n == 100) {
  console.log('This is a special number!');
}
if (n < 1000) {
  console.log('');
} else {
  console.log('Just a regular number');
}
if (n % 10 == 0) {
  console.log('This number is multiple of 10');
}
```
After tweaking and optimizing the previous code, we are left with this:		      

```javascript

var n = 100;
console.log ('The current assigned value is: ', n)

if (n == 100) {
console.log ('This is a special number!');
} else if (n < 1000 && n % 10 == 0) {
console.log ('This number is almost special.');
} else { 
console.log ('Just a regular number.')
}

```

</p>
</details>

<h2 align="center"> Week # 2 </h2>

<details><summary> Monday April 18th </summary>
<p>

</p>
</details>

<details><summary> Tuesday April 19th </summary>
<p>

### Multiply Exercise

Corrected code so it will run properly. This was the code provided:

```javascript

function multiply(a, b){
  a * b
}

```

> corrected code:

```javascript

function multiply(a, b){
  return a * b;
}

```

### ASCII Total

We were given a string, and have to return the sum of all characters as an int. The function should be able to handle all ASCII characters.

```javascript

function uniTotal(str) {
  let total = 0;
  for (let i = 0, length = str.length; i < length; i++) {
    total = total + str[i].charCodeAt();
  }
  return total;
}

```

> The ```String.prototype.charCodeAt()``` allows us to show the String in the UTF-16 code unit (ASCII).

### Char From ASCII Value

Write a function ```get_char()``` / ```getChar()``` which takes a number and returns the corresponding ASCII char for that value.

```javascript

function getChar(c){
    return String.fromCharCode (c);
  }

```

> The ```String.fromCharCode()``` allows to show the String (number) as the letter/number assigned in the UTC-16 code (ASCII).

### Binary Addition 

Function that adds two numbers together and returns their sum in binary. The conversion can be done before, or after the addition.

```javascript

function addBinary(a,b) {
    let addb = a + b;
    return addb.toString(2);
}

```

> With the object ```Object.prototype.toString()``` we can show a String (number) in a base 2 (binary) numbers.

### Student's Final Grade

_Coming soon..._

</p>
</details>

<details><summary> Wednesday April 20th </summary>
<p>

### Holiday VIII - Duty Free

The purpose of this kata is to work out just how many bottles of duty free whiskey you would have to buy such that the saving over the normal high street price would effectively cover the cost of your holiday.

You will be given the high street price _(normPrice)_, the duty free discount _(discount)_ and the cost of the holiday.

```javascript

function dutyFree(normPrice, discount, hol) {
    let calc = Math.floor( hol / ( (discount * normPrice) / 100 ) );
    return calc;
}

```

> I was able to shorten my code after a few tries.

```javascript

function dutyFree(normPrice, discount, hol) {
    return Math.floor( hol / ( (discount * normPrice) / 100 ) );
}

```

### Twice As Old

_Coming soon..._

### Valid Spacing

Your task is to write a function called _valid_spacing()_ or _validSpacing()_ which checks if a string has valid spacing. The function should return either true or false (or the corresponding value in each language).

```javascript

function validSpacing(s) {
  if(s.charAt(0) === ' ' || s.charAt(s.length - 1) === ' ') { 
     return false;
  }
  
  for(let i = 0; i < s.length; i++) {
    if(s.charAt(i) === ' '){ 
      if(i != 0 && s.charAt(i-1) === ' ') {
        return false;
      }
      if(i != (s.length - 1) && s.charAt(i+1) === ' ') {
        return false;
      }
    }
  
  }
  
  return true;
}

```

### Fake Binary

_Coming soon..._

</p>
</details>

<details><summary> Thursday April 20th </summary>
<p>

### Remove All Exclamation Marks From The End Of Sentence

_Coming soon..._
		      
### Vowel Remover

_Coming soon..._

### Rock Paper Scissors!

_Coming soon..._

### Persistent Bugger

_Coming soon..._

</p>
</details>

<details><summary> Friday April 21st </summary>
<p>

### Exam Code

_Not ready yet, please come back later..._

</p>
</details>

<h2 align="center"> Week # 3 </h2>

<details><summary> Monday April 25th </summary>
<p>

### Who likes it?

People can "like" blog posts, pictures or other items. We want to create the text that should be displayed next to such an item.

Implement the function which takes an array containing the names of people that like an item. It must return the display text as shown in the examples:

```
[]                                -->  "no one likes this"
["Peter"]                         -->  "Peter likes this"
["Jacob", "Alex"]                 -->  "Jacob and Alex like this"
["Max", "John", "Mark"]           -->  "Max, John and Mark like this"
["Alex", "Jacob", "Mark", "Max"]  -->  "Alex, Jacob and 2 others like this"
```

> Note: For 4 or more names, the number in "and 2 others" simply increases.

```javascript

function likes (names) {
    if (names.length === 0) return 'no one likes this';
    if (names.length === 1) return names[0] + ' likes this';
    if (names.length === 2) return names[0] + ' and ' + names[1] + ' like this';
    if (names.length === 3) return names[0] + ', ' + names[1] + ' and ' + names[2] + ' like this';
    return (
        names[0] + ', ' + names[1] + ' and ' + (names.length - 2) + ' others like this'
    );
}

```

</p>
</details>
