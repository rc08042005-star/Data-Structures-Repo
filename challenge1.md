Phase 0 - Design It
Answer each of these questions in your challenge1.md

What does the undo button need to remember?
It need to remeber every action of user.

When a new action happens, where should it go?
The new action should be remeberered and stored on the top.

When the user clicks undo, which action should be removed first?
The most recent action should be removed first. Meaning the action that is stacked on the top .

Why is a stack a better fit than a queue for this problem?
Because a stack uses LIFO method. And queue uses FIFO method.

What should happen if the user clicks undo but there is nothing left to undo?
It should display " THere is no acitons to be undone"

Psudo Code
1._init_
     Create a empty stack
       The stack will store the user's all actions.
2.do_action
     Recieve the action 
        Stack the action on top of the stack
3.udo_action
     Check if the stack is empty or not
       If it is empty display a no actions remaining text.
          Otherwise remove the action on top stack
          return to the removed action
4.show_history
   If there is no items display helpful message 
      otherwise display all the remaining stack in order from top to bottom
