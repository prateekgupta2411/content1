# content1
hoe to crud work

Scaffold-DbContext "server= PRATEEKGUPTA\SQLEXPRESS; database = CodeFirstDb; trusted_connection=true; TrustServerCertificate=True;" Microsoft.EntityFrameworkCore.sqlServer -OutputDir Models

var provider = builder.Services.BuildServiceProvider();
var confiq = provider.GetRequiredService<IConfiguration>();
builder.Services.AddDbContext<CollageContext>(Item => Item.UseSqlServer(confiq.GetConnectionString("dbcs")));

var data = context.Students.ToList();
