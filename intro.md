Presenters: Joe Nelson @begriffs
Brain Lonsdorf @drboolean

1> Silence: Recognizing seperate things.
writing pure code.

2> The Voyage
The code is transported to new vessels where it is executed.

3> Demo
Practice the patterns

In the Beginning
1> Anything goes
2> Everything changes
3> Weird names
Principle:
Discipline Wins
  Exercising restraint while coding feels weird at first, but it's worth it.
The Symptoms
1> custom names
2> Looping patterns
3> Glue code
4> Side effects
1:> Seperate inputs from environment
remove the secret inputs or assumptions and pass it as paramters.
make your arguments explicit.The code is more likly to run in other places.
Principle of seperation:
Seperating Mutation from Calculation
Anti Pattern:
function teaser(size, elt)
{
  setText(elt, slice(0, size, text(elt)));
  }

map(teaser(50),all('p'));

Modified:
var teeaser = slice(0);
map(compose(setText.teaser(50), text),all('p'));

Recognize pure functions
Functions that don't change anything are called "pure"l
Advantages of pure functions:
1> Testable

2> Portable
3> memorizable Ex -> 0xack13/memoizable
in other contexts: Memoization is an optimization that saves the return value of
a method so it doesn't need to be re-computed every time that method is called.
4> parallelizable
Pure Vs Impure
Example:
function chattyAdd(a, b, console){
 var c = a+b;
 console.log(a, '+',b, '=',c);
 return c;
  }
  // function is modifying the object called console.
  // composing pure fuctions is still pure
