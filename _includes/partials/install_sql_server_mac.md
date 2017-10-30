1. In order to run SQL Server on your Mac you need to [install Docker](https://docs.docker.com/engine/installation/mac/).
2. Configure at least 4GB of memory for your Docker environment, also consider adding multiple cores if you want to evaluate performance. You can do this in the [Docker Preferences](https://docs.docker.com/docker-for-mac/#preferences) option on the menu bar.
3. Next, start a new **Terminal prompt** and use the following commands to download and start the **SQL Server on Linux** Docker image. Make sure to use a strong password with special characters.

```terminal
sudo docker pull microsoft/mssql-server-linux
docker run -e 'ACCEPT_EULA=Y' -e 'SA_PASSWORD=yourStrong(!)Password' -p 1433:1433 -d microsoft/mssql-server-linux
```

> You now have SQL Server running locally in Docker! Check out the next section to continue installing prerequisites.
