# Error Log


Made with love by Sam ☘

#### Matplotlib Errors


- If matplotlib(.pyplot) are giving any errors, here's a quick fix for that.  

1. Check the code to see if `plt`, has been used as a variable. plt is a callable module, NOT a random variable. 
2. Check the directory to see if there is plt.py module anywhere in your project. plt is a callable module, NOT a file nor should it be. 
3. Run the following commands, (feel free to copy paste, I'm not gonna check, what am I? A Cop?)
4. The print(plt) line will give you the `<class 'module'>`
5. Running `print(matpolotlib.__version__)` will get you the version of matplotlib. If its <= 3.5, you need to update it asap, as older stuff may be incompatible with python 3.10.5 (what this venv is running. `3.10.7` is the result of the version we're currently running. 
6. Sketch a basic figure to see if runs. 
7. IF ERROR: 
    1. Deactivate venv.
    2. Restart Kernel. 
    3. Reactivate venv
    4. Initially _run_ only the modules where `plt` is to be tested
8. IF graph prints, success!
```

#Code to Check if Matplotlib is working.

import os
print(os.listdir())
import matplotlib.pyplot as plt
print(plt)
print(type(plt))
import matplotlib
print(matplotlib.__version__)
plt.figure()
plt.plot([1,2,3],[4,5,6])
plt.show()

```