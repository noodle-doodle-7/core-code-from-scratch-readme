# core-code-from-scratch-readme

## Compiled vs Interpreted programming languages

### Compiled Languages

These are instructions that our processor can handle and understand, and have to be manually compiled. These are faster and efficent to handle and provide better control over hardware. 

> there are 3 parts for these code: source code, compiler & machine code (executable).
            
| Pros ✅ | Cons ❌ |
| ---- | ---- |
| Ready to run | Not cross-platform |
| Open faster | Not flexible |
| Source Code stays private/secured | Too much steps |

### Interpreted Languages

These are processed on a line-by-line format, this makes them slower than compiled languages but they're some simpler to code. Also this types of languages can be changed on-the-go and display real-time changes as well.

> this code is not compiled, that means that everybody will need a interpreter to execute the code.

| Pros ✅ | Cons ❌ |
| ---- | ---- |
| Cross-platform | Interpreter required |
| Simpler to test | Ofter Slower |
| Easier to debug | Source Code is public |

<hr>

> *JavaScript is considered a hybrid, due to it has characteristics of both compiled and interpreted languages.*

<hr>

## Pseudocode for currency converter

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

## Low-Level vs High-Level Programming Languages

> The level of a coding languages represents the amount of abstraction between *Programming Languages* and *Machine Languages*

| Low-Level | High-Level |
| ---- | ---- |
| Little or no distortion of programming concepts | Rely on functions, objects or other abstractions |
| Close to hardware | Simpler to use |
| No complier or interpreter needed | Independent of architecture |
| Very efficient | Not as efficent due to line-by-line operation |
| Great for OS or firmware applications | Easier to develop |
| Difficult to use & takes longer to develop | Mainly used on Web applications |

