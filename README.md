## About
This is a build-updated version of the ThreadSample app that is referred to in a lot of the multi-threading
articles still current on developer.android.com:

Here is a list of all of the articles that reference code from this sample app.
https://developer.android.com/s/results?q=ThreadSample

While learning about threading on Android, we were looking around for working code examples that showed
the different ways of sharing information between threads and the documentation above extensively refers
to this example.

## Updating

It looks like it was originally built in Eclipse back in 2012 and
hasn't been updated since. We are using Android Studio 4.0.0 and gradle 6.1.1 with slightly more recent build targets
so it took us a minute to figure out how to get this app working in this environment.

* The google support libraries used by the original code were out of date. Updated to use AndroidX support packages. MinSdkVersion is now 14.

* The original code pulled from the Picasa public image feed. Since Google shuttered Picasa in 2016 we needed
to pull from a different feed. As of this writing flckr still has a public RSS feed at
https://www.flickr.com/services/feeds/photos_public.gne?format=rss2

* There were dependencies on deprecated apache cookie date utilities that had to be replaced with the DateUtil
class found here: http://www.java2s.com/Tutorial/Java/0320__Network/ParsingandformattingHTTPdatesasusedincookiesandotherheaders.htm

* There are some archaic components still used by this sample project. For example the RSS parser is based
on XmlPullParser which was added in the original Android API 1. It still works, but hasn't been updated since
2004 and there are more modern and popular XML parsers available. It's not our purpose to modernize this example -
we just want it working as a base to experiment with.

## Getting Help
### Nope - not from here
We are a high school robotics team. We are not qualified to provide help with multi-threading apps on Android.
We are just learning about this subject, so please refer your questions to more
### User Documentation and Tutorials

Again, the articles that reference this example are extensive and can be found here:
https://developer.android.com/s/results?q=ThreadSample

We can definitely recommend the Coding in Flow tutorial videos.
https://codinginflow.com/#services-background-tasks
