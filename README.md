```mermaid
graph TD
  a--> Actor
  a--> System1
  Actor -- Action 1 --> 1
  Actor -- Action 2 --> 2
  Actor -- Action 3 --> 3
 1 -- Action 4 --> System
 2 -- Action 5 --> System
 3 -- Action 6 --> System
  Actor -- Action 1 --> 11
  Actor -- Action 2 --> 21
  Actor -- Action 3 --> 31
 11 -- Action 4 --> System1
 21 -- Action 5 --> System1
 31 -- Action 6 --> System1
  Actor -- Action 1 --> 12
  Actor -- Action 2 --> 22
  Actor -- Action 3 --> 32
 12 -- Action 4 --> System
 22 -- Action 5 --> System
 32 -- Action 6 --> System
 System -- Action 4 --> shamim
 System -- Action 5 --> shamim
 System -- Action 6 --> shamim
 System1 -- Action 4 --> shamim
 System1 -- Action 5 --> shamim
 System1 -- Action 6 --> shamim
```
