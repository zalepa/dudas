# Dudas CLI Tools
A set of tools for working with PATFT data. Very much a work in progress. Tools do not require third party libraries. Created using: `ruby 2.1.4p265 (2014-10-27 revision 48166) [x86_64-darwin14.0]`

## Current toolchain:

* `download`: pipe a list of patents (e.g., "patents.list") and get a list of HTML source (see patents.out for a sample, basically it's one HTML file per line)
* `parse`: pipe in output of download and (for now) get a list of patent numbers and titles

Example: `cat patents.list | ./download | ./parse > titles.out`

Example: `./download patents.list | ./parse > titles.out`

## Immediate work

* ❗️ Parse should default to a certain format (JSON?)
* ❗️ Fill in the rest of the patent details
* ‼️ Testing (esp. with respect to regex)
* 😎 Use method_missing? instead of individual getter methods
* 😎 Clean up structure of `parse`

# License 

The MIT License (MIT)

Copyright (c) 2015 George David Zalepa

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.