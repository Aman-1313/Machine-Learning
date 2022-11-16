# Artificial Intelligence Concepts And Theory
## 1. Background and Pre-requisites.
Learning has remained a challenging area for AI. The importance of learning, however, is beyond question, particularly as this ability is one of the most important components of intelligent behavior of machines.
To begin with, you would need some basic knowledge of predicate and propositional calculas, including rules of inferences, unification, etc.
Here is a good resource from University of Ottawa to brush up on your [basic calculas](https://www.site.uottawa.ca/~lucia/courses/2101-10/lecturenotes/04InferenceRulesProofMethods.pdf) requirement.

## 2. AI Programming language.
Once you are confident in your calculas requirement, Let's look at some Artificial Intelligence programming languages. Two most commonly used programming languages in machine learning are Prolog and Lisp.
We would focus on programming in Prolog for the sake of this course.
| English   | Prolog    |   
| :-----------: | :-----------: |    
| If    | 	:-  |       
| Not   | Not   |   
| Or    |  ;    |   
| and   |	,   |     
### Syntax Rules in Prolog:
1. Variable names start with UpperCase Alphabets.
2. Predicates(or functions in general) start with lowercase.
i.e father(X, Y) represents X is father of Y. Numbers of parameters of a prolog predicate represents the **arity**.
3. Prolog language basically has three different elements −
**Facts** − The fact is predicate that is true, for example, if we say, “Tom is the son of Jack”, then this is a fact.
**Rules** − Rules are extinctions of facts that contain conditional clauses. To satisfy a rule these conditions should be met.
Example
`
grandfather(X, Y) :- father(X, Z), parent(Z, Y)
`
Here X is grandfather of Y if there exist Z, s.t X is father of Z and Z is parent of Y.

### Running our first program in prolog: 
To keep stuff neat we seperate our prolog program specifications in a seperate file with .pl extension and refer to it whenever needed.
let's first create a file called db.pl, which contains the following code:
```Prolog
fact(0,1).
fact(X, Y):-
    X>0,
    Z is X-1,
    fact(Z,A),
    Y is X*A.
```
The given prolog program calculates factorial of a given integer. To run this program open terminal type 'gprolog' to open prolog env. 
Example output: 
```
?- fact(3, Y).
Y is 6
```
Explanation: the first predicate of our prolog program, checks if X = 0, and returns 1 if true. The second predicate takes (X,Y) parameters, checks if X>0, initiate a new var Z = X-1, makes a recursive call with new parameters (Z,A), where A woud be the returned value from recursive call.
Thus it goes like this, 3*(2*(1*(1))) where innermost (1) is returned by first predicate.

To learn more concepts about prolog i.e algorithms and data structures in prolog here is a good resource for you to [learn prolog](https://wps.pearsoned.com/wps/media/objects/5771/5909832/PDF/Luger_0136070477_1.pdf). 

