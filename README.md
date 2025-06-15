**Power BI YouTube Analytics Capstone Project**

# YouTube Channel Performance Dashboard – Power BI Capstone

This project is a complete **Power BI capstone** analyzing a global YouTube dataset. It explores video performance, subscriber behavior, and content trends to help content creators and marketers make data-driven decisions. The report meets all the project tasks required by the Intellipaat Power BI capstone assignment.

##  Files Included
| `YouTubeStats.pbix` | Power BI dashboard file |
| `GlobalYT.xlsx` | Cleaned dataset |
| `Power-BI-Capstone.pdf` | Project instruction sheet |
| `README.md` | This documentation file |

## 🛠 Tools Used

- **Power BI Desktop**
- **DAX (Data Analysis Expressions)**
- **Excel for dataset formatting**
- **Power BI Service** (for publishing & exporting PDF)

##  Project Objective
Analyze a YouTube dataset to extract meaningful insights and provide actionable recommendations for content creators. Visualize patterns in engagement, rank, uploads, and subscriber growth.
> 
##  Step-by-Step Task Breakdown

###  **1. Display Maximum Uploads in a Card**
- **Action**: Used a *Card Visual*.
- **Measure**: MAX(uploads)
- **Insight**: Shows the highest number of uploads among all YouTube channels.


###  **2. Display Minimum Rank in a Card**
- **Action**: Used MIN(rank) in a *Card Visual*.
- **Insight**: Identifies the top-ranked (most-viewed) channel.


###  **3. Display Average Views (Last 30 Days)**
- **Action**: 
  - Cleaned video_views_for_the_last_30_days column.
  - Used AVERAGE(video_views_for_the_last_30_days) in a card.
- **Insight**: Shows platform-wide recent engagement levels.


###  **4. Line Chart – Uploads Over 200K**
- **Action**: Filtered channels with `uploads > 200000`.
- **Visual**: *Line chart* showing `Title` vs `Uploads`.
- **Insight**: Highlights extreme uploaders (e.g., news/media).

###  **5. Packed Bubble Chart – Category vs Subscribers**
- **Action**: Summed `subscribers` by `category`.
- **Visual**: *Packed bubble chart*.
- **Insight**: Identifies dominant categories in terms of subscriber base.

###  **6. Calculated Column – Viewed by Subscriber**
- **Formula**:  
  ```DAX
  Viewed by Subscriber = [video views] / [subscribers]

* **Insight**: Shows how actively each subscriber watches content. 

###  **7. Table – Channel Type vs Views per Subscriber**

* **Action**: Grouped by `channel_type`, used the new calculated column.
* **Visual**: Table sorted by `Viewed by Subscriber`.
* **Insight**: Compares engagement depth across types.

###  **8. Measure – Total Uploads**

* **Formula**:

  ```DAX
  Total Uploads = SUM([uploads])
  ```
* **Visual**: Card visual.
* **Insight**: Summarizes the total publishing activity in the dataset.


###  **9. Decomposition Tree – Rank by Category**

* **Action**: Dragged `Min(rank)` into *Analyze* field.
* **Breakdown**: By `Category`.
* **Insight**: Lets users drill into how rank is distributed among categories.


###  **10. Report Formatting**

* **Headings**: Added using text boxes (report title, section titles).
* **Logo**: YouTube/Power BI logo inserted via `Insert → Image`.
* **Theme**: Styled with dark backgrounds and accent colors (purple, white).

---

###  **11. Publish to Power BI Service**

* Published the `.pbix` file to Power BI Service via “Publish” button.
* Enabled web export and dashboard sharing.


###  **12. Dashboard with  Key Visuals**

Created a dashboard view in Power BI Service.

### ✅ **13. Export as PDF**

* Used Power BI Service → File → Export → `PDF` format.
* File included as `Power-BI-Capstone.pdf`.


##  Filters & Interactivity

**Filters added:**

* Category
* Channel Type
* Country
* Uploads Range
* Subscriber Range
* Created Year

> These slicers allow users to explore insights dynamically.



## 💡 Key Insights

* **Music** and **Entertainment** dominate subscriber count.
* Channels like **T-Series** and **SET India** are high-upload, high-engagement.
* **Education** and **Gaming** channels perform well in rank vs. subscriber efficiency.
* Views per subscriber helps highlight **loyal audiences**.

---

## 🚀 How to Use This Report

1. Clone/download this repo.
2. Open `YouTubeStats.pbix` using **Power BI Desktop**.
3. Make sure `GlobalYT.xlsx` is placed in the same directory or re-map the data source.
4. Explore visuals, slicers, and decomposition tree.
5. Publish or share from Power BI Service.

---

## 📜 License

This project is for educational use. All data complies with YouTube’s public API and privacy policies.

---

## 🙌 Credits

**Developed by**: Jagriti Bihagra
**Based on Project Prompt from**: Intellipaat Power BI Course
**Tools**: Power BI, Excel, DAX

