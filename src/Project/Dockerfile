FROM mcr.microsoft.com/dotnet/core/aspnet:3.1-buster-slim AS runtime

EXPOSE 4335
WORKDIR /app
COPY ./release ./

ENTRYPOINT ["dotnet", "City.Node.dll"]