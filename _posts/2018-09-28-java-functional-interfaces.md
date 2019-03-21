---
layout: post
title: Java functional interfaces
description: Java functional interfaces
categories: java
---
# Functional interfaces

|  Type      |  Descriptor    |
|-----------------|-----------|
|Predicate<T>     |T->boolean |
|Consumer<T>      |T->void    |
|Function<T,R>    |T->R       |
|Supplier<T>      |()->T      |
|UnaryOperator<T> |T->T       |
|BinaryOperator<T>|(T,T)->T   |
|BiPredicate<L,R> |(L,R)->boolean|
|BiConsumer<T,U>  |(T,U)->void|
|BiFunction<T,U,R>|(T,U)->R   |

