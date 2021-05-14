API
========

This is the offical API for PocektMineStudio!

$player
--------

.. note::

    Use $sender if you are using in a CommandEvent function

Usage: Gets the player who ran an event

Example:

.. code-block:: sh

  function PlayerJoinEvent{
      $player->sendMessage('Welcome!');
  }
   

$sender
------------

.. note::

    $sender can only be used in a CommandEvent function

Usage: Gets the player who ran a command

Example:

.. code-block:: sh

  function CommandEvent{
      $sender->sendMessage('You Died!');
  }

clearInventory
----------

Usage: This function is used to create commands.

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

Usage: Gets the player who killed the player

Example:

.. code-block:: sh

  function PlayerQuitEvent{
      $killer->sendMessage("You killed " . $player->getName() . "!");
  }
