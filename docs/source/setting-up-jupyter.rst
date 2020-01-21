Setting up Jupyter on COLA Servers
####################################

1. Follow the steps in `Configure Jupyter <http://pangeo.io/setup_guides/hpc.html#configure-jupyter>`_. The main point of this step is to create a password for when you log in to the Jupyter server you will start up on COLA.

2. Log in to colaX.gmu.edu, where X refers to a COLA Server

.. code-block:: bash

   ssh -Y -l <YOURUSERNAME>@colaX.gmu.edu

3. Go to the Pangeo-at-AOES directory:

.. code-block:: bash
   
   cd Pangeo-at-AOES

4. Start up the Jupyter server with the following command:

.. code-block:: bash

   jupyter lab --no-browser --ip=`hostname` --port=8878

5. In a separate terminal, log in to colaX again with the following command:

.. code-block:: bash

   ssh -N -L 8878:colaX.gmu.edu:8878 <YOURUSERNAME>@colaX.gmu.edu

6. Open your browser and go to http://localhost:8878. It will ask you to enter the password you created in step 1.

7. Your Jupyter server should appear in your local browser.

8. In the upper right corner, you will see your current environemnt is `Python (aoes)`

