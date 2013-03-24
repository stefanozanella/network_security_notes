---
layout: page
title: "Lecture 1"
comments: false
sharing: true
footer: true
---
## Outline

* Security taxonomy
 * Objectives
 * Threats/attacks
 * Services
 * Mechanisms

## Overview

Network and Internet security rely heavily on cryptographic algorithms and
protocols, which can be grouped into four main areas:

* **Symmetric encryption**
* **Asymmetric encryption**
* **Data integrity algorithms**
* **Authentication protocols**

The field of **network and Internet security** consists of measures to deter,
prevent, detect and correct security violations that involve the transmission
of information.

## Computer Security Concepts

Definition of _Computer Security_ as given by NIST:

> **Computer Security**  
> The protection afforded to an automated information system in order to attain
> the applicable objectives of preserving the integrity, availability, and
> confidentiality of information system resources (includes hardware, software,
> firmware, information/data, and telecommunications).

### Objectives
From the above definition we can identify a bunch of objectives (or goals) that
security try to achieve:

* **(Data) Confidentiality**: private or confidential information is not made
available or disclosed to unauthorized individuals
* **Integrity**: can be splitted into
  * **Data** integrity: assures that information and programs are changed only
 in a specified and authorized manner
  * **System** integrity: assures that a system preforms its intended function
 in an unimpaired manner, free from inadvertent or deliberate unauthorized
 manipulation of the system
* **Availability**: assures that systems work promptly and service is not
denied to authorized users
* **Accountability**: assures that actions of an entity can be traced uniquely
* to that entity
* **Privacy / Anonimity**: assures that individuals control or influence what
information related to them may be collected and stored and by whom and to whom
that information may be disclosed.

### The OSI Security Architecture
[RFC 2828 (_Internet Security Glossary_)](http://www.rfc-editor.org/rfc/rfc2828.txt)
provides the following definitions:

* **Threat**: a potential for violation of security, which exists when there is
a circumstance, capability, action, or event that could breach security and
cause harm. That is, a threat is a possible danger that might exploit a
vulnerability.
* **Attack**: an assault on system security that derives from an intelligent
threat; that is, an intelligent act that is a deliberate attempt (especially
in the sense of a method or technique) to evade security services and violate
the security policy of a system.

That said, the manager responsible for security needs some systematic way of
defining the requirements for security and characterizing the approaches to
satisfying those requirements. ITU-T Recommendation X.800, 
[Security Architecture for OSI](http://www.itu.int/rec/dologin_pub.asp?lang=e&id=T-REC-X.800-199103-I%21%21PDF-E&type=items), 
defines such a systematic approach. The OSI security architecture focuses on:

* **Attacks**: actions that compromise the security of information owned by an
organization
* **Mechanisms**: processes (or devices incorporating such processes) that are
designed to detect, prevent or recover from a security attack
* **Services**: processing or communication services that ehhance the security
of the data processing systems and the information transfers of an
organization.

### Attacks
We can distinguish between two main categories:

* **Passive** attacks: attempt to learn or make use of information from the
but does not affect system resources.
* **Active** attacks: attempt to alter the system resources or affect their
operation.

Digging into these categories, we can find specific forms of attacks. Some
examples are:

* eavesdropping (against confidentiality)
* modification (against integrity)
* denial of service (against availablity)
* forgery (against accountability)
* repudiation (against accountability, can be applied to both sender and
receiver)
* profiling / fingerprinting (against privacy)

### Services
A security service is a service that is _provided by a protocol layer of
communicating open systems and ensures adequate security of the systems or of
data transfers_. A security service is provided to give a _specific kind of
protection to system resources; security services implement security policies
and are implemented by security mechanisms_.

The OSI Security Architecture defines the following taxonomy of security
services:

* Authentication
  * Peer entity authentication
  * Data origin authentication
* Access control
* Data confidentiality
  * Connection confidentiality
  * Connectionless confidentiality
  * Selective-field confidentiality
  * Traffic-flow confidentiality
* Data integrity
  * Connection integrity with/without recovery
  * Selective-field connection integrity
  * Connectionless integrity
  * Selective-field connectionless integrity
* Nonrepudiation
  * Nonrepudiation of the origin
  * Nonrepudiation of the destination
* Availability service

### Mechanisms
X.800 also defines a taxonomy of security mechanisms, which can be divided into
two main categories: those that are implemented in a specific protocol layer,
such as TCP of an application-layer protocol, and those that are not specific
to any particular protocol layer or security service. Each mechanisms can then
be used by one or more security services to fullfil their goals. The taxonomy
is as follows:

* **Specific security mechanisms**
  * _Encipherment_: use of mathematical algorithms to transform data into a
  form that is not readily intelligible.
  * _Digital Signature_: data appended to a data unit (or a transformation of
  it) that allows a recipient to prove the source and integrity of data
  * _Access Control_
  * _Data Integrity_
  * _Authentication Exchange_: ensuring the identity of an entity by exchanging
  information with it
  * _Traffic Padding_: insertion of bits into gaps in a data stream to mitigate
  traffic analysis attempts
  * _Routing Control_: in particular, ability to change a route when a security
  breach is detected/suspected
  * _Notarization_: use of a third party to assure certain properties of a data
  exchange
* **Pervasive security mechanisms**
  * _Trusted Functionality_: which is, correct with respect to some criteria
  * _Security Label_: marking bound of a resource that names the security
  attibutes of that resource
  * _Event Detection_
  * _Security Audit Trail_: data collected to facilitate a security audit
  * _Security Recovery_: deals with requests from mechanisms, such as event
  handling and management functions, and takes recovery actions

