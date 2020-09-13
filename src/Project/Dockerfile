FROM mcr.microsoft.com/dotnet/core/aspnet:3.1-buster-slim AS runtime

EXPOSE 80
WORKDIR /app
COPY ./publish ./

ENTRYPOINT ["dotnet", "Company.Web.dll"]