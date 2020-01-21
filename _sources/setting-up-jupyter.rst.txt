Setting up Jupyter on COLA Servers
####################################

1. Follow the steps in `Configure Jupyter http://pangeo.io/setup_guides/hpc.html#configure-jupyter_` The main point of this step is to create a password for when you log in to the Jupyter server you will start up on COLA.

2. Log in to colaX.gmu.edu, where X refers to a COLA Server

3. Start up the jupyter server with the following command:

.. code-block:: bash

   jupyter lab --no-browser --ip=`hostname` --port=8877

4. In a separate terminal, log in to colaX again with the following command:

.. code-block:: bash

   ssh -N -L 8877:colaX.gmu.edu:8877 -L 8878:colaX.gmu.edu:8878 <your user name>@colaS.gmu.edu

5. Open your browser and go to http://localhost:8877. It will ask you to enter the password you created in step 1.

6. Your Jupyter server should appear in your local browser.

