
## About

Enyo is a lightweight multistage partition-based encryption algorithm.
Enyo cipher demonstrates good resistance to a brute-force attack.
It is well suited for small-scale applications where the computational power is a bottleneck.

- Combines the performance of primitive ciphers with enhanced security
- Custom encoding ensures URL safe encryption
- Transposition stage for additional security

## Modules

- `enyoencryption` - Enyo Encryption module
- `enyodecryption` - Enyo Decryption module


## Example Usage

#### Encryption

```python
# Third parameter is an optional integer for partition (by default 2), the fourth parameter is optional Boolean for transposition (default False)
test = EnyoEncryption("test", "secretkey", partition=2, transposition=True)

# To print the encrypted text
print(test.encrypted)
```
##### Output

```python
SaSQpN
```

#### Decryption

```python
# Third parameter is an optional integer for partition (by default 2), the fourth parameter is optional Boolean for transposition (default False)
test = EnyoDecryption("SaSQpN", "secretkey", partition=2, transposition=True)

# To print the decrypted text
print(test.decrypted)
```

##### Output

```python
test
```

## Links

- [Research Paper](https://link.springer.com/chapter/10.1007/978-981-16-1089-9_32)
- [Demo](https://enyo.owaspvit.com)
