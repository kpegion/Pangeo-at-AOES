Setting up Jupyter on COLA Servers
####################################

1. Follow the steps in `Configure Jupyter http://pangeo.io/setup_guides/hpc.html#configure-jupyter_` The main point of this step is to create a password for when you log in to the Jupyter server you will start up on COLA.

2.  Setup Jupyter Notebook to find the aoes environment you created:
    
.. code-block:: bash
    python -m ipykernel install --user --name aoes --display-name "Python (aoes)"

2. Log in to colaX.gmu.edu, where X refers to a COLA Server

3. Start up the jupyter server with the following command:

.. code-block:: bash

   jupyter lab --no-browser --ip=`hostname` --port=8878

4. In a separate terminal, log in to colaX again with the following command:

.. code-block:: bash

   ssh -N -L 8878:colaX.gmu.edu:8878 <YOURUSERNAME>@colaX.gmu.edu


5. Open your browser and go to http://localhost:8878. It will ask you to enter the password you created in step 1.

6. Your Jupyter server should appear in your local browser.

7.  In the upper right corner, you will see your current environemnt is `Python (aoes)`

