# existdb-strings
Utility extension module for eXist-db that provides a mix of string functions.

[![Build Status](https://travis-ci.com/Trundler/existdb-strings.svg?branch=master)](https://travis-ci.com/Trundler/existdb-strings)
[![Java 8](https://img.shields.io/badge/java-8-blue.svg)](http://java.oracle.com)
[![License](https://img.shields.io/badge/license-LGPL%202.1-blue.svg)](https://www.gnu.org/licenses/lgpl-2.1.html)

## Available functions

### Distance

Provides access to https://commons.apache.org/proper/commons-codec/

- hamming#2
- levenshtein#2
- cosine#2

### Codec

Provides access to https://commons.apache.org/proper/commons-text/ 

- soundex#1
- nysiis#1
- metaphone#1
- cologne-phonetic#1

## Examples

```xquery
xquery version "3.1";

import module namespace distance = "http://exist-db.org/extensions/strings/distance" 
                at "java:org.exist.extensions.strings.DistanceModule";
                
distance:levenshtein("tik", "tak")
```

```xquery
xquery version "3.1";

import module namespace codec = "http://exist-db.org/extensions/strings/codec" 
                at "java:org.exist.extensions.strings.CodecModule";
                
codec:metaphone("tik")
```
