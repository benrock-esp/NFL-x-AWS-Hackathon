**README**

Matchup Control is a quantitative modelling project built around NFL pass protection. Using player-tracking time-series data, we developed a metric to grade individual offensive linemen on how effectively they control a one-on-one block and protect the quarterback.

Approach

We used the player-tracking data to measure the geometry of each block, including ground conceded towards the quarterback, blocker-rusher separation and how consistently the blocker maintained protection. We then used logistic regression to combine these features into a single control grade, validating the model against PFF's hit, hurry and sack labels.

Dashboard

We built an interactive Streamlit dashboard to explore the results, including a player leaderboard filterable by team and position, model validation and feature importance, and a film-room view showing player trajectories alongside a control-over-time curve. The dashboard also includes team-level comparisons and an additional receiver-versus-defender analysis.

Run locally

From the repository root:

pip install -r requirements.txt
streamlit run matchup/app.py

Ensure the nfl-big-data-bowl-regional-event-data/data/ directory is present alongside matchup/. Click Run pipeline in the sidebar to calculate the grades. Results are cached for subsequent runs.
