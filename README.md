# CompositeAdapter

<img src="https://github.com/Victorious/CompositeAdapter/blob/master/art/demo.gif"/>

## Why use it?

CompositeAdapter allows you to build a single list with a RecyclerView that contains distinct and separate data sets.

The composition strategy in place allows you to reuse and combine existing adapters without needing to learn any new and elaborate APIs. Just build vanilla RecyclerView.Adapters and add them to the CompositeAdapter.

## How to use it?

- Build out your RecyclerViewAdapters as needed for different sets of data.
- Add each Adapter to an instance of CompositeAdapter.
- Pass the CompositeAdapter instance to your RecyclerView. 

```
PeopleAdapter peopleAdapter = new PeopleAdapter(generatePeopleList());
TextMessagesAdapter textAdapter = new TextMessagesAdapter(generateTextMessages());

CompositeAdapter<RecyclerView.Adapter> compositeAdapter = new CompositeAdapter<>();
compositeAdapter.addAdapter(peopleAdapter);
compositeAdapter.addAdapter(textAdapter);

RecyclerView recyclerView = (RecyclerView) findViewById(R.id.composite_list);
recyclerView.setAdapter(compositeAdapter);
```

## Demo & Other Info

See the [Demo App](https://github.com/Victorious/CompositeAdapter/tree/master/app) for a quick example of CompositeAdapter in action.

[GDG LA Slides](https://docs.google.com/presentation/d/1HOyf1KRG5kjBIBVAGA3txhRVIvazDDPI9FIhVZhmocs/edit?usp=sharing) for additional information.

## Gradle Support

- Coming soon!

## License

```
Copyright 2017 Victorious,Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
