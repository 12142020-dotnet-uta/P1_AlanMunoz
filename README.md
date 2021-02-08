# P1_SuperStore

## Project Description

This is a ASP.NET Core MVC project utilizing Entity Framework Core to create a Web Store Application that allows a user to create an account then view orders by user and store location. The user can create an order, view their order history, and view the order history of a store location.

## Technologies Used

* ASP.NET Core MVC
* ASP.NET Identity for authentication
* Entity Framework Code First
* Razor 

## Features

* The cart will still be available if the user want to change from a store location
* Authentication with Identity
* The users can add products into the store warehouse.
* The users can display a list of products available in the warehouse.

To-do list:
* Implement an Admin Role.
* Verify if the user want to continue the order or it want's to cancel.
* Use JavaScript for display the amount of products available in the cart.

## Getting Started
   
`git clone https://github.com/12142020-dotnet-uta/P1_AlanMunoz.git`

For the creation of a Database using EF Code First will be required:
* In the project `P1_RepositoryLayer` it haves the `StoreDbContext.cs` file, and inside the file we have the connection string to the Database in the method OnConfiguring(...), we change the connection string to our database to work with.
`protected override void OnConfiguring(DbContextOptionsBuilder optionsBuilder)
        {
            if (!optionsBuilder.IsConfigured)
            {
                optionsBuilder.UseSqlServer(@"NewConnectionString");
            }
        }`
* Then it require a Migration for apply the `Migrations` files and to implement the models in the file with the command in the Package Manager Console: 
`Update-Database`

When the migration have created the Database, navigate into the SuperApp Folder in a command line, and execute `dotnet run`, and it will grab an available port for accessing the application.

## Usage

New users can view the main dashboard and will have the Log In or Register, will require basic information and a password for gain access to the application.
Once logged in, it will gain access to the diferent pages for generating an order, register a store, manages users and add new products.



## License

This project uses the following license: [MIT Licence](https://github.com/git/git-scm.com/blob/master/MIT-LICENSE.txt).

