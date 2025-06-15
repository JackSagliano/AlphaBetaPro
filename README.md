# ♟️ MNKGame – AlphaBetaPro

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
