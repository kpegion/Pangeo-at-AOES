Setting up Jupyter on COLA Servers
####################################

1. Setup a Password for Jupyter

.. code-block:: bash

   jupyter notebook --generate-config
   jupyter notebook password

2. Issue the following command so that your environment will appear in Jupyter

.. code-block:: bash

   python -m ipykernel install --user --name aoes --display-name "Python (aoes)"

3. Log in to colaX.gmu.edu, where X refers to a COLA Server

.. code-block:: bash

   ssh -Y -l <YOURUSERNAME>@colaX.gmu.edu

4. Go to the Pangeo-at-AOES directory:

.. code-block:: bash
   
   cd Pangeo-at-AOES

5. Start up the Jupyter server with the following command:

.. code-block:: bash

   jupyter lab --no-browser --ip=`hostname` --port=8878

6. In a separate terminal, log in to colaX again with the following command:

.. code-block:: bash

   ssh -N -L 8878:colaX.gmu.edu:8878 <YOURUSERNAME>@colaX.gmu.edu

.. warning::  You must use the same COLA server in this step as you did in step 3.  If you do not, then you get an invalid credentials error when you attempt to login to Jupyter.

7. Open your browser and go to http://localhost:8878. It will ask you to enter the password you created in step 1.

8. Your Jupyter server should appear in your local browser.

9. In the upper right corner, you will see your current environemnt is `Python (aoes)`.  If it only says `Python`, click on `Python` and a menu will appear. Select `Python (aoes)`

Troubleshooting
################

.. warning::

   Traceback (most recent call last):
  File "/homes/sknapp4/.conda/envs/aoes/lib/python3.6/site-packages/traitlets/traitlets.py", line 528, in get
    value = obj._trait_values[self.name]
KeyError: 'allow_remote_access'

   Try launching Jupyter with the following commane

   ```jupyter lab --no-browser --ip=`hostname` --port=8878```

.. warning:: Invalid Credentials

.. note::

   Check the messages on the screen where you launched `jupyter lab `
   Sometimes port 8878 is in use and it will find a different port.  The error messages will tell you which port you should use.

