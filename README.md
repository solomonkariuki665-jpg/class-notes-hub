Class Notes Hub

A simple website for keeping university class notes in one place, hosted on AWS EC2.

Built by Solomon Kariuki Kihumba, Actuarial Science student at Multimedia University of Kenya (MMU).

What's in this repo
File	Purpose
index.html	The static website (the front page of the notes hub)
user-data.sh	EC2 user data script that sets up the server and deploys the site on launch
README.md	This file
How it works
Launch an EC2 instance on AWS.
Paste the contents of user-data.sh into the User data field (Advanced details) when launching.
When the instance boots, the script runs automatically and serves index.html.
Open the instance's public IP address in your browser to see the site.

Make sure the instance's security group allows inbound HTTP (port 80).

Run it locally

No build step is needed. Clone the repo and open the page in your browser:

bash
git clone https://github.com/solomonkariuki665-jpg/class-notes-hub.git
cd class-notes-hub
xdg-open index.html
Updating the notes
bash
git pull                      # get the latest version
# edit index.html or add new files
git add .
git commit -m "Describe what you changed"
git push
Tech used
HTML (static site)
Bash (EC2 user data script)
AWS EC2
Git and GitHub
Roadmap
[ ] Add notes organised by course
[ ] Improve the site design
[ ] Add a search feature
Author

Solomon Kariuki Kihumba GitHub: @solomonkariuki665-jpg
