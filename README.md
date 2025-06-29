# Pallavi
from flask import Flask, render_template_string

app = Flask(__name__)

# HTML content
html = """
<!DOCTYPE html>
<html>
<head>
    <title>My First Web Page</title>
    <style>
        body { font-family: Arial, sans-serif; background-color: #f2f2f2; padding: 20px; }
        h1 { color: #333366; }
        p { font-size: 18px; }
    </style>
</head>
<body>
    <h1>Welcome to My Web Page</h1>
    <p>This page is created using Python and Flask!</p>
</body>
</html>
"""

@app.route('/')
def home():
    return render_template_string(html)

if __name__ == '__main__':
    app.run(debug=True)

