
# Highlights Week 1.1 - Circom Exercises

## Multiplicación de dos números:

```circom
pragma circom 2.1.6;

include "circomlib/poseidon.circom";
// include "https://github.com/0xPARC/circom-secp256k1/blob/master/circuits/bigint.circom";

template AdditionProof() {
    // declaration of signals
    signal input a;
    signal input b;
    signal output result;

    // constraint
    result <== a * b;
}

component main = AdditionProof();

/* INPUT = {
    "a": 5,
    "b": 5
} */

```

## Multiplicación de tres números:

```circom
pragma circom 2.1.6;

include "circomlib/poseidon.circom";
// include "https://github.com/0xPARC/circom-secp256k1/blob/master/circuits/bigint.circom";

template AdditionProof() {
    // declaration of signals
    signal input a;
    signal input b;
    signal input c;
    signal intermediate;
    signal output result;

    // constraint
    intermediate <== a * b;
    result <== intermediate * c;
}

component main = AdditionProof();

/* INPUT = {
    "a": 5,
    "b": 1,
    "c": 3
} */
```
## HashingProof:

```circom
pragma circom 2.1.6;

include "circomlib/poseidon.circom";
// include "https://github.com/0xPARC/circom-secp256k1/blob/master/circuits/bigint.circom";

template HashingProof() {
    // declaration of signals
    signal input preimage;
    signal input hashOut;
    signal output hashOutput;

    // constraint
    component hasher = Poseidon(1);   
    hasher.inputs[0] <== preimage;
    hashOutput <== hasher.out;
    hashOutput === hashOut;

}

component main = HashingProof();

/* INPUT = {
    "preimage": "123456",
    "hashOut": "3607056778794995795434385085847334626017449707154072104308864676240828390282"
} */
```

