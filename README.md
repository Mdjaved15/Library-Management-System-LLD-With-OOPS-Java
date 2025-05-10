📚 Library Management System (LMS) – Project Properties
✅ 1. Object-Oriented Design Principles
Encapsulation: Data and operations are bundled in classes (Book, Member, etc.). Access is controlled through getters/setters or method interfaces.

Inheritance: Member class extends the abstract User class to reuse and specialize user behavior.

Abstraction: User class is abstract, allowing different user types (e.g., Librarian, Member) to have their own implementations of behavior.

Polymorphism: showUserDetails() can be invoked on a User reference, and it behaves according to the actual object type (Member).

✅ 2. Class Breakdown
📘 Book Class
Represents metadata: title, author, ISBN, category.

Used as a base for physical copies of books (BookItem).

📗 BookItem Class
Represents a physical copy of a book.

Includes:

Barcode

Availability status (isAvailable)

Due date (future extension for late fees)

👤 User (Abstract Class)
Common base for all users.

Contains: userId, name, and email.

👨‍🎓 Member Class
Inherits from User.

Includes:

Password for login

List of issued books

Methods for borrowBook() and returnBook()

🏢 Library Class
Central manager for:

Books (add, search, list)

Members (register, login)

Stores books and members using collections (List, Map).

🖥️ Main Class
Runs the program.

Displays menus for:

Login/Register

View, borrow, return books

Logout or exit

Uses loops and conditions to manage interaction flow.

✅ 3. Functional Features
Feature	Description
Registration	New users can sign up with unique IDs.
Login Authentication	Validates user ID and password.
Book Management	Add 10 books at startup. Search and list them.
Borrow Book	Marks the book as unavailable and stores in user's record.
Return Book	Marks the book as available again.
Logout & Re-login	Users can switch accounts without restarting the program.

✅ 4. Technical Design Choices
Element	Justification
HashMap	Fast member lookup by user ID.
ArrayList	Dynamic list of books and issued books.
Scanner	For simple CLI interaction.
Encapsulation	Keeps class internals hidden.
Abstraction	Promotes extensibility (e.g., librarian roles).

✅ 5. Extendability
This design is easily extendable to support:

Admin or librarian role (e.g., add/remove books)

Due dates, late fees

Persistent storage (file/database)

GUI (JavaFX, Swing, web interface)

Book search by category, author, ISBN
