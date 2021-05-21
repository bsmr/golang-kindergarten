---
title: "Golang"
date: 2021-05-21T15:56:34+02:00
draft: false
---


## A bash example

```shell
ls -l | wc -l
sudo find / -delete
```

## Go examples

### a dummy test function

This code snipped is my base for `_test.go` files.

```golang
package dummy

import "testing"

func TestDummy(t *testing.T) {
	t.Skip("dummy test not implemented")
}
```

### get the current user name

```golang
// CurrentUsername tries to return the current user name.
func CurrentUsername() (string, error) {
	u, err := user.Current()
	if err != nil {
		return "", err
	}
	return u.Username, nil
}
```