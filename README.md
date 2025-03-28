# FantasyPros MCP Server

An MCP server that provides access to the FantasyPros API for sports data, news, rankings, and projections.

## Setup

1. Get a FantasyPros API key by emailing them
2. Create a `.env` file and add your API key:
```
FANTASYPROS_API_KEY=your_api_key_here
```
3. Install dependencies:
```bash
npm install
```
4. Build the server:
```bash
npm run build
```

## Available Tools

### get_sport_news
Get news for a specific sport (NFL, MLB, NBA, NHL)
- Parameters:
  - sport: Sport to get news for ('nfl', 'mlb', 'nba', 'nhl')
  - limit: Number of news items to return (max 25)
  - category: Type of news ('injury', 'recap', 'transaction', 'rumor', 'breaking')

### get_players
Get player information for a specific sport
- Parameters:
  - sport: Sport to get players for ('nfl', 'mlb', 'nba', 'nhl')
  - playerId: Filter by specific player ID (optional)

### get_rankings
Get consensus rankings for a sport
- Parameters:
  - sport: Sport to get rankings for ('nfl', 'nba')
  - position: Position to filter by (optional)
  - scoring: Scoring type for NFL ('STD', 'PPR', 'HALF')

### get_projections
Get player projections for a sport
- Parameters:
  - sport: Sport to get projections for ('nfl', 'mlb', 'nba')
  - season: Season year
  - week: Week number (for NFL)
  - position: Position to filter by (optional)
