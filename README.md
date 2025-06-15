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

1. **Human vs Computer**  
   Launch a game between a human and a bot on a 3×3 board:

        java -cp ".." mnkgame.MNKGame 3 3 3 mnkgame.RandomPlayer

2. **Computer vs Computer**  
   Launch a match between two bots on a 5×5 board (4 in a row to win):

        java -cp ".." mnkgame.MNKGame 5 5 4 mnkgame.RandomPlayer mnkgame.QuasiRandomPlayer

---

### 3. 🧪 Run `MNKPlayerTester` (Tournament Mode)

1. **Score-only output**  
   Run a tournament with results summary:

        java -cp ".." mnkgame.MNKPlayerTester 5 5 4 mnkgame.RandomPlayer mnkgame.QuasiRandomPlayer

2. **Verbose output**  
   Run with full move-by-move details:

        java -cp ".." mnkgame.MNKPlayerTester 5 5 4 mnkgame.RandomPlayer mnkgame.QuasiRandomPlayer -v

3. **Verbose + timeout + repetitions**  
   Run 10 matches with 1-second timeout per move:

        java -cp ".." mnkgame.MNKPlayerTester 5 5 4 mnkgame.RandomPlayer mnkgame.QuasiRandomPlayer -v -t 1 -r 10

