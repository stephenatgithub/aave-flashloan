### add dependency for aave

`forge install aave/aave-v3-core --no-commit`

[forge install](https://book.getfoundry.sh/reference/forge/forge-install?highlight=forge%20install#forge-install)



### update import path

change from

https://github.com/aave/aave-v3-core/blob/master/

to

aave-v3-core/



### deploy

forge create 
--rpc-url <your_rpc_url> 
--private-key <your_private_key> src/SimpleFlashLoan.sol:SimpleFlashLoan 
--constructor-args <PoolAddressesProvider-Aave>

[forge create](https://book.getfoundry.sh/reference/forge/forge-create?highlight=forge%20create#forge-create)


### testnet Faucet 

https://app.aave.com/faucet/



### Sign and publish a transaction

cast send 0x705D07DE206df80AF8a3361e928fa60a2715c212 
--rpc-url <your_rpc_url> 
--private-key <your_private_key>
"fn_RequestFlashLoan(address,uint256)" 0x68194a729C2450ad26072b3D33ADaCbcef39D574 1000000000000000000

[cast send](https://book.getfoundry.sh/reference/cast/cast-send?highlight=cast%20send#cast-send)




### results

#### sepolia testnet

msg.sender
0x2f482f5adaF95dAC725A9eb0b456F406830600d0

PoolAddressesProvider-Aave        
0x0496275d34753A48320CA58103d5220d394FF77F

flash loan contract 
0x705D07DE206df80AF8a3361e928fa60a2715c212

DAI-TestnetMintableERC20-Aave  
0x68194a729C2450ad26072b3D33ADaCbcef39D574

DAI
1 = 1000000000000000000

Transaction Hash
0xea39bc5a6d93606be485925147587a0e00aadfde326092eb1590e21d9c10c3f2



#### polygon mumbai

msg.sender
0xa81FEeCd460D3f87C5BCA3605Ae4809f908F6A92

PoolAddressesProvider-Polygon      
0xeb7A892BB04A8f836bDEeBbf60897A7Af1Bf5d7F

flash loan contract
0x9D6bb92AaB3292DcCF40D4f4Ce16b72458B012cD

USDC-TestnetMintableERC20-Polygon  
0xe9DcE89B076BA6107Bb64EF30678efec11939234

USDC
1 = 1000000

Transaction Hash
0x73af827da7bcd5119c2c258350db1aa343804052f9d0ba9af7cdcc1e10ff19a3

