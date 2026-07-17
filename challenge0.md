#code challge 0

driver : Rahul
reporter : jordan
verifier: kensho


prediction : I think the best time would be (9-11)

      FUNCTION find_best_study_time

1. Create an empty list to store all start and end events.

2. For each student's availability interval:
      - Record the start time as a START event.
      - Record the end time as an END event.

3. Sort all events by time.
      - If a START and an END happen at the same time,
        process the END event first.

4. Set the current attendance to 0.

5. Set the maximum attendance to 0.

6. Set the best study interval to empty.

7. Process each event in order:
      - If the event is a START event, increase the current attendance by 1.
      - If the event is an END event, decrease the current attendance by 1.

8. After processing the events at the current time:
      - Compare the current attendance with the maximum attendance.
      - If the current attendance is greater than the maximum,
        save the current interval as the best interval and update the maximum attendance.

9. Continue until all events have been processed.

10. Return the best study interval and the maximum number of students who can attend.

END FUNCTION

#Real World Scenarios better suited for Static and Dynamic Structures

      # shortest_route.py

class CampusMap:
    def __init__(self):
        self.graph = {}

    def add_location(self, location: str) -> None:
        if location not in self.graph:
            self.graph[location] = {}

    def add_path(self, first: str, second: str, distance: int) -> None:
        self.add_location(first)
        self.add_location(second)
        self.graph[first][second] = distance
        self.graph[second][first] = distance

    def find_shortest_route(
        self, start: str, destination: str
    ) -> tuple[int | float, list[str]]:
        """
        Return (distance, route) for the shortest route from start to destination.

        Return (float('inf'), []) if destination cannot be reached.
        """
        # YOUR CODE HERE
        pass  # Erase this line when you add your own code


ensign = CampusMap()

ensign.add_path("Mathematics", "Admissions", 5)
ensign.add_path("Library", "IT Offices", 6)
ensign.add_path("Interior Design", "Computer Science", 4)
ensign.add_path("Administration", "Admissions", 8)
ensign.add_path("Business", "Outpost", 5)
ensign.add_path("Computer Science", "Outpost", 3)
ensign.add_path("Library", "Admissions", 1)
ensign.add_path("Communications", "Mathematics", 2)
ensign.add_path("Administration", "Mathematics", 3)
ensign.add_path("Administration", "Interior Design", 2)
ensign.add_path("Library", "Outpost", 2)
ensign.add_path("Admissions", "Business", 4)
ensign.add_path("Outpost", "Administration", 9)
ensign.add_path("IT Offices", "Administration", 1)
ensign.add_path("Mathematics", "Computer Science", 3)
ensign.add_path("Business", "Library", 3)

distance, route = ensign.find_shortest_route("Business", "Computer Science")
print(f"Distance: {distance}")
print(f"Route: {' -> '.join(route)}")
