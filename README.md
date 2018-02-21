sfcc-catalog-inspector
=========================

This app does some simple inspection of SFCC xml files, generates a list of products with their primary and classification category assignments (if any) as well as a list of master products and variation products, their variation values and category assignments if any.

Building from this repo
------------------------
1. install dotnet core (https://dot.net) for your platform. On windows, find this at https://www.microsoft.com/net/download/windows, and as of the time of this writing, this would be the 64bit latest SDK: https://www.microsoft.com/net/download/thank-you/dotnet-sdk-2.1.4-windows-x64-installer. I'm not totally certain the SDK is necessary for just running this.
1. Clone this repository. Alternatively, just grab the three files in the root (README.md, Program.cs, sfcc-catalog-inspector.csproj) and put them in a single directory locally

running
-----------------

1. Export your SFCC master catalog as xml (name it "master-catalog") from Business manager (Merchant Tools >  Products and Catalogs >  Import & Export > Catalogs-Export)
1. Export your SFCC site catalog as xml (name it "site-catalog") from Business manager (unless all your catalog data is in the master, then you'll just specify the same master file below)
1. Download both of those files (master-catalog.xml, site-catalog.xml) to this directory (Merchant Tools >  Products and Catalogs >  Import & Export > Import & Export Files-Download)
1. Run this app from command line (powershell or git bash will work)

`dotnet run`

(expects master-catalog.xml and site-catalog.xml to exist in this current directory)

or

`dotnet run -- -h`

or 

`dotnet run -- -s sitecatalog.xml -m mastercatalog.xml`


Publishing self contained app
----------------------
`dotnet publish -c Release -r win7-x64`

then to run

`./sfcc-catalog-inspector -h`
