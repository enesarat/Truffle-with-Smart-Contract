Developer: Enes Arat

First of all, if you are going to work in a new directory:
Run the "npm install truffle -g" command in that directory.
  Then you can use the "truffle init" command to create the necessary files in the directory.
  If the "contracts","migrations" and "test" folders are empty except for git files:
Run the "truffle unbox" command and answer "y" to the questions on the console.

  You can define the solidity version in the smart contracts you will write through the "truffle-config.js" file.
  Example usage:

    compilers: {
        solc: {
          version: "^0.8.7",

Contract Compile:
After writing a smart contract to the "contracts" folder for testing purposes, run the "truffle compile" command on the console.
As a result of this process, you will see that the "build" folder is created.

Contract Deploy:
  Before deploying the contract, create a migration file in the "migrations" folder and make the necessary definition for your contract.
  Then run the "truffle migrate" command in the console.
  Run the "truffle develop" command in the console to open the chain to be used in the development environment. This command runs a local ethereum.
  Then run the "truffle migrate" command in the console. So we connect to local insctance.
  Now you can create an instance from the contract you deployed for testing and call a method it has.
  Example usage:

    truffle(develop)> let instance = await HelloWorld.deployed()
    output:undefined
    truffle(develop)> instance.hello()
    output:'Hello Ethereum World!'