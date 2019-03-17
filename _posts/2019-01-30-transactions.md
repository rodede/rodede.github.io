---
layout: post
title: transaction definitions
description: transaction vocabulary and definitions
categories: programming
---
**A**tomicity  
**C**onsistency  
**I**solation  
**D**urability  

### Dirty reads
> One client reads another client’s writes before they have been committed. The read committed isolation level and stronger levels prevent dirty reads.

### Dirty writes
> One client overwrites data that another client has written, but not yet committed. Almost all transaction implementations prevent dirty writes.

### Read skew (nonrepeatable reads)
> A client sees different parts of the database at different points in time.

### Write skew
> A transaction reads something, makes a decision based on the value it saw, and writes the decision to the database. However, by the time the write is made, the premise of the decision is no longer true. 

### Phantom reads
> A transaction reads objects that match some search condition. Another client makes a write that affects the results of that search. 

