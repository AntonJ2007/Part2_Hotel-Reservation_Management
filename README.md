# Part2_Hotel-Reservation_Management

SmartStay: Hotel Reservation and Room Allocation System
Short Description

SmartStay is a hotel reservation and room allocation system for small and mid-size hotels. It builds on the Hotel Time Johor Bahru system (Koh & Hassim, 2021) and addresses its main weakness: there is no real-time conflict handling, so double booking is possible.

Guests can search availability by date range, book rooms, and join a waitlist for fully booked dates. Front desk staff can confirm, cancel, move, check in and check out bookings. Housekeeping gets a prioritized cleaning list, and admins get sorted reports, reward points and vouchers.

The system is built around these data structures and algorithms:

Feature	Data structure / algorithm
Fast lookup of guests, bookings and rooms	Hash table (O(1) average)
Availability check and double-booking prevention	Sorted list per room with binary search and interval-overlap check
Housekeeping priority (e.g., same-day arrivals first)	Min-heap priority queue
Waitlist for fully booked dates	FIFO queue
Sorted reservations and reports (by date, name, amount)	Merge sort
Instructions on How to Run the Project

I don’t have your source code, so these steps assume a Python console implementation with main.py as the entry point. Adjust the file names and commands to match your project.

Requirements: Python 3.10 or later. The project uses only the standard library (heapq, collections, datetime, bisect), so nothing needs to be installed.
Get the project: Download or clone the project folder and open a terminal in it:
cd smartstay

Run the program:
python main.py

On some systems, use python3 main.py.
4. Use the menu: Choose a role at the main menu and follow the prompts:

Guest: search availability, make or cancel a booking, join the waitlist.
Front desk: search by name or reference, confirm or cancel, change room, check in or out.
Housekeeping: view and complete cleaning tasks in priority order.
Admin: view sorted daily reports, rewards and vouchers.
Try these scenarios to see the algorithms work:
Book a room, then try to book the same room for overlapping dates. The system should reject it (interval-overlap check).
Fully book a date range and join the waitlist, then cancel one booking. The first guest in line should be offered the room (FIFO queue).
Check out two guests, one with a same-day arrival next, and the room for the same-day arrival should appear first in the cleaning list (min-heap).
