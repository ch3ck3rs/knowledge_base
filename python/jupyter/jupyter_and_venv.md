# When working with Jupyter, Virtualenv and on linux (maybe mac???)

First off... ensure you are using Python 3.  In linux, the terminal `python`
defaults to python 2, which is often used in the os kernel.  Same goes for `pip`.
Check this by doing `which python` in your terminal add see where it takes you.

### USE `python3` and `pip3` when working with Jupyter

[This guide will work if you use `pip3` and `python3`](https://janakiev.com/blog/jupyter-virtual-envs/)

Once you launch Jupyter, check to make sure you are using the correct kernel.

    import sys
    sys.path
    sys.executable

The `sys.executable` should show something like `path-to-venv/bin/python` my venv named 'NIU' looks like this `/home/lauren/PycharmProjects/NIU/bin/python3`

If you are still seeing the base kernel `/usr/bin/python3` then you should modify your `kernel.json` for the venv.
[This thread was pretty helpful](https://github.com/jupyter/notebook/issues/2359)

In short you will need to do the following:
- in the terminal, activate your venv
- run `which python`
- copy the path that is returned
- locate the venv ipykernel (likely in `/usr/local/share/jupyter/kernels/`)
- change the "argv" path the path displayed by `which python`


    {
     "display_name": "NIU",
     "language": "python",
     "argv": [
      "/home/lauren/PycharmProjects/NIU/bin/python3",
      "-m",
      "ipykernel_launcher",
      "-f",
      "{connection_file}"
     ]
    }


### If you are on Windows...

If you use Anaconda base kernel for your venv you should be good to go.

If you use the Python Foundation kernel for your venv you will need to ensure that you


	# in main kernel and venv
	pip install prompt_toolkit==2.*

as version 3.* is not compatible with Jupyter as of 2/16/2020.
