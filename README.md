CryptoQuest - AI Powered Adventure Game

An interactive text-based adventure game built on *GenLayer Testnet *, where AI dynamically generates unique story responses to player actions. Every playthrough is different!

[![GenLayer](https://img.shields.io/badge/GenLayer-Testnet%20Bradbury-green)](https://www.genlayer.com/)
[![Python](https://img.shields.io/badge/Python-3.9+-blue)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow)](LICENSE)

---

#  What Makes This Special?

Unlike traditional blockchain games with hardcoded responses, *CryptoQuest* uses GenLayer AI capabilities to:

✨ Generate unique stories - Every action gets a creative AI-generated response  
🎲 **Dynamic gameplay** - No two playthroughs are the same  
⛓️ **On-chain state** - Your progress is stored on the blockchain  
🤖 **LLM-powered** - Uses GenLayer's `gl.exec_prompt for AI responses  
🏆 **Leaderboard** - Compete with other players for the highest score

---

##  How It Works

1. **Connect** your MetaMask wallet to GenLayer Testnet
2. **Start** a new game with your character name
3. **Explore** by typing actions like "explore the forest" or *talk to the merchant*
4. **Survive** - manage your health and gold to maximize your score
5. **Compete** - see how you rank on the leaderboard

### Game Mechanics

- **Health**: Ranges from 0-100. Reach 0 and it's game over!
- **Gold**: Earn or lose gold through your adventures
- **Inventory**: Collect items throughout your journey
- **Score**: Earn points for every action you take
- **Locations**: Explore different areas with unique encounters

---

##  Deployment Guide

### Prerequisites

- MetaMask wallet installed
- GenLayer Testnet added to MetaMask
- Testnet GEN tokens from the [faucet] (https://testnet-faucet.genlayer.foundation/)

### Steps

1. **Open GenLayer Studio*
   - Go to https://studio.genlayer.com/](https://studio.genlayer.com/)
   - Connect your MetaMask wallet

2. **Deploy the Contract**
   - Copy the contents of `cryptoquest.py`
   - Paste into GenLayer Studio
   - Click "Run and Debug" (▶ play button)
   - Confirm the transaction in MetaMask
   - Copy your contract address

3. **Update Frontend**
   - Open `cryptoquest-frontend.html`
   - Find line: `const CONTRACT_ADDRESS = "YOUR_CONTRACT_ADDRESS_HERE";`
   - Replace with your deployed contract address
   - Save the file

4. **Host Frontend**
   - Option A: Upload to GitHub Pages
   - Option B: Use any static hosting service (Netlify, Vercel, etc.)
   - Option C: Run locally by opening the HTML file in your browser

---

##  How to Play

### Starting a Game

```javascript
// Call the start_game function with your character name
start_game("YourHeroName")
```

### Taking Actions

Type any action you want to perform:
- "explore the dark forest"
- "talk to the mysterious stranger"
- "search for treasure"
- "fight the dragon"
- "rest at the inn"

The AI will generate a unique response and update your game state!

### Example Gameplay

```
You: "explore the forest"
AI: "You venture into the dense forest. Sunlight barely pierces through 
     the canopy. You hear rustling in the bushes and find 20 gold coins!"
     
You: "search the bushes"
AI: "You carefully search the area and discover a hidden sword! 
     Your combat abilities have increased."
```

---

##  Contract Functions

### Write Functions

- `start_game(player_name: str)` - Begin a new adventure
- `take_action(action: str)` - Perform an action (AI-powered)
- `reset_game()` - Start over with a new character

### View Functions

- `get_player_stats()` - Check your current stats
- `get_leaderboard()` - View top 10 players by score

---

##  Technical Architecture

### Smart Contract (Intelligent Contract)

```python
@gl.contract
class CryptoQuest:
    players: dict[str, dict]  # Player state storage
    
    @gl.public.write
    async def take_action(self, action: str) -> dict:
        # Uses gl.exec_prompt() to generate AI responses
        result = await gl.exec_prompt(prompt)
        # Updates player state based on AI response
```

### Key Technologies

- **GenLayer Blockchain** - AI-native blockchain platform
- **Python** - Smart contract language
- **LLM Integration** - Via `gl.exec_prompt()`
- **HTML/CSS/JavaScript** - Frontend interface

---

##  Features

✅ AI-generated dynamic storytelling  
✅ On-chain game state storage  
✅ Real-time health/gold/inventory tracking  
✅ Player leaderboard system  
✅ Quick action buttons for common commands  
✅ Retro terminal aesthetic UI  
✅ Mobile-responsive design  

---

## Future Enhancements

- [ ] Multi-player interactions
- [ ] Item trading system
- [ ] Boss battles with special mechanics
- [ ] Achievement/badge system
- [ ] NFT rewards for high scores
- [ ] Multiple character classes
- [ ] Persistent world state

---

##  Development

### Local Testing

1. Install GenLayer CLI tools
2. Run local simulator:
   ```bash
   genlayer init
   genlayer deploy cryptoquest.py
   ```

### Modify the Game

The AI prompt is in the `take_action()` function. Customize it to:
- Change the game theme (sci-fi, horror, comedy)
- Add new game mechanics
- Implement special events
- Create custom locations

---

##  Resources

- [GenLayer Documentation](https://docs.genlayer.com/)
- [GenLayer Studio](https://studio.genlayer.com/)
- [GenLayer Portal](https://portal.genlayer.foundation/)
- [Get Testnet Tokens](https://testnet-faucet.genlayer.foundation/)

---

##  Contributing

Contributions are welcome! Feel free to:
- Submit bug reports
- Propose new features
- Improve the AI prompts
- Enhance the UI/UX

---

##  Author

**Richardweb1**
- GitHub: [@Richardweb1](https://github.com/Richardweb1)
- Built for GenLayer Testnet Bradbury

---

##  License

MIT License - Feel free to use this code for your own projects!

---

##  Play Now!

Ready to embark on your adventure? Deploy the contract and start playing!
