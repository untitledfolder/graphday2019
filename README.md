# Philly GraphDB - Graph Day April 15, 2019

Celebrating Leonhard Euler's birthday!

## Event Details

Read more about what makes [Graph Day Graph Day here](https://neo4j.com/blog/leonhard-euler-global-graph-celebration-day/)

Excerpt from Karin Wolok:

"Join us and the global Neo4j community on April 15, 2019 to celebrate the birth of the inventor of graph theory, Leonhard Euler!. Help us lead this day of celebration, collaboration and advocacy around the topic of graph-thinking and those who have accelerated thought leadership in this space.

We invite our Neo4j community members around the world to participate by hosting a local event or gathering with friends and colleagues on this monumental day! We plan to build a big graph from the events and attendees on [GlobalGraphCelebrationDay](GlobalGraphCelebrationDay.com)"

Also from Karin, a video for more information: [Hello on Global Graph Celebration Day!](https://www.youtube.com/watch?v=LJKxgRDpsm0&feature=youtu.be)

## Graph Day Community Graph

[Neo4j DB - user: event, password: event](https://88f0bc82.databases.neo4j.io/browser/)

Some templated queries:

```
/// Find any events in New York and who is attending:
MATCH path=(e:Event)<-[:ATTENDING]-(p:Person)
WHERE e.City CONTAINS "New York"
RETURN path

/// Which event has the most attendees interested in GraphQL?
MATCH (e:Event)<-[:ATTENDING]-(p:Person)-[:USES]->(:Tool {name: "GraphQL"})
RETURN e.City AS city, e.Description AS description, COUNT(p) AS num
ORDER BY num DESC LIMIT 10
```

## Project Details

Example of what we are trying to do: [Hardest puzzle](https://miro.com/app/board/o9J_kxv70t4=/)
Project Details: [Realtime Board](https://miro.com/app/board/o9J_kxv70t4=/)
