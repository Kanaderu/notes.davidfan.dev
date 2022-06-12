Docker References
=================


.. toctree::
    :maxdepth: 2
    :caption: Contents:


-------------------------------------

Debugging
#########

Shell Into Running Docker Container
***********************************

Shell into a running container by using `exec` and enabling interactive (`-i`) and tty (`-t`). This can be used to run any commands though running a shell is the most useful for debugging.

.. code-block:: bash
    :linenos:

    # syntax
    docker exec -it <docker_container> <command>
    
    # example
    docker exec –it nginx /bin/bash


Cleanup
#######

Purge All Unused or Dangling Images, Containers, Volumes, and Networks
**********************************************************************

.. code-block:: bash
    :linenos:

    # syntax
    docker system prune -a
