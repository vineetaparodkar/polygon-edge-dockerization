# Polygon-Edge-Dockerization

## Setup

- Step 1: Initialize data folders for IBFT and generate validator keys

    polygon-edge secrets init --data-dir test-chain-1

    polygon-edge secrets init --data-dir test-chain-2

    polygon-edge secrets init --data-dir test-chain-3

    polygon-edge secrets init --data-dir test-chain-4

- Step 2: Generate the genesis file with the 4 nodes as validators

  polygon-edge genesis --consensus ibft --ibft-validators-prefix-path test-chain- --bootnode /ip4/<vm-ip>/tcp/8002/p2p/16Uiu2HAmJxxH1tScDX2rLGSU9exnuvZKNM9SoK3v315azp68DLPW --bootnode /ip4/<vm-ip>/tcp/8005/p2p/16Uiu2HAmS9Nq4QAaEiogE4ieJFUYsoH28magT7wSvJPpfUGBj3Hq 
