HTTP server running on the respository is required for it to work, i.e. python -m http.server 8000

The visualization shows procurement data. I used sample data but the code should be theoretically able to create the visualization for any dataset in the right format. The arrow points to the buyer and side with no arrow is the seller. There are 500 procurements shown in the visualization made between 825 people. People are organized by number of procurements made. The lines color depends on the price of the procurement, the legend is on the right side. The position of the line depends on the time of the procurement and matches the axis on top. 

Actions: 

•	Expanding/Collapsing: People are collapsed into bins by the number of procurements made. By clicking on the triangle right of the number of procurements it will expand/collapse the people inside the bin. Showing their names/numbers and the procurements they’ve made.

•	Hovering: Hovering over a procurement line will show who the buyer and seller are and also the price of procurement, the item procured, and the exact time of the procurement. 

•	Selecting: People can be selected/unselected shown by the circle left of the person name/number. Red is selected and white unselected. Procurement lines between two unselected people are dimmed, grayed and won’t show information on hover. 

-o	Select All: Clicking on the top left circle next to select/unselect all text will select everyone if they are not all already selected. If they are all selected it will unselect all. 

-o	Bin Selecting: Similar to selecting all, by clicking on the circle left of the bin it will select everyone in the bin if not all selected and unselect all if they are. Other People line can also be selected/unselected selecting/unselecting everyone in the group. 

-o	Group selecting: On expanded bins under the selecting circle there will be a rectangle. Clicking on the rectangle will draw a red line and clicking again will draw a red rectangle between the red line and where you clicked the second time. People within the red rectangle (marked by the tiny red dots inside the rectangle) will be all selected if they are not all already and unselect all if they are all selected. Red rectangle will disappear by clicking anywhere in the visualization.

-o	Individual Selecting: Clicking on the circle left of the person’s name/number will select/unselect him. 

•	Deleting People: Clicking on the process button on the top left will delete any unselected people. If everyone in a bin is deleted the bin will be deleted too. If there is a procurement line going from a non-deleted person to deleted one the procurement line will go to the other people line. The other people line can also be deleted, then if one person is deleted the procurement line will be too. If the lowest or highest price procurement line is deleted it will update the procurement price legend and the colors of all the procurement lines. Clicking on the restore button on the top left of the screen will restore all deleted people, select everyone, and collapse all bins. 

•	Swapping: People and bins can be swapped. Clicking on a bin’s text or a person’s name/number will change the color of the clicked text to red. Clicking on a different bin or person will swap the two. Clicking on people in different bins won’t swap them, it will highlight both red and swap with the next clicked within the same bin. Other people line can be swapped with bins. 

•	Filtering by time: Clicking once on the timeline will draw a red line on the timeline. Clicking a second time will zoom into the timeline to show just the time in between the two clicks. The time interval between ticks will be appropriately reduced to 15, 5, and 1 min. Procurement lines will be appropriately updated, deleting any lines outside of the two clicked times and moving the ones inside to their correct place. It will update the procurement price legend and colors of the lines same way deleting people does. Clicking on the restore button right of the timeline restores the timeline and updates the colors and legend appropriately taking in count deleted people too. 

•	Filtering by price: The procurement legend has two draggable slides, can be dragged by using the circles below the colored rectangle. They slide from the max/min and can’t go past the other slide. The text below the slide can be clicked and it allows the user to manually enter the price of the slide. It accepts values between min/max (depending if it’s the left or right slide) and the other slide. It will automatically update the position of the slide. Clicking on the process button inside the procurement price legend will remove any procurement lines not within the prices of the two slides and will update the legend and colors of the procurement lines according to the new maximum and minimum prices of procurements. Clicking on restore in the procurement price legend will restore the colors of procurement lines and legend to the maximum and minimum price without filtering by price.  
