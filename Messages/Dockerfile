FROM microsoft/dotnet:2.2-sdk AS build
WORKDIR /app

COPY *.csproj ./
RUN dotnet restore Messages.csproj

COPY . ./
RUN dotnet pack Messages.csproj -c Release -o out

FROM microsoft/dotnet:2.2-aspnetcore-runtime AS runtime

WORKDIR /app

COPY --from=build /app/out .

ENTRYPOINT ["dotnet", "Messages.dll"]`