ReadMe:       KiruthigaSekar 
Contract Directory Name: ..\CappedToken\contracts
Migrations DirectoryName: ..\CappedToken\migrations
Clarification:  As this is a large Reademe file, be patient to scroll down as it includes all the steps and the detailed solution :) Thanks
Installation:

Node js v8.9.0 
https://nodejs.org/en/download/releases/

Truffle:
npm install -g truffle@4.1.15

Truffle Initialization:
truffle init

NPM Initialization:
npm init

Open-Zeppelin :
npm install openzeppelin-solidity@1.11.0 --save-dev

Server (Ganache):
npm install -g ganache-cli

Server Initialization:
ganache-cli

GitHub Repository Link:

https://github.com/KiruthigaSekar/SolidityContract

***************************************************************Steps************************************************************************
Testing the Program:


C:\Users\RajGanesh\Desktop\CappedToken>truffle compile --all
Compiling .\contracts\ExampleToken.sol...
Compiling .\contracts\ExampleTokenCrowdsale.sol...
Compiling .\contracts\Migrations.sol...
Compiling openzeppelin-solidity/contracts/crowdsale/Crowdsale.sol...
Compiling openzeppelin-solidity/contracts/crowdsale/emission/MintedCrowdsale.sol...
Compiling openzeppelin-solidity/contracts/crowdsale/validation/CappedCrowdsale.sol...
Compiling openzeppelin-solidity/contracts/token/ERC20/DetailedERC20.sol...
Compiling openzeppelin-solidity/contracts/token/ERC20/MintableToken.sol...
Compiling openzeppelin-solidity/contracts/token/ERC20/StandardToken.sol...
Compiling openzeppelin-solidity\contracts\crowdsale\Crowdsale.sol...
Compiling openzeppelin-solidity\contracts\math\SafeMath.sol...
Compiling openzeppelin-solidity\contracts\ownership\Ownable.sol...
Compiling openzeppelin-solidity\contracts\token\ERC20\BasicToken.sol...
Compiling openzeppelin-solidity\contracts\token\ERC20\ERC20.sol...
Compiling openzeppelin-solidity\contracts\token\ERC20\ERC20Basic.sol...
Compiling openzeppelin-solidity\contracts\token\ERC20\MintableToken.sol...
Compiling openzeppelin-solidity\contracts\token\ERC20\SafeERC20.sol...
Compiling openzeppelin-solidity\contracts\token\ERC20\StandardToken.sol...

Compilation warnings encountered:

openzeppelin-solidity/contracts/crowdsale/Crowdsale.sol:133:5: Warning: Unused function parameter. Remove or comment out the variable name to silence this warning.
    address _beneficiary,
    ^------------------^
,openzeppelin-solidity/contracts/crowdsale/Crowdsale.sol:134:5: Warning: Unused function parameter. Remove or comment out the variable name to silence this warning.
    uint256 _weiAmount
    ^----------------^
,openzeppelin-solidity/contracts/crowdsale/Crowdsale.sol:175:5: Warning: Unused function parameter. Remove or comment out the variable name to silence this warning.
    address _beneficiary,
    ^------------------^
,openzeppelin-solidity/contracts/crowdsale/Crowdsale.sol:176:5: Warning: Unused function parameter. Remove or comment out the variable name to silence this warning.
    uint256 _weiAmount
    ^----------------^
