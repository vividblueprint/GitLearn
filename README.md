





'''mermaid
graph LR
  A((void main())) --> B[year, month, maxday]
  B --> C{month >= 1 && month <= 12}
  C -- Yes --> D{month == 2}
  D -- Yes --> E[year % 4 == 0]
  D -- No --> F[maxday = 28]
  E -- Yes --> G[year % 100 == 4]
  E -- No --> H[maxday = 28]
  G -- Yes --> I[maxday = 29]
  G -- No --> H
  C -- No --> J{month == 4 or month == 6 or month == 9 or month == 11}
  J -- Yes --> K[maxday = 30]
  J -- No --> L[maxday = 31]
  L --> M["cout << \"The MaxDay is: \" << maxday << endl;"]
'''

