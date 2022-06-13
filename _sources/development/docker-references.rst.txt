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

    # remove all dangling docker artifacts
    docker system prune -a

    # remove dangling volumes
    docker volume prune

Remove All Exited Containers
****************************

.. code-block:: bash
    :linenos:

    docker rm $(docker ps -a -f status=exited -q)

Stop and Remove All Containers
******************************

.. code-block:: bash
    :linenos:

    docker stop $(docker ps -a -q)
    docker rm $(docker ps -a -q)

Remove All Docker Images
************************

.. code-block:: bash
    :linenos:
    
    docker rmi $(docker images -a -q)