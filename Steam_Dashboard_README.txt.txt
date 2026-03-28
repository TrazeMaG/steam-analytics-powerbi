================================================================================
                    STEAM MARKET ANALYTICS DASHBOARD
                    Business Intelligence Assignment
                          MSc Business Analytics 
================================================================================

STUDENT INFORMATION:
-------------------
Student Name:    Nikhil Upadhyay
Student ID:      20066392
Course:          MSc Business Analytics
Module:          Business Intelligence & Visualization
Institution:     Dublin Business School
Submission Date: December 9, 2025

================================================================================
                            EXECUTIVE SUMMARY
================================================================================

This dashboard provides comprehensive market intelligence for Steam game 
publishing decisions through three distinct analytical modes:

• PROFESSIONAL MODE: Corporate market overview for executive stakeholders
• GAMING MODE: Player engagement analysis for product teams  
• PERFORMANCE/ECO MODE: Pricing strategy optimization for revenue analysts

The dashboard analyzes 1,293 actively-played Steam games across 28 countries,
providing actionable insights for publishing strategy, pricing optimization,
and market positioning.

================================================================================
                            QUICK FACTS
================================================================================

Dataset Size:           1,293 games (filtered from 10,000)
Data Attributes:        26 key fields
Geographic Coverage:    28 countries
Time Period:            Current Steam catalog
Total Visuals:          10+ interactive charts
KPI Metrics:            5 core indicators
Interactive Features:   Bookmarks, Mode switching, slicers, dynamic insights
Tools Used:             PowerBI Desktop, DAX

================================================================================
                          DATASET OVERVIEW
================================================================================

