
🎮 VideoGameApi
A clean and efficient RESTful API built with .NET 9, Entity Framework Core, and SQL Server to manage video games using full CRUD operations via Code-First Migrations.

✨ Features
🔁 Full CRUD (Create, Read, Update, Delete) functionality

🏗️ Code-First Migrations using EF Core

🗃️ SQL Server database integration

🚀 Built on the latest .NET 9 framework

⚙️ Scalable and maintainable project structure

📤 RESTful API architecture

🛠️ Tech Stack
Layer	Technology
Backend	.NET 9 Web API
ORM	Entity Framework Core
Database	SQL Server
Tooling	Swagger, EF CLI

📁 Project Structure
pgsql
Copy
Edit
VideoGameApi/
├── Controllers/
│   └── VideoGamesController.cs
├── Models/
│   └── VideoGame.cs
├── Data/
│   └── AppDbContext.cs
├── Migrations/
│   └── [EF generated files]
├── Program.cs (.NET 9 minimal API)
└── appsettings.json
🚀 Getting Started
✅ Prerequisites
.NET 9 SDK

SQL Server installed locally or remotely

Visual Studio 2022+ / VS Code

(Optional) Postman or Swagger UI for testing

1. Clone the Project
bash
Copy
Edit
git clone https://github.com/yourusername/VideoGameApi.git
cd VideoGameApi
2. Configure Connection String
In appsettings.json, set your SQL Server connection:

json
Copy
Edit
"ConnectionStrings": {
  "DefaultConnection": "Server=.;Database=VideoGameDb;Trusted_Connection=True;"
}
Or for SQL Server with authentication:

json
Copy
Edit
"ConnectionStrings": {
  "DefaultConnection": "Server=.;Database=VideoGameDb;User Id=youruser;Password=yourpassword;"
}
3. Apply Migrations & Create Database
bash
Copy
Edit
dotnet ef migrations add InitialCreate
dotnet ef database update
4. Run the App
bash
Copy
Edit
dotnet run
Visit:

bash
Copy
Edit
https://localhost:5001/swagger
to explore the API using 

🧪 API Endpoints
Method	Route	Description
GET	/api/videogames	Get all games
GET	/api/videogames/{id}	Get a single game by ID
POST	/api/videogames	Add a new game
PUT	/api/videogames/{id}	Update an existing game
DELETE	/api/videogames/{id}	Delete a game

📌 Sample Model: VideoGame.cs
csharp
Copy
Edit
public class VideoGame
{
    public int Id { get; set; }
    public string Title { get; set; }
    public string Genre { get; set; }
    public string Platform { get; set; }
    public DateTime ReleaseDate { get; set; }
}
💡 Future Enhancements
🔒 Add Authentication (JWT)

🎮 Add player reviews or user system

📊 Add search, filtering, and pagination

🚀 Deploy to Azure, Render, or Railway

🤝 Contribution
Contributions, feedback, and pull requests are welcome!

🙏 Acknowledgements
Microsoft .NET Documentation

EF Core Docs
