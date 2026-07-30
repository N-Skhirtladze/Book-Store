# API Endpoints

## Authentication

- POST /api/auth/register
Receive name, last name, email, password, password confirmation and add new user in the database.
Returns user profile and JWT access token.

- POST /api/auth/login
Receive email and password.
Returns user profile and JWT access token.

## Books

- GET    /api/books
Returns a paginated list of books.
Supports searching, filtering and sorting.

- GET    /api/books/:bookId
Returns the details of a specific book.

- POST   /api/books
Receives the book title, description, published year, author, price, stock, and cover image. Creates a new book.  
Returns the newly created book.

- PATCH  /api/books/:bookId
Updates the information of a specific book.  
Returns the updated book.

- DELETE /api/books/:bookId
Deletes a specific book from the database.

## Favorites

- GET    /api/favorites
Returns the authenticated user's favorite books.

- POST   /api/favorites/:bookId
Adds the specified book to the authenticated user's favorites.

- DELETE /api/favorites/:bookId
Removes the specified book from the authenticated user's favorites.

## Ratings

- POST   /api/books/rating/:bookId
Creates the authenticated user's rating for the specified book.

- DELETE /api/books/rating/:bookId
Removes the authenticated user's rating for the specified book.

## Genre

- GET /api/genres
Returns all available genres

## Review

- GET /api/review/:bookId
Returns all reviews for the specified book.

- POST /api/review/:bookId
Creates a new review for the specified book.

- DELETE /api/review/:bookId/:reviewId
Deletes a specific review.
