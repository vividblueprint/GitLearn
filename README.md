```mermaid
    graph LR;
    A([Rider/\nPassenger]):::green;
    B([Driver]):::orange;
    C([Navigation\nEngine]):::blue;
    D([Admin]):::red;
    E([Payment\nGateway]):::red;
    A --- 1([Register/Sign In])
    B ---- 1
    A --- 2([Manage Account])---2.1([Update/Change\nInfromation])
    B ---- 2
    A --- 3([Request Ride])---3.1([Select Type\nof Ride])
    B ---- 3
    C --- 3
    A --- 4([Cancel Ride])
    B ---- 4
    C --- 4
    A --- 5([Track Ride])
    B ---- 5
    C---5
    A --- 6([Make Payment])
    A --- 7([Send Messages/Make Calls])
    B ---- 7
    A --- 8([Rate Driver])
    A --- 9([View Travel History])
    9 ---- D
    B ---- 9
    A --- 10([Calculate Fare])---11([Make Payment])---12([Select Payment\nMethord])
    12 --- E
    A --- 13([Split Payment])---10
    B --- 14([Next Ride])
    A --- 15([Book for Others]) ---3.1
    C --- 15
    B ---- 16([Start Ride])
    16 --- C
    A --- 17([End Ride])
    B ---- 17
    17 --- C
    A --- 18([Log Out])
    B ---- 18
    B --- 19([Complete Ride])
    19 --- C
    20([Manage User])----D
    21([Manage Ride])----D
    %%A --> 16([ ])
    classDef blue fill:#2374f7,stroke:#000,stroke-width:2px,color:#fff;
    classDef orange fill:#fc822b,stroke:#000,stroke-width:2px,color:#fff;
    classDef green fill:#16b552,stroke:#000,stroke-width:2px,color:#fff;
    classDef red fill:#ed2633,stroke:#000,stroke-width:2px,color:#fff;
    classDef none fill:#none,stroke:#000,stroke-width:2px,color:#fff;
    subgraph USE[Use Case\nDiagram];
    1;2;2.1;3;3.1;4;5;6;7;8;9;10;11;12;13;14;15;16;17;18;19;20;21
    end

```

```mermaid
graph TD
  subgraph "Presentation Layer (UI)"
    A(Mobile App)
    B(Web Interface)
    C(Voice Assistant)
    D(Wearables)
  end
  subgraph "Application Layer (Logic)"
    E(Matching Algorithm)
    F(Pricing Algorithm)
    G(Payment Processing)
  end
  subgraph "Service Layer (Backend)"
    H(Geolocation Service)
    I(Notification Service)
    J(SMS Gateway)
  end
  subgraph "Data Layer (Storage)"
    K(User Profiles)
    L(Ride History)
    M(Payment Information)
    N(Driver Qualifications)
  end
  subgraph "Infrastructure Layer (Hardware)"
    O(Servers)
    P(Databases)
    Q(Network Components)
    R(Cloud Services)
  end
  subgraph "Analytics Layer (Data Analysis)"
    S(Service Performance Monitoring)
    T(Rider & Driver Behavior Analysis)
  end
  subgraph "Security Layer (Protection)"
    U(Authentication & Access Control)
    V(Data Encryption)
    W(Monitoring)
  end
  subgraph "Integration Layer (Third-party)"
    X(Payment Processor)
    Y(Mapping Service)
    Z(Social Media Platform)
  end
  A -->|Requests rides| E
  E -->|Connects drivers with riders| H
  H -->|Tracks location of drivers and passengers| K
  K -->|Stores user profiles| U
  B -->|Requests rides| F
  F -->|Determines ride costs| I
  I -->|Alerts drivers and riders| W
  L -->|Stores ride history| T
  C -->|Requests rides| G
  G -->|Handles payments| J
  M -->|Stores payment information| V
  D -->|Requests rides| S
  Q -->|Provides infrastructure support| O
  P -->|Manages data storage| M
  R -->|Provides cloud services| S
  V -->|Provides data encryption| W
  U -->|Provides authentication| W
  J -->|Processes payments| X
  Y -->|Provides mapping services| H
  Z -->|Provides social media integration| T

```

