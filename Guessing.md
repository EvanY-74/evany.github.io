``` mermaid
    graph TD;
    start([START])-->generate{{generate random number}}
    generate-->store[("`number`")]
    store-->input[[Ask user for a number 1-10]];
    input --> validation{is input valid and in the range?}
    validation-->|No|errormsg>Input is invalid]
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

## How the program works
1. The program generates a random number and stores it in `number`.
1. The user is prompted to enter a number.
1. If the input is not valid or not in range, then say it is invalid.
1. Otherwise continue
1. Check if the user got the number correct
1. If they did, then they win.
1. If they didn't, check if it is *higher or lower**
1. Tell the user if they are too high too low and reprompts the user.