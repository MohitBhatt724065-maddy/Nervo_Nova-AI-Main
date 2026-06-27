(1) Date: 2083/03/12
- Created the project folder architecture and set up the virtual environment.

(2) Date: 2083/03/13
- Opened `src/config/settings.py`.
- Defined the initial configuration constants: `APP_NAME`, `APP_VERSION`, `IMAGE_SIZE`, and `CLASS_NAMES`.
- Opened `src/utils.logger.py`
-Firstly before writing any of the code i first understood the concept . In many of the ML applications, when a user uploads a MRI scan, the system does many things internally:-
                            `(1) Loads the model`
                            `(2) Preprocess the images.`
                            `(3) Runs the inferences.`
                            `(4) Generates a report.`
- So, Without a logging system, if something silently fails duriing any of these steps, then there is absolutely no way to know where,when or why it broke.
-So, I understand about a logger:- A logger is a essential diary that records everything happening inside the application with the timestamps and severity level giving full visibility into the systems behavior at all the time and keeps updated.
- Then I configured the project logger using Python’s logging module as:-
                                     `import logging
                                   `logging.basicConfig(`
                                       `level=logging.DEBUG,`
                                       `format="%(asctime)s %(levelname)s %(messages)s",`
                                   `)`
                                   `logger = logging.getLogger("NervoNova")`
-