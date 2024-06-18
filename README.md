![xbYRPTwo9WN5Y3c9VOGLd](https://github.com/0xmoei/alignedlayer-testnet/assets/90371338/de340f64-6873-4171-b608-d7027e61eef0)

> Aligned aims to accelerate Ethereum's roadmap by making proof verification faster and cheaper, reducing costs by up to 90%
>
> Ethereum wasn't initially designed for ZK proofs, and integrating new primitives is challenging. Aligned Layer will transform Ethereum into an efficient, cost-effective platform for SNARK verification
>
> They maintain neutrality, supporting all involved in zero-knowledge technology development and research, focused on expanding Ethereum's ZK capabilities to enable a future of trustless applications using verifiable computation and Ethereum's security.


# Submit a zkProof via AligendLayer

## Install
```console
# Update packages
sudo apt-get update && sudo apt-get upgrade -y
sudo apt-get install curl -y

# Download Binaries
curl -L https://raw.githubusercontent.com/yetanotherco/aligned_layer/main/batcher/aligned/install_aligned.sh | bash

source /root/.bashrc

curl -L https://raw.githubusercontent.com/yetanotherco/aligned_layer/main/batcher/aligned/get_proof_test_files.sh | bash
```

## Submit Proof
```console
cd /root/.aligned/test_files

aligned submit \
--proving_system SP1 \
--proof ~/.aligned/test_files/sp1_fibonacci.proof \
--vm_program ~/.aligned/test_files/sp1_fibonacci-elf \
--aligned_verification_data_path ~/aligned_verification_data \
--conn wss://batcher.alignedlayer.com
```

#

> Save the output link
>
> ![Screenshot_1](https://github.com/0xmoei/alignedlayer-testnet/assets/90371338/fecc9c64-8332-4cc7-a29d-5e0f5d1093e1)

#

## Verify Proof
```console
aligned verify-proof-onchain \
--aligned-verification-data ~/aligned_verification_data/*.json \
--rpc https://ethereum-holesky-rpc.publicnode.com \
--chain holesky
```
![Screenshot_1](https://github.com/0xmoei/alignedlayer-testnet/assets/90371338/42d31743-b464-45c5-a02e-aed31f6dbd75)


> Now post your submit-proof screenshot + output link in Twitter and tag @alignedlayer + #aligned ✅
>
> ![Screenshot_3](https://github.com/0xmoei/alignedlayer-testnet/assets/90371338/88d7b164-182d-4d89-b324-5e1025ae9a93)
>
> Enough for now, but we will follow the future opportunities to contribute to AlignedLayer
