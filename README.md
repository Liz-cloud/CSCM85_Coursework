# CSCM85_Coursework

## Modelling and Verification Coursework

### Question1

An LTS(S,α)over an alphabet A is called trace-deterministic if for all states s,s1,s2 ∈ S and every label a∈A, if s a→s1 and s a→ s2, then s1 =T s2. Let(S,α)and(T,β) be trace-deterministic LTSs. Prove: For all states s∈S and t∈T, if s=Tt, then s∼t. Your proof should be a copy of the proof of part(b)of the Theorem on Page 8 of the lecture notes verification-lts.pdf where exactly one sentence is altered appropriately.

### Question2 

Consider the following statements about trace equivalence(=T) and bisimilarity(∼) of processes(where a is a visible event, different from the termination event,that is, a ∈{τ, }): (1)(a→P) (a→Q)=T a→(P Q) (2)(a→P) (a→Q) ∼ a→(P Q). Which of these statements are true for arbitrary processes PandQ? In each case either prove trace equivalence respectively bisimilarity or give a concrete counter-example.

### Question3 

Consider the following definition of a robot that can repeatedly report its positions, move to the left or right(within a given finite range), or do some work.

`min=0 max=5 `

`Range={min..max}`

`datatypeDirection=L|R `

`channelmove: Direction `

`channel position: Range `

`channel work` 

`inc(x)=if x<max then x+1 else x `

`dec(x)= if x>min then x-1 else x `

`Robot(x)=position.x->Robot(x)[]`

`  move.L->Robot(dec(x))[] `

`  move.R->Robot(inc(x))[]`

`  work->Robot(x) `
  
Suppose doing work empties the robot’s battery so that it needs at least two movements to recharge the battery. We assume that, initially, the robot starts at position 0 and its battery is empty. Define a process Battery(n), with an integer parameter n and a suitable synchronisation set X such that the process Robot(0) [|X|] Battery(0) models this behaviour
