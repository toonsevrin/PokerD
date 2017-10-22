# Pokerd
This is the pokerd design doc without implementation

Possible project names: pokerd.io, subitus.io

## Peer to peer deck selection
Deck selection is arguably the most difficult part to achieve in decentralized poker. Let's start with hand selection. This is heavily inspired by 'Mental Poker'.

Let's start with a two hand game, between Bob and Alice.

Bob starts by encrypting each card in the 52 cards deck, and sends the encrypted versions to Alice. Alice picks two of the encrypted cards for bob (which only he knows the values of).

Now Alice encrypts the other 50 cards with a second encryption and sends these to bob again, bob decrypts two of them and sends them to Alice, which she can finaly decrypt to see the values.

All players have a hand, we just need to generate the community cards. Bob still has 48 cards encrypted by alice, he can pick some of these and allow alice to decrypt them.

