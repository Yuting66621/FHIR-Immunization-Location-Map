# Immunization Location Map

## Project Overview
This project visualizes patient immunization records on an interactive map using Leaflet.js and FHIR API data. It displays a specific patient's vaccination history with geographic markers showing where each immunization was administered.

## Data Source
- **FHIR Server**: https://r3.smarthealthit.org
- **Patient ID**: 30d44805-5e26-4f59-9cac-6ce7bd9b1058
- **Resources Used**: Immunization

## Features
- Interactive map with markers for each immunization
- Hover tooltip showing: Immunization ID, Vaccine name, and Date
- Click popup displaying: Full details including coordinates
- Delete button to remove markers
- Auto-zoom on marker click

## Data Limitation & Solution
During development, I encountered a data limitation with the FHIR test server:

1. **Issue**: The Immunization resources in the FHIR API do not contain direct `location` or `position` fields
2. **Investigation**: I searched for Location resources on the server and found that only 2 unique geographic coordinates exist, with most locations being duplicates (same hospitals appearing multiple times)
3. **Solution**: To demonstrate the mapping functionality for this assignment, I generated random coordinates within North Carolina (where the patient is located) to represent immunization locations

This approach allows the project to fulfill the assignment requirements of creating an interactive geographic visualization while acknowledging the real-world data constraints of the test FHIR server.

## How to Use
1. Open the HTML file in a web browser
2. The map will automatically load and display 4 immunization markers
3. Hover over markers to see basic information
4. Click markers to view detailed information and zoom in
5. Click [X] button in popup to remove a marker

## Technologies Used
- Leaflet.js for mapping
- jQuery for AJAX requests
- FHIR API for healthcare data
- OpenStreetMap for map tiles

## Assignment
This project was completed as a class assignment for CHIP690.297 (Developing Health Apps with JavaScript and FHIR) at UNC-Chapel Hill.# FHIR-Immunization-Location-Map
