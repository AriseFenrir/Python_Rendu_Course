# Python_Rendu_Course

## Day 2 - CRUD FastAPI

The Day 2 lab (CRUD API with FastAPI) is located in the `day2-lab/` directory.

### Setup & Run

```bash
cd day2-lab

# Create virtual environment with Python 3.14
# We explicitly use 3.14 because Python 3.15 is too recent and causes
# compatibility issues with some dependencies.
py -3.14 -m venv .venv

# Activate the virtual environment
source .venv/Scripts/activate

# Install dependencies
pip install -r requirements.txt

# Run the server
uvicorn main:app --reload --port 8000
```

### API Usage

Once the server is running, open the interactive docs at `http://localhost:8000/docs` and test:

1. **`POST /servers`** :

   ```json
   {"name": "api-prod-1", "host": "httpbin.org", "port": 443}
   ```
2. **`GET /servers`** — Verify server
3. **`POST /servers/1/check`** — Trigger a health check on a server
4. **`GET /servers?status=UP`** — Filter servers by status
5. **`DELETE /servers/2`** — Remove server

