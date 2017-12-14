sfcc-catalog-inspector
=========================

This app does some simple inspection of SFCC xml files, generates a list of products with their primary and classification category assignments (if any) as well as a list of master products and variation products, their variation values and category assignments if any.

running
-----------------
install dotnet core (https://dot.net)

`dotnet run`

or

`dotnet run -- -h`

or 

`dotnet run -- -s sitecatalog.xml -m mastercatalog.xml`


Publishing self contained app
----------------------
`dotnet publish -c Release -r win7-x64`

then in the directory

`./sfcc-catalog-inspector -h`