# Front end exercise

I implemented a non-responsive design here. As I explained during the technical interview, I have no prior experience with responsive design. In every application I worked on previously, the customers did not want responsive design, so I have never had any need to learn this skill until now.

I chose to implement this particular app in Vue.js, the JavaScript framework I know to reduce the number of unknowns.

I ran into all sorts of trouble getting Vue to install from either its command line client or it's fancy browser based installer on my Linux laptop (npm wouldn't work was the primary issue) and finally gave up after 4 hours and just included a link to Vue in the head of `index.html`. Unfortunately that meant that I couldn't get Karma or Jest or any other test runners working with Vue and had no time to re-write this in React (which I don't know yet, so that would have taken even longer).

I was able to implement the functionality requested in the original README and am reasonably happy with how that turned out.

In addition to the requirements listed, I also implemented a super basic validation notification system which you'll see if you insert invalid data.

## Running this app
All you need to do to run this app is open `index.html` in your browser from your local file system on your computer.

This app uses some modern ES6 browser features, so may only work in recent versions of Google Chrome.