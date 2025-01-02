Installed with "pip install " function
Library used for test automation and web page navigation testing (including integration testing). Can be used for web scrapping in pair with [[BeautifulSoup]] or standalone.

02-Jan-2025 issue: there is an old version on setting up the driver to be available from code:

from selenium import webdriver 
-Set the path to the Chromedriver 
DRIVER_PATH = '/path/to/chromedriver' 
-Initialize the Chrome driver driver = webdriver.Chrome(executable_path=DRIVER_PATH)

From certain version the setup process is the following:

from selenium import webdriver
from selenium.webdriver.chrome.service import Service

DRIVER_PATH = 'Path_to_driver/chromedriver.exe'
service = Service(DRIVER_PATH)
driver = webdriver.Chrome(service=service)

To set up the headless mode for Selenium (run all commands during testing/web scrapping without opening actual window):
options = Options()
options.headless = True  # Enable headless mode
options.add_argument("--window-size=1920,1080")
driver = webdriver.Chrome(options=options, executable_path=DRIVER_PATH)