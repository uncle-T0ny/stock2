
[tags]: <> (ambiutils, utils, eth)
http://rawgit.com/Ambisafe/etoken-lib/master/utils/index.html?http://node.ambisafe.com

https://rawgit.com/Ambisafe/etoken-lib/master/utils/index.html?https://node.ambisafe.com

http://rawgit.com/Ambisafe/etoken-lib/master/utils/index.html?http://geth.ambisafe.co

You can specify custom node adding it as parameter

[tags-end]: <>

[tags]: <> (ambiutils, utils, transactions)
### Get transactions count
```javascript
web3.eth.getTransactionCount('0x652c85746ca740457dc90876339d5ae45632693d', cbval);
```

### Get transaction receipt(details)
```javascript
eth.getTransactionReceipt('0x61d2631e0823b6ea2bb89e5455dad956f2951f356ed3f14b851157ec7d60965d', cbval);
```

[tags-end]: <>

[tags]: <> (kubectl, kubernetes)
### change context
kubectl config use-context production

kubectl config use-context staging

### view namespaces
kubectl get namespaces

### view server status
kubectl get pods -n rc

### view server logs
kubectl get pods -n rc

kubectl -n rc logs orderbook-67457c6c8b-gpwdg

kubectl -n rc logs --tail 150 -f orderbook-765c4cdd4f-g5c9n

### stop the api
kubectl -n rc delete deployment api

### connect to redis
kubectl -n develop get pods

kubectl -n develop exec -it redis-6d65fc4959-nzgg4 redis-cli

### show supernode url
kubectl -n rc get svc supernode

or

kubectl -n rc get service supernode

on dev

kubectl -n develop describe ingress orderbook
### restrart RC back
kubectl -n rc delete pods -l tier=backend

### connect to production server
kubectl -n production exec -it orderbook-6746499554-c45w8 bash

[tags-end]: <>

[tags]: <> (ambiutils, utils, erc20)
### Sent ERC-20 tokens

