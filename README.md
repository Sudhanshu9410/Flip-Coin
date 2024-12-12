# Flip Coin Game

A simple and interactive Flip Coin Game built with React.js, where users can flip a coin and see the result (Heads or Tails). This project demonstrates basic React concepts such as state management, event handling, and component composition.

## Features

- Simulates a coin flip with random outcomes: Heads or Tails.
- Tracks the total number of flips.
- Displays the count of Heads and Tails results.
- Interactive and responsive UI.

## Technologies Used

- **React.js**: For building the user interface.
- **CSS**: For styling the components.
- **JavaScript**: For logic and interactivity.

## Installation

Follow these steps to set up and run the Flip Coin Game on your local machine:

1. **Clone the repository**:
   ```bash
   git clone [https://github.com/yourusername/flip-coin-game.git](https://github.com/Sudhanshu9410/Flip-Coin)
   cd flip-coin-game
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

3. **Start the development server**:
   ```bash
   npm start
   ```

4. Open your browser and navigate to `http://localhost:3000` to see the app in action.

## Usage

1. Click the **Flip Coin** button to flip the coin.
2. Observe the result (Heads or Tails) displayed on the screen.
3. View the updated counters for Heads, Tails, and total flips.

## File Structure

```
flip-coin-game/
├── public/
│   ├── index.html
│   └── ...
├── src/
│   ├── components/
│   │   ├── Coin.js       // Component to display the coin image
│   │   └── FlipCoin.js   // Main game logic and UI
│   ├── App.js            // App entry point
│   ├── index.js          // ReactDOM render logic
│   └── styles.css        // Custom styles
├── package.json
└── README.md
```

## Components

1. **Coin**
   - Displays the coin image based on the result (Heads or Tails).

2. **FlipCoin**
   - Contains the game logic, button, and counters.

## Example Code

Here is a brief snippet from the `FlipCoin.js` component:

```javascript
import React, { useState } from 'react';
import Coin from './Coin';
import './styles.css';

function FlipCoin() {
  const [result, setResult] = useState(null);
  const [flips, setFlips] = useState(0);
  const [heads, setHeads] = useState(0);
  const [tails, setTails] = useState(0);

  const handleFlip = () => {
    const isHeads = Math.random() < 0.5;
    setResult(isHeads ? 'Heads' : 'Tails');
    setFlips(flips + 1);
    if (isHeads) setHeads(heads + 1);
    else setTails(tails + 1);
  };

  return (
    <div className="flip-coin">
      <h1>Flip Coin Game</h1>
      {result && <Coin side={result} />}
      <button onClick={handleFlip}>Flip Coin</button>
      <p>Total Flips: {flips}</p>
      <p>Heads: {heads}</p>
      <p>Tails: {tails}</p>
    </div>
  );
}

export default FlipCoin;
```

## Screenshots

### Game Interface
![Game Interface](https://via.placeholder.com/800x400?text=Flip+Coin+Game+UI)

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## Acknowledgments

- Inspired by basic React.js tutorials and coin flip probability concepts.

---

Feel free to contribute, suggest improvements, or report issues!
