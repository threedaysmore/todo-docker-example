#<Build Image>
FROM mcr.microsoft.com/dotnet/core/sdk:3.1 AS build-env
WORKDIR /api

# Copy csproj and restore as distinct layers
COPY *.csproj ./
RUN dotnet restore

# Copy everything else and build
COPY . ./
RUN dotnet publish -c Release -o out
#</Build Image>

#<Runtime Image>
FROM mcr.microsoft.com/dotnet/core/aspnet:3.1
WORKDIR /api
COPY --from=build-env /api/out .
ENTRYPOINT ["dotnet", "TodoApi.dll"]
#</Runtime Image>