```javascript
const ETHER_TOKEN_ABI = [{"constant":true,"inputs":[{"name":"_address","type":"address"}],"name":"balanceEth","outputs":[{"name":"","type":"uint256"}],"payable":false,"type":"function"},{"constant":false,"inputs":[{"name":"_spender","type":"address"},{"name":"_value","type":"uint256"}],"name":"approve","outputs":[{"name":"","type":"bool"}],"payable":false,"type":"function"},{"constant":false,"inputs":[{"name":"_from","type":"address"},{"name":"_to","type":"address"},{"name":"_value","type":"uint256"}],"name":"transferFrom","outputs":[{"name":"","type":"bool"}],"payable":true,"type":"function"},{"constant":true,"inputs":[{"name":"","type":"address"}],"name":"balances","outputs":[{"name":"","type":"uint256"}],"payable":false,"type":"function"},{"constant":false,"inputs":[{"name":"receiver","type":"address"},{"name":"amount","type":"uint256"}],"name":"mint","outputs":[],"payable":false,"type":"function"},{"constant":true,"inputs":[{"name":"_owner","type":"address"}],"name":"balanceOf","outputs":[{"name":"","type":"uint256"}],"payable":false,"type":"function"},{"constant":false,"inputs":[{"name":"_enabled","type":"bool"}],"name":"setAutoDeposit","outputs":[{"name":"","type":"bool"}],"payable":false,"type":"function"},{"constant":false,"inputs":[{"name":"_to","type":"address"},{"name":"_value","type":"uint256"}],"name":"transfer","outputs":[{"name":"","type":"bool"}],"payable":true,"type":"function"},{"constant":true,"inputs":[{"name":"_to","type":"address"}],"name":"isAutoDeposit","outputs":[{"name":"","type":"bool"}],"payable":false,"type":"function"},{"constant":true,"inputs":[{"name":"","type":"address"},{"name":"","type":"address"}],"name":"allowance","outputs":[{"name":"","type":"uint256"}],"payable":false,"type":"function"},{"constant":true,"inputs":[{"name":"","type":"address"}],"name":"autoDeposit","outputs":[{"name":"","type":"bool"}],"payable":false,"type":"function"},{"constant":false,"inputs":[{"name":"_to","type":"address"}],"name":"deposit","outputs":[{"name":"","type":"bool"}],"payable":true,"type":"function"},{"constant":false,"inputs":[{"name":"_to","type":"address"},{"name":"_value","type":"uint256"}],"name":"withdraw","outputs":[{"name":"","type":"bool"}],"payable":false,"type":"function"},{"payable":true,"type":"fallback"},{"anonymous":false,"inputs":[{"indexed":true,"name":"from","type":"address"},{"indexed":true,"name":"to","type":"address"},{"indexed":false,"name":"value","type":"uint256"}],"name":"Transfer","type":"event"}];

const COIN_ABI = [{"constant":true,"inputs":[{"name":"_address","type":"address"}],"name":"balanceEth","outputs":[{"name":"","type":"uint256"}],"payable":false,"type":"function"},{"constant":false,"inputs":[{"name":"_spender","type":"address"},{"name":"_amount","type":"uint256"}],"name":"approve","outputs":[{"name":"","type":"bool"}],"payable":false,"type":"function"},{"constant":false,"inputs":[{"name":"_from","type":"address"},{"name":"_to","type":"address"},{"name":"_amount","type":"uint256"}],"name":"transferFrom","outputs":[{"name":"","type":"bool"}],"payable":false,"type":"function"},{"constant":true,"inputs":[{"name":"","type":"address"}],"name":"balances","outputs":[{"name":"","type":"uint256"}],"payable":false,"type":"function"},{"constant":false,"inputs":[{"name":"receiver","type":"address"},{"name":"amount","type":"uint256"}],"name":"mint","outputs":[],"payable":false,"type":"function"},{"constant":true,"inputs":[{"name":"_address","type":"address"}],"name":"balanceOf","outputs":[{"name":"","type":"uint256"}],"payable":false,"type":"function"},{"constant":false,"inputs":[{"name":"_to","type":"address"},{"name":"_value","type":"uint256"}],"name":"transfer","outputs":[{"name":"","type":"bool"}],"payable":false,"type":"function"},{"constant":true,"inputs":[{"name":"","type":"address"},{"name":"","type":"address"}],"name":"allowance","outputs":[{"name":"","type":"uint256"}],"payable":false,"type":"function"},{"inputs":[],"payable":false,"type":"constructor"},{"payable":true,"type":"fallback"},{"anonymous":false,"inputs":[{"indexed":true,"name":"from","type":"address"},{"indexed":true,"name":"to","type":"address"},{"indexed":false,"name":"value","type":"uint256"}],"name":"Transfer","type":"event"}];
var tokens = {
 ether:  Promise.promisifyAll(web3.eth.contract(ETHER_TOKEN_ABI).at('0xd1ebc82ffe1e480330f460eee105343375f01d91')),
 btcs:  Promise.promisifyAll(web3.eth.contract(COIN_ABI).at('0x622136475c0cd6b173b07815da2f0fb051718f5e')),
 dollar: Promise.promisifyAll(web3.eth.contract(COIN_ABI).at('0xc875bc521f3980050b3c1c1a10d254a46f8e56ae')),
 foo:    Promise.promisifyAll(web3.eth.contract(COIN_ABI).at('0x1b8e20909c8ea86505cf4e66dbf20438d3091c5f')),
 bar:    Promise.promisifyAll(web3.eth.contract(COIN_ABI).at('0xf5ddaa0486f607d0fb56dad6b87a28701e622a31')),
 baz:    Promise.promisifyAll(web3.eth.contract(COIN_ABI).at('0xe64213ea11f6f516188795d93a6c13e0a7a556c1')),
};

const stageTokens = {
 ETH:  Promise.promisifyAll(web3.eth.contract(ETHER_TOKEN_ABI).at('0x7ca335a0aa873c89338070dcbb71c1ff4e83e13b')),
 OBTCRPS:  Promise.promisifyAll(web3.eth.contract(COIN_ABI).at('0xE7029dC10e940d8dAcd3b4310085261Af677E9B2')),
 OUSDRPS: Promise.promisifyAll(web3.eth.contract(COIN_ABI).at('0x5411c8212cad1baa571dfa6dca755addc59a2ee3')),
 AMM:    Promise.promisifyAll(web3.eth.contract(COIN_ABI).at('0x6B15c86cB19a92a7B99f1A7e106012B12C351E39'))
};

safeTransaction(tokens.dollar.mint, ['0x033e52d315300bf218fe49c6cbc710d3d4b8a0d3', '10000000000'], address) //100 dollars
safeSend('0x033e52d315300bf218fe49c6cbc710d3d4b8a0d3', web3.toWei(1), address, {waitReceipt: false, gasPrice: web3.toWei(4, 'gwei')}); // 1 eth
 @Aromankov
Owner

```

[tags-end]: <>
