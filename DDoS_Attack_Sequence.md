``` mermaid
    sequenceDiagram
    participant Attacker
    create participant BotNet
    Attacker->>BotNet: Acquires botnet (often by<br/> hacking into other computers)
    box rgba(5, 5, 5, 0.25) Legitimate systems
    participant Firewall
    participant WebServer as Web Server
    participant User as Legitimate User
    end
    User->> WebServer: User sends request<br/>to web server
    WebServer-->> User: Server responds<br/>with website
    Note right of Attacker: Attack starts
    Attacker->>BotNet: Tells BotNet to attack a particular service
    BotNet->>WebServer: Floods server with bogus requests
    BotNet->>WebServer: 
    BotNet->>WebServer: 
    BotNet->>WebServer: 
    BotNet-xFirewall: Some or all requests<br/>by Firewall
    BotNet-xFirewall: 
    WebServer-->>BotNet: Server tries to respond to all the requests
    WebServer-->>BotNet: 
    WebServer-->>BotNet: 
    User-xWebServer: User tries to send<br/>a request
    WebServer--x WebServer: Server is overloaded<br/>and cannot respond
```

## Documentation
* A hacker can hack into any device that has connection to the internet, even IoT devices like security cameras.
* Under normal circumstances, the web server communicates with legitimate users with requests and responses.
* The botnet, floods the web server with requests and doesn't wait for responses as the attack is just trying to force the server to respond to as much bogus requests as possible.
* The amount the firewall can stop is dependent on the the complexity of the firewall and how sophisticated the attack is.
* Assuming the attack is sucessful, the Web Server cannot cannot respond to legitimate users because it is too busy responding to the bogus requests.