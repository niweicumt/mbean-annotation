## Mbean annotation

[![Build Status](https://travis-ci.org/wacai/config-annotation.png?branch=master)](https://travis-ci.org/wacai/config-annotation)
[![Codacy Badge](https://www.codacy.com/project/badge/b9158949586c439cb05e21333f52798b)](https://www.codacy.com/public/zhonglunfu/config-annotation)

It provides an easy-to-use method of exposing MBean by scala [macro annotation][mcr].

[mcr]:http://docs.scala-lang.org/overviews/macros/annotations.html

## Usage

```
import com.wacai.mbean.annotation._


@mbean class ThrottleActor extends Actor {
  def receive = {
    case i: Int => count += i
  }

  var count = 0

  @attribute var threshold = 100

  @operation def isOverload = count > threshold
}

```

## Installation

Comming soon.
