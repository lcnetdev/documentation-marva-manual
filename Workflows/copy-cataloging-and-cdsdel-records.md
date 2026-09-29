# Copy cataloging and cdsdel records

When there is a copycat record that has an LCCN in Folio but does not exist in the BFDB:

1.	Go to Folio and search for the record by ISBN.
a.	If the resulting record has: 001 cdsdel_
2.	Open the bib record in Folio
a.	delete the LCCN
b.	save the record
3.	Derive a copy of the record
a.	Add the LCCN to the newly derived record	
b.	Save the new record
4.	Mark the original record (the one without an LCCN) for deletion
5.	Go back to MARVA Copy Cat Search
a.	Search OCLC and check for an existing record by searching by LCCN
b.	If the derived record does not show up, do a record sync

Background: Over the years various records (many epcn records for 
which no books were received) were marked for deletion, and
original system numbers were replaced with system numbers beginning 
with cdsdel_ With the migration to Folio, these records were suppressed.
