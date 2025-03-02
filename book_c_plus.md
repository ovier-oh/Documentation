# Chapter 1: 

# Chapter 2: Literals 

Traditionally, a literal is an expersion denoting a constant whoese type and value are evident from its spelling. For example, 42 is a literal, while x is not since one must see its declaration toknow its type and read previous lines of code to know its value. 

However, C++11 also added user-defined literals, which are not literals in the traditional sense but can be used as a shorthand for function calls. 

## Section 2.: this 

Within a memeber function of a class, the keyword `this` is a pointer to the instance of the class on which the function was calle. `this`cannot be used in static member function. 

```
struct S {
    int x;
    S& operator=(const S& other){
        x= other .x;
        // return a reference to the object begin assigned to 
        return *this;
    }
};

```

The type of `this`depends on the cv-qualification of the member function: if X::f is `const`, then the type of  `this`within f is const X*, so `this cannot be used to modify non-static data members from within a const member function. Likewise, this inerits volatile qualification from the function it apprars 