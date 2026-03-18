# KitsapTDM

This script takes in Streetlight O-D data, summarize the number of OD trips by Day Type, Time of Day, and Trip Purpose. It outputs heatmaps of OD zones for trips to and from designated, custom-designed areas within Kitsap County & includes overlay of KT operating hours for visual reference.

Python 3.11.11 with Pandas 2.2.3

Input data: '2014261_BI_Corridor_Volume_2025_dayparts_purpose.csv'

1) Day Type: '0: Average Day (M-Su)', '1: Average Weekday (Tu-Th)', '2: Average Weekend Day (Sa-Sa)'

2) Day Part: '0: All Day (12am-12am)': 'All Day', '1: Early AM (12am-6am)': 'Early AM', '2: Peak AM (6am-10am)': 'Peak AM', '3: Mid-Day (10am-3pm)': 'Mid-Day', '4: Peak PM (3pm-7pm)': 'Peak PM', '5: Late PM (7pm-12am)': 'Late PM'

3) Trip Purpose: 'Home to Work': 'Home to Work', 'Home to Other': 'Home to Other', 'Non-Home Based Trip': 'Non-Home Based'

4) KT Operating Hours = 'weekday': 4:30 AM - 7:15 PM, 'saturday': 9:00 AM - 6:00 PM, 'sunday': 9:00 AM - 4:00 PM

Output: Heatmap plots by OD, Day Type, ToD, and Trip Purpose

---

This script takes in Streetlight O-M-D data, summarize the number of OMD trips by Day Type, Time of Day, and Middle Filter.
It outputs heatmaps of OD zones for trips to and from any where in the county through designated commercial corridors within Kitsap County.

Python 3.11.11 with Pandas 2.2.3

Input data: '2013907_BI_Corridor_Volume_2024_mf_all.csv'


1) Day Type: '1: Monday (M-M)', '2: Tuesday (Tu-Tu)', '3: Wednesday (W-W)', '4: Thursday (Th-Th)', '5: Friday (F-F)', '6: Saturday (Sa-Sa)', '7: Sunday (Su-Su)'

2) Day Part: '00: All Day (12am-12am)', AM Peak - '08: 7am (7am-8am)', '09: 8am (8am-9am)', PM-Peak - '17: 4pm (4pm-5pm)', '18: 5pm (5pm-6pm)'

3) Middle Filters: 'HIGH_SCHOOL_RD', 'SPORTSMAN_CLUB', 'SR305_MID', 'SR305_N', 'SR305_S', 'WINSLOW_WAY'

4) KT Operating Hours = 'weekday': 4:30 AM - 7:15 PM, 'saturday': 9:00 AM - 6:00 PM, 'sunday': 9:00 AM - 4:00 PM
   
Output: Heatmap plots by OD, Day Type, ToD, and Middle Filter