DATA SOURCE:
-----------
Steam game catalog data retrieved via Steam Spy API (https://steamspy.com/)

Steam Spy is a third-party analytics service that provides comprehensive Steam 
game statistics including:
• Ownership estimates
• Player counts and playtime data
• Review statistics (positive/negative breakdown)
• Pricing information across regions
• Genre and tag classifications
• Publisher and developer information
• Geographic distribution data

API Access Method:
The dataset was obtained through Steam Spy's public API, which aggregates data
from Steam's public profiles and store information. The API provides reliable,
regularly-updated statistics on Steam games without requiring direct Steam API
authentication.

Data Collection Date: November-December 2024
Original Dataset: 10,000 games retrieved via API calls
Data Freshness: Current Steam catalog reflecting active market conditions

FILTERING METHODOLOGY:
---------------------
Original Dataset:    10,000 games
Filtered Dataset:    1,293 games (12.9%)
Filtering Criteria:  average_playtime > 0 OR total_reviews > 0

RATIONALE:
77% of original games had zero engagement (no playtime, no reviews). These
represent abandoned, unreleased, or non-viable titles. Filtering to engaged
games ensures:
  • More accurate market insights
  • Cleaner visualizations
  • Actionable publishing intelligence
  • Professional BI data quality standards

STATISTICAL VALIDITY:
1,293 games provides 6-12x the minimum sample size needed for reliable
statistical analysis across genres, price points, and geographic regions.

KEY ATTRIBUTES (26 fields):
--------------------------
• Game Identification: AppID, Name
• Pricing: Price (EUR), Price tier classifications
• Engagement: Average playtime, Total reviews, Reviewed titles
• Sentiment: Positive reviews, Negative reviews, Sentiment score
• Publisher: Publisher name, Country of origin
• Classification: Genre (top_tag), Categories, Tags
• Geographic: Publisher country (28 countries represented)
• Performance: Engagement tier (High/Medium/Low)
• Revenue: Revenue Potential Index (RPI) - custom metric

================================================================================
                       THREE-MODE DASHBOARD SYSTEM
================================================================================

CONCEPT:
--------
Inspired by gaming graphics settings (Low/Medium/Ultra), the dashboard offers
three modes optimized for different user contexts and decision-making needs.

MODE 1: PROFESSIONAL MODE (Corporate Blue Theme)
------------------------------------------------
PURPOSE:       Executive market intelligence and strategic planning
TARGET USER:   C-suite executives, stakeholders, investors, board members
AESTHETICS:    Clean blue gradient, boardroom-ready, trustworthy
KEY VISUALS:   
  • Global Publishing Activity Map (geographic distribution)
  • Genre Distribution Overview (market composition)
  • Genre × Engagement Heatmap (competitive performance)
  • Dynamic Country Insights (comparative analysis)
  • 5 Core KPIs (market summary metrics)

KEY INSIGHTS:
  • Geographic concentration: US, Europe, and China dominate (60% of games)
  • Genre distribution: Action (94 games) and Adventure (89) lead market
  • Engagement patterns: Action genres achieve 58 high-engagement titles
  • Regional performance: Comparative RPI analysis by country

DESCRIPTION:
This mode provides executive stakeholders with comprehensive market 
intelligence for strategic planning. It reveals geographic distribution of 
publishing activity, genre market composition, and competitive positioning 
across 28 countries. The visuals use a clean, corporate blue gradient design 
to make market trends, regional strengths, and competitive dynamics clear and 
accessible for boardroom presentations and investment decisions.


MODE 2: GAMING MODE (Dark + Gold Cinematic Theme)
-------------------------------------------------
PURPOSE:       Player engagement and sentiment analysis
TARGET USER:   Product managers, gaming industry professionals, creative teams
AESTHETICS:    Dark background with gold accents, cinematic, immersive
KEY VISUALS:
  • Player Engagement Funnel (conversion analysis)
  • Sentiment Score by Genre (player satisfaction)
  • Price vs Sentiment Scatter Chart (pricing psychology)
  • Top 10 Publishers by RPI (commercial leaders)

KEY INSIGHTS:
  • Engagement conversion: 62.6% of reviewed games achieve high engagement
  • Genre satisfaction: Strategy and Serious Combat genres score 0.99 sentiment
  • Pricing impact: Scatter plot reveals optimal price-sentiment relationships
  • Publisher performance: Top 10 publishers ranked by revenue potential

DESCRIPTION:
This mode gives publishing teams a sharp, tactical view of Steam market 
performance. It highlights which genres and titles drive the strongest player 
engagement, where revenue opportunities exist based on pricing and sentiment, 
and how publishers perform commercially. The visuals use a high-contrast, 
game-inspired design to make patterns in player behavior, satisfaction, and 
commercial potential easy to spot. By blending cinematic styling with data 
insights, the dashboard helps product managers quickly identify winning genres, 
undervalued titles, and strategic pricing decisions that can boost visibility 
and revenue.


MODE 3: PERFORMANCE/ECO MODE (Green Efficiency Theme)
----------------------------------------------------
PURPOSE:       Pricing strategy optimization and revenue analysis
TARGET USER:   Pricing strategists, financial analysts, portfolio managers
AESTHETICS:    Green/teal efficiency-focused design, balanced, optimized
NAMING:        "Performance/Eco Mode" combines efficiency (eco) with optimization
               (performance), emphasizing balanced, sustainable revenue strategy
KEY VISUALS:
  • Price Band Distribution (market pricing structure)
  • Engagement Tier by Price Band (price-performance correlation)
  • Revenue Potential Leaderboard (top commercial opportunities)

KEY INSIGHTS:
  • Pricing sweet spot: €5-15 contains 561 games (43.35% of market)
  • Highest engagement: €5-15 band shows 324 high-engagement titles
  • Market opportunity: €15-40 premium space is underutilized (only 15.15%)
  • Revenue leaders: Top titles by Revenue Potential Index identified

DESCRIPTION:

This Performance/Eco Mode delivers optimized pricing intelligence and revenue 
analytics for publishing strategists. The dual naming reflects both aspects of 
this view: "Performance" emphasizes revenue optimization and commercial success, 
while "Eco" represents efficiency, balance, and sustainable pricing strategy—
similar to eco rounds in competitive gaming where resource optimization is key.

It reveals which price tiers achieve the strongest player engagement, identifies 
high-potential titles through comprehensive revenue metrics, and exposes market 
opportunities across different pricing strategies. The visuals use a balanced, 
efficiency-focused design with green color coding to make pricing patterns, 
engagement correlations, and commercial opportunities immediately actionable. 

By combining clean data presentation with strategic insights, the dashboard 
helps analysts quickly identify optimal price points, underperforming segments, 
and revenue-maximizing opportunities that can improve portfolio performance and 
market positioning.

================================================================================
                        KEY PERFORMANCE INDICATORS
================================================================================

The dashboard tracks 5 core KPIs across all modes:

1. TOTAL ACTIVE TITLES: 1,293 games
   Calculation: COUNT of games with engagement (reviews > 0 OR playtime > 0)
   Purpose: Market size indicator, filtered catalog volume

2. MARKET SENTIMENT SCORE: 0.79
   Calculation: AVERAGE(positive_reviews / total_reviews) across all games
   Purpose: Overall player satisfaction metric, quality indicator

3. HIGH ENGAGEMENT TITLES: 810 games
   Calculation: COUNT of games with engagement_tier = 'High'
   Purpose: Success rate metric, quality game identification

4. AVERAGE REVENUE POTENTIAL INDEX (RPI): 31.13
   Calculation: AVERAGE(Price × LOG10(total_reviews + 1))
   Purpose: Commercial viability metric, revenue opportunity indicator
   Note: Log scaling balances viral hits against quality titles

5. COUNTRIES REPRESENTED: 16 countries
   Calculation: DISTINCTCOUNT(publisher_country) with active games
   Purpose: Market diversity metric, geographic reach indicator

================================================================================
                          DEVELOPMENT PROCESS
================================================================================

STEP 1: DATA PREPARATION
------------------------
• Imported 10,000 Steam game records
• Analyzed data quality (77% zero-engagement identified)
• Applied engagement-based filtering (playtime > 0 OR reviews > 0)
• Created price band classifications (€0-5, €5-15, €15-40, €40+)
• Established engagement tiers (High/Medium/Low based on playtime quartiles)

STEP 2: MEASURE CREATION (DAX)
------------------------------
Created custom calculated measures:
• Total Active Titles = COUNT with engagement conditions
• Market Sentiment Score = AVERAGE(positive/total reviews)
• High Engagement Count = COUNT with tier filter
• Revenue Potential Index = Price × LOG10(reviews) 
• Geographic Diversity = DISTINCTCOUNT(countries)

STEP 3: VISUALIZATION DESIGN
----------------------------
Designed 10+ interactive visuals:
• Interactive global map with country labels and tooltips
• Bar charts with gradient coloring for visual hierarchy
• Donut chart with strategic color coding (sweet spot = green)
• Stacked bar chart showing engagement distribution by price
• Heatmap matrix for genre × engagement analysis
• Scatter plot for price-sentiment correlation
• Funnel chart for engagement conversion
• Comprehensive data table with revenue metrics

STEP 4: MODE IMPLEMENTATION
---------------------------
• Created three distinct visual themes using color psychology
• Implemented bookmark-based navigation for seamless mode switching
• Applied consistent layouts across modes while varying aesthetics
• Added mode switching buttons for user control

STEP 5: INTERACTIVITY & POLISH
------------------------------
• Added 4 slicers (Name, Tags, Genres, Categories) for filtering
• Implemented year filter for temporal analysis
• Created dynamic country insight feature (comparative RPI analysis)
• Added tooltips to map showing country-level details
• Refined spacing, alignment, and visual hierarchy
• Tested all interactive features and mode switching

================================================================================
                       KEY INSIGHTS & FINDINGS
================================================================================

GEOGRAPHIC INSIGHTS:
-------------------
1. Publisher Concentration: United States dominates with largest market share,
   followed by Poland, Germany, and United Kingdom in Europe
   
2. Regional Performance: Austria shows 11% lower RPI than global average,
   indicating potential market underperformance or opportunity
   
3. Geographic Diversity: 16 active countries with significant publishing
   activity, concentrated in North America, Europe, and Asia

GENRE INSIGHTS:
--------------
4. Market Composition: Action (94 titles) and Adventure (89 titles) lead
   market volume, followed by Indie and Strategy genres
   
5. Quality Leaders: Strategy and Serious Combat genres achieve highest
   sentiment scores (0.99), indicating strong player satisfaction
   
6. Engagement Performance: Action genre achieves 58 high-engagement titles,
   demonstrating both volume and quality success

PRICING INSIGHTS:
----------------
7. Sweet Spot Identified: €5-15 price band contains 561 games (43.35%) and
   achieves highest absolute high-engagement count (324 titles)
   
8. Market Opportunity: €15-40 premium band is underutilized at only 195 games
   (15.15% of market) despite showing strong engagement potential
   
9. Ultra-Premium Niche: €40+ band contains only 19 games (1.47%), representing
   low-competition but high-risk pricing strategy

ENGAGEMENT INSIGHTS:
-------------------
10. Conversion Rate: 62.6% of reviewed games achieve high engagement,
    indicating strong quality filtering effectiveness
    
11. Price-Engagement Correlation: €5-15 band shows optimal balance of
    volume (561 games) and quality (324 high-engagement titles)

COMMERCIAL INSIGHTS:
-------------------
12. Revenue Leaders: "This War of Mine" (RPI: 162.14, 49,829 reviews) and
    "BioShock Remastered" (RPI: 299.84) demonstrate premium pricing success
    
13. Publisher Performance: Top 10 publishers by RPI identified, with Ubisoft,
    Bandai Namco, and Square Enix leading commercial potential

================================================================================
                       TECHNICAL SPECIFICATIONS
================================================================================

SOFTWARE & TOOLS:
----------------
• PowerBI Desktop (Free Version)
• DAX (Data Analysis Expressions) for calculated measures
• PowerBI Bookmarks for mode switching
• Microsoft Azure Maps integration (for geographic visualization)

DASHBOARD FEATURES:
------------------
• 3 analytical modes with distinct visual themes
• 10+ interactive visualizations
• 5 core KPI cards with gradient styling
• 4 slicer filters (Name, Tags, Genres, Categories)
• Year filter for temporal analysis
• Dynamic country insight feature
• Mode switching via bookmark buttons
• Interactive tooltips on map visual
• Drill-down capabilities on charts

FILE SPECIFICATIONS:
-------------------
• File Format: .pbix (PowerBI Desktop file)
• File Size: ~9.2 MB
• Data Rows: 1,293 games (after filtering)
• Data Columns: 26 attributes
• Calculated Measures: 5+ custom DAX formulas
• Visuals: 10+ charts across 3 pages
• Bookmarks: 3 (one per mode)

COLOR PALETTES:
--------------
Professional Mode (Blue):
  • Header: #2B5797 (Corporate blue)
  • Card Gradient: #1E40AF → #2563EB → #3B82F6 → #60A5FA → #93C5FD
  • Charts: Blue tones (#1E40AF to #DBEAFE)
  • Background: #F8FAFC (Light gray-blue)

Gaming Mode (Dark + Gold):
  • Background: #1F1F1F (Dark charcoal)
  • Accent: #FCD34D (Gold/Yellow)
  • Text: #FFFFFF (White) and #9CA3AF (Gray)
  • Cinematic background image for immersion

Performance/Eco Mode (Green):
  • Header: #047857 (Dark teal-green)
  • Charts: Green tones (#059669, #10B981, #34D399)
  • Price bands: Green (sweet spot), Blue (entry), Gold (premium), Red (ultra)
  • Background: #F0FDF4 (Light mint)
  • Naming rationale: Green reinforces efficiency (eco) and optimization (performance)

================================================================================
                    CHALLENGES & SOLUTIONS
================================================================================

CHALLENGE 1: Data Quality - Zero Engagement Records
---------------------------------------------------
PROBLEM: 77% of original 10,000 games had zero playtime and zero reviews,
         indicating abandoned, unreleased, or non-viable titles.

SOLUTION: Implemented engagement-based filtering using criteria:
          (average_playtime > 0 OR total_reviews > 0)
          
RATIONALE: Zero-engagement games provide no actionable insights for publishing
           decisions. Including them would skew averages and create misleading
           visualizations.

OUTCOME: Filtered dataset of 1,293 games produces cleaner insights, more 
         accurate sentiment scores, and actionable publishing intelligence.


CHALLENGE 2: Revenue Metric Design
----------------------------------
PROBLEM: Simple price × reviews multiplication heavily favors viral free games
         with millions of reviews over quality paid games.

SOLUTION: Created Revenue Potential Index (RPI) using logarithmic scaling:
          RPI = Price × LOG10(total_reviews + 1)

RATIONALE: Log scaling balances volume (review count) against pricing while
           preventing free viral games from dominating the metric. This creates
           a more balanced view of commercial potential.

OUTCOME: RPI successfully identifies both high-volume hits (This War of Mine)
         and premium successes (BioShock Remastered) as top performers.


CHALLENGE 3: Genre Complexity
-----------------------------
PROBLEM: Steam games have multiple overlapping genres, making clean 
         classification difficult.

SOLUTION: Used "top_tag" field which represents the primary genre assigned
          by Steam's algorithm based on user tags.

RATIONALE: Primary genre provides cleanest categorization while still being
           user-generated and accurate.

OUTCOME: Clear genre distribution analysis with minimal overlap or ambiguity.


CHALLENGE 4: Geographic Data Standardization
--------------------------------------------
PROBLEM: Publisher country data included some "Unknown" entries and needed
         consistent formatting.

SOLUTION: Retained "Unknown" category for transparency rather than removing
          or imputing data. Standardized country names for consistency.

RATIONALE: Removing unknowns would reduce dataset size unnecessarily. Keeping
           them shows honest data management and acknowledges real-world data
           quality issues.

OUTCOME: Transparent geographic analysis with 16 clearly identified countries
         plus unknown category tracked separately.

================================================================================
                      LEARNINGS & REFLECTIONS
================================================================================

TECHNICAL SKILLS DEVELOPED:
--------------------------
• Advanced DAX formula creation for custom business metrics
• PowerBI bookmark implementation for multi-page navigation
• Color theory application for mode-based visual theming
• Interactive map visualization with geographic data
• Data quality assessment and professional filtering techniques
• Heatmap and matrix visualization for cross-dimensional analysis

BUSINESS INTELLIGENCE INSIGHTS:
-------------------------------
• Quality over quantity: 1,293 quality records > 10,000 noisy records
• Context-specific visualization: Different users need different views
• Actionable metrics: RPI more valuable than raw sales or review counts
• Visual hierarchy: Color can communicate data meaning (green = sweet spot)
• User-centric design: Dashboard should adapt to user context

DESIGN PHILOSOPHY:
-----------------
• Form follows function: Gaming Mode looks like games because users are gamers
• Consistency within variance: Each mode maintains data consistency while
  adapting visual presentation
• Accessibility: Multiple interaction methods (slicers, buttons, tooltips)
• Professional polish: Small details (gradients, spacing, borders) matter

PROJECT MANAGEMENT:
------------------
• Iterative development: Built and refined each mode sequentially
• User persona clarity: Defined distinct users for each mode
• Time management: Prioritized high-impact features first
• Quality assurance: Tested all interactive features before submission

FUTURE IMPROVEMENTS:
-------------------
If continuing this project, I would add:
1. Temporal trend analysis showing genre popularity changes over release years
2. Drill-through detail pages for individual game deep-dives
3. Predictive analytics using engagement patterns to forecast new game success
4. External data integration (Twitch viewership, Reddit sentiment)
5. Mobile-optimized responsive layouts for tablet viewing
6. Automated refresh for live Steam data updates
7. Additional modes (Competitive Analysis, Regional Deep-Dive)

================================================================================
                     BUSINESS VALUE & APPLICATIONS
================================================================================

USE CASES:
---------
1. STRATEGIC PLANNING (Professional Mode)
   • Market entry decisions: Identify undersaturated geographic regions
   • Genre portfolio balancing: Compare genre performance and saturation
   • Competitive positioning: Benchmark against regional leaders

2. PRODUCT DEVELOPMENT (Gaming Mode)
   • Genre selection: Choose genres with high sentiment scores
   • Pricing psychology: Understand player satisfaction by price point
   • Quality benchmarking: Target high-engagement performance standards

3. PRICING STRATEGY (Eco Mode)
   • Optimal pricing: €5-15 sweet spot identified with data support
   • Premium positioning: Evaluate €15-40 opportunities
   • Revenue forecasting: Use RPI to estimate commercial potential

4. PORTFOLIO MANAGEMENT
   • Risk assessment: Balance high-volume (€0-5) vs. premium (€15-40) titles
   • Market gaps: Identify underserved price bands or genres
   • Publisher analysis: Benchmark against top 10 commercial leaders

TARGET DECISION-MAKERS:
----------------------
• Publishing Executives: Market overview and investment decisions
• Product Managers: Genre and feature prioritization
• Pricing Analysts: Revenue optimization strategies
• Business Development: Partnership and acquisition targets
• Marketing Teams: Campaign targeting based on genre sentiment

ACTIONABLE RECOMMENDATIONS:
--------------------------
Based on dashboard insights, publishing recommendations include:

1. FOCUS ON €5-15 PRICE BAND
   • Contains 43% of market with highest absolute engagement
   • Shows optimal price-performance balance
   • Recommendation: Target this band for new releases

2. EXPLORE €15-40 PREMIUM OPPORTUNITY
   • Only 15% of market, indicating low competition
   • Strong engagement potential shown in stacked bar chart
   • Recommendation: Test premium pricing for quality titles

3. PRIORITIZE STRATEGY AND ACTION GENRES
   • Strategy achieves 0.99 sentiment (highest player satisfaction)
   • Action shows 58 high-engagement titles (largest quality volume)
   • Recommendation: Focus development on these proven genres

4. EXPAND GEOGRAPHIC REACH
   • Only 16 countries with active publishing presence
   • Opportunity to enter emerging markets
   • Recommendation: Research Asian and South American expansion

5. BENCHMARK AGAINST TOP PERFORMERS
   • Top 10 publishers by RPI provide performance targets
   • "This War of Mine" and "BioShock Remastered" show different success paths
   • Recommendation: Study both volume (reviews) and premium (price) strategies

================================================================================
                       USER GUIDE & NAVIGATION
================================================================================

GETTING STARTED:
---------------
1. Open Steam_Analysis_Ne.pbix in PowerBI Desktop
2. Dashboard opens in Professional Mode (default landing page)
3. Use mode buttons at top to switch between analytical views

MODE SWITCHING:
--------------
• Click "PERFORMANCE MODE" or "DISABLE PERFORMANCE..." button to toggle 
  Performance/Eco Mode
• Click "ENABLE GAME MODE" or "DISABLE GAME MODE" to switch to/from Gaming Mode
• Dashboard supports seamless switching between Professional Mode, Gaming Mode, 
  and Performance/Eco Mode
• Buttons are always visible at top of each page for easy navigation
• Current mode is indicated by button state and visual theme

FILTERING DATA:
--------------
Use the 4 slicers at the top of each page:
• NAME: Search for specific game titles
• TAGS: Filter by Steam user tags
• GENRES: Select specific game genres
• CATEGORIES: Filter by game categories

Additional filter:
• YEAR: Filter by release year (top right)

INTERACTIVE FEATURES:
--------------------
• MAP: Click countries to see focus; hover for tooltips
• CHARTS: Click bars/segments to cross-filter other visuals
• COUNTRY INSIGHT: Changes dynamically based on selected country
• TOOLTIPS: Hover over any visual for detailed information

RESETTING FILTERS:
-----------------
• Clear individual slicers using the eraser icon
• Click outside selected items to deselect
• Use "Clear All Filters" if available in your PowerBI version

EXPORTING DATA:
--------------
• Right-click any visual → "Export data" to CSV
• Use "File → Export → PDF" for presentation-ready output
• Screenshots can be taken using Windows Snipping Tool

================================================================================
                          REFERENCES & SOURCES
================================================================================

DATA SOURCE:
-----------
Steam Spy API (https://steamspy.com/)
• Platform: Independent analytics service for Steam games
• API Documentation: https://steamspy.com/api.php
• Data Provider: Steam Spy (founded by Sergey Galyonkin)
• Coverage: Comprehensive Steam catalog with ownership and engagement data
• Access: Public API with rate limiting, no authentication required
• Update Frequency: Daily data refresh from Steam public profiles
• Reliability: Industry-standard source used by game developers and publishers

Steam Platform (Valve Corporation)
• Original Data Source: Steam Store and Community profiles
• Platform: Steam digital distribution service
• Attributes: Pricing, reviews, playtime, publisher information
• Coverage: Global Steam catalog across 28+ countries
• Public Data: Game metadata, user reviews, pricing information

TOOLS & TECHNOLOGIES:
--------------------
• Microsoft PowerBI Desktop (Data visualization platform)
• DAX (Data Analysis Expressions) - Microsoft documentation
• Azure Maps (Geographic visualization component)

DESIGN INSPIRATION:
------------------
• Gaming graphics settings metaphor (Low/Medium/Ultra quality settings)
• Gaming industry best practices for player analytics
• Corporate BI dashboard standards for executive reporting
• Eco/efficiency mode concepts from software and hardware optimization

COLOR THEORY:
------------
• Blue: Trust, professionalism, corporate standards
• Green: Efficiency, balance, sustainability, "go" signal
• Gold/Yellow: Premium, attention, energy, gaming culture
• Dark themes: Immersion, focus, gaming aesthetics

BUSINESS INTELLIGENCE PRINCIPLES:
--------------------------------
• Data quality over volume (professional filtering practices)
• User-centric design (mode-based adaptation)
• Actionable insights over raw data (KPIs and RPI metric)
• Visual hierarchy (color-coded insights)

================================================================================
                         SUBMISSION CHECKLIST
================================================================================

FILES INCLUDED:
--------------
[✓] Steam_Analysis_Ne.pbix - Main PowerBI dashboard file
[✓] Steam_Dashboard_README.txt - This comprehensive documentation
[✓] Steam_Dashboard.docx - Microsoft Word version of documentation
[✓] Steam_Dashboard_Presentation.pptx - PowerPoint presentation slides
[✓] Supporting documentation as required by assignment brief

DOCUMENTATION FORMATS:
---------------------
This assignment includes comprehensive documentation in multiple formats:

1. README.txt - Plain text version for universal compatibility
2. README.docx - Microsoft Word document with professional formatting,
                 including tables, formatted sections, and visual hierarchyn
4. Presentation.pptx - PowerPoint slides for 4-minute presentation including:
   • Title slide with student information
   • Introduction to 3-mode concept
   • Dashboard screenshots (Professional, Gaming, Performance/Eco modes)
   • Key insights and findings
   • Technical implementation details
   • Business value and recommendations
   • Conclusion and Q&A slide

DASHBOARD COMPLETENESS:
----------------------
[✓] Professional Mode - Complete with blue gradient theme
[✓] Gaming Mode - Complete with dark + gold cinematic theme
[✓] Performance/Eco Mode - Complete with green efficiency theme
[✓] Mode switching buttons functional
[✓] All slicers working (Name, Tags, Genres, Categories)
[✓] All 5 KPIs displaying correctly
[✓] 10+ visuals across 3 modes
[✓] Interactive features tested
[✓] Data filtering applied (1,293 games)
[✓] DAX measures created and functional

DOCUMENTATION:
-------------
[✓] Executive summary included
[✓] Data source documented (Steam Spy API)
[✓] Data filtering rationale documented
[✓] Mode descriptions written (Professional, Gaming, Performance/Eco)
[✓] Key insights identified
[✓] Technical specifications listed
[✓] Challenges and solutions documented
[✓] Business value articulated
[✓] Multiple documentation formats (TXT, DOCX, HTML, PPTX)

PRESENTATION PREPARATION:
------------------------
[✓] 3-mode concept clearly articulated
[✓] Data filtering justification prepared
[✓] Key insights memorized
[✓] Technical implementation understood
[✓] Question responses rehearsed
[✓] 4-minute timing practiced

================================================================================
                         FREQUENTLY ASKED QUESTIONS
================================================================================

Q: Why only 1,293 games instead of all 10,000?
A: Professional BI practice prioritizes quality over quantity. 77% of the 
   original games had zero engagement (no playtime, no reviews), which would 
   skew insights and create misleading visualizations. The filtered dataset 
   is statistically valid and produces more actionable intelligence.

Q: How was Revenue Potential Index (RPI) calculated?
A: RPI = Price × LOG10(total_reviews + 1). This formula balances pricing 
   against review volume using logarithmic scaling to prevent viral free 
   games from dominating the metric while still recognizing their reach.

Q: Why three modes instead of one comprehensive dashboard?
A: Different stakeholders need different perspectives. Executives need 
   corporate aesthetics (Professional Mode), product teams benefit from 
   gaming-aligned visuals (Gaming Mode), and analysts need efficiency-focused 
   pricing views (Eco Mode). The 3-mode system serves all users optimally.

Q: Can this dashboard be used with real-time Steam data?
A: Yes, with modifications. PowerBI can connect to live data sources. The 
   current version uses a static dataset snapshot, but could be configured 
   for automated refresh with Steam API integration.

Q: Why is it called "Performance/Eco Mode" instead of just one name?
A: The dual naming captures both aspects of this analytical view. "Performance" 
   emphasizes revenue optimization and commercial success metrics. "Eco" 
   represents efficiency, balance, and sustainable pricing strategy—drawing 
   from gaming terminology where "eco rounds" refer to resource optimization. 
   Together, they communicate that this mode focuses on balanced, efficient 
   revenue strategy. The green color scheme reinforces both concepts: efficiency 
   (eco-friendly) and optimization (high-performance).

Q: What is the most important insight from this dashboard?
A: The €5-15 pricing sweet spot is underutilized. It contains 43% of games, 
   shows the highest engagement (324 high-engagement titles), yet represents 
   a massive market opportunity for new publishing decisions.

================================================================================
                              CONCLUSION
================================================================================

This Steam Market Analytics Dashboard demonstrates professional-grade business
intelligence capabilities through innovative multi-mode design, rigorous data
quality management, and actionable strategic insights.

The three-mode system—Professional, Gaming, and Eco—provides a comprehensive
analytical framework that serves diverse stakeholders from executive leadership
to pricing specialists, all while maintaining consistent data integrity.

Key achievements include:
• Smart data filtering (1,293 quality games from 10,000 original records)
• Custom business metrics (Revenue Potential Index)
• Advanced visualizations (interactive maps, heatmaps, scatter plots)
• Innovative mode-based navigation system
• Clear, actionable publishing recommendations

The dashboard successfully transforms raw Steam catalog data into strategic
intelligence that can guide market entry, genre selection, pricing strategy,
and portfolio management decisions in the competitive gaming market.

This project represents not just technical proficiency in PowerBI and DAX,
but also demonstrates critical thinking in data quality management, creative
problem-solving in multi-mode design, and business acumen in generating
actionable insights from complex datasets.

================================================================================
                           CONTACT INFORMATION
================================================================================

For questions about this dashboard or its methodology:

Student:     Nikhil Upadhyay
Student ID:  2066392
Email:       Nikhil25000@gmail.com
Course:      MSc Business Analytics
Institution: Dublin Business School
Module:      Business Intelligence & Visualization
Date:        December 9, 2025

================================================================================
                            ACKNOWLEDGMENTS
================================================================================

• Dublin Business School Faculty for Business Intelligence & Visualization 
  instruction and guidance throughout the module
• Steam Spy (Sergey Galyonkin) for providing comprehensive Steam analytics 
  via public API access
• Steam/Valve Corporation for maintaining publicly available game metadata 
  and community features
• PowerBI Community for technical guidance and best practices
• Gaming industry for inspiring the multi-mode dashboard concept

================================================================================
                          END OF DOCUMENTATION
================================================================================

Last Updated: December 9, 2025
Version: 1.0 (Final Submission)
Document: Steam_Dashboard_README.txt
Associated File: Steam Dashboard Analysis.pbix

================================================================================
