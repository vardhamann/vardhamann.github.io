---
layout: post
title: Extending Org-Capture systemwide in Mac OS.
author: "B E Vardhamann"
---

# Why?
Org-Capture allows us to use templates to quicky note down things, extending this function accross the system allows one to quickly capture thoughts and get back to what they were initially doing.

# My setup 
I am currently using Doom Emacs and have installed all packages through *init.el*.

## Writing the script 
1. In Automator.app we choose the Quick Action option.  
     
    ![automator.app > Quick actions](/assets/images/org-capture/qa.png)
2. We add the *Run Shell Script* codeblock and change the shell to *zsh*. We then enter  
`/opt/homebrew/bin/emacsclient -ne "(+org-capture/open-frame)"`  
as the command in this codeblock.  

    ![Shell command](/assets/images/org-capture/shell_command.png)
3. Save this as Capture.

## Setting up the keybinding.

1. Open System preferences > Keyboard > Shortcuts > Services. Scroll down to the General section and you will find your saved quick action.  

    ![System preference > Keyboard ](/assets/images/org-capture/sys_pref.png)
2. Map it to your desired keybinding, in my case `⌥ + .`

3. Test it!  

    ![Example](/assets/images/org-capture/final_example.jpeg)  
   
   
--- 
# Conclusions 
This is not as complex as [Aaron's tutorial on using Org-Protocol](https://blog.aaronbieber.com/2016/11/24/org-capture-from-anywhere-on-your-mac.html) to copy links and highlighted text into the capture, but this seemed simple enough for me and allowed to get through my workflow.

