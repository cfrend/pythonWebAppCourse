# Pricing Service

Version by: Chauncey Frend.

This is an application built to allow the periodic scanning of online webstores, to notify users of changes in prices of items they select.

This application is part of the course The Complete Python Web Developer, a course aimed at beginners, to teach the creation of web applications using Python. If that sounds interesting, check it out httpswww.udemy.comthe-complete-python-web-course-learn-by-building-8-apps

It allows administrators (defined via `srcconfig.py`) to add, remove, and edit online stores.

You will need a Mailgun account and API details for the e-mailing to work.
E-mails are sent via executing the `srcalert_updater.py` file. In order to check e.g. every 10 minutes, the file must be executed every 10 minutes. This can be done with a cron job or a Windows service.

It parses the store websites using `requests` and `BeautifulSoup`.

It does not work with Stores that dynamically inject content using JavaScript.

It allows users to register, log in, and create and modify their alerts.

Technology stack MongoDB, Python (Flask & Jinja2), HTMLCSSBootstrap, Mailgun.

## Installation

1. Clone the repository (going to a terminal and run `git clone git@github.comschoolofcode-meprice-of-chair.git`.
2. Define your administrator e-mail in `srcconfig.py`.
3. Define your Mailgun API details on `srcmodelsalertsconstants.py`.
4. Create a virtual environment for the repository (run `virtualenv --python=python3.5 venv`)
5. Run the Flask server by executing `venvbinpython price-of-chairsrcrun.py`.
6. Whenever you want to check prices of items (caution can take a long time if you have a lot of items!), run `venvbinpython price-of-charsrcalert_updater.py`.
