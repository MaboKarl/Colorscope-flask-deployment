# ColorScope

ColorScope is a Flask web application that identifies the approximate color of a pixel at the center of a webcam frame or uploaded image. It is designed as a practical example of image processing, browser camera access, authentication, and OpenCV-based color analysis.

## Features

- Live webcam color detection
- Image upload and color analysis
- HSV sampling from the center region of an image
- Human-readable color names and lightness labels
- HSV, RGB, and hexadecimal color values
- Copy-ready detected color values
- User registration and login
- SQLite-backed user accounts
- Dark and light interface modes

## Tech Stack

- Python
- Flask
- OpenCV
- NumPy
- SQLite
- HTML, CSS, and JavaScript
- Gunicorn

## How It Works

ColorScope captures the center of a webcam frame or decodes an uploaded image, converts it to HSV color space, and averages a small region around the center. The resulting hue, saturation, and value are converted into:

- A descriptive color name
- HSV values
- RGB values
- A hexadecimal color code

## Getting Started

### Prerequisites

- Python 3.9 or newer
- A browser with webcam access
- Camera permission enabled for the local site

### Installation

Clone the repository and enter its directory:

```bash
git clone https://github.com/MaboKarl/Colorscope-flask-deployment.git
cd Colorscope-flask-deployment
```

Create and activate a virtual environment:

```bash
python -m venv .venv
```

On Windows:

```powershell
.venv\Scripts\Activate.ps1
```

On macOS or Linux:

```bash
source .venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

### Run the Application

```bash
python app.py
```

Open `http://localhost:5000` in a browser.

Register an account, sign in, and choose either **Webcam** or **Upload**.

## Supported Upload Formats

- PNG
- JPG and JPEG
- BMP
- WebP

## Project Structure

```text
Colorscope-flask-deployment/
├── app.py
├── requirements.txt
├── users.db
└── templates/
    ├── index.html
    ├── login.html
    ├── login_success.html
    ├── register.html
    ├── upload.html
    └── webcam.html
```

## Notes

- Webcam detection requires browser camera permission.
- `users.db` stores registered account credentials, with passwords hashed using Werkzeug.
- Set `PORT` in the environment to change the server port.
- Replace the development secret key and authentication setup before deploying publicly.

## Authors

- Karl Mago
- Adrian Liao
- Genesis Navarro
- Lar Ry
