<h1 align="center"> Visit Counter </h1>

This service generates a dynamic visitor count badge for your GitHub repository. It tracks unique visitors and displays a weekly visualization of visitor traffic.
This project was inspired by the blt project https://blt.owasp.org

[![Visitor Badge](https://visit-counter-y3x4.onrender.com//badge/visit-counter)](https://visit-counter-y3x4.onrender.com//badge/visit-counter)

## Features

* Tracks unique visitors using IP addresses
* Shows last 7 days of visitor statistics
* Displays total visitor count
* Updates in real-time
* Clean, minimal design

## Usage

Add this badge to your repository by inserting the following line in your README.md:

Note: Replace:

your-render-app-name with your actual Render service name
your-repo-name with your repository name

## Deployment Instructions

# 1. Fork the Repository
* Clone this repository to your GitHub account by clicking the Fork button.
  
# 2. Deploy to Render
* Sign up for a free account at render.com
* Create a new Web Service
* Connect your GitHub repository
* Configure the following settings:
           * Build Command: pip install -r requirements.txt
           * Start Command: gunicorn app:app
           * Environment Variable:

  * Key: PYTHON_VERSION
  *  Value: 3.12.0


# 3. Post-Deployment Steps

* Note your Render service URL
* Update the badge URL in your README.md
* Wait a few minutes for the service to fully deploy

# 4. Verification
Verify the badge appears correctly in your repository's README.
Local Development
To run the service locally:
# Clone the repository
    git clone https://github.com/yourusername/visitor-badge-service
    cd visitor-badge-service

    # Create virtual environment
    python -m venv venv

    # Activate virtual environment
    # On Unix/macOS:
    source venv/bin/activate
    # On Windows:
    venv\Scripts\activate

    # Install dependencies
    pip install -r requirements.txt

    # Run the application
    python app.py


## Technical Details

* Badge updates occur on each README view
* Visitor counting mechanism:

  * Based on unique IP addresses
  * Data stored in SQLite database

* Visualization features:

  * Displays last 7 days of traffic
  * Week boundaries marked with vertical lines
  * Proper handling of month transitions



## License
This project is licensed under the MIT License - see the LICENSE file for details.


