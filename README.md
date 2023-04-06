# GitHub Experiment

1. [Learned commands](#learned-commands)
1. [Newly learned commands](#newly-learned-commands)

```mermaid
graph TD;
  A-->B;
  A-->C;
  B-->D;
  C-->D;
```


```mermaid
import base64
from IPython.display import Image, display
import matplotlib.pyplot as plt

def mm(graph):
  graphbytes = graph.encode("ascii")
  base64_bytes = base64.b64encode(graphbytes)
  base64_string = base64_bytes.decode("ascii")
  display(Image(url="https://mermaid.ink/img/" + base64_string))

mm("""
graph LR;
    A--> B & C & D;
    B--> A & E;
    C--> A & E;
    D--> A & E;
    E--> B & C & D;
""")
```
