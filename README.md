# Notes on Network Security

This repository contains the source of notes taken about the Network Security
class held by prof. Nicola Laurenti at Università di Padova during 2nd semester
of A.A. 2012/13.

Due to the high amount of math involved in the notes, they're written in the
superset of Markdown provided by the 
[kramdown gem](http://kramdown.rubyforge.org/).

## Source conversion
You can convert the notes to all available outputs formats by simply installing
the `kramdown` gem:

```
gem install kramdown
```
or, if you prefer, there's a `Gemfile` available:

```
bundle install
```

## References
_(cite books references here)_

## Table of Contents

* Security Taxonomy
  * Objectives
  * Threats / Attacks
  * Services
  * Mechanisms
* Positioning of security services in network
* General model of an encryption system
* The guessing attack to an encryption system
* Perfect secrecy
* Review of information theory: entropy, equivocation, mutual information
* Necessary condition for perfect secrecy
* Adversarial indistinguishability
* Computational secrecy
* Computational security: the complexity / success probability tradeoff
* Block ciphers: general model and simple examples (monoalphabetic substitution,
transposition, linear)
* Random oracle model
* Feistel ciphers
* Data Encryption Standard (DES): design principles and history, subkey
generation structure, description of round function
* Classification of attacks: on the message/on the key, known/chosen
  plaintext/ciphertext

