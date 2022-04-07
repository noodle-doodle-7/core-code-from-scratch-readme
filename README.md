# core-code-from-scratch-readme

<details><summary> Week #1 </summary>
<p>

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

```
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
            
STEP 1 > First we get the year that we want to convert --> 1999
            
STEP 2 > Then we need the powers of 2 to find a big enought power that equal or the closest to "1999" but not bigger than "1999"

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
            
STEP 3 > We need to keep track that we used one (1) 2^10 = 1024 and we substract "1024" from "1999".
            
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
            
STEP 4 > After substracting all the powers of 2 until we get "0", fill up the spaces between the numbers that we did not used with a "0" and organize it.
            
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
> This code was created on the MIPS platform.
            
```
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
> This code was created on the MIPS platform.

```
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

</p>
</details>
