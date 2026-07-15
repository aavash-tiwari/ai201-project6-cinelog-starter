\# PR Response Doc — CineLog Watchlist Feature



\## AI Usage

<!-- Fill in at the end — how you used AI tools during this project -->



\## Comment 1 — Rename

\*\*What I did: I renamed `save_to_watchlist` to `add_to_watchlist` in `services/watchlist_service.py` and updated the call site in `routes/watchlist/watchlist.py`.\*\*

\*\*How I verified: I used my code editor's global search to search the entire project for `save_to_watchlist` and confirmed that no other call sites were missed.\*\*



\## Comment 2 — Deduplication

\*\*What I did: I added a deduplication check at the top of `add_to_watchlist`. It queries `WatchlistEntry` using the `user_id` and `film_id`. If a duplicate is detected, it raises an error, stopping the function from inserting a second identical record.\*\*

\*\*How I verified: I directly referenced the existing `add_to_collection()` pattern in `services/collection_service.py` to ensure my implementation mirrored how the codebase currently handles this exact edge case.\*\*



\## Comment 3 — Missing test

\*\*What I did:\*\*

\*\*How I verified:\*\*



\## Comment 4 — Default visibility

\*\*My position:\*\*

\*\*Reasoning:\*\*

\*\*Tradeoff acknowledged:\*\*



\## Comment 5 — Sort order

\*\*My position:\*\*

\*\*Reasoning:\*\*

\*\*Engagement with reviewer's point:\*\*



\## Comment 6 — Rebase

\*\*What conflicted:\*\*

\*\*How I resolved it:\*\*

\*\*How I verified no conflict remains:\*\*



\## PR Description

<!-- Written at the end — feature overview, design decisions, manual testing steps -->

