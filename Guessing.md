``` mermaid
    graph TD;
    start([START])-->generate{{generate random number}}
    generate-->store[("`number`")]
    store-->input[[Ask user for a number 1-10]];
    input --> validation{is input in the range ?}
    validation-->|No|errormsg>Input not in range]
    errormsg-->input
    validation-->|Yes|equal{"⠀
    is <code style='padding: 4px; border-radius: 8px; background-color: #444444'>number == input</code> ?
    ⠀"}
    equal-->|Yes|successmsg>You win!]
    successmsg-->End([END])
    equal-->|No|highorlow{"⠀
    is <code style='padding: 4px; border-radius: 8px; background-color: #444444'>number > input</code> ?
    ⠀"}
    highorlow-->higher>higher!]
    highorlow-->lower>lower!]
    higher-->input
    lower-->input
```



[inline code source](https://stackoverflow.com/questions/77011134/mermaid-how-to-use-inline-code-syntax-highlighting)