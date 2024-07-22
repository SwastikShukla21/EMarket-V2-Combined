## Features

- **Asynchronous Task Execution**: Uses Celery and Redis to handle background tasks efficiently.
- **Email Reports**: Sends summary reports via email.
- **CSV Report Generation**: Dynamically creates CSV files for generating reports.
### Starting the backend

### Note: Open all in seperate terminals

1. Create a virtual enviroment
   python3 -m venv venv
2. Activate the virtual enviroment
   venv\Scripts\activate
3. Install the requirements
   pip install -r requirements.txt
4. Start the backend
   python app.py
5. In wsl start redis server
   sudo serivce redis-server start
6. In wsl start celery worker
   celery -A tasks worker --loglevel=info -P eventlet
7. In wsl start celery beat
   celery -A tasks beat --loglevel=info
8. To deactivate virtual enviroment
   deactivate
