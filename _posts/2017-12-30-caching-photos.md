---
layout: post
title: Caching photos
date: 2017-12-30
---
Back to the mobile web course.
Nothing really difficult here, but I still lack confidence with those quizzes...

(notes from the Udacity Mobile Web course by Jake Archibald)
The goal is to cache photos as they appear without losing streaming/performance impact.
So we'll be using the [cache API](https://developer.mozilla.org/en-US/docs/Web/API/Cache).

Cache API methods:
Returning a Promise:
 
    cache.match(request, options)
    cache.matchAll(request, options)
    cache.keys(request, promise)
    cache.delete(request, promise)

Not returning a Promise:
    
    cache.add(request)
    cache.addAll(requests) 
    cache.put(request, options)

/Note to myself: PLEASE DON't CONFUSE 'cache' with 'caches'/

remember the promise is something like this:

    api.promisingMethod(something).then(function(somethingElse){
        return 'yay it works';
    }).catch(function(whoReadThis){
         return 'oh no it didn't work sorry'
    })


Process:

the browser makes a request. It goes to the Service Worker. Then it's out on the network, and when we get a response, it goes back to the service worker which does 2 things at the same time: it puts the response in the cache and it displays it on the browser. 

So what happens next time you're requesting that same image: the request goes from the browser to the Service Worker, then it goes to the cache and retrieve the picture, which get sent to the browser. This is a much shorter and quicker circuit.

*Rule to remember*

YOU CAN ONLY USE THE BODY OF A RESPONSE ONCE

example : you can read the response as json response.json(); and then as a blob response.blob(); or use the response again as event.respondWith(response);

So how do you store your photos?
The trick is to use response.clone() : your cloning the response.

     event.respondWith(
         caches.open(yourApp-content-imgs).then(function(cache){
             return fetch(request).then(function(response){
                 cache.put(request, response.clone());
                 return response;
             })
         })
     )

The clone goes to the cache, while the original is displayed on the browser.

*Glossary* (aka Speak like a Dev)
From what I gather, "expression" means an action-step (=one line of code, one instruction) inside a function. So you can hear about a function with a single expression as the function body.

