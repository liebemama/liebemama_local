# LiebeMama – B2B Product Management Platform

LiebeMama is a product management platform designed for wholesalers and restaurants, built with Python and Flask.

---

## 🚀 Getting Started

Follow these steps to install and run the project locally:

### 1. Clone the repository

```bash
git clone https://github.com/liebemama/liebemama.git
cd liebemama
```

### 2. Create a virtual environment

```bash
python3 -m venv venv
```

### 3. Activate the environment

- On Linux / macOS:
  ```bash
  source venv/bin/activate
  ```

- On Windows:
  ```bash
  venv\Scripts\activate
  ```

### 4. Install the requirements

```bash
pip install -r requirements.txt
```

### 5. Configure the `.env` file

Create a `.env` file in the root directory and add your environment variables:

```
DATABASE_URL=postgresql://postgres:12345@localhost:5432/liebemama
```

### 6. Initialize the database

Inside your Flask environment, run:

```myapp.py 
if __name__ == '__main__':
    env_mode = os.getenv('FLASK_ENV', 'development')
    debug_mode = os.getenv('FLASK_DEBUG', '1') == '1'
    port = int(os.getenv('FLASK_PORT', '1705'))

    with app.app_context():
        inspector = inspect(db.engine)
        db.create_all()
        create_super_admin_if_needed()

    app.run(debug=debug_mode, host='0.0.0.0', port=port)
```

### 7. Run the application

```bash
python -m myapp
```

> Replace `myapp` with the actual module or script name, such as `app.py`.

---

## 📂 Project Structure (example)

```
liebemama/
├── app.py
├── run.py
├── venv/
├── requirements.txt
├── .env
├── templates/
├── static/
├── models/
├── routes/
└── ...
```

---

## 🧑‍💻 Developer

Tamer – [github.com/TamerOnLine](https://github.com/TamerOnLine)

---

## ⚖️ License

This project is currently closed-source. For usage or collaboration inquiries, please contact the developer.