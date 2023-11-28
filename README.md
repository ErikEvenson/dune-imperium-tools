# Dune Imperium Tools

This repository's goal is to develop tools that might be useful to develop and train an AI player.  These tools will include:

- Data files describing the various game elements.
- A standard way to represent game state.  This would be analagous to the way FEN strings capture the state of a chess game.  The representation should work for player viewpoints and an all-knowing viewpoint.
- A standard way to represent game moves.
- A script to determine possible moves given a board state.
- A script to modify a game state given a move selection.

## Data Files

See [Game Data](./gamedata/dune-imperium).

- [Board Spaces](./gamedata/dune-imperium/board-spaces.json)
- [Conflict Cards](./gamedata/dune-imperium/conflict-cards.json)
- [Imperium Deck Cards](./gamedata/dune-imperium/imperium-deck-cards.json)
- [Intrigue Cards](./gamedata/dune-imperium/intrigue-cards.json)
- [Leader Cards](./gamedata/dune-imperium/leader-cards.json)
- [Reserve Cards](./gamedata/dune-imperium/reserve-cards.json)


## Game State

To encode a board position for "Dune: Imperium," similar to how Forsyth-Edwards Notation (FEN) encodes chess positions, we need to develop a system that captures all the critical elements of the game. Dune: Imperium has various components, including player decks, hands, boards, and different types of resources, so this will be a multi-faceted encoding. Here's a proposed structure:

1. **Board State:**
    - **Agents:** Encode the positions of Agents on the board.
    - **Maker Bonuses:** Encode the state of Maker Bonuses.

1. **Player State (For Each Player):**
   - **Deck Composition:** Encode the composition of each player's deck, including card types and quantities.
   - **Hand:** Represent the cards in the player's hand.
   - **Discard and Used Piles:** Encode cards in the discard pile and used pile.
   - **Resources:** Quantities of each type of resource the player has (spice, water, influence, etc.).
   - **Victory Points:** Current victory points of the player.

1. **Game Round and Player Turn:**
   - Indicate the current game round and whose turn it is.

1. **Imperfect Information Elements (for Player Viewpoints):**
   - **Hidden Cards:** Indicate hidden cards or information, if any, for each player.

1. **All-knowing Viewpoint:**
   - Include all hidden information, such as the exact composition of each player's deck and hand.

1. **Special Conditions:**
   - Any special game conditions or effects in play that affect the game state.

## Game Moves

TBD

## Moves

TBD

## Move Propagation

TBD
