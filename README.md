# Java Velocity Snippets for Sublime Text

## Vars

### [set] set var

**Descrição:** método para setar variável

**Retorno:** Void

```java
#set($${1:var}=${2:""})
```

### [var] use var

**Descrição:** método para escrever variável

```java
$!{${2:var}}
```

## Array

### [aa] array.add

**Descrição:** Adiciona o parâmetro como valor no array

**Retorno:** Boolean

```java
$!{${1:array}.add(${2:value})}
```


### [aa] array.add

**Descrição:** Adiciona o parâmetro como valor no array, primeiro parâmetro é a key e o segundo é valor

**Retorno:** void

```java
$!{${1:array}.add(${2:pos},${3:value})}
```

### [aaa] array.addAll

**Descrição:** Recebe array por parâmetro e faz o merge dos arrays e values (sobreescreve os iguais)

**Retorno:** Array

```java
$!{${1:array}.addAll(${2:array2})}
```

### [aaa] array.addAll

**Descrição:** Recebe a key da inserção por parâmetro e faz o merge dos arrays.

**Retorno:** Array

```java
$!{${1:array}.addAll(${2:pos}, ${3:array2})}
```

### [acr] array.clear

**Descrição:** Remover todos os dados dentro do array

**Retorno:** Array

```java
$!{${1:array}.clear()}
```

### [acl] array.clone

**Descrição:** Retorna um clone do array

**Retorno:** Array

```java
$!{${1:array}.clone()}
```

### [ac] array.contains

**Descrição:** Verifica se o parâmetro informado existe como valor no array

**Retorno:** Boolean

```java
$!{${1:array}.contains(${2:value})}
```

### [aca] array.containsAll

**Descrição:** Recebe array por parâmetro e verifica se todos os valores dele existem no array de referência.

**Retorno:** Boolean

```
$!{${1:array}.containsAll(${2:array2})}
```

### [aeq] array.equals

**Descrição:** Verifica se o array informado por parâmetro é igual ao da referência

**Retorno:** Boolean

```java
$!{${1:array}.equals(${2:array2})}
```

### [ag] array.get

**Descrição:** Retorna valor do array a partir do parâmetro que informa a posição

**Retorno:** Valor da posição

```java
$!{${1:array}.get(${2:pos})}
```

### [aie] array.isEmpty

**Descrição:** Verifica se o array esta vazio

**Retorno:** Boolean

```java
$!{${1:array}.isEmpty()}
```

### [ar] array.remove

**Descrição:** Remove o parâmetro do array.

1. O parâmetro pode ser o índice do array.
2. O parâmetro pode ser o valor do array.

**Retorno:**

1. Object
2. Boolean

```java
$!{${1:array}.remove(${2:posOrValue})}
```


### [ara] array.removeAll

**Descrição:** Recebe array por parâmetro e remove os valores informados do array de referência

**Retorno:** Boolean

```java
$!{${1:array}.removeAll(${2:array2})}
```

### [arta] array.retainAll

**Descrição:** Compara os arrays e retorna os itens que existem em comum.

**Retorno:** Array

```java
$!{${1:array}.retainAll(${2:array2})}
```


### [as] array.size

**Descrição:** Retorna o tamanho do array

**Retorno:** Int

```java
$!{${1:array}.size()}
```

### [asl] array.subList

**Descrição:** Retorna um array de itens a partir dos parâmetros de início e fim informados

**Retorno:** Array

```java
$!{${1:array}.subList(${2:initialPos}, ${3:finalPos})}
```


## Object

### [oc] object.clear

**Descrição:** Remover todos os dados dentro do objeto

**Retorno:** Object

```java
$!{${1:object}.clear()}
```

### [ock] object.containsKey

**Descrição:** Verifica se o parâmetro informado existe como key no objeto

**Retorno:** Boolean

```java
$!{${1:object}.containsKey("${2:key}")}
```

### [ocv] object.containsValue

**Descrição:** Verifica se o parâmetro informado existe como valor no objeto

**Retorno:** Boolean

```java
$!{${1:object}.containsValue("${2:value}")}
```

### [oe] object.equals

**Descrição:** Verifica se dos objetos possuem o mesmo conteúdo

**Retorno:** Boolean

```java
$!{${1:object}.equals(${2:object2})}
```

### [oie] object.isEmpty

**Descrição:** Verifica se o objeto esta vazio

**Retorno:** Boolean

```java
$!{${1:object}.isEmpty()}
```

### [op] object.put

**Descrição:** Adicionar valor a uma determinada key

**Retorno:** Object

```java
$!{${1:object}.put("${2:key}", "${3:value}")}
```

### [op] object.putAll

**Descrição:** Recebe objeto por parâmetro e faz o merge dos key's e values (sobreescreve os iguais)

**Retorno:** Object

```java
$!{${1:object}.putAll("${2:object2}")}
```

