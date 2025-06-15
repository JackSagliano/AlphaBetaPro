# ⭕❌ MNKGame – AlphaBetaPro

**MNKGame** is a Java implementation of the generalized (M, N, K)-game — an extended version of Tic-Tac-Toe, where two players compete to align K symbols on an MxN grid.

This project includes several AI players, including **AlphaBetaPro**, an advanced algorithm based on alpha-beta pruning and heuristic evaluation.

---

## 🧠 What is the (M, N, K)-Game?

Two players take turns selecting free cells on an M×N grid.  
The first to align **K symbols** in a row — horizontally, vertically, or diagonally — wins.  
If the board fills up with no winner, the game ends in a draw.

---

## 🏆 Scoring System

| Outcome                                 | Points |
|----------------------------------------|--------|
| 🥇 Win as **second player**            | 3      |
| 🥈 Win as **first player** or by forfeit | 2      |
| 🤝 Draw                                 | 1      |
| ❌ Loss                                  | 0      |

---

## 📦 Project Structure

This project includes:
- A modular Java engine for (M, N, K)-game rules
- Several AI players:
  - 🎲 `RandomPlayer` — chooses moves randomly
  - 🎯 `QuasiRandomPlayer` — mixes randomness with logic
  - 🤖 `AlphaBetaPro` — alpha-beta pruning and smart evaluation (our algorithm)
- A test suite for head-to-head comparisons

---

## 🚀 How to Run

### 1. 🛠️ Compile the Code

In the `mnkgame/` directory, run:

    javac -cp ".." *.java

---

### 2. 🕹️ Run `MNKGame` (Application Mode)

1. **Human vs AlphaBetaPro**  
   Launch a match between a human and your custom bot on a 3×3 board:

        java -cp ".." mnkgame.MNKGame 3 3 3 mnkgame.AlphaBetaPro

2. **AlphaBetaPro vs RandomPlayer**  
   Launch a game between your bot and a simple random opponent:

        java -cp ".." mnkgame.MNKGame 5 5 4 mnkgame.AlphaBetaPro mnkgame.RandomPlayer

3. **AlphaBetaPro vs QuasiRandomPlayer**  
   Launch a game between your bot and a smarter bot:

        java -cp ".." mnkgame.MNKGame 5 5 4 mnkgame.AlphaBetaPro mnkgame.QuasiRandomPlayer

---

### 3. 🧪 Run `MNKPlayerTester` (Tournament Mode)

1. **Score-only output**  
   Run a tournament and display final scores:

        java -cp ".." mnkgame.MNKPlayerTester 5 5 4 mnkgame.AlphaBetaPro mnkgame.QuasiRandomPlayer

2. **Verbose output**  
   Show full move logs during evaluation:

        java -cp ".." mnkgame.MNKPlayerTester 5 5 4 mnkgame.AlphaBetaPro mnkgame.QuasiRandomPlayer -v

3. **Verbose + timeout + repetitions**  
   Run 10 games with 1-second timeout per move:

        java -cp ".." mnkgame.MNKPlayerTester 5 5 4 mnkgame.AlphaBetaPro mnkgame.QuasiRandomPlayer -v -t 1 -r 10

