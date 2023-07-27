## Process

### Problem 
My favorite basketball team is the Warriors. I currently live in Louisiana and am willing to travel to Texas and Tennessee to watch a game. I also want my sister to be able to see Lebron James play live - she doesn't care what team he is on. To plan basketball game trips, I often look up the Warriors schedule and see when they are in nearby cities (New Orleans, Memphis, Houston, Dallas, or San Antonio) - and sometimes San Francisco or L.A. if my spouse and I have a trip planned. I also look up the Lakers shedule to see when they are in Memphis or New Orleans so my sister doesn't have to drive too far from Mississippi. I - and I'm sure others - would like to be able to plan game days without sifting through different team schedules.

### Needs
- NBA game schedule with host team, visiting team, and date
  - NBA API? Use last year's data for now since schedule isn't out for this NBA season?
    - Add info to a database
  	  - Delete info from database yearly so only searching current season
      - Store NBA teams name, city, state, stadium, and players
      - Update db schedule and player's team monthly? Weekly?

### Possible UX
- Chatbot or similar NLP if I want user to be able to ask a question and get an answer (natural experience for the user, not as difficult to process the language for me)
- User selects from dropdown lists (desired team, city, date(s), etc)

### Questions to answer in SQL or by Alexa
- When do [team] play [team]? Ex: When do the Warriors play the Grizzlies?
- When do [team] and [team] play? Ex: When do the Warriors and the Lakers play?
- When are [team] at [team]? Ex: When are the Warriors at the Pelicans? (*note*: at signifies host)
- When are [team] at [stadium]? Ex: When are the Warriors at Chase Center?
- When are [team] at home? Ex: When are the Warriors at home?
- When are [team] in [city]? Ex: When are the Warriors in New Orleans?
- When are [team] in [state]? Ex: When are the Warriors in Texas? (*note*: some states have multiple teams)
- When is [player] in [city]? Ex: When is Lebron James in Memphis?
- When is [player] in [state]? Ex: When is Lebron James in Tennessee?
- When is [team/player] in [city/state]? *allow multiple city/state Ex: Whe is Lebron James in Memphis or Texas?
- When does [player] play [team]? Ex: When does Lebron James play the Warriors?
- Are [team/player] in [city/state] on [date]? Ex: Are the Warriors in San Francisco on 12/25/2023?
- Are [team/player] in [city/state] from [date range]? Ex: Are the Warriors in New York from 12/19/2023-12/25/2023?
- Are [team/player] in [city/state] in the [season]? Ex: Are the Warriors in New Orleans, Texas, or Memphis in the spring?
- Are [team/player] at [team/stadium] on [date]? Ex: Are the Warriors at the Nets on March 20, 2024?
- Are [team/player] at [team/stadium] from [date range]? Ex: Are the Warriors at the Nets or the Knicks from March 13, 2024-March 27, 2024?
- Are [team/player] at [team/stadium] next [season]? Ex: Are the Warriors at the Nets or the Knicks next spring?
- Do [team/player] play [team/player] on [date]? Ex: Do the Warriors play the Nuggets on 12/25/2023?
- Are [team/player] at [team/player] from [date range]? Ex: Is Lebron James at Memphis from October 1, 2023-1/6/2024?
- Are [team/player] at [team/player] in the [season]? Ex: Is Lebron James at Memphis in the fall?

### Tradeoffs
- Store players as JSON in teams table or have a players table since they can be traded but not super frequently?
- MySQL or PostgreSQL?
- API or web scraping?
