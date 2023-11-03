# How to send FT using flow cli 

If you know your private key you can run transactions in the terminal manually. 

In this repo there are two files:
 - flow.json: the configuration of your account
 - sendFt.cdc: the transaction we will send

Either clone down this repo manually or copy paste the raw contents of those files into a directory on your computer

## Prerequisites

 - you need flow.cli installed https://developers.flow.com/tools/flow-cli/install
   - if on mac install homebrew first https://brew.sh/

 - you have to verify that the accounts block user in flow.json is correct. 
   - modify the address field to be your address
   - lookup your keys here https://www.flowdiver.io/account/0x9f085985e3012a1d?tab=keys, replacing the address with your address
   - ensure that the index/signing and hash are correct

 - make the environment know about your private key on the environment as USER_PK. 
   - example: `export USER_PK=abc`
   - never never ever share your PK with anybody

## sending flow

we will now use the flow cli`s send transactions command to manually send a transaction using your account

the command comes in the form of
flow transactions send \<fileName\> -n \<network\> --signer \<signerNameInFlowJson\> \<amountInDouble\> \<account\>
```
flow transactions send sendFlow.cdc -n mainnet --signer user 0.42 0x886f3aeaf848c535
```


