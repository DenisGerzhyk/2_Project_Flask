# 2_Project_Flask

This code sets up a basic Flask application with SQLAlchemy integration for a simple blogging platform. It defines a class called Article that represents a blog post, with columns for the id, title, intro, text, and date of each post. It also defines several routes that handle various operations on the blog posts.

The app variable is created using the Flask class from the flask module, and the SQLAlchemy class is used to create a database for storing blog posts. The database is stored in a local SQLite file called blog.db.

The Article class is defined as a subclass of db.Model, which is the base class for all models in SQLAlchemy. It has several attributes representing the columns of the table that will be created in the database.

The __repr__ method is defined to return a string representation of the Article object when it is printed, which will be helpful for debugging.

Several routes are defined using the @app.route decorator. The index route returns a template called index.html. The about route returns a template called about.html. The posts route queries the database for all blog posts and returns a template called posts.html with the results. The post_detail route queries the database for a specific blog post and returns a template called post_detail.html with the results. The post_delete route deletes a specific blog post from the database and returns the user to the posts page. The post_update route updates a specific blog post in the database and returns the user to the posts page. The create_article route allows the user to create a new blog post and stores it in the database.

Each route returns a rendered template using the render_template function from the flask module. The templates are located in the templates directory.

The if __name__ == '__main__': block runs the Flask application if the script is executed directly. The debug=True option enables debug mode for the application, which allows for more detailed error messages during development.
