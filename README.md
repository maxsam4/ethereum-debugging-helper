# ethereum-debugging-helper
This is a tiny script that helps in debugging solidity smart contracts on kovan testnet

##extract.py
It is a python script extracts abi, bytecode and function hashes from the build file that solidity compiler generates

####How to use
1. Copy the script to your project folder such that the build files reside in /build/contracts from the script's location (where truffle config, package,json etc reside in a default structure).
2. Create an empty directory named "extract".
3. Install python 2.7.x and pysha3 module using "pip install pysha3".
4. Compile your contracts using truffle compile or solc directly.
5. Execute the script and it will create separate abi and bytecode files for all your contracts and a cumulative function hashes file in the extract directory.


##Userscript script
It adds a button to kovan vmtrace page that expands all the Show more fields and decodes the calldata to show the function called.
It uses functionHashes generated by the python script to decode, so you need to add hashes for your functions to it. You can generate the hashes using the python script.

####How to use
1. Install tampermonkey (chrome) or Greasemonkey (firefox).
2. Copy the script and paste it as new a script in tampermonkey/greasemonkey.
3. Reload etherscan, and there should now be a "Show Details" button above Decoded Traces that you can press to see the magic.
