```mermaid
graph LR
A[Start] --> B[parse(input)]
B --> C{index == len(tokens)?}
C --> |Yes| D[print valid syntax]
C --> |No| E[raise ValueError]
D --> F[End]
E --> F[End]
B --> F[End]
B --> G[try]
G --> H[S()]
H --> I[E()]
I --> J[T()]
J --> K[TPrime()]
K --> L[F()]
L --> M[F()]
M --> N[F()]
N --> O[EPrime()]
O --> P[EPrime()]
P --> |+| Q[match('+')]
Q --> R[T()]
R --> S[TPrime()]
S --> T[F()]
T --> U[F()]
U --> V[F()]
V --> W[EPrime()]
W --> O
P --> |ε| O
J --> K
I --> J
H --> I
G --> C

```
