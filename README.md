# Schrodinger Notebooks

This repo contains a collection of notebooks discussing solutions to different forms of the [Schrödinger Equation](https://en.wikipedia.org/wiki/Schrödinger_equation) for different quantum mechanical systems.

These notebooks discuss both analytic and numerical techniques for solving such equations, and contain code to graph these solutions as well.
Within these code snippets, you can change parameters like particle mass, energy level, etc. to see how these changes affect solutions.

## Using These Notebooks

If you aren't familiar with Jupyter notebooks, the easiest way to use the ones in this repo is via [GitHub Codespaces](https://github.com/features/codespaces).
To get started, find this repo on GitHub (if you aren't there already) and click the green button labeled "<> Code" in the upper right area of the page.
Click the "Codespaces" tab, and then click the "+". (or click your existing Codespace in the list below the "+", if you've already created one for this repo.)
Doing so will open a new tab in your browser containing an instance of [VSCode](https://code.visualstudio.com) which is connected to a machine in the cloud.
This way, you can play with these notebooks on your desktop/laptop machine or tablet without going through the hassle of installing software on your own computer.

An important note: once you're finished using these notebooks, navigate back to this repo on GitHub, click "<> Code" again, select the "Codespaces" tab, find the Codespace you created in the list that appears, click the three dots to the right of it, and select either "Stop Codespace" or "Delete".
If you don't, your Codespace will continue to run even after you close its tab, and you will quickly burn through the hours of Codespace usage you are allowed each month with a free GitHub account.
If you click "Stop Codespace", you won't use any more Codespaces hours, but you will use some of your storage since your work is saved so you can come back to it later.
(Free GitHub accounts only have 15GB of this storage.)
You can free up this space by selecting "Delete", although you will lose any changes you have made.

Note for more experienced users: you can obviously open these notebooks in whatever editor you prefer, but (IMHO) the Codespaces approach described above is second in convenience only to Colab, which has far worse variable explorer/debugging functionalities than VSCode.
So, Codespaces is what I recommend for beginners.

Regardless of what editor you use, you'll need to do a few things before you can run the code in these notebooks. (If you're only interested in viewing their contents and **not** running any of the  code, you don't need to follow any of these steps.)

1. Clone this repository, and navigate to it in your command line. (Codespaces users, this is already done for you, so you can skip this step.)

2. Ensure Python 3.8 or newer is installed. (Codespaces users, this is also already done for you, so you can skip this step as well.)

3. Create a new virtual environment within a new hidden directory named `.venv`.
(A [virtual environment](https://docs.python.org/3/library/venv.html) is, put simply, a Python installation isolated from the rest of your machine, so you can play around without fear of breaking something important.)
Do this using the command:
```
python3 -m venv .venv
```

4. Enter into the virtual environment.
Once you do this, you should see `(.venv)` appear before the prompt in your command line.
Its important that you don't skip this step, because otherwise packages will be installed globally, which is most likely not what you want.
Enter into the virtual environment using the command:
```
source ./.venv/bin/activate
```

5. Install all necessary packages listed in the `requirements.txt` file.
(The code in this notebook depends on a **lot** of other code written by other people, who have kindly put their code together into packages and made it available online for the rest of us.)
Do this using the command:
```
pip install -r ./requirements.txt
```

6. If you're using Codespaces/VSCode, you'll need to install the [Python extension](https://marketplace.visualstudio.com/items?itemName=ms-python.python) and the [Juptyter extension](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter) which you can do from the Extensions menu in the menu bar on the left side of the window.
Then, open the file explorer (also in the menu bar on the left side of the screen) and click on a notebook to open it.
Once its open, click "Select Kernel" in the upper right corner.
In the menu that appears, select "Python Environments..." and then select ".venv" (or whatever you named the file containing your virtual environment in Step 4.)
Then, to execute a cell, click the triangle next to the upper left corner of the cell.

The environment is now set up, and you're ready to use these notebooks.