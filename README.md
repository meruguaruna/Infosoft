Problem 3 explanation where i make changes
Added the condition node.start < self.end and node.end > self.start to check if the new event overlaps with the current node.
This ensures that two events cannot overlap even partially.
Events that start after or at the end of the current event (node.start >= self.end) are inserted into the right_child.
Events that end before or at the start of the current event (node.end <= self.start) are inserted into the left_child.
If the calendar is empty (self.root is None), the first event becomes the root node.
