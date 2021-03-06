Konsole Kommander
=================

Konsole Kommander est une application en ligne de commande pour piloter 
Phraseanet. Elle s'execute simplement : 

  .. code-block:: bash

    php bin/console

Vous aurez à votre écran une liste de commande de la sorte :

  .. code-block:: bash

    Available commands:
      help                       Displays help for a command
      list                       Lists commands
    about
      about:authors              List authors and contributors
      about:license              This program license
    scheduler
      scheduler:start            Start the scheduler
      scheduler:state            Get scheduler state
      scheduler:stop             Stop the scheduler
    system
      system:backupDB            Backup Phraseanet Databases
      system:clearCache          Empty cache directories, clear Memcached, Redis if avalaible
      system:configCheck         Check the configuration
      system:templateGenerator   Generate template files
      system:upgrade             Upgrade Phraseanet to the lastest version
    task
      task:list                  List tasks
      task:run                   Run task

Les commandes disponible sont listées.

Pour obtenir de l'aide sur une commande : 

  .. code-block:: bash

    php bin/console help nomdecommande

  