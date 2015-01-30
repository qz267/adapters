# Eaternet::Adapters

**We're bringing the whole world's restaurant health inspections online,**
into as many sites and apps as possible.

**The plan in a nutshell:** each agency which inspects restaurants can have an "adapter".
Its adapter converts its source format into a simple, standard one which we define here. Anybody can then use these adapters to get the
data and do analysis and work with it how they like. [Eaternet](http://eaternet.io/), in particular, will use the production-ready 
adapters to pull and publish the information daily on our website and in feeds to partner organizations.


## Roadmap

Here's how we're going to get the whole world's data online:

Phase 1: **Finish open-sourcing** Eaternet's [Ruby adapter framework](https://github.com/eaternet/adapters-ruby) (in progress). This will include several
adapters to provide examples for different source data types (csv, web scraping, etc.).

Phase 2: **Second-stage conversion** code will be open-sourced. E.g., converting the Phase 1 results to a [LIVES](http://www.yelp.com/healthscores)-compatible format.

Phase 3: **Python support**. The framework will be translated to Python. We're starting [the codebase](https://github.com/eaternet/adapters-python) now. 
Cross-language support will be enabled by executing all adapters
in a seperate VM, exporting their results (probably as [MessagePack](http://msgpack.org) or [ProtoBufs](http://blog.codeclimate.com/blog/2014/06/05/choose-protocol-buffers/)) to storage. The
adapter-runner will then notify the app via a queue that there is data ready to be imported.
Support for any language will possible.


## Contributing

Lots of ways to help:

* Critique a PR, even a closed one.
* Do a small refactor.
* Add documentation. 
* Write an adapter for your city's restaurant health scores. 

Our Ruby code is currently the most mature:

* [Ruby code](https://github.com/eaternet/adapters-ruby)
* [Python code](https://github.com/eaternet/adapters-python)
* More languages are welcome. Drop us a line: info@eaternet.io.
