### Payment Module

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

For more examples see [machineeconomy/iota-payment](https://github.com/machineeconomy/iota-payment/tree/master/examples).
