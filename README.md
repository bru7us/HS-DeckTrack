HS-DeckTrack
============

A Terminal-based Deck Tracker for Hearthstone on MacOS

Inspired by this thread: http://www.reddit.com/r/hearthstone/comments/26seey/automatic_deck_tracker_and_more_with_ingame/
Original credit for the logging tips from: http://www.reddit.com/r/hearthstone/comments/268fkk/simple_hearthstone_logging_see_your_complete_play/

I've thrown this together as a quick hack for those of us who play on MacOS.
Of course, if you're just a Terminal junky, it's Perl, so you can run it wherever you like!

If you have the screen real-estate, just keep the Terminal window visible on one side of the Hearthstone app.

Requirements
------------
All you really need is the perl script 'HS-DeckTrack' and a deck file, but you can clone the whole project if you like.
Your log.config must have [Zone] and [Bob] console printing enabled. See examples/log.config or copy it to ~/Library/Preferences/Blizzard/Hearthstone/log.config

Decks
-----
You'll need to create deck files yourself for now. Just a simple text file with the (case sensitive) card names.
See a couple of samples in the examples/ directory. Cards with multiples must be entered multiple times.
Card order is not important.

Usage
-----
Simply copy HS-DeckTrack, make it executable (`chmod +x /path/to/HS-DeckTrack`) and run it in a Terminal window. Basic help will be printed to get you going.
Screen will refresh every 2 seconds showing the curent state of your latest game.
As soon as a game ends, the game state will reset to a new full deck.

Example
-------
    Bru7us:HS-DeckTrack bru7us$ ./HS-DeckTrack -d examples/zoo.deck 
    
    Cards in Deck:
    
    Shieldbearer             2
    Harvest Golem            2
    Voidwalker               2
    Shattered Sun Cleric     2
    Soulfire                 2
    Abusive Sergeant         2
    Defender of Argus        2
    Doomguard                2
    Scarlet Crusader         2
    Dark Iron Dwarf          2
    Flame Imp                2
    Dire Wolf Alpha          2
    Mortal Coil              2
    Argent Squire            2
    Knife Juggler            2
    
    
    
    Cards Played:


TODO
----
* Add Mana cost of all cards
* Sort/Display by mana cost
* Optional: Display cards in hand (but why? we can see them already)
* Allow user to define refresh/sleep period


If you'd like to donate:
  .. image:: https://www.paypal.com/en_US/i/btn/btn_donate_LG.gif
    :target: https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=W3UX3VM22WRQY&item_name=HS-DeckTrack
