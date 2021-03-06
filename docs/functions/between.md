---
layout: with-sidebar
sidebar: documentation
title: between ... and ...

type: function
datatypes:
- number
- double
- money
- floating_timestamp
description: Returns TRUE for values in a given range 
---

{% include function_header.html function_name=page.title description=page.description datatypes=page.datatypes %}

`between` is used with the `$where` parameter to return numeric or time stamp values between two input values. For example, to get all of the individuals who make between $40,000 and $60,000 at the White House:

{% include tryit.html domain='open.whitehouse.gov' path='/resource/9j92-xfdk.json' args="$where=salary between '40000' and '60000'" %}

It can also be used on [Floating Timestamps](/docs/datatypes/floating_timestamp.html). For example, to get all of the crimes that occurred between noon and 2PM on January 10th, 2015 in Chicago:

{% include tryit.html domain='data.cityofchicago.org' path='/resource/6zsd-86xi.json' args="$where=date between '2015-01-10T12:00:00' and '2015-01-10T14:00:00'" %}
