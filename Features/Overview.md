# Basic features

 - Process a CSV ([CSV Processing](obsidian://open?vault=expense-analyzer-docs&file=Features%2FCSV%20Processing))
 - Link an operation to an account
 - Filter grouped expenses
 - Give the total income
 - Give the total expense
 - Security

# Long term features

 - Show the evolution of the income and expenses
 - Show incomes & expenses in a graph
 - Identify recurring expenses
 - Let the user link an specific account to a description (ex: link a bank account to a brand like Colruyt, Delhaize, Amazon, Zalando, etc)
 - Show the regular expenses of the user across multiple months
 - Show the accounts where the regular expenses are done
 - Upload a ZIP/RAR/Compressed file with multiple expense sheets in CSV
 - Add more file support
 - List, download and delete precedent files
 - Allow the user to configure the column used for data selection

# Containerization
- Should host the db
- Should host the files linked to a user => keep the path to the expense sheets

# API documentation

Do not forget to `@Operation(summary="")` & `@ApiResponses(value= {@ApiResponse(responseCoce="", description="")})` to methods.
Fields in the models should also be annotated with `@ModelProperty(notes = "", example = "", required = true/false)`.
Look at [this](https://www.baeldung.com/swagger-set-example-description) page to find an example and [this](https://docs.swagger.io/swagger-core/v1.5.0/apidocs/index.html?io/swagger/annotations/package-summary.html) to look at the documentation.