# **Flask Blog Application**

This is a simple blog application built using Flask, SQLAlchemy, and Flask-Login. It allows users to create, update, and delete blog posts. Users can also register, log in, and log out.

## Features

- User authentication (login, logout)
- Create, read, update, and delete blog posts
- User-specific content display
- Flash messages for feedback

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/Halip26/blog-app-using-flask.git
    cd blog-app-using-flask
    ```

2. Create a virtual environment and activate it:

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. Install the dependencies:

    ```bash
    pip install -r requirements.txt
    ```

4. Set up the database:

    ```bash
    flask db init
    flask db migrate -m "Initial migration."
    flask db upgrade
    ```

## Configuration

- `SQLALCHEMY_DATABASE_URI`: The database URI that should be used for the connection.
- `SQLALCHEMY_TRACK_MODIFICATIONS`: Whether to track modifications of objects and emit signals.
- `SECRET_KEY`: A secret key for the session management.

## Usage

1. Run the application:

    ```bash
    flask run
    ```

2. Open your web browser and go to `http://127.0.0.1:5000/`.

## Routes

- `/`: Home page displaying all blog posts.
- `/about`: About page.
- `/addpost`: Page to add a new blog post.
- `/update/<int:id>`: Page to update an existing blog post.
- `/delete/<int:id>`: Route to delete a blog post.
- `/login`: Login page.

## Models

- `Halip_Blog`: Model for blog posts.
  - `id`: Primary key.
  - `title`: Title of the blog post.
  - `author`: Author of the blog post.
  - `post_date`: Date and time of the blog post.
  - `content`: Content of the blog post.

- `User`: Model for users.
  - `id`: Primary key.
  - `username`: Username of the user.
  - `password`: Password of the user (hashed).

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
