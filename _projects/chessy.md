---
title: "chessy"
excerpt: "Performant, classical stand-alone chess engine written in Rust."
header:
  teaser: /assets/images/chessy-screenshot.png
sidebar:
  - title: "Techniques used"
    image: /assets/images/chessy-screenshot.png
    image_alt: "logo"
    text: "Rust, Alpha-Beta pruning, Low-Level optimizations"
  - text: <a href="https://github.com/Conzel/chessy"><i class="fab fa-github"></i> GitHub repository</a>
--- 
Chessy is a Rust implementation of a _classical_ chess engine (as opposed to the recently emerging
engines based on neural networks). The goal is to provide a performant chess engine that works as a standalone
and later as a WebASM file to be embedded in webpages, written with clean, performant and well tested code.

# Why?
I believe that Rust is an excellent language for writing a performant chess engine - easily parallelizable,
allows fine control over low level details, has const functions for precalculations and is blazingly fast.

As for why, when Stockfish already exists? Mostly for fun, it has been a great learning exercise so far :) 
I don't really expect to beat Stockfish, but maybe I can at least beat some humans. 

# How does it work?
Chessy is based on an algorithm called alpha-beta pruning (like most classical chess engines). Alpha-beta
pruning is a slightly improved variation of the minimax algorithm, which tries to evaluate moves for both players 
in tandem and tries to find the best move for the player it is currently optimizing under the strongest move that
the opponent has. This resembles the technique that strong human players also use when playing chess 
(or Shogi, Checkers, even Tic-Tac-Toe).

To make this efficient, there are of course a lot of specific tricks used (as we easily have to evaluate 
ten million positions on every move or more). We currently use Bitboards, Magic Bitboards, Transposition
Tables, Quiescence Search and Move Preordering together with some interesting Rust unstable features 
(const functions and inline assembly). In the future, I also plan on adding Opening Databases and Endgame tables.

# At what level does it play?
Not fully evaluated, but it should currently be at around 1600 ELO, from tests against humans.

For further information and instructions on how to use, please refer to the [GitHub repository](https://github.com/Conzel/chessy)!
