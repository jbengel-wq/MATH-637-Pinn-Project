## SI Cleaned Dataset (Quick Summary)

- **Rows:** 436 daily observations  
- **Date range:** 2020-02-25 to 2021-05-05  
- **Population used (`N`):** 83,166,711  

### Current Columns
- `day_since_start` (0-based day index)
- `Report Date` (parsed datetime)
- `S` (susceptible stock)
- `I_raw` (daily new infections, non-cumulative)
- `I_cumulative` (running total infections)

### Key Stats
- **`I_cumulative`**: 16 → 3,451,550  
- **`I_raw`**: no negative values (peak daily increase: **33,777**)  
- **`S`**: 83,166,695 → 79,715,161  
- **Data checks passed:**  
  - `S + I_cumulative = N`  
  - `I_raw = diff(I_cumulative)` (after first row handling)
