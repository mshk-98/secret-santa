Family Secret Santa

A tiny web app for running a Secret Santa draw. It works on any phone or computer, with nothing to install.

How it works
The organizer enters everyone's names and any pairs who shouldn't draw each other.
The app runs the draw in the browser and creates one private link per person.
Each person opens their own link, taps Show who I drew, and sees who they're buying for.

There is no server and no database. Each person's match is encoded inside their link, so nothing is stored anywhere.

Run it yourself
Create a public GitHub repository.
Upload index.html and this README.
Go to Settings → Pages, set the source to Deploy from a branch, choose main and / (root), then save.
After a minute or two, your app is live at https://<your-username>.github.io/<repo-name>/.
Using it
Open the live address, add names (one per line), and add optional exclusions as Name, Name pairs.
Click Run the draw, then copy each person's link and send it to them privately.
Organizers: don't open your own link if you want to be surprised.
Run the draw only once. Running it again creates new links, and the old ones will still work.
Privacy

Links hide the match from casual viewing, but they are encoded rather than encrypted. Anyone who knows how to decode a link could read it. That's fine for a family gift exchange, but not for anything sensitive.

Files
index.html: the whole app (HTML, CSS and JavaScript in one file)
README.md: this file