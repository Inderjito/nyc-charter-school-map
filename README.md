# NYC Charter School Explorer

**An interactive map and searchable directory of New York City charter school locations.**

[**View Live Interactive Map**](https://inderjito.github.io/nyc-charter-school-map/)

## Project Overview

The NYC Charter School Explorer is a lightweight, browser-based application designed to help users discover and explore charter school locations across New York City's five boroughs.

The application combines publicly available New York State education geospatial data with an interactive map, school directory, and filtering capabilities.

The goal was to deliver a functional, accessible, and easy-to-use mapping experience without requiring users to install software, create accounts, or configure API keys.

## Key Features

- **Interactive NYC map:** Explore charter school locations using clickable map markers.
- **Five-borough coverage:** View records across the Bronx, Brooklyn, Manhattan, Queens, and Staten Island.
- **Search functionality:** Find schools by name, address, or ZIP code.
- **Borough filtering:** Narrow the results to a specific borough.
- **Dynamic school count:** See the number of records matching the selected filters.
- **School details:** View school names, physical addresses, and borough information.
- **Google Maps integration:** Open directions to a selected school.
- **Responsive interface:** Designed for desktop and mobile browsers.

## Live Application

**[Launch NYC Charter School Explorer](https://inderjito.github.io/nyc-charter-school-map/)**

The application runs directly in the browser and is hosted using GitHub Pages.

No installation or login is required.

## Data Source

The application retrieves publicly available charter school geospatial records from **New York State ITS Geospatial Services**, based on New York State Education Department information.

**References:**

- [New York State Education Department — Charter School Directory](https://www.nysed.gov/charter-schools/charter-schools-directory)
- [New York State GIS Clearinghouse](https://gis.ny.gov/)

The application queries a New York State ArcGIS Feature Service, processes the returned geographic records, and filters them to the five NYC boroughs.

At the time of testing, the application displayed **425 mapped charter school records**.

### Data Quality and Coverage Considerations

The displayed count represents records returned from the geospatial dataset, not necessarily the number of unique, currently operating charter school campuses.

Important considerations include:

- The source may contain school-level records representing multiple grades, divisions, or locations.
- Current operating status is not independently verified.
- Geospatial records may not reflect the latest openings, closures, relocations, or directory updates.
- Multiple records may share the same physical address.

**This application should be considered an exploratory mapping tool, not a certified or exhaustive current directory of operating NYC charter schools.**

A production-ready version would reconcile the mapped locations against the latest official NYSED charter school directory and apply school-level and campus-level deduplication rules.

## Technology Stack

| Technology | Purpose |
|---|---|
| HTML5 | Application structure |
| CSS3 | Layout and responsive styling |
| JavaScript | Data retrieval, filtering, and interaction |
| Leaflet.js | Interactive map and school markers |
| OpenStreetMap / HOT | Map background tiles |
| NYS ArcGIS REST API | School geospatial records |
| GitHub Pages | Static website hosting |

The application uses a lightweight architecture without a backend server or database.

## How It Works

1. **Retrieve:** Request school records from the New York State ArcGIS geospatial service.
2. **Process:** Normalize school names, addresses, and geographic coordinates.
3. **Filter:** Restrict the results to the five New York City boroughs.
4. **Visualize:** Display matching locations as interactive map markers.
5. **Explore:** Allow users to search, filter, select schools, and open directions.

## Running the Project Locally

1. Clone the repository:

   `git clone https://github.com/Inderjito/nyc-charter-school-map.git`

2. Open the project folder.

3. Open `index.html` in a modern web browser.

An internet connection is required to retrieve school records, map tiles, and the Leaflet library.

## Product Decisions and Trade-offs

**1. Prioritized a functional minimum viable product (MVP).**

Focused on the core user journey: locating NYC charter schools and exploring them by borough or search term.

**2. Used publicly available education data.**

Selected an existing government geospatial service to avoid manually maintaining school coordinates.

**3. Kept the architecture simple.**

Used JavaScript, Leaflet, and GitHub Pages to minimize deployment complexity and ongoing infrastructure requirements.

**4. Made data limitations transparent.**

Distinguished mapped source records from a verified count of operating campuses rather than presenting potentially misleading totals.

**5. Designed for immediate access.**

Provided a live, shareable website that works without registration or installation.

## Future Enhancements

With additional development time, potential improvements include:

- Reconcile mapped records against the latest NYSED directory to validate current operating status and completeness.
- Deduplicate records and distinguish charter school organizations, schools, and physical campuses.
- Add grade-level and school-operator filters where authoritative data is available.
- Add marker clustering to improve readability in dense areas.
- Display the data refresh date and source metadata.
- Add automated data validation and monitoring for API failures or changes.
- Improve accessibility and conduct cross-browser and mobile usability testing.

## Project Status

**Functional MVP**

The interactive map, school directory, school search, and borough filtering have been tested successfully in a browser.

The application is intended as a demonstration of rapid product development, geospatial data integration, and user-centered design.

---

**Developed as a technical take-home project for the Leader, AI Product Manager opportunity at Success Academy Charter Schools.**
