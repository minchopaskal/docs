---
acl_categories:
- '@admin'
- '@search'
arguments:
- name: option
  type: string
- name: value
  type: string
categories:
- docs
- develop
- stack
- oss
- rs
- rc
- oss
- kubernetes
- clients
complexity: O(1)
deprecated_since: 8.0.0
description: Sets runtime configuration options
doc_flags:
- deprecated
group: search
hidden: false
linkTitle: FT.CONFIG SET
module: Search
replaced_by: '[`CONFIG SET`]({{< relref "/commands/config-set" >}})'
since: 1.0.0
stack_path: docs/interact/search-and-query
summary: Sets runtime configuration options
syntax: FT.CONFIG SET option value
syntax_fmt: FT.CONFIG SET option value
syntax_str: value
title: FT.CONFIG SET
---

Set the value of a RediSearch configuration parameter.

Values set using `FT.CONFIG SET` are not persisted after server restart.

RediSearch configuration parameters are detailed in [Configuration parameters]({{< relref "/develop/ai/search-and-query/administration/configuration" >}}).

{{% alert title="Note" color="warning" %}}
As detailed in the link above, not all RediSearch configuration parameters can be set at runtime.
{{% /alert %}}

[Examples](#examples)

## Required arguments

<details open>
<summary><code>option</code></summary> 

is name of the configuration option, or '*' for all. 
</details>

<details open>
<summary><code>value</code></summary> 

is value of the configuration option. 
</details>

## Return

FT.CONFIG SET returns a simple string reply `OK` if executed correctly, or an error reply otherwise.

## Examples

<details open>
<summary><b>Set runtime configuration options</b></summary>

{{< highlight bash >}}
127.0.0.1:6379> FT.CONFIG SET TIMEOUT 42
OK
{{< / highlight >}}
</details>

## See also

[`FT.CONFIG GET`]({{< relref "commands/ft.config-get/" >}}) | [`FT.CONFIG HELP`]({{< relref "commands/ft.config-help/" >}}) 

## Related topics

[RediSearch]({{< relref "/develop/ai/search-and-query/" >}})
