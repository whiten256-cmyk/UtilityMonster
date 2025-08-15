# Utility Monster Simulation

**⚠️ WARNING: This project contains code that has not been vetted by a human. Use at your own risk.**

A web-based simulation game for exploring utility maximization scenarios through strategic voting on various cards. Players can experiment with different vote combinations and card orderings to find optimal utility outcomes.

## Features

- **Interactive Card Game**: 7 unique cards with different utility payoff structures
- **Strategic Voting**: Enter votes as 6-digit strings (1=YES, 0=NO) for quick experimentation
- **Real-time Scoring**: Automatic recalculation as you change votes
- **Score Progression**: See cumulative scores before each card to inform decisions
- **Card Reordering**: Drag and drop cards or processing order to test different sequences
- **"Eat The Rich" Mechanics**: Special redistribution card that affects timing strategy

## How to Play

1. **Start New Game** - All votes default to "111111" (all players vote YES)
2. **View Score Progression** - Yellow boxes show each player's score before each card
3. **Experiment with Votes** - Change any card's vote string (e.g., "000100" = only Player 4 votes YES)
4. **Reorder Cards** - Test different sequences to optimize "Eat The Rich" timing
5. **Find Maximum Utility** - Iterate to discover optimal strategies

## Files

- `simulation.html` - Main game interface (single-file application)
- `index.html` - Original card management interface
- `utility-monster-cards.json` - Card data definitions
- `memory-bank/` - Project documentation and context

## Usage

Simply open `simulation.html` in a web browser. No server or build process required.

## Card Types

### Grid Cards
- **The Countdown**: Decreasing rewards based on YES vote count
- **The Warmup**: Equal rewards regardless of vote pattern
- **The Threesome**: High reward only when exactly 3 players vote YES
- **The Wedding**: High reward only when exactly 2 players vote YES
- **The Switch**: Different rewards for low vs high YES counts
- **Bonnie and Clyde**: Rewards based on specific vote patterns

### Text Cards
- **Eat The Rich**: Redistributes utils from highest scorers to others (if 4+ YES votes)

## Strategy Tips

- Use "Scores Before" displays to see standings before each card
- Position "Eat The Rich" strategically in the processing order
- Experiment with vote patterns to maximize total utility
- Consider both individual and team scoring implications

## Technical Details

- Pure HTML/CSS/JavaScript implementation
- No external dependencies
- Local storage for game state persistence
- Responsive 4-column card layout for efficient overview
