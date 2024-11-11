# DeedHub

Designed and developed Deed Hub, a comprehensive land registration
website featuring streamlined procedures, and detailed document
requirements, and integrated a user-friendly platform for advertising land.

Tech stack used:HTML, CSS, Javascript ,Bootstrap ,Flask ,Mysq


This web application allows users to manage property listings with details such as location, description, contact information, and images. It also includes features for user signup, login, viewing area-based property prices, and deleting listings. Built using Flask, MySQL, and Flask-Mail, this application enables secure user authentication and a simple interface for managing property data.

## Features

- **User Signup and Login**: Users can sign up and log in securely, with hashed passwords stored in the database.
- **Upload Property Data**: Users can upload property details including name, contact, dimensions, description, location, district, and an image.
- **Display and Search Listings**: Users can view all property listings or filter listings by a specific seller.
- **Delete Listings**: Admin or authorized users can delete specific property listings.
- **Area Price Display**: Provides a list of property prices across different areas and taluks.

## Installation

1. **Clone the Repository**
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. **Install Dependencies**
   Ensure you have Python installed, then install required packages:
   ```bash
   pip install -r requirements.txt
   ```

3. **Database Setup**
   - Create a MySQL database with the name `site_details`.
   - In the database, create a table `seller_information` to store user and property details.
   - Update the `db_config` dictionary in the code with your MySQL connection details.

4. **Run the Application**
   Start the Flask server:
   ```bash
   python app.py
   ```
   The application will be accessible at `http://127.0.0.1:5000`.

## Usage

1. **Home Page**: The main page provides access to sign-up and sign-in options.
2. **Signup**: Users can create an account by entering a username and password.
3. **Signin**: Existing users can log in using their username and password.
4. **Upload Property Data**: After logging in, users can add property details through a form.
5. **View Listings**: Users can view all properties or filter by specific sellers.
6. **Delete Listings**: Authorized users can delete listings using the `delete_row` endpoint.
7. **Area Prices**: View a list of typical property prices across different regions.

## Application Routes

- `/`: Home page with navigation options.
- `/index`: Redirects to the signup page.
- `/signin`: Login page.
- `/upload/<username>`: Endpoint to upload property data (requires POST).
- `/get_user_data/<username>`: Retrieves data for a specific user.
- `/display_data`: Displays all property listings.
- `/signup`: Endpoint for signing up (requires POST).
- `/signin`: Endpoint for signing in (requires POST).
- `/delete_row/<int:id>`: Deletes a specific listing by ID (requires POST).
- `/area_display`: Displays area-wise property prices.

## Security and Data Handling

- **Password Hashing**: Passwords are hashed using bcrypt before being stored in the database.
- **Image Uploading**: Images are stored as binary data in the database.
- **Data Validation**: Ensures that user input is properly sanitized and verified.

## Area Price Data

The `/area_display` route displays a list of typical property prices for different neighborhoods and taluks, providing users with an idea of local real estate market trends.

