# MLops text

### virtual enviroment
<pre>
python3 -m venv venv
source venv/bin/activate
python3 -m pip install pip setuptools wheel
python3 -m pip install -e .
<pre>

<pre>
uvicorn app.api:app --host 0.0.0.0 --port 8000 --reload --reload-dir tagify --reload-dir app  # dev
<pre>

<pre>
gunicorn -c app/gunicorn.py -k uvicorn.workers.UvicornWorker app.api:app  # prod
<pre>


