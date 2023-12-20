The project is organized into the following directories and files:

models.py/: Contains SQLAlchemy model classes for Restaurant, Customer, and Review.
migrations/: Contains Alembic migration scripts for database schema changes.
seeds.py: A script for seeding the database with initial data.
tests/test_models.py: Unit tests for the models module using pytest.
Getting Started
Clone the Repository:

bash
Copy code
git clone https://github.com/22koki/restaurant-review-assignment.git
Setup Virtual Environment:

bash
Copy code
cd restaurant-review-assignment
python -m venv venv
source venv/bin/activate  # On Linux/Mac
# Or
.\venv\Scripts\activate  # On Windows
Install Dependencies:

bash
Copy code

Run Migrations:

bash
Copy code
alembic upgrade head
Seed Database:

bash
Copy code
python seeds.py
Run the Application:

bash
Copy code

Project Details
Object Relationship Methods
Review Class:

customer(): Returns the Customer instance for this review.
restaurant(): Returns the Restaurant instance for this review.
Restaurant Class:

reviews(): Returns a collection of all the reviews for the Restaurant.
customers(): Returns a collection of all the customers who reviewed the Restaurant.
Customer Class:

reviews(): Returns a collection of all the reviews that the Customer has left.
restaurants(): Returns a collection of all the restaurants that the Customer has reviewed.
Aggregate and Relationship Methods
Customer Class:

full_name(): Returns the full name of the customer, with the first name and last name concatenated, Western style.
favorite_restaurant(): Returns the restaurant instance that has the highest star rating from this customer.
add_review(restaurant, rating): Adds a new review for the given restaurant.
delete_reviews(restaurant): Removes all reviews for a specific restaurant.
Review Class:

full_review(): Returns a formatted string for a review.
Restaurant Class:

fanciest(): Returns one restaurant instance for the restaurant that has the highest price.
all_reviews(): Returns a list of strings with all the reviews for this restaurant.
Contributing
Feel free to contribute to this project by creating issues or submitting pull requests. Your feedback and contributions are welcome!







