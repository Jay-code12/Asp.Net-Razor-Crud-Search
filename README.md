# ASP.NET Core CRUD Using Entity Framework Core and SQL Server

create an ASP.NET Razor Pages CRUD app using Entity Framework Core and SQL Server. 

## Introduction
## Create Project 
## Create Database SQL Server
## Asp.NET Core Connection Db SQL Server
## Install Nugets ASP.NET Core ( Entity Framework )
## Create Application Db Context Class
## Register Database Connections
## Create Product Model  ASP.NET Core
## Add-Migrations ASP.NET Core
## Update-Database (Create Tables) Asp.Net Core
## Create Administration
## List Products
## Create ProductDto Model
## Create the Form Asp.Net Core
## Form Validation Asp.Net Core
                <div class="row mb-3">
                <label  class="col-sm-4 col-form-label">Name</label>
                <div class="col-sm-8">
                 <input asp-for="ProductDto.Name" class="form-control" />
                    <span asp-validation-for="ProductDto.Name" class="text-danger"></span>
                </div>

             </div>
## Upload Image on Server
             string newFilename = DateTime.Now.ToString("yyyyMMddHHmmssfff");
             newFilename += Path.GetExtension(ProductDto.ImageFileName!.FileName);
             string ImageFullPath = environment.WebRootPath + "/Images/" + newFilename;
             using (var stream = System.IO.File.Create(ImageFullPath))
                {
                ProductDto.ImageFileName.CopyTo(stream);
               }
## Delete Image on Server

                //Delete Old Image on the server 
                string OldimageFullPath = environment.WebRootPath + "/images/" + product.ImageFileName;
                System.IO.File.Delete(OldimageFullPath);
## Save On Database
                product.Name = ProductDto.Name;
                product.Brand = ProductDto.Brand;
                product.Category = ProductDto.Category;
                product.Price = ProductDto.Price;
                product.Description = ProductDto.Description ?? "";
                product.ImageFileName = newFileName;

                context.SaveChanges();
                Product = product;
                successMessage = "Product Updated";
                
## Pagination(Page Size)  ASP.NET Core
## Search  ASP.NET Core
## Sporting  ASP.NET Core



