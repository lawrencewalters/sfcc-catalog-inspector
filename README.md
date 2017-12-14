sfcc-catalog-inspector
=========================

This app does some simple inspection of SFCC xml files, generates a list of products with their primary and classification category assignments (if any) as well as a list of master products and variation products, their variation values and category assignments if any.

Building from this repo
------------------------
clone this repo
install dotnet core (https://dot.net)

running
-----------------

1. Export your SFCC master catalog as xml from Business manager
1. Export your SFCC site catalog as xml from Business manager (unless all your catalog data is in the master, then you'll just specify the same master file below)
1. Run it from command line (powershell or git bash will work)

`dotnet run`

or

`dotnet run -- -h`

or 

`dotnet run -- -s sitecatalog.xml -m mastercatalog.xml`


Publishing self contained app
----------------------
`dotnet publish -c Release -r win7-x64`

then to run

`./sfcc-catalog-inspector -h`