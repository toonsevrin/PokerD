# Pokerd
This is the pokerd design doc without implementation

Possible project names: pokerd.io, subitus.io, hodlem.io

## Peer to peer deck selection
Deck selection is arguably the most difficult part to achieve in decentralized poker. Let's start with hand selection. This is heavily inspired by 'Mental Poker'.

Let's start with a two hand game, between Bob and Alice.

Bob starts by encrypting each card in the 52 cards deck, and sends the encrypted versions to Alice. Alice picks two of the encrypted cards for bob (which only he knows the values of).

Now Alice encrypts the other 50 cards with a second encryption and sends these to bob again, bob decrypts two of them and sends them to Alice, which she can finaly decrypt to see the values.

All players have a hand, we just need to generate the community cards. Bob still has 48 cards encrypted by alice, he can pick some of these and allow alice to decrypt them.

* Zero-knowledge proof
* https://en.wikipedia.org/wiki/Mental_poker
* Requires commutative encryption


## Level of blockchain involvement
### As a settlement layer
The blockchain can behave as a means of verifying the fairness of the game and holding the funds in escrow. The deck selection and gameplay is completely p2p.

### As a gameplay layer
All p2p communications go over the blockchain.

## Secure against orphan blocks
When an orphan block is created at some point, a game can be reverted.
e should be warry that people can not take advantage of this.

## Secure against collusion
Colluding players can be an issue in poker, let's see how traditional sites mitigate this. Random matching will be a good start.


## Useful links
* [Poker through MPC (Multi-Party Computation)](https://www.reddit.com/r/Bitcoin/comments/3xdoaf/how_to_use_bitcoin_to_play_decentralized_poker/)
* [Lessons learned from decentralized game development](https://medium.com/@graycoding/lessons-learned-from-making-a-chess-game-for-ethereum-6917c01178b6)


## Alternatives
* [Unclefinneys (the game itself is run by a server)](https://www.unclefinneys.com)
* [Pokereum (MPC based)](https://github.com/pokereum)
* [Virtue.poker (Mental Poker based, crowdsale)](https://virtue.poker/)
* [Smartholdem (Own chain, not developed](http://smartholdem.io)
