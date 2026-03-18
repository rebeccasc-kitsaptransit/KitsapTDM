# KitsapTDM -  Commercial Corridor Analysis - Streetlight

Evaluate traffic patterns through commercial corridors on designated zones created by hand-drawing street segments in Streetlight to create a zone set. 

## Notebooks

| Notebook | Analysis | Description |
|----------|-------|-------------|
| `KT_O_COMM.ipynb` | Origin = Commercial | Trips originating in commercial zones (identified zone set) |
| `KITSAP_D_COMM.ipynb` | Destination = Commercial | Trips ending in commercial zones |
| `KT_OMD_MiddleFilter.ipynb` | Pass-Through Analysis | Trips that start or end anywhere in Kitsap County but pass through commercial corridors as intermediate zones |
| `KT_OD_TripPurpose_AGGR.ipynb` | Trip Purpose - Aggregated | Analysis of trip reasons (Home-Based Work, Home-Based Other, Non-Home Based) using aggregated time periods |
| `KT_OD_TripPurpose_detailed.ipynb` | Trip Purpose - Detailed | Same purpose breakdown using hourly data for finer granularity |
| `KT_SEASONAL_VOLUME.ipynb` | Seasonal Comparison | Compares summer traffic volumes to off-season patterns |
| `MODE_SHARE.ipynb` | Mode Share Analysis | Breaks down trips by mode (auto, pedestrian, bike) |
| `OD_HEATMAP.ipynb` | Origin-Destination Matrix | Creates heatmaps visualizing O-D pairs |

## Parameters

### KT operating hours (these are for 98110)
- **Weekday**: 4:30 AM - 7:15 PM
- **Saturday**: 9:00 AM - 6:00 PM
- **Sunday**: 9:00 AM - 4:00 PM

### Commercial corridors (for 98110 analyses) 
- `HIGH_SCHOOL_RD` - Just west of 305 intersection until Sportsman Club Road
- `SPORTSMAN_CLUB` - From Woodward Middle School/Coppertop until just before 305 intersection
- `SR305_MID` - Just north of High School Road until Sportsman Club Road
- `SR305_N` - Just north of Sportsman Club Road, over Agate Pass, until Kingston Ferry turnoff
- `SR305_S` - Just below Winslow Way & Olympic until just south of High School Road on 305
- `WINSLOW_WAY` - Just west of 305 along corridor until Madison Ave
- `LYNWOOD_CENTER` - South end commercial zone

### Time Periods (aggregated, adjustable)
- `0: All Day (12am-12am)` - All Day
- `1: Early AM (12am-6am)` - Early AM
- `2: Peak AM (6am-10am)` - Peak AM
- `3: Mid-Day (10am-3pm)` - Mid-Day
- `4: Peak PM (3pm-7pm)` - Peak PM
- `5: Late PM (7pm-12am)` - Late PM

### Day Types -- break up by day if needed
- `0: All Days (M-Su)`
- `1: Weekday (M-Th)`
- `2: Friday (F-F)`
- `3: Saturday (Sa-Sa)`
- `4: Sunday (Su-Su)`

### Trip Purposes
- `Home to Work` - Home-based work trips
- `Home to Other` - Home-based other trips
- `Non-Home Based Trip` - Non-home based trips

## Data Sources

Streetlight Data O-D and O-M-D files (working list):
- `2014261_BI_Corridor_Volume_2025_dayparts_purpose.csv` - Aggregated trip purpose data
- `2014231_BI_Corridor_Volume_2025_dayparts\2014231_BI_Corridor_Volume_2025_dayparts_mf_all.csv` - Corridor volume by day
- `2013907_BI_Corridor_Volume_2024_mf_all.csv` - Middle filter (corridor) volume data
- `2013907_BI_Corridor_Volume_2024_mf_traveler_trip_purpose_all.csv` - Detailed trip purpose data
- `2014263_BI_Commecial_OD_all_vehicles_od_trip_all.csv` - Commercial origin-destination data

## Outputs

- Heatmaps by day type, time period, and analysis dimension
- Summary tables (CSV format)
- PDF exports of visualizations
- Statistical summaries of traffic patterns

## Requirements

- Python 3.11.11
- pandas 2.2.3
- numpy
- matplotlib
- seaborn
- jupyter

## Usage

1. Input data files are in working directory
2. Update file paths in configuration section if needed
3. Run all cells
4. Review generated heatmaps and summary tables in output directories

## Key Metrics Calculated

- Traffic volume by corridor, time period, and day type
- Trip length distributions (short/local vs long/pass-through)
- Speed as congestion proxy
- Mode shift potential scores (0-100 scale)
- Shuttle-eligible trips (short trips outside transit hours)
- Seasonal volume comparisons
- Mode share percentages (auto, pedestrian, bike)