```mermaid
graph TD
  A["Presentation Layer (UI)"] -->|Mobile App| B["Application Layer (Logic)"]
  A -->|Web Interface| B
  A -->|Voice Assistant| B
  A -->|Wearables| B
  B -->|Matching Algorithm| C["Service Layer (Backend)"]
  B -->|Pricing Algorithm| C
  B -->|Payment Processing| C
  C -->|Geolocation Service| D["Data Layer (Storage)"]
  C -->|Notification Service| D
  C -->|SMS Gateway| D
  D -->|User Profiles| E["Infrastructure Layer (Hardware)"]
  D -->|Ride History| E
  D -->|Payment Information| E
  D -->|Driver Qualifications| E
  E -->|Servers| F["Analytics Layer (Data Analysis)"]
  E -->|Databases| F
  E -->|Network Components| F
  E -->|Cloud Services| F
  F -->|Service Performance Monitoring| G["Security Layer (Protection)"]
  F -->|Rider & Driver Behavior Analysis| G
  G -->|Authentication & Access Control| H["Integration Layer (Third-party)"]
  G -->|Data Encryption| H
  G -->|Monitoring| H
  H -->|Payment Processor| I(( ))
  H -->|Mapping Service| I(( ))
  H -->|Social Media Platform| I(( ))
```

```mermaid
    graph LR
    shamim
```

```mermaid
graph TD
    subgraph "Presentation Layer (UI)"
    A[Mobile App]
    B[Web Interface]
    C[Voice Assistant]
    D[Wearables]
    end

    subgraph "Application Layer (Logic)"
    E[Matching Algorithm]
    F[Pricing Algorithm]
    G[Payment Processing]
    end

    subgraph "Service Layer (Backend)"
    H[Geolocation Service]
    I[Notification Service]
    J[SMS Gateway]
    end

    subgraph "Data Layer (Storage)"
    K[User Profiles]
    L[Ride History]
    M[Payment Information]
    N[Driver Qualifications]
    end

    subgraph "Infrastructure Layer (Hardware)"
    O[Servers]
    P[Databases]
    Q[Network Components]
    R[Cloud Services]
    end

    subgraph "Analytics Layer (Data Analysis)"
    S[Service Performance Monitoring]
    T[Rider & Driver Behavior Analysis]
    end

    subgraph "Security Layer (Protection)"
    U[Authentication & Access Control]
    V[Data Encryption]
    W[Monitoring]
    end

    subgraph "Integration Layer (Third-party)"
    X[Payment Processor]
    Y[Mapping Service]
    Z[Social Media Platform]
    end

    A -->|Interacts with| E
    B -->|Interacts with| E
    C -->|Interacts with| E
    D -->|Interacts with| E
    E -->|Uses| F
    E -->|Uses| G
    F -->|Uses| H
    F -->|Uses| I
    G -->|Uses| J
    H -->|Uses| K
    H -->|Uses| L
    I -->|Uses| M
    K -->|Related To| N
    O -->|Supports| P
    O -->|Supports| Q
    O -->|Supports| R
    P -->|Uses| K
    P -->|Uses| L
    P -->|Uses| M
    P -->|Uses| N
    K -->|Uses| S
    L -->|Uses| S
    N -->|Uses| S
    S -->|Generates Data For| T
    T -->|Provides Insights For| E
    U -->|Protects| M
    V -->|Protects| M
    W -->|Monitors| M
    X -->|Integrates With| G
    Y -->|Integrates With| H
    Z -->|Integrates With| B

```


```mermaid
graph LR
A[Customer and Driver Details Management (CRM)]
B[Booking Management]
C[Vehicle Detail Management (if self-owned)]
D[Location and Fares Management]
E[Call System Management]
F[Communication]
G[Ratings and Reviews]
H[Promotions and Discounts]
I[Payroll Management]
J[Content Management]
K[Customer Support and Help]

A -->|Manage| B
A -->|Manage| C
D -->|Manage| B
E -->|Manage| B
F -->|Communicate with<br>users
G -->|Manage| B
H -->|Create and Manage<br>Promotional offers
I -->|Manage| C
J -->|Manage content<br>on website or app
K -->|Provide Customer<br>support and help

```
