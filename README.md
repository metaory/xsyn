XSYN
====

<div align=center>
  <img alt="logo-of-xsyn" src="https://raw.githubusercontent.com/metaory/xsyn/master/.github/assets/ico.png" width="50%">
  <h2>XSYN</h2>
  <h5>get fixed length similar words</h5>
</div>

```ex
NAME
	xsyn - get similar words in a fixed or free length


SYNOPSIS
  xsyn <WORD> [<LENGTH>]


DESCRIPTION
	xsyn is a thin wrapper on some public APIs,
  it get similar words to arg <WORD> in with [<LENGTH>] characters


.
EXAMPLES

	# get similar words to done with 7 characters
	xsyn done 7
		# ALLOVER	ATANEND	CORRECT	THROUGH	YIELDED

	# get similar words to done with 4 characters
	xsyn done 4
		# DEED	FINI	GAVE	OVER	SHOT	TADA

	# get similar words to done with any length
	xsyn done
	 # accomplished	achieved	agreed		approved	baked
	 # boiled		bygone		compacted	complete	completed
	 # concluded	consummate	consummated	cooked		determined
	 # discharged	done with	ended		executed	finished
	 # forgotten	fried		full		full-fledged	gone
	 # gone by		over		past		performed	settled
	 # signed		terminated	through
```

---

Requirements
------------

- [column](https://archlinux.org/packages/?q=column)
- [curl](https://github.com/curl/curl)
- [jq](https://archlinux.org/packages/?q=jq)
- [sort](https://archlinux.org/packages/?q=sort)
- [uniq](https://archlinux.org/packages/?q=uniq)
- [yank](https://archlinux.org/packages/?q=yank)

---


Installation
------------

- clone repo
- give execution permissions
- place it in your path

```ex
# Clone the repo
git clone git@github.com:metaory/xsyn.git

# Navigate to repo
cd xsyn

# Give execution permissions
chmod +x xsyn

# Link it somewhere in your PATH
ln -sfv xsyn /usr/bin/xsyn

# Use it anywhere

# Usage
xsyn void 7
	# ABOLISH	ABSENCE	BEGGING	DEADPAN	EXCRETE	INVALID	LACKING
	# MISSING	NULLIFY	REPRESS	RESCIND	SCHLOCK	SUBJECT	UNKNOWN
	# UNMOVED	UNNAMED	UNTRIED	URINATE	USELESS	VACUOUS	WANTING

```

TODO
====
- [ ] Makefile
- [ ] Pager mod
- [ ] Fallback providers

---

## License

[MIT](LICENSE)
