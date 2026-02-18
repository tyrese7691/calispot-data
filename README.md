CaliSpot is a location-based web application that helps users discover outdoor calisthenics spots, filter them by available equipment, and save favourites.
Live app: https://apps.apple.com/gb/app/calispot/id6747050360
Tech stack: JavaScript, React, Next.js

Problem
Finding reliable outdoor calisthenics spots is fragmented across social media, Google Maps, and word of mouth. Equipment availability is often unclear, outdated, or missing entirely.
CaliSpot solves this by providing a single, structured source of spot information with clear equipment tagging and map-based discovery.

Key Features
Browse calisthenics spots on an interactive map
Filter spots by available equipment
View detailed spot information and photos
Save favourite spots for quick access
Responsive UI for mobile and desktop

How It Works 
Spot data is stored in a structured JSON format
The application loads this data and stores it in component state
Users apply filters via the UI, which updates the displayed spots
List views re-render based on the active filters
This approach keeps the interface fast and easy to reason about for the current dataset size.

Technical Decisions
Client-side filtering: Chosen because the dataset is small and allows instant UI feedback
Structured equipment tags: Enables consistent filtering and prevents ambiguous results
Component-based UI: Keeps map, filters, and list views isolated and maintainable

Challenges & Solutions
Issue:
Some spots had missing or inconsistent equipment tags, which caused filtering to behave unpredictably.
Solution:
Standardised the data so every spot includes an explicit tags field and updated the filtering logic to safely handle empty values.

Future Improvements
Add validation to catch incorrect or missing tags earlier
Display the number of matching spots for each filter option
Move filtering to a data layer if the dataset grows significantly

About the Developer
Built and maintained by Tyrese Bewry as a real-world project to explore frontend development, data-driven UI, and iterative problem solving.
