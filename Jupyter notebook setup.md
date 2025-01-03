One way to set Jupyter notebook is to do that as a part of Anaconda (Python versioning system) setup.
To setup the Jupyter notebook following steps standalone should be taken:
- Install Python
- Perform following from PowerShell (https://www.geeksforgeeks.org/install-jupyter-notebook-in-windows/):
	- Find Python installation directory (sample case  C:\Users\UserNam\AppData\Local\Programs\Python\Python312)
	- run python (or py) -m pip install --upgrade pip
	- run python (or py) -m pip install jupyter
		- for some cases (if the terminal is opened within Python installation/root directory commands (presented as .exe files) must be run prefixed with ".\" symbols)
	- locate Jupyter related folder in Scripts folder
	- jupyter notebook --generate-config
	- open the "jupyter_notebook_config.py" file
	- Uncomment "c.ServerApp.root_dir" property and set it equal to desired default directory, where projects, working files and folders will be stored.
	- Save changes and close the file
	- Run the Jupyter from PowerShell (with relative or absolute path) by typing "jupyter notebook" (or with absolute path ex. " C:\Users\UserName\AppData\Local\Programs\Python\Python312\Scripts\jupyter notebook")
	- Error may appear in browser. Should be disregarded
	- Default address to access web ui:http://localhost:8888/ or http://127.0.0.1:8888
- On first launch a password will need to be created for running it on public domain (https://jupyter-server.readthedocs.io/en/latest/operators/public-server.html):
	- run "jupyter server password" or the same with absolute path
	- set the password
	- restart Jupiter service by pressing Ctrl+C 2 times and running it again.
After those steps UI should show contents of the selected default directory and activities should be reflected there as well.

Tools required for web scrapping:
- [[BeautifulSoup]]
- [[Selenium]]
- [[Chrome Web Driver]]

Additional:
- https://saturncloud.io/blog/how-to-change-jupyter-notebook-default-folder/#:~:text=By%20default%2C%20Jupyter%20Notebook%20creates,convenient%20location%20for%20your%20work.

