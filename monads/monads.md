# Discovering Monads

## Introduction

Monads let us _compose computations_. 
It is useful to think of a monad as _a strategy for combining computations into more complex computations._

## Maybe

The `Maybe` type constructor allows us to deal with absence of values.

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
