# Discovering Monads

## Introduction

Monads let us _compose computations_.

But that is just the practical aspect.

On a slightly deeper level, it is useful to think of a monad as _a strategy_ for _combining computations_ into more complex computations._



## Maybe

The `Maybe` type constructor allows us to deal with absence of values.

E.g., let us consider the problem of modelling genetically engineered sheep. 

``` haskell
data Sheep = Sheep {...}

-- our functions dealing with Sheep...
```

Each such sheep may or may not have a father/mother (being a clone).
Hence, the question "Who is the mother/father of Sheep xyz" may have the answer "None".

How do we model this in Haskell?

In the ideal scenario, a Sheep would *always* have both its parents (i.e., father & mother)

Hence, the type signature of the father/mother functions would be as follows:

``` haskell
data Sheep = Sheep {...}

father :: Sheep -> Sheep

mother :: Sheep -> Sheep

```

Clearly, the "father" or "mother" of a given sheep is a one-to-one mapping (& hence, a perfect example of a function).

But what happens in case of our Genetically Engineered Sheep?
We have to factor in the possibility of a sheep *not* having one of the parents.

This can be done via the `Maybe` type constructor to construct a new type called `Maybe Sheep`

The format of `Maybe` is as follows:

``` haskell
data Maybe a = Just a 
	         | Nothing
```

where, `Just` & `Nothing` are the data/value constructors.

``` haskell
data Sheep = Sheep {...}

father :: Sheep -> Maybe Sheep
mother :: Sheep -> Maybe Sheep

maternalGrandFather :: Sheep -> Maybe Sheep

paternalGrandMother :: Sheep -> Maybe Sheep

```

## List 

A list represents possibilities.

``` haskell

```
