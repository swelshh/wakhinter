wakhinter
=========

Wakanda server side script to jshint all the js files in a project.

Installation
=========

You should put the waklinter folder in your Project/Modules/ folder.

You will also need a copy of underscore.js in your Project/Modules/ folder.

Usage
=========

Open any .js file in Studio and run this line of code:

```javascript
require("wakhinter").run();
```

wakhinter will walk through all the .js files in your project and run them through jshint.  The first time it finds a .js file with any errors it will display the errors in the Studio  output panel.  If no files are found with an error it will output "Done!" to the output panel.

You can optionally pass a Wakanda Folder object to  waklinter.run() and it will recursively find and jshint any .js files within that folder and any of its subfolders.

jshint Tweaks
=========

You can modify the included files to modify how jshint will behave:

* **jshintrc.json** this is the main configuration file used by jshint where you can setup options for which warning to show and globals 
* **jshintigore.json** this is a file I kind of made up where you can specify files to skip or lines of code to skip
* I also added an option to comment a line of code with //jshint_ignore and any errors on that line will be skipped

License (MIT License)
=========

Copyright (c) 2014 CoreBits DataWorks LLC

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.