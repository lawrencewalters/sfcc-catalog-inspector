sfcc-catalog-inspector
=========================

This app does some simple inspection of SFCC xml files, generates a list of products with their primary and classification category assignments (if any) as well as a list of master products and variation products, their variation values and category assignments if any.

Building from this repo
------------------------
1. clone this repo
1. install dotnet core (https://dot.net)

running
-----------------

1. Export your SFCC master catalog as xml from Business manager (Merchant Tools >  Products and Catalogs >  Import & Export > Catalogs-Export)
1. Export your SFCC site catalog as xml from Business manager (unless all your catalog data is in the master, then you'll just specify the same master file below)
1. Download both of those to this directory (Merchant Tools >  Products and Catalogs >  Import & Export > Import & Export Files-Download)
1. Run this app from command line (powershell or git bash will work)

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
