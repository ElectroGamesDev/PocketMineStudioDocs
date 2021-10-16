Methods
========

This is the offical API for PocektMineStudio!

.. note::

    PocketMine Studio is NOT case sensitive

$player
--------

.. note::

    You can use both $player and $p to get the player

Usage: Gets the player who ran an event

Example:

.. code-block:: sh

  PlayerJoinEvent{
      $player->sendMessage("Welcome!");
      $p->sendMessage("Welcome!");
  }
  
sendMessage
----------

Usage: This method is used to send a player a message

.. note::

    $player = the player you are sending the message to. You can use sm, sendmessage, and message to send messages

Example:

.. code-block:: sh

  PlayerJoinEvent{
      $player->sendMessage("Welcome!");
      $player->sm("Welcome!");
      $player->message("Welcome!");
  }

clearInventory
----------

Usage: This method is used to clear a players inventory

$sender = The player who sends the command

Example:

.. code-block:: sh

  function CommandEvent{
      command "clear":
              $sender->clearInventory(true);
  }

$killer
-------

.. note::

    $killer can only be used in a PlayerDeathEvent function

Usage: Gets the player who killed a player

Example:

.. code-block:: sh

  PlayerDeathEvent{
      $killer->sendMessage("You killed " . $victim->getName() . "!");
  }
  
$victim
-------

.. note::

    $victim can only be used in a PlayerDeathEvent function

Usage: Gets the player who was killed

Example:

.. code-block:: sh

  PlayerDeathEvent{
      $victim->sendMessage("$killer->getName() . " killed you!");
  }

