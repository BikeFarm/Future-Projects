Bike Farm Ox
============
We aim to write micro web services to help Bike Farm's shop operations. We have a desire to create a better user experience for our volunteer\member time tracking and our cash log. We currently use Google Forms and Google Docs to handle user input and data storage. The limits of these applications are hindering any furthur development on our goals so we are figure out a new solution.

Project Planning
---------------
This project will start with an ___exploratory phase___, then an ___build out phase___, then a ___deployment and enhancment phase___.  The ___exploratory phase___ will define what our architecture will be and determine the detailed requirements to reach pairity with our current system. The ___build out phase___ will build, test, and gain approval from Bike Farm. It should have pairity with the current system at the very least. Finally, the ___deployment and enhancement phase___ will take our new system live and we will continue to maintain the software. Ideally we will complete the first two phases in a minimal amount of time, and the last phase will allow iterative development of new features and bug fixes.

Ideas
=====
Architecture
------------
To keep pairity, we would like to continue to integrate with Google Docs. Google docs has spreadsheets that our accountant use to collect data. No additional training is required to access this information. However, this is dependent on a working internet connection and the organizations willingness to use this in the future. We want to write an application, perhaps a web or chrome app that works independently from Google Spreadsheets. This solution creates a local service that persists a database of our cash logs and volunteer hours and will back itself up to Google Spreadsheets.

User Application (Chrome App) [local data storage] <-> Local Service [long term data storage] <-> Google Spreadsheet [long term data storage that is synced]

This should help decouple the front end application from Google Spreadsheets just incase we want to move on to something different. The draw back is that it pushes us away from Google Spreadsheets in the long run. It is not desireable to maintain synchronization code as our spreadsheets and local data storage changes. It is still worth concidering if we want to contain this within the chrome app itself.