### [or] object.remove

**Descrição:** Remover uma determinada key

```java
$!{${1:object}.remove("${2:key}")}
```

### [os] object.size

**Descrição:** Retorna o tamanho do objeto

**Retorno:** Int

```java
$!{${1:object}.size()}
```

### [ov] object.values

**Descrição:** Retorna um array com todos os values do objeto

**Retorno:** Array

```java
$!{${1:object}.values()}
```

## String

### [sc] string.concat

**Descrição:** Recebe valor por parâmetro e concatena na string de referência.

**Retorno:** String

```java
$!{${1:string}.concat("${2:value}")}
```

### [sce] string.contains

**Descrição:** Verifica se o valor informado por parâmetro existe dentro da string de referência.

**Retorno:** Boolean

```java
$!{${1:string}.contains("${2:string2}")}
```

### [sce] string.contentEquals

**Descrição:** Verifica se o valor informado por parâmetro é examente igual ao da string de referência.

**Retorno:** Boolean

```java
$!{${1:string}.contentEquals("${2:string2}")}
```

### [sew] string.endsWith

**Descrição:** Verifica se a string informada por parâmetro é o final da string da referência.

**Retorno:** Boolean

```java
$!{${1:string}.endsWith("${2:string2}")}
```

### [seic] string.equalsIgnoreCase

**Descrição:** Compara a string informada pelo parâmetro com a de referência ignorando case

**Retorno:** Boolean

```java
$!{${1:string}.equalsIgnoreCase("${2:string2}")}
```

### [sio] string.indexOf

**Descrição:** Retorna a posição da primeira ocorrência do valor informado por parâmetro ou retorna -1 caso não encontre.

**Retorno:** Number

```java
$!{${1:string}.indexOf("${2:string2}")}
```

### [sie] string.isEmpty

**Descrição:** Verifica se a string esta vazia

**Retorno:** Boolean

```java
$!{${1:string}.isEmpty()}
```

### [slio] string.lastIndexOf

**Descrição:** Retorna a posição da última ocorrência do valor informado por parâmetro ou retorna -1 caso não encontre.

**Retorno:** Number

```java
$!{${1:string}.indexOf("${2:string2}")}
```

### [sl] string.length

**Descrição:** Retorna o tamanho da string

**Retorno:** Number

```java
$!{${1:string}.isEmpty()}
```

### [sre]  string.replace

**Descrição:** Faz o replace da ocorrência do 1o parâmetro pelo 2o parâmetro informado

**Retorno:** String

```java
$!{${1:string}.replace("${2:find}", "${3:replace}")}
```

**Descrição:** Faz o replace da ocorrência do 1o parâmetro pelo 2o parâmetro informado

**Retorno:** String

### [sra] string.replaceAll

**Descrição:** Faz o replace de todas as ocorrências do 1o parâmetro pelo 2o parâmetro informado na string de referência

**Retorno:** String

```java
$!{${1:string}.replaceAll("${2:find}", "${3:replace}")}
```

### [sra] string.replaceFirst

**Descrição:** Faz o replace da 1a ocorrência do 1o parâmetro pelo 2o parâmetro informado na string de referência

**Retorno:** String

```java
$!{${1:string}.replaceFirst("${2:find}", "${3:replace}")}
```

### [ssw] string.startsWith

**Descrição:** Verifica se a string informada por parâmetro é o começo da string da referência.

**Retorno:** Boolean

```java
$!{${1:string}.startsWith("${2:string2}")}
```

### [sca] string.toCharArray

**Descrição:** Retorna a própria string da referência em array onde cada posição é um caractere.

**Retorno:** Array

```java
$!{${1:string}.toCharArray()}
```

### [slc] string.toLowerCase

**Descrição:** Retorna em caixa baixa a própria string da referência.

**Retorno:** String

```java
$!{${1:string}.toLowerCase()}
```

### [suc] string.toUpperCase

**Descrição:** Retorna em caixa alta a própria string da referência.

**Retorno:** String

```java
$!{${1:string}.toUpperCase()}
```

### [st] string.trim

**Descrição:** Remove espaços em branco do início e do fim da própria string da referência.

**Retorno:** String

```java
$!{${1:string}.trim()}
```

## StringUtils

### [scap] stringUtils.captalize

**Descrição:** Recebe valor por parâmetro e deixa a primeira letra em maiúsculo.

**Retorno:** String

```java
$!{stringUtils.capitalize(${1:string})}
```

## Files

### [p] parse

**Descrição:** Adiciona o arquivo informado ao contexto e interpreta o conteúdo velocity caso possua.

```java
#parse("${1:file}")
```

### [rp] rparse

**Descrição:** A partir do diretório atual, faz uma busca até o diretório raiz, pasta por pasta de forma recursiva pelo arquivo informado por parametro.

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
