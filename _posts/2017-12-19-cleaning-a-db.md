---
layout: post
title: 'cleaning a db'
date: 2017-12-19
---

Today I learned about cursors. It's a way to mark the objectStore and from then you can keep or delete data. 

What I needed: 
* store.index('the-index-you-want').openCursor()
* cursor.advance(numberOfItemsYouWant)
* cursor.delete()
* cursor.continue()

Valuable docs and videos:
[Sarah Clarke's course on IndexDB](https://youtu.be/_idFGKbYzqU)

[Another Sarah Clarke's course](https://youtu.be/vCumk1sXHcY) (almost the same, but I could focus more on the slides)

[The unavoidable MDN doc](https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API/Using_IndexedDB)

[and indications on Jake Archibald's github](https://github.com/jakearchibald/idb)

Might be valuable later:

[storing images and files](https://hacks.mozilla.org/2012/02/storing-images-and-files-in-indexeddb/)

And lots of info I need for this course:
[Google Study Guide](https://developers.google.com/training/certification/mobile-web-specialist/StudyGuide_MobileWebSpecialist.pdf)
