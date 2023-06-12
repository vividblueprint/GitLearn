```mermaid
graph LR

classDFA[DFA] -->|contains| states(State[])
classState[State] -->|has| name(string)
classState -->|has| transitions(dict)
classState -->|has| isFinal(boolean)

classDFA -->|has| startState(State)
classDFA -->|has| alphabet(set)

classDFA -->|creates| createState(name)
classDFA -->|sets| setStartState(state)
classDFA -->|sets| setFinalState(state)

createState -->|creates| state(State)
createState -->|adds| stateList(State[])
createState -->|returns| state

setStartState -->|sets| startState

setFinalState -->|marks| isFinal

regexToDFA -->|creates| dfa(DFA)
regexToDFA -->|creates| startState(State)
regexToDFA -->|sets| startState
regexToDFA -->|marks| startState as final

regexToDFA -->|loops| i(0 to len(regex))
i -->|gets| symbol(regex[i])

i -->|checks| symbol '('
i -->|creates| newState(State)
i -->|transitions| currentState to newState

i -->|checks| symbol '|'
i -->|creates| newState(State)
i -->|transitions| currentState to startState
i -->|transitions| startState to newState

i -->|checks| symbol ')'
i -->|transitions| currentState to startState

i -->|checks| symbol '*'
i -->|creates| newState(State)
i -->|loops| currentState.transitions to newState
i -->|loops| newState.transitions to currentState

i -->|else|
i -->|creates| newState(State)
i -->|transitions| currentState to newState
i -->|adds| symbol to alphabet

dfa -->|returns| dfa

printFancyDFA -->|prints| NFA States
printFancyDFA -->|prints| DFA States
printFancyDFA -->|prints| Start State
printFancyDFA -->|prints| Alphabet

printFancyDFA -->|loops| states(State[])
states -->|prints| stateString
stateString -->|checks| isFinal

regexToDFA -->|returns| dfa

regexToDFA -->|uses| printFancyDFA(dfa)

regexToDFA -->|returns| dfa

regex -->|input to| regexToDFA
dfa -->|returns| dfa

dfa -->|input to| printFancyDFA

printFancyDFA -->|prints| Regular Expression
printFancyDFA -->|prints| DFA States


```
