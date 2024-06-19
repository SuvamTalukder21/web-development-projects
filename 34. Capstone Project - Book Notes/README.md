# Book Review Web Application
## Overview

This project is a web application that displays detailed information and reviews about books. It is built using Express.js, EJS for templating, and Bootstrap for styling. One of the key features of this application is the ability to switch between different languages for the entire page content.


## Features

- **Dynamic Book Information:** View detailed information about books including the title, author, publication year, description, and a personal review.
- **Efficient Data Handling:** The application efficiently fetches book details and reviews from a database, ensuring that the content is current and consistently presented.
- **Responsive Design:** Styled with Bootstrap to be fully responsive across different devices.
- **High-Quality Cover Images:** The application fetches and displays high-quality cover images for each book using the book's ISBN.


## Technologies Used

- **Backend:** Node.js, Express.js
- **Templating Engine:** EJS
- **Database:** PostgreSQL
- **Frontend:** HTML, CSS, Bootstrap
- **JavaScript:** Vanilla JavaScript for handling dynamic content updates
## Installation

Follow these steps to set up and run the Book Review Web Application locally on your machine.

### Prerequisites

Before you begin, ensure you have the following installed on your machine:

- **Node.js**: Download and install from [nodejs.org](https://nodejs.org/).
- **npm** (Node Package Manager): Installed automatically with Node.js.
- **PostgreSQL**: Download and install from [postgresql.org](https://www.postgresql.org/download/).

1. **Clone the repository:**

```bash
  https://github.com/SuvamTalukder21/web-development-projects/blob/main/34.%20Capstone%20Project%20-%20Book%20Notes.git
  cd 34. Capstone Project - Book Notes
```

2. **Install dependencies:**

```bash
  npm install
```

3. **Setup database:**

- Create a new database 
```SQL
CREATE DATABASE book_reviews;
```
- Create a table for books
```SQL
CREATE TABLE books (
    id SERIAL PRIMARY KEY,
    title VARCHAR(255) NOT NULL,
    author VARCHAR(255) NOT NULL,
    publication_year INTEGER,
    rating DECIMAL(3, 1),
    isbn VARCHAR(20) UNIQUE,
    description VARCHAR(500),
    review TEXT
);
```

4. **Start the server from terminal:**

- Install nodemon globally
```bash
npm install -g nodemon
```
- Run the following command to start the server
```bash
nodemon index.js
```
*It's hust a suggestion to start server with nodemon, otherwise you can start server with node also i.e.* `node index.js`

5. **Access the Application:**
Open your web browser and go to:
```bash
http://localhost:3000
```
## Usage

### Adding Books
- You can add books directly to your PostgreSQL database.
- Ensure each book entry includes all required fields: title, author, publication_year, description, review, and rating.
- Once you have the Book Review Web Application set up and running, follow these instructions to use its features.

### Navigating the Application

The application provides the following primary sections:

**Homepage**

   - View a list of recently added books.
   - Use the navigation menu to explore different sections.

**Inventory**

   - Browse all available books in the inventory.
   - Use the search bar to find specific books by title, author, or genre.

**Book Details**

   - Click on any book in the inventory to view its detailed information.
   - Each book detail page displays the book's title, author, publication year, description, and a my review.

### Detailed Features

1. **Viewing Book Information**

   - Click on a book title or image to view its detailed information, including a cover image, author, publication date, description, and my reviews.
   - Example URL: `http://localhost:3000/book?id=1`

2. **Adding a New Review**

   - To add a review, navigate to the “Add Review” section via the navigation menu.
   - Fill in the required details (book title, author, review text, etc.) and submit your review.
   - Example URL: `http://localhost:3000/add-review`

3. **Searching for Books**

   - Use the search functionality on the inventory page to find books by entering keywords related to the book's title, author, or genre.
   - The results will dynamically update to match your search criteria.

### Customizing the Application

2. **Styling**

   - Customize the appearance by editing the CSS files in the `public/styles` directory.
   - The application uses Bootstrap for styling, so you can easily adjust the layout and components by updating Bootstrap classes.

3. **Database Management**

   - Add or modify book records in your PostgreSQL database as needed.
   - Use database management tools or direct SQL queries to insert, update, or delete book entries.

### Example Workflows

1. **Viewing a Book Review**

   - Start the server.
   - Navigate to the inventory and select a book.
   - Read the detailed review provided for that book.

2. **Submitting a Review**

   - Start the server.
   - Go to the “Add Review” section.
   - Fill out the form with the book details and your review.
   - Submit the form to add your review to the inventory.

### Troubleshooting Common Issues

1. **Server Not Starting**

   - Check for any errors in the terminal where you ran `npm start`.
   - Ensure your database is running and accessible.
   - Verify that all environment variables in the `.env` file are correctly set.

2. **Database Connection Issues**

   - Confirm your PostgreSQL is running on port `5432`.
   - Ensure the PostgreSQL server is running and the database exists.

3. **Styling Issues**

   - Check if the Bootstrap and custom CSS files are correctly linked in your `header.ejs` or `footer.ejs` file.
   - Clear your browser cache or try accessing the application in an incognito window.

### Additional Resources

- [Bootstrap Documentation](https://getbootstrap.com/docs/5.3/getting-started/introduction/)
- [EJS Documentation](https://ejs.co/)
- [Node.js Documentation](https://nodejs.org/en/docs/)
- [PostgreSQL Documentation](https://www.postgresql.org/docs/)
## Contributing

We welcome contributions to the Book Review Web Application! Whether you want to report a bug, suggest new features, improve documentation, or contribute to the codebase, your input is valuable. Please follow the guidelines below to ensure a smooth and effective contribution process

If you would like to contribute to this project, please follow these steps:

* Fork the repository.
* Create a new branch.
* Make your changes and commit them.
* Push your changes to your forked repository.
* Create a pull request.

Certainly! Here's a detailed "Contributing" section for your `README.md` file to guide users on how they can contribute to your Book Review Web Application:

### How to Contribute

 **Fork the Repository**

   Start by forking the repository to your GitHub account:

   - Go to the repository on GitHub.
   - Click the "Fork" button at the top right of the page.

3. **Create a New Branch**

   Create a new branch for your feature or bug fix:

   ```bash
   git checkout -b feature/your-feature-name
   ```

   Choose a descriptive name for your branch, such as `feature/add-search-functionality` or `bugfix/fix-review-display`.

**Make Your Changes**

   - Make the necessary changes or additions to the codebase.
   - Ensure your code follows the project's coding standards and conventions.
   - Update or add tests to cover your changes, if applicable.
   - Document your changes in the `README.md` or appropriate documentation files.

**Commit Your Changes**

   Commit your changes with a descriptive message:

   ```bash
   git add .
   git commit -m "Add detailed description of your changes"
   ```

**Push to Your Fork**

   Push your changes to your forked repository:

   ```bash
   git push origin feature/your-feature-name
   ```

**Open a Pull Request**

   Open a pull request from your branch to the `main` branch of the original repository:

   - Go to the original repository on GitHub.
   - Click on the "Pull Requests" tab.
   - Click the "New Pull Request" button.
   - Select your branch from the list.
   - Provide a clear and detailed description of your changes in the pull request.

### Code of Conduct

To maintain a welcoming and inclusive community, we expect all contributors to adhere to the [Contributor Covenant Code of Conduct](CODE_OF_CONDUCT.md).

### Reporting Issues

If you encounter any bugs or have suggestions for new features, please open an issue on GitHub:

1. Go to the repository's "Issues" tab.
2. Click the "New Issue" button.
3. Provide a clear and detailed description of the issue or suggestion.
4. Include any relevant screenshots or logs to help us understand the problem.

### Style Guide

To maintain consistency across the project, please follow these coding style guidelines:

- **JavaScript**: Follow the [Bootstrap JavaScript Guide](https://getbootstrap.com/docs/5.3/getting-started/javascript/).
- **CSS**: Use BEM (Block Element Modifier) naming convention for classes.
- **HTML**: Ensure proper semantic HTML structure.
- **Commit Messages**: Write clear and concise commit messages. Follow the [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) specification.

### Testing Your Changes

Before submitting your pull request, ensure your changes do not break existing functionality:

**Run the Tests**

   Execute the tests to verify your changes:

   ```bash
   npm test
   ```

**Manual Testing**

   - Start the application using `npm start`.
   - Navigate through the application to ensure all features work as expected.
   - Verify that your changes do not introduce any new issues.

### Community Guidelines

- **Be Respectful**: Please be respectful and considerate of others in all communications.
- **Provide Feedback**: Offer constructive feedback when reviewing pull requests or participating in discussions.
- **Stay Focused**: Keep discussions and contributions relevant to the project.

Thank you for your interest in contributing to the Book Review Web Application! We look forward to your input and collaboration.
