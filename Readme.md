# Duke Restaurants Postgres Dev Environment

This project provides a reproducible development environment for working with a PostgreSQL database of Durham restaurants, using Python and Docker.

## Features

- **Postgres 16** database with sample restaurant data ([init.sql](init.sql))
- **Python 3.11** dev container with required libraries ([requirements.txt](requirements.txt))
- **Automated setup** via Docker Compose and devcontainer configuration
- **Sample query script** ([scripts/query.py](scripts/query.py)) for CRUD operations

## Getting Started

1. **Open in VS Code**  
   Use [Visual Studio Code](https://code.visualstudio.com/) with the [Dev Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers).

2. **Build the Dev Container**  
   VS Code will automatically build and start the container.  
   The database will be initialized with sample data from [init.sql](init.sql).

3. **Run the Query Script**
   ```sh
   python3 scripts/query.py
   ```

## Database Details

- **Host:** `db` (inside container), `localhost` (outside)
- **Port:** `5432` (or `55432` mapped on host)
- **User:** `vscode`
- **Password:** `vscode`
- **Database:** `duke_restaurants`

See [init.sql](init.sql) for schema and initial data.

## Customization

- Add more scripts to the [`scripts/`](scripts/) folder.
- Place data files in [`data/`](data/).
- Modify environment variables in [`.devcontainer/.env`](.devcontainer/.env).

## Troubleshooting

- If the database is not ready, check container logs for errors.
- Rebuild the container if you change dependencies or the database schema.

---

**Happy coding!**