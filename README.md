Slidr
================
[![Maven Central](https://maven-badges.herokuapp.com/maven-central/com.r0adkll/slidableactivity/badge.svg?style=flat)](https://maven-badges.herokuapp.com/maven-central/com.r0adkll/slidableactivity)

Easily add slide-to-dismiss functionality to your Activity by calling `SlidableAttacher.attach(this)` in your `onCreate(..)` method. 

![Slidr Example](images/slidr_gif.gif "Gif Example")

## Usage

An example usage:

	public class ExampleActivity extends <Activity|FragmentActivity|ActionBarActivity> {
		
		@Override
		public void onCreate(Bundle savedInstanceState){
			super.onCreate(savedInstanceState);
			setContentView(R.layout.activity_example);
	        int primary = getResources().getColor(R.color.primaryDark);
	        int secondary = getResources().getColor(R.color.secondaryDark);
	        Slidr.attach(this, primary, secondary);
		}
		
	}
	
or

	public class ExampleActivity extends <Activity|FragmentActivity|ActionBarActivity> {
		
		@Override
		public void onCreate(Bundle savedInstanceState){
			super.onCreate(savedInstanceState);
			setContentView(R.layout.activity_example);
	        Slidr.attach(this);
		}
		
	}
	
`Slidr.attach(...)` will return a `SlidrInterface` which gives you access to two methods:

	SlidrInterface.lock();
	SlidrInterface.unlock();
	
These methods lock or unlock the slidable touch interface.
	
## Including in your project

Include this line in your gradle build file:

	compile 'com.r0adkll:slidableactivity:{latest_version}'
	
## Author

-	Drew Heavner, **[r0adkll](http://r0adkll.com)**

## License

	Copyright (c) 2014 Drew Heavner
	
	Licensed under the Apache License, Version 2.0 (the "License"); 
	you may not use this file except in compliance with the License. 
	You may obtain a copy of the License at
	
	http://www.apache.org/licenses/LICENSE-2.0
	
	Unless required by applicable law or agreed to in writing, 
	software distributed under the License is distributed on an 
	"AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, 
	either express or implied. See the License for the specific 
	language governing permissions and limitations under the License.
