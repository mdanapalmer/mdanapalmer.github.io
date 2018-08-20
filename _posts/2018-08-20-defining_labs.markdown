---
layout: post
title:      "Defining Labs"
date:       2018-08-20 06:56:10 +0000
permalink:  defining_labs
---

def display_board(board)
  puts " #{board[0]} | #{board[1]} | #{board[2]} "
  puts "-----------"
  puts " #{board[3]} | #{board[4]} | #{board[5]} "
  puts "-----------"
  puts " #{board[6]} | #{board[7]} | #{board[8]} "
end
#puts " cell [0]" | " cell [1]" | "cell [2]" 

**we have defined the "board" array in our CLI 'move' file. 
now we must interpolate the elements with their index defined for the user_input to
correspond to. 

def input_to_index(user_input)
  user_input.to_i - 1
end

#in human language, this says.  The user_input is being changed into an integer from a
#string, and subtracting 1 from that input integer.
#user_input = "4"
#"4" to integer 4 - 1 = index 3

def move(board, index, player = "X")
  board[index] = player
end

tbc

