# The intelligent agent

Agent perceives through sensors and acts through effectors

1. Agent should be rational
    - Does the right thing by always maximising performance
    - rationality will then depend on data train set, knowledge on environment etc

2. Agent can learn if autonomous
    - does not only use built-in knowledge on environment
    - agent can adapt to changes in environment
    - note that an autonomous agent may not imply rational as it depends on the code logic

## Types of agent

1. Simple reflex agents
    - rule based logic, and acts when condition is met
    - only acts based on current perception
    - agent can only succeed if env is fully observable

2. Reflex agent with state
    - agent stores state which it uses as a variable in deciding its action
    - agent still operates on rule, but now with memory
    - agent can handle partially observable env

3. Goal based agent
    - concept of reflex agent with state with additional variable of goal
    - agent  evaluates the actions needed to reach goal state and chooses steps that reduces distance

4. Utility based agent
    - idea of goal based agent with optimisation
    - searches best solution to solve problem
