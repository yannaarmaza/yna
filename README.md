# Hello World

This Solidity program is a simple "Hello World" program that demonstrates the basic syntax and functionality of the Solidity programming language. The purpose of this program is to serve as a starting point for those who are new to Solidity and want to get a feel for how it works.

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has a single function that returns the string "Hello World!". This program serves as a simple and straightforward introduction to Solidity programming, and can be used as a stepping stone for more complex projects in the future.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:

```javascript
/*
Assessment Requirements
1. Create a variable that can hold a number of NFT's. What type of variable might this be?
2. Create an object inside your mintNFT function that will hold the metadata for your NFTs. 
   The metadata values will be passed to the function as parameters. When the NFT is ready, 
   you will store it in the variable you created in step 1
3. Your listNFTs() function will print all of your NFTs metadata to the console (i.e. console.log("Name: " + someNFT.name))
4. For good measure, getTotalSupply() should return the number of NFT's you have created
*/

// create a variable to hold your NFT's
const NFTs = []
// this function will take in some values as parameters, create an
// NFT object using the parameters passed to it for its metadata, 
// and store it in the variable above.
function mintNFT(_name, _eyeColor, _shirtType, _accessories) {
    const NFT = {
        "name":  _name,
        "eyeColor": _eyeColor,
        "shirtType": _shirtType,
        "accessories": _accessories
    }
    NFTs.push (NFT);
    console.log ("Minted: " + _name);
}

// create a "loop" that will go through an "array" of NFT's
// and print their metadata with console.log()
function listNFTs() {
    for(let i = 0; i < NFTs.length; i++){
        console.log("\nID \t\t\t\t" + (i + 1));
        console.log("\nName: \t\t\t" + NFTs[i].name);
        console.log("Eye Color: \t\t" + NFTs[i].eyecolor);
        console.log("Shirt Type: \t" + NFTs[i].shirtType);
        console.log("Accessories: \t" + NFTs[i].accessories);
    }

}

// print the total number of NFTs we have minted to the console
function getTotalSupply () {
    console.log("\n" + NFTs.length);
}

// call your functions below this line
mintNFT ("jen", "Brown", "Croptop", "Choker");
mintNFT ("kat", "Black", "Sweatshirt", "Gold Chains");
mintNFT ("jom", "Black", "Hoodie", "Ring");
mintNFT ("cad", "Brown", "Suit", "Necklace");
mintNFT ("mor", "Brown", "Croptop", "Necklace");
listNFTs();
getTotalSupply();



```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile HelloWorld.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "HelloWorld" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the sayHello function. Click on the "HelloWorld" contract in the left-hand sidebar, and then click on the "sayHello" function. Finally, click on the "transact" button to execute the function and retrieve the "Hello World!" message.

## Authors

Metacrafter  
[@yannaarmaza]


