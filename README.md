# Nonogram (Picross) Puzzle Game

A beautifully designed, interactive Nonogram puzzle game built with Next.js, TypeScript, and Tailwind CSS.

## Features

- **5 Puzzle Presets**: From easy to hard difficulty levels
- **Excellent Keyboard Navigation**: Full keyboard support for seamless gameplay
- **Attractive UI**: Modern design with gradient backgrounds and smooth animations
- **Real-time Validation**: Instant feedback on mistakes and completion
- **Multiple Difficulty Levels**: Easy (5×5), Medium (7×7, 10×10), and Hard (10×10) puzzles

## How to Play

Nonogram is a logic puzzle where you fill in cells based on numeric hints to reveal a hidden picture.

### Rules

1. **Row and Column Hints**: Numbers indicate consecutive filled cells
2. **Multiple Groups**: Multiple numbers mean multiple groups of filled cells with at least one empty cell between them
3. **Goal**: Fill in all correct cells to complete the puzzle

### Controls

#### Keyboard

- **Arrow Keys**: Navigate between cells
- **Space/Enter**: Cycle through states (Empty → Filled → Marked)
- **F**: Toggle filled state
- **X**: Toggle marked state

#### Mouse

- **Click**: Cycle through cell states
- **Yellow Ring**: Shows currently selected cell

### Cell States

- **Empty** (Dark): Unfilled cell
- **Filled** (Blue): Cell is filled
- **Marked** (Gray with X): Cell is marked as empty

## Getting Started

### Install Dependencies

```bash
npm install
```

### Run Development Server

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### Build for Production

```bash
npm run build
npm start
```

## Puzzle Difficulty

- **Easy**: 5×5 grid (Heart, Smiley)
- **Medium**: 7×7 and 10×10 grids (House, Cat)
- **Hard**: 10×10 complex grids (Skull)

## Tech Stack

- **Framework**: Next.js 14
- **Language**: TypeScript
- **Styling**: Tailwind CSS
- **Font**: Inter (Google Fonts)

## Project Structure

```
nonogram/
├── app/
│   ├── layout.tsx          # Root layout with metadata
│   ├── page.tsx            # Main game page
│   └── globals.css         # Global styles
├── components/
│   ├── Cell.tsx            # Individual cell component
│   ├── HintDisplay.tsx     # Row/column hint display
│   └── NonogramGrid.tsx    # Main grid with keyboard navigation
└── lib/
    ├── types.ts            # TypeScript type definitions
    ├── puzzles.ts          # Puzzle data
    └── gameLogic.ts        # Game logic utilities
```

## Game Features

### Visual Design

- Gradient backgrounds and borders
- Smooth hover and focus animations
- Color-coded difficulty levels
- Congratulations modal on completion
- Mistake counter with color indicators

### Game Mechanics

- Real-time puzzle validation
- Mistake tracking
- Auto-detection of puzzle completion
- Reset functionality
- Easy puzzle navigation

## Contributing

Feel free to add more puzzles by editing `lib/puzzles.ts`:

```typescript
{
  id: 'unique-id',
  name: 'Puzzle Name',
  difficulty: 'easy' | 'medium' | 'hard',
  size: 5 | 7 | 10,
  grid: [
    // 2D array where 1 = filled, 0 = empty
  ]
}
```

## License

MIT

---

Enjoy solving puzzles!
