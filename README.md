# pqm4
Post-quantum crypto library for the ARM Cortex-M4

## Introduction

## Schemes included in pqm4

## Setup/Installation

## Running tests and benchmarks

## API documentation

## Benchmarks

### Speed Evaluation
#### Key Encapsulation Schemes
| scheme | implementation | key generation [cycles] | encapsulation [cycles] | decapsulation [cycles] |
| ------ | -------------- | ----------------------- | ---------------------- | -----------------------|
| frodo640-cshake (10 executions) | opt | AVG: 94,191,951 <br /> MIN: 94,191,921 <br /> MAX: 94,192,027 |  AVG: 111,688,861 <br /> MIN: 111,688,796 <br /> MAX: 111,688,895 | AVG: 112,156,317 <br /> MIN: 112,156,264 <br /> MAX: 112,156,389 |
| kindi256342 (10 executions) | ref | AVG: 22,940,741 <br /> MIN: 22,928,176 <br /> MAX: 22,947,668 |  AVG: 29,659,234 <br /> MIN: 29,645,532 <br /> MAX: 29,674,037 | AVG: 37,821,962 <br /> MIN: 37,805,302 <br /> MAX: 37,840,627 |
| kyber768 (10 executions) | m4 | AVG: 1,200,351 <br /> MIN: 1,199,831 <br /> MAX: 1,200,671 |  AVG: 1,497,789 <br /> MIN: 1,497,296 <br /> MAX: 1,498,094 | AVG: 1,526,564 <br /> MIN: 1,526,070 <br /> MAX: 1,526,868 |
| kyber768 (10 executions) | ref | AVG: 1,379,979 <br /> MIN: 1,379,339 <br /> MAX: 1,380,339 |  AVG: 1,797,604 <br /> MIN: 1,796,996 <br /> MAX: 1,797,947 | AVG: 1,950,350 <br /> MIN: 1,949,742 <br /> MAX: 1,950,693 |
| newhope1024cca (10 executions) | ref | AVG: 1,502,435 <br /> MIN: 1,502,179 <br /> MAX: 1,502,707 |  AVG: 2,370,157 <br /> MIN: 2,369,901 <br /> MAX: 2,370,429 | AVG: 2,517,215 <br /> MIN: 2,516,959 <br /> MAX: 2,517,488 |
| newhope1024cca (9 executions) | m4 | AVG: 1,246,626 <br /> MIN: 1,246,404 <br /> MAX: 1,246,772 |  AVG: 1,966,358 <br /> MIN: 1,966,137 <br /> MAX: 1,966,505 | AVG: 1,977,753 <br /> MIN: 1,977,532 <br /> MAX: 1,977,899 |
| ntruhrss701 (10 executions) | ref | AVG: 197,262,297 <br /> MIN: 197,261,894 <br /> MAX: 197,262,845 |  AVG: 5,166,153 <br /> MIN: 5,166,153 <br /> MAX: 5,166,155 | AVG: 15,069,480 <br /> MIN: 15,069,478 <br /> MAX: 15,069,485 |
| saber (10 executions) | ref | AVG: 7,122,695 <br /> MIN: 7,122,695 <br /> MAX: 7,122,695 |  AVG: 9,470,634 <br /> MIN: 9,470,634 <br /> MAX: 9,470,634 | AVG: 12,303,775 <br /> MIN: 12,303,775 <br /> MAX: 12,303,775 |
| sikep751 (1 executions) | ref | AVG: 3,508,587,555 <br /> MIN: 3,508,587,555 <br /> MAX: 3,508,587,555 |  AVG: 5,685,591,898 <br /> MIN: 5,685,591,898 <br /> MAX: 5,685,591,898 | AVG: 6,109,763,845 <br /> MIN: 6,109,763,845 <br /> MAX: 6,109,763,845 |
#### Signature Schemes
| scheme | implementation | key generation [cycles] | sign [cycles] | verify [cycles] |
| ------ | -------------- | ----------------------- | ------------- | ----------------|
| dilithium (100 executions) | ref | AVG: 2,888,788 <br /> MIN: 2,887,878 <br /> MAX: 2,889,666 |  AVG: 17,318,678 <br /> MIN: 5,395,144 <br /> MAX: 58,367,745 | AVG: 3,225,821 <br /> MIN: 3,225,481 <br /> MAX: 3,226,288 |
| sphincs-shake256-128s (1 executions) | ref | AVG: 4,433,268,654 <br /> MIN: 4,433,268,654 <br /> MAX: 4,433,268,654 |  AVG: 61,562,227,280 <br /> MIN: 61,562,227,280 <br /> MAX: 61,562,227,280 | AVG: 70,943,476 <br /> MIN: 70,943,476 <br /> MAX: 70,943,476 |
### Memory Evaluation
#### Key Encapsulation Schemes
| scheme | implementation | key generation [bytes] | encapsulation [bytes] | decapsulation [bytes] |
| ------ | -------------- | ----------------------- | ---------------------- | -----------------------|
| frodo640-cshake | opt | 36,536 |  58,328 | 68,680 |
| kindi256342 | ref | 10,632 |  10,736 | 16,912 |
| kyber768 | m4 | 10,304 |  13,464 | 14,624 |
| kyber768 | ref | 10,304 |  13,464 | 14,624 |
| newhope1024cca | m4 | 11,160 |  17,456 | 19,656 |
| newhope1024cca | ref | 11,160 |  17,456 | 19,656 |
| ntruhrss701 | ref | 10,024 |  8,996 | 10,244 |
| saber | ref | 12,616 |  14,888 | 15,984 |
| sikep751 | ref | 11,128 |  11,672 | 12,224 |
#### Signature Schemes
| scheme | implementation | key generation [bytes] | sign [bytes] | verify [bytes] |
| ------ | -------------- | ----------------------- | ------------- | ----------------|
| dilithium | ref | 51,372 |  87,544 | 55,752 |
| sphincs-shake256-128s | ref | 2,904 |  3,032 | 10,768 |

## Adding new schemes and implementations

## License