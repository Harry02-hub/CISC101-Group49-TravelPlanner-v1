

Generate a filtered list of activites that match the users preferences, budget, dietiery needs, accessibility, and importents bust-see items.

required feild
- id
- Name
- type
- Theme
- Location
- Distanve_from_lodging (in minutes)
- Duration (minutes)
- cost_range (CAD)
- open_hours
- weather_suitabalitiy (indoor/outdoor)

  Optional feilds
  - booking
  - accesibility
  - popularity
  - tags
    if the lodging location is missing, use a landmork and label distance as "approximate"

    Use time-window blocks and transit buffers to build the days

    Time window
    - morning 8:00-12:00
    - Noon 12:00-15:00
    - after noon 15:00-18:00
    - Evening 18:00-21:00

    ADD atlest 30-45 minute buffer between activities for trevel; prefered around 30 minutes of travel times.

    Morning
    -choose activity near the lodging
    -must open by 8:00-10:00
    -if weather is bad prefered it to be indoor

    Noon
    - activity should be close enough to the last activity
    - include luch and match any dietary needs
    - within the hours
   
      after noon
      - different theme from noon
      - within the provided time window
      - maintain the 30 transit time
     
      Evening
      - choose restauratn within budget
      - optionally add an event if enough time is left

    Constraints 
    - Avoid repeating the same actviites and thems across the same day
    - renforce the budget limit
    - make sure that all ativities are wihting the time-window
    - incorporate accessible routes and venues when requested
    - prevent long walks:
    - provide indoor or outdoor depending on the weather
    - make sure to leave a gap betwwen activitys for transti

    if no activity fitls the slot
    - provide a new activity that fits in the slot and meets all the requirments
    - if the timin is too time, create a shorter duration of activiites
    - if exceeds the budgets, select free or any activites within the budget

    Edge casses
    -Missing lodging: annotate the travel time as estimation
    -if weather is bad: recoment more indoor activites
    - if booking required: swap or flag
    - budget: if budget exceed suggest a free activites or a cheaper one to stay within the budget
    