,openzeppelin-solidity/contracts/crowdsale/Crowdsale.sol:117:3: Warning: Function state mutability can be restricted to pure
  function _preValidatePurchase(
  ^ (Relevant source part starts here and spans across multiple lines).
,openzeppelin-solidity/contracts/crowdsale/Crowdsale.sol:132:3: Warning: Function state mutability can be restricted to pure
  function _postValidatePurchase(
  ^ (Relevant source part starts here and spans across multiple lines).
,openzeppelin-solidity/contracts/crowdsale/Crowdsale.sol:174:3: Warning: Function state mutability can be restricted to pure
  function _updatePurchasingState(
  ^ (Relevant source part starts here and spans across multiple lines).

Writing artifacts to .\build\contracts


C:\Users\RajGanesh\Desktop\CappedToken>truffle develop
Truffle Develop started at http://127.0.0.1:9545/

Accounts:
(0) 0x627306090abab3a6e1400e9345bc60c78a8bef57
(1) 0xf17f52151ebef6c7334fad080c5704d77216b732
(2) 0xc5fdf4076b8f3a5357c5e395ab970b5b54098fef
(3) 0x821aea9a577a9b44299b9c15c88cf3087f3b5544
(4) 0x0d1d4e623d10f9fba5db95830f7d3839406c6af2
(5) 0x2932b7a2355d6fecc4b5c0b6bd44cc31df247a2e
(6) 0x2191ef87e392377ec08e7c08eb105ef5448eced5
(7) 0x0f4f2ac550a1b4e2280d04c21cea7ebd822934b5
(8) 0x6330a553fc93768f612722bb8c2ec78ac90b3bbc
(9) 0x5aeda56215b167893e80b4fe645ba6d5bab767de

Private Keys:
(0) c87509a1c067bbde78beb793e6fa76530b6382a4c0241e5e4a9ec0a0f44dc0d3
(1) ae6ae8e5ccbfb04590405997ee2d52d2b330726137b875053c36d94e974d162f
(2) 0dbbe8e4ae425a6d2687f1a7e3ba17bc98c673636790f1b8ad91193c05875ef1
(3) c88b703fb08cbea894b6aeff5a544fb92e78a18e19814cd85da83b71f772aa6c
(4) 388c684f0ba1ef5017716adb5d21a053ea8e90277d0868337519f97bede61418
(5) 659cbb0e2411a44db63778987b1e22153c086a95eb6b18bdf89de078917abc63
(6) 82d052c865f5763aad42add438569276c00d3d88a2d062d36b2bae914d58b8c8
(7) aa3680d5d48a8283413f7a108367c7299ca73f553735860a87b08f39395618b7
(8) 0f62d96d6675f32685bbdb8ac13cda7c23436f63efbb9d07700d8669ff12b7c4
(9) 8d5366123cb560bb606379f90a0bfd4769eecc0557f1b362dcae9012b548b1e5

Mnemonic: candy maple cake sugar pudding cream honey rich smooth crumble sweet treat

⚠️  Important ⚠️  : This mnemonic was created for you by Truffle. It is not secure.
Ensure you do not use it on production blockchains, or else you risk losing funds.

truffle(develop)> migrate --reset
Using network 'develop'.

Running migration: 1_initial_migration.js
  Deploying Migrations...
  ... 0x03264bd3ea465c6d2ac14bd1712ce7e14616767272d7b50e22bf2b4acc3e7a38
  Migrations: 0x8cdaf0cd259887258bc13a92c0a6da92698644c0
Saving artifacts...
Running migration: 2_deploy_contracts.js
  Replacing ExampleToken...
  ... 0x8b7630c7f771d5d7506d191ae53a08e6416f00f8215e0a2e4cd6a4a82a05529f
  ExampleToken: 0xf12b5dd4ead5f743c6baa640b0216200e89b60da
  Replacing ExampleTokenCrowdsale...
  ... 0x863ee5fecc19555b6e6fdbf28135ade3a1377cce73abcc0c7318bad3641f812f
  ExampleTokenCrowdsale: 0x345ca3e014aaf5dca488057592ee47305d9b3e10
Saving artifacts...
truffle(develop)> ExampleToken.deployed("CSC6890 Token", "GSU", 18).then((t) => {token = t;})
undefined
truffle(develop)> ExampleTokenCrowdsale.deployed(450, web3.eth.accounts[0], token.address , new web3.BigNumber(web3.toWei(150, 'ether'))).then((t) => {sale = t;})
undefined
truffle(develop)> token.transferOwnership(sale.address)
{ tx: '0x444555d010eed52b72862c0f3d4f9c750bd316f71ba80f3c63f665221438b1b0',
 receipt:
   { transactionHash: '0x444555d010eed52b72862c0f3d4f9c750bd316f71ba80f3c63f665221438b1b0',
     transactionIndex: 0,
     blockHash: '0x48b9d42530b040767afbb72fa3bfe4dd7ac53dacb9f544e89be7aea96b1a8aab',
     blockNumber: 4,
     gasUsed: 30792,
     cumulativeGasUsed: 30792,
     contractAddress: null,
     logs: [ [Object] ],
     status: '0x1',
     logsBloom: '0x00000000000000000000000000000000000000000000000000800000000000000000000000000000000400200000000000000000000000000000000000000000000000000000000010000000000000000001000000000000000000000080000000000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000010080000002000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000' },
  logs:
   [ { logIndex: 0,
       transactionIndex: 0,
       transactionHash: '0x444555d010eed52b72862c0f3d4f9c750bd316f71ba80f3c63f665221438b1b0',
       blockHash: '0x48b9d42530b040767afbb72fa3bfe4dd7ac53dacb9f544e89be7aea96b1a8aab',
       blockNumber: 4,
       address: '0xf12b5dd4ead5f743c6baa640b0216200e89b60da',
       type: 'mined',
       event: 'OwnershipTransferred',
       args: [Object] } ] }
truffle(develop)>

*****************************************************Executing the first transaction:********************************************************

Since the mincap for our program is 5, and the Ether passed in the transaction is 2.5, it fails, below is the output:

truffle(develop)> sale.buyTokens(web3.eth.accounts[1], {value : new web3.BigNumber(web3.toWei(2.5, 'ether')) , from : web3.eth.accounts[1]});
Error: VM Exception while processing transaction: revert
    at Object.InvalidResponse (C:\Users\RajGanesh\AppData\Roaming\npm\node_modules\truffle\build\webpack:\~\web3\lib\web3\errors.js:38:1)
    at C:\Users\RajGanesh\AppData\Roaming\npm\node_modules\truffle\build\webpack:\~\web3\lib\web3\requestmanager.js:86:1
    at C:\Users\RajGanesh\AppData\Roaming\npm\node_modules\truffle\build\webpack:\packages\truffle-provider\wrapper.js:134:1
    at XMLHttpRequest.request.onreadystatechange (C:\Users\RajGanesh\AppData\Roaming\npm\node_modules\truffle\build\webpack:\~\web3\lib\web3\httpprovider.js:128:1)
    at XMLHttpRequestEventTarget.dispatchEvent (C:\Users\RajGanesh\AppData\Roaming\npm\node_modules\truffle\build\webpack:\~\xhr2\lib\xhr2.js:64:1)
    at XMLHttpRequest._setReadyState (C:\Users\RajGanesh\AppData\Roaming\npm\node_modules\truffle\build\webpack:\~\xhr2\lib\xhr2.js:354:1)
    at XMLHttpRequest._onHttpResponseEnd (C:\Users\RajGanesh\AppData\Roaming\npm\node_modules\truffle\build\webpack:\~\xhr2\lib\xhr2.js:509:1)
    at IncomingMessage.<anonymous> (C:\Users\RajGanesh\AppData\Roaming\npm\node_modules\truffle\build\webpack:\~\xhr2\lib\xhr2.js:469:1)
    at emitNone (events.js:111:20)
    at IncomingMessage.emit (events.js:208:7)
    at endReadableNT (_stream_readable.js:1056:12)
    at _combinedTickCallback (internal/process/next_tick.js:138:11)
   at process._tickDomainCallback (internal/process/next_tick.js:218:9)

   
*****************************************************Executing the second transaction*****************************************************   
   Buying 15 ethers, below is the response:

   
truffle(develop)> sale.buyTokens(web3.eth.accounts[1], {value : new web3.BigNumber(web3.toWei(15, 'ether')) , from : web3.eth.accounts[1]});
{ tx: '0x7352427a2c8a9833cc4f65d9b7717c572c3159aa36625b48e369f3c9ce5b93e0',
  receipt:
   { transactionHash: '0x7352427a2c8a9833cc4f65d9b7717c572c3159aa36625b48e369f3c9ce5b93e0',
     transactionIndex: 0,
     blockHash: '0x01508327146f6361897c3f0884357a8d289846e242034417560ba0490ee6bfa4',
     blockNumber: 6,
     gasUsed: 122728,
     cumulativeGasUsed: 122728,
     contractAddress: null,
     logs: [ [Object], [Object], [Object] ],
     status: '0x1',
     logsBloom: '0x00000000000000000000000000000000000000004000000000000000000000000000000000000020000400200000000000000000000000000000000000000000000000000020000000000008000000000000000000010000000080000080000000000000020000000000000000000800000000000000400000000010000000040000000000010000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000004000000000000020000000000000000000000000000000000000000000000020000010000000000000' },
  logs:
   [ { logIndex: 2,
       transactionIndex: 0,
       transactionHash: '0x7352427a2c8a9833cc4f65d9b7717c572c3159aa36625b48e369f3c9ce5b93e0',
       blockHash: '0x01508327146f6361897c3f0884357a8d289846e242034417560ba0490ee6bfa4',
       blockNumber: 6,
       address: '0x345ca3e014aaf5dca488057592ee47305d9b3e10',
       type: 'mined',
       event: 'TokenPurchase',
       args: [Object] } ] }
truffle(develop)>


*****************************************************Executing the fourth transaction*****************************************************
Buying 25 Ethers again, below is the response:
truffle(develop)> sale.buyTokens(web3.eth.accounts[1], {value : new web3.BigNumber(web3.toWei(25, 'ether')) , from : web3.eth.accounts[1]});
{ tx: '0xdb8e42f198722947101b9e2fed3380da70d37fa07efe126d957d718044c37a20',
  receipt:
   { transactionHash: '0xdb8e42f198722947101b9e2fed3380da70d37fa07efe126d957d718044c37a20',
     transactionIndex: 0,
     blockHash: '0x8258f789e647c988bc7cf5f631ad2f11f082ef1316796eb8229d6f9e728e05bb',
     blockNumber: 7,
     gasUsed: 62728,
     cumulativeGasUsed: 62728,
     contractAddress: null,
     logs: [ [Object], [Object], [Object] ],
     status: '0x1',
     logsBloom: '0x00000000000000000000000000000000000000004000000000000000000000000000000000000020000400200000000000000000000000000000000000000000000000000020000000000008000000000000000000010000000080000080000000000000020000000000000000000800000000000000400000000010000000040000000000010000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000004000000000000020000000000000000000000000000000000000000000000020000010000000000000' },
  logs:
   [ { logIndex: 2,
       transactionIndex: 0,
       transactionHash: '0xdb8e42f198722947101b9e2fed3380da70d37fa07efe126d957d718044c37a20',
       blockHash: '0x8258f789e647c988bc7cf5f631ad2f11f082ef1316796eb8229d6f9e728e05bb',
       blockNumber: 7,
       address: '0x345ca3e014aaf5dca488057592ee47305d9b3e10',
       type: 'mined',
       event: 'TokenPurchase',
       args: [Object] } ] }
truffle(develop)>



