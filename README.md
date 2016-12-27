# ServerProcess

Generic server process

The purpose of this server is to abstract the server common functions.

The KeyValueStore will emulate a Map structure to easily follow the
way that the server process works.

## Installation

- Clone the repo
- cd repo
- mix deps.get
- iex -S mix


## Use
    #Calling directly the server process
    pid = ServerProcess.start(KeyValueStore)
    ServerProcess.call(pid, {:put, :my_key, "Value of my key"})
    ServerProcess.call(pid, {:get, :my_key})
    
    #Calling the KeyValuStore funcitons
    pid = KeyValueStore.start
    KeyValueStore.put(pid, {:put, :my_key, "Value of my key"})
    KeyValueStore.get(pid, {:get, :my_key})
