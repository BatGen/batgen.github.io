This is a simple yet powerful code generator that will generate the SQL, MyBatis mapper files, MyBatis interface files, supporting Data Access Object (DAO) and Business Object (BO) objects with the basic CRUD operations.

To keep it simple, we rely heavily on creating conventions for how projects are setup and how database column types are associated with corresponding class variable types.

For this reason, we recommend using this product on new projects, as existing projects will already have established standards.

This is a conscious choice we made and it dramatically simplifies the setup and configuration of new projects. It also causes all projects that use this product to have a standard directory structure for the project.

Features include:

The code generator generates clean, readable and maintainable code that you check in with the rest of the code. There is a reserved area in each generated file that you can write custom code into. This reserved area is preserved during code generation, so if you change something, you can still maintain the code you wrote in it.
Table definitions are stored in text files, and they describe the tables, columns, related classes, related class variables, and type information used to generate the code.
The tutorial provides all the information you need to get started building applications using Eclipse and Maven.

## License

[MIT](http://opensource.org/licenses/MIT)
