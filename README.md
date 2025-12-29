# Table Schema

## Events
- Event Name (Primary)
- Event Code (Formula)
- Status (Planning, Confirmed, Completed)
- Start Date
- End Date
- Venue (Linked → Venues)
- Artists (Linked → Artists)
- Assets Required (Linked → Assets)
- Event Manager (Linked → Staff)
- Budget
- Notes

## Artists
- Artist Name (Primary)
- Genre
- Country
- Email
- Phone
- Events (Linked → Events)
- Contract Sent (Checkbox)

## Venues
- Venue Name (Primary)
- Location
- Capacity
- Indoor / Outdoor
- Events (Linked → Events)

## Assets
- Asset Name (Primary)
- Asset Type
- Quantity
- Assigned Events (Linked → Events)
- Return Date
- Status (Available, In Use, Returned)

## Staff
- Staff Name (Primary)
- Role
- Email
- Assigned Events (Linked → Events)
- Tasks (Linked → Tasks)
- Notes

## Tasks
- Task Name (Primary)
- Event (Linked → Events)
- Assigned To (Linked → Staff)
- Due Date
- Status (To Do, In Progress, Done)

