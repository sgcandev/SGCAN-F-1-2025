FROM mcr.microsoft.com/dotnet/sdk:6.0 AS dev
WORKDIR /app

COPY ./src/*.csproj ./src/
RUN dotnet restore ./src/hub.csproj

COPY ./src ./src

WORKDIR /app/src
EXPOSE 5000

ENTRYPOINT ["dotnet", "watch", "run", "--urls=http://0.0.0.0:5000"]