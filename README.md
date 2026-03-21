# NHLdata

Download historical NHL game data accurately from the official NHL Web API. Produces clean, analysis-ready datasets for player stats, team stats, and game schedules.

![Python](https://img.shields.io/badge/Python-3.11+-blue) ![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange) ![License](https://img.shields.io/badge/License-MIT-green)

## Features

- **Full Season Schedule** — Scrapes every regular-season game from the NHL Web API
- **Detailed Boxscores** — Player-level stats for every game (goals, assists, shots, hits, TOI, etc.)
- **Positional Breakdown** — Separate stats for forwards, defensemen, and goalies
- **Team Game Stats** — Per-game team performance with starting goalie and scratch tracking
- **Clean Output** — Ready-to-use CSV files for analysis or ML pipelines

## Quick Start

```bash
# Clone the repo
git clone https://github.com/natedoggzCD/NHLdata.git
cd NHLdata

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter
jupyter notebook
```

Run `nhl_data_collection.ipynb` to download the full season schedule and player stats, then `nhl_team_game_stats.ipynb` for team-level aggregations.

## Notebooks

| Notebook | Purpose |
|----------|---------|
| `nhl_data_collection.ipynb` | Download schedule + player game stats for entire season |
| `nhl_team_game_stats.ipynb` | Aggregate team-level stats per game |

## Output Datasets

| File | Description | Row Granularity |
|------|-------------|-----------------|
| `nhl_20242025_schedule.csv` | Full season schedule | One row per game |
| `nhl_20242025_game_team_stats.csv` | Team performance per game | One row per team per game |
| `nhl_20242025_player_game_stats.csv` | Player stats per game | One row per player per game |
| `nhl_20242025_player_game_stats_with_latest_team.csv` | Player stats with current team | One row per player per game |

## Data Source

All data is sourced from the **NHL Web API** (`api-web.nhle.com`). This is the same API used by the official NHL website.

## Dependencies

- **pandas** — Data manipulation
- **requests** — HTTP calls to NHL API
- **tqdm** — Progress bars for batch downloads
- **jupyter** — Notebook environment

## License

[MIT](LICENSE)
