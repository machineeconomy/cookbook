## Welcome to the Machine Economy Cookbook

Here you get information, tutorials and code snippets about the machine economy based on the iota technology.  

### IOTA payment Module

The IOTA payment module brings an IOTA Wallet to your device. 
This module can easily extend your nodejs or express app or ran as a standalone server and brings an IOTA payment API. 

#### Level 
Low

#### Skills

  \++ Javascript: nodejs

  \+ Docker (optional)

#### Example 
```markdown
var paymentModule = require('iota-payment')
var app = require('express')()

let server = paymentModule.createServer(app)

// Start server with iota-payment module on '/payments'
server.listen(3000, function () {
    console.log(`Server started on http://localhost:3000 `)
})

```

For more details see [machineeconomy/iota-payment](https://github.com/machineeconomy/iota-payment).

### Build your Machine Economy

#### Level 
Advanced

#### Skills

  \+++ Javascript: nodejs

  \++ Hardware: Raspberry pi

  \+ Docker (optional)

This is a tutorial for building your own machine economy with custom machines, energy providers and governments.

Our machine economy has three participants. A robot, a wind energy provider and an energy government. 

#### The use case
You can pay a robot for a service.
The robot will pay the energy for itself to the wind energy provider.
The government takes some taxes from the wind energy provider. 

[Robot](https://github.com/machineeconomy/akita-robot).
[Wind Provider](https://github.com/machineeconomy/akita-energy).
[Energy Government](https://github.com/machineeconomy/akita-government).

### Support or Contact

Having trouble with this? Check out our [Discord](https://discord.gg/DXg6SHP). 
