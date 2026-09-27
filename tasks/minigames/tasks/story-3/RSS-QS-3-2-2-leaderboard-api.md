# Task RSS-QS-3-2-2: Top Players Leaderboard API Integration (15 points)

## Description

Load and render the Home page Top Players leaderboard from the backend REST API.

## Acceptance Criteria

- **API Data Fetching:** Leaderboard rows are fetched from the backend API endpoint for top players.
- **Dynamic Table Rendering:** Rank, player name, score/stats, and other required leaderboard fields are rendered from the response.
- **Loading & Error States:** Skeleton loader while pending; error banner with retry or equivalent feedback on failure.
- **Empty State:** If the API returns an empty leaderboard list, show an empty-state placeholder instead of a broken table.
