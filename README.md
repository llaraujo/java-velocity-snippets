# Java Velocity Snippets for Sublime Text

## Vars

### [set] set var

```java
#set($${1:var}=${2:""})
```

### [var] use var

```java
$!{${2:var}}
```

## Array
### [aa] array.add

```java
$!{${1:arrayName}.add($!{${1:arrayName}.size()}, ${2:value})}
```

### [ar] array.remove

```java
remove(${1:numericKey})
```


## Object

### [op] object.put

```java
put("${1:key}", ${2:value})
```

### [or] object.remove

```java
remove("${1:key}")
```


## String

### [sie] string.isEmpty

```java
$!{${1:var}.isEmpty()}
```

### [sre]  string.replace

```java
$!{${1:var}.replace("${2:find}","${3:replace}")}
```

### [sra] string.replaceAll

```java
$!{${1:var}.replaceAll("${2:find}","${3:replace}")}
```

### [suc] string.toUpperCase

```java
$!{${1:var}.toUpperCase()}
```


## Files

### [p] parse

```java
#parse("${1:file}")
```

### [rp] rparse

```java
#rparse("${1:file}")
```

## Conditionals

### [if] if

```java
#if (${1:logic})
	${2}
#end
```

### [ife] if-else

```java
#if (${1:logic})
	${2:if}
#else
	${3:else}
#end
```

## Loop

### [fe] forEach

```java
#foreach ($${1:item} in $!{${2:myCollection}})
	${0}
#end
```

### [fe] forEach Numeric

```java
#foreach ($${1:item} in [${2:0}..${3:1}])
	${0}
#end
```

### [fi] for in

```java
#foreach ($${1:item} in $!{${2:myCollection}.keySet()})
	${0}
#end
```

## Date Tool

### [dd] date.toDate

```java
$!{date.toDate("${1:format}", "${2:toDate}")}
```

### [df] date.format

```java
$!{date.format("${1:newFormat}", "${2:date}")}
```

## Include Tool

### [iex] include.exists

```java
$!{include.exists("${1:file}")}
```


## Json Tool

### [jso] _json.open

```java
$_json.open("${1:file}")
```

### [jss] _json.toString

```java
$_json.toString("{${1:json}")
```


## Link Tool

### [ld] link.decode

```java
$!{link.decode(${1:var})}
```

### [le] link.encode

```java
$!{link.encode(${1:var}.replace(' ','%20'))}
```

### [lgh] link.getHost

```java
$!{link.getHost()}
```

### [lgp] link.getPort

```java
$!{link.getPort()}
```

### [lgr] link.getRoot

```java
$!{link.getRoot()
```

### [lsp] link.setPort

```java
$!{link.setPort()}
```


## Math Tool

### [mn] math.toNumber

```java
$!math.toNumber(${1:var})
```

### [ma] math.add

```java
$math.add(${1:number1}, ${2:number2})
```

### [ma] math.sub

```java
$math.sub(${1:number1}, ${2:number2})
```

### [ma] math.mul

```java
$math.mul(${1:number1}, ${2:number2})
```

### [mr] math.random

```java
$!{math.random(${1:number1}, ${2:number2})}
```


## Reader Tool

### [rr] _reader.read

```java
$_reader.read("${1:file}")
```


## Render Tool

### [re] render.eval

```java
$render.eval("${1:var}")
```


## Request Tool

### [rgp] request.getParameter

```java
$!{request.getParameter("${1:logic}")}
```

### [rqs] request.getQueryString

```java
${request.getQueryString()}
```


## Response Tool

### [rct] response.setContentType

```java
$response.setContentType("${1:application/json}")
```

### [rsh] response.setHeader

```java
$response.setHeader("${1:attr}", "${2:value}")
```

### [rcc] response.setHeader: "Cache-Control"

```java
$response.setHeader("Cache-Control", "max-age=${1:20}")
```

### [rsr] response.sendRedirect

```java
$response.sendRedirect("${1:url}")
```

### [rst] response.setStatus

```java
$response.setStatus(${1:301})
```


## Sort Tool

### [sna] sort.asNumber.asc

```java
$_sort.asNumber.asc(${1:collection}, "${2:field}")
```

### [snd] sort.asNumber.desc

```java
$_sort.asNumber.desc(${1:collection}, "${2:field}")
```

### [sta] sort.asText.asc

```java
$_sort.asText.asc(${1:collection}, "${2:field}")
```

### [std] sort.asText.desc

```java
$_sort.asText.desc(${1:collection}, "${2:field}")
```

## UserAgent

### [uw] _userAgent.isWeb

```java
$!{_userAgent.isWeb()}
```

### [us] _userAgent.isSmartPhone

```java
$!{_userAgent.isSmartPhone()}
```

### [uf] _userAgent.isFeaturePhone

```java
$!{_userAgent.isFeaturePhone()}
```


## Miscellaneous

## [vm] hash utf-8
```java
#!vm; utf-8
```

### [igp] if request.getParameter

```java
#if ($!{request.getParameter("${1:logic}")})
	${2}
#end
```

### [st] stop
```java
#stop
```


## Debug

### [dh] debug html

```java
<!-- DEBUG [${1:varName}]: ${2:var} -->
```

### [dj] debug js

```java
<script>console.log("${1:var}")</script>
```



## License

[MIT License](http://llaraujo.mit-license.org/) © Leonardo Lima Araujo
