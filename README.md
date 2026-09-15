Sandhi
Sandhi is the junction: the seam where one thing has ended and the next has not begun. It is the technical term for the hinge in the breath that the Vijñāna Bhairava points at on day one, and the root of sandhyā, the twilight hours traditionally set aside for practice. It is also the name of the app.
A daily contemplative practice organised as twelve four-week blocks, drawing on Kashmir Shaivism, early Buddhism, Advaita Vedānta and Sufism.
One HTML file. No build step, no dependencies, no server, no account. Everything you record stays in your browser.
What it is
Most meditation apps flatten every tradition into the same generic mindfulness and then hold you with a streak counter. This does neither.
The traditions are kept separate. Kashmir Shaivism, Advaita and Dzogchen run on recognition: you are already that, and the work is noticing. Early Buddhism and most Sufi practice run on cultivation: something is built through repetition over time. Blended carelessly they cancel out. Blocks alternate between the two and never mix them, and the interface marks which spine you are on in gold or blue throughout.
Blocks, not a daily shuffle. Four weeks on one text or method, with weekly themes inside it and a session format that varies by day. You do not restart every morning, and a switch only happens at a boundary you can see coming.
No streak. The calendar fills as you sit. A day you missed is an empty square, not a reset to zero. Nothing records depth or quality of a sit, because a number you can chase becomes the thing you sit for.
Running it
Open index.html in a browser. That is all.
To host it:
Push this repository to GitHub.
Settings, then Pages, then set the source to your default branch and the root folder.
It will be live at https://<your-username>.github.io/<repo-name>/ in a minute or two.
On a phone, open that URL and use "Add to Home Screen". It behaves like an app from then on.
Your data
Sits, notes and your start date live in localStorage under the key sandhi.v1. They never leave the device and there is no analytics of any kind.
That also means clearing site data erases the record, and a different browser or device starts from zero. The Days screen has Export a copy, which downloads a JSON file, and Import a file, which merges one back in. Export occasionally if the record matters to you.
Day one of the year on the same screen sets which block you are in. Move it back if you want to start partway through, or if you want to sit a particular block next.
What is written and what is not
Four blocks are written in full, which is 112 days of distinct daily practice:
Block	Path	Source
1	The Vijñāna Bhairava Tantra	recognition	Kashmir Shaivism, c. 9th century
2	Ānāpānasati	cultivation	Majjhima Nikāya 118
3	Self-enquiry	recognition	Ramana Maharshi, Aṣṭāvakra Gītā
4	Dhikr and murāqaba	cultivation	al-Ghazālī, Naqshbandī and Chishtī practice
Blocks 5 to 12 have their four weekly themes set but no daily pointers. The Today screen says so plainly when you reach one rather than showing filler.
Adding a block
All content sits in the first <script> block of index.html, in the BLOCKS array. Each day is one call to D():
js
D(
  "Where the in-breath ends",              // title
  "Find the point where breathing in has  // the pointer, set large as the hero
   finished and breathing out has not yet
   begun. Rest there.",
  "t",                                     // format: s, t or g
  "<p>Two short paragraphs of teaching.</p>", // HTML
  "Whenever you notice you are breathing   // the line carried into the day
   today, look for the turn at the top."
)
Formats are s for a silent sit with one pointer, t for a short teaching then a sit, and g for a longer guided piece. A written block needs exactly four weeks of exactly seven days. To convert an outline block, replace stub:1 with days on each week.
Day 28 of each written block does a particular job: it names what that month's method can and cannot do, and hands over honestly to the opposite path. Worth preserving if you write more.
On the writing
The pointers and teachings are written in plain English rather than quoted from any translation. Two reasons. Most well-known English renderings are under copyright, and several of the popular ones are loose adaptations by people who do not read the source language, which lose the actual technique.
When you go to the sources, prefer a translator who reads the original and says so. The Read screen inside the app lists where to go for each tradition, including what is legitimately free:
Kashmir Shaivism — Christopher Wallis at hareesh.org, working through the Vijñāna Bhairava verse by verse. In print, Jaideva Singh and Mark Dyczkowski.
Buddhism — SuttaCentral for the canon with parallel translations, Access to Insight for the practice essays.
Advaita — free Ramana books, and the ashram at gururamana.org.
Sufism — the complete Masnavi in three languages at masnavi.net, and the Ibn Arabi Society for over two hundred free journal articles.
A caution
This is a personal tool, not a teacher. The direct-path material in particular can be destabilising when practised intensively without someone to talk to. If long sits start producing anxiety, dissociation or anything that does not settle when you stop, stop and speak to a teacher in whichever of these living traditions you are drawn to. They all have one.
Licence
Code and written content are MIT licensed. See LICENSE. The underlying texts are centuries old and in the public domain; no translation is reproduced here.
