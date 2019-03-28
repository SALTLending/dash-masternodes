# Setting up a Dash Masternode against your SALT Collateral Wallet

In order to run a masternode using your collateral, DO NOT send it onto the platform in a standard transaction.
If you have already sent your collateral to your wallet, withdraw it and follow the below steps.
If you are unable to withdraw because you have an active loan, contact support with the information listed in section 2
and we will issue the ProRegTx for you.

## 1. Setup the Masternode Software
follow the instructions at https://docs.dash.org/en/stable/masternodes/setup.html
SKIP the sections `Send the collateral` and `Register your masternode` 

## 2. Collect ProRegTx Parameters
Find or generate, and write down the following parameters:
1. Your SALT Collateral Wallet address
  - You can find this by logging into the portal, going to your Dash wallet, and clicking "Deposit"
2. Your Masternode IP address and port
  - The IP is the public IP of the host running your masternode
  - The port is the number found after the `:` of the `dashd bind ip address` when you run `dashman status`
