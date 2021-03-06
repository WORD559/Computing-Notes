# Digital Signatures #

In order to verify the integrity of a message, you can add a digital signature to the message. The sender creates the digital signature by irreversably reducing the unencrypted message to produce a hash and then encrypting the hash using their private key. The recipient can then verify the message by hashing the received message, decrypting the hash with the sender's public key, and comparing this hash with a hash of the received message.

The hash could not be modified without knowing the sender's private key, and the hash could not be reversed to produce another message with the same hash. Since the signature can only be correctly decrypted using the sender's public key, the message can be regarded as genuine and unaltered.


However, we need to be able to confirm that the sender is the genuine sender.

The receiver can confirm this with a third party by checking a digital certificate. A trusted company called a Certificate Authority provide these, which include:

 - A serial number
 - The name of the CA
 - Expiry date
 - Subject (name of the holder)
 - Subject's public key
 - CA's digital signature of the certificate to verify the certificate's origin and identity.

The most important things here are the domain name, public key, and the CA's signature. This validates the owner's identity and provides you with their key.

This is used extensively in HTTPS communications.
