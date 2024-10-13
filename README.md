<div align=center>
  <img alt="logo-of-xsyn" src="https://raw.githubusercontent.com/metaory/xsyn/master/.github/assets/ico.png" width="168px">
  <h2>XSYN</h2>
</div>

> [!Note]
> No API Key needed

---

```ex
NAME
	xsyn - get similar words



SYNOPSIS
  xsyn [<TYPE>] <WORD>


DESCRIPTION
	xsyn is a thin wrapper on Datamuse API, it get similar words to arg <WORD>


TYPES
  ml 	MeanLike [DEFAULT] (OneLook)
		# ocean → sea expanse oceanic seabed seafloor oceanographic pelagic oceanography marine midstream coast pond water seawater waters seaway bucket marina seagoing seafaring

  sn 	Synonym (WordNet synset)
		# ocean → sea

  nn 	Noune (Google Books Ngrams)
		# gradual → increase

  aj 	Adjective (Google Books Ngrams)
		# beach → sandy

.
EXAMPLES

# MeanLike
  xsyn ml ocean
    # same as
  xsyn ocean
		# sea		oceanography	waters
		# expanse	marine		seaway
		# oceanic	midstream	bucket
		# seabed	coast		marina
		# seafloor	pond		seagoing
		# oceanographic	water		seafaring
		# pelagic	seawater

# Synonym
  xsyn sn ocean
	# → sea

# Noun
  xsyn nn gradual
	# → increase

# Adjective
  xsyn aj beach
	# → sandy
```

<!--

	#	xsyn - get similar words in a fixed or free length
```
	# get similar words to done with 7 characters
	xsyn done 7
		# ALLOVER	ATTEND	CORRECT	THROUGH	YIELDED

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
-->

---

## Requirements

- [jq](https://archlinux.org/packages/?q=jq)
- [curl](https://github.com/curl/curl)
- [sort](https://archlinux.org/packages/?q=sort)
- [uniq](https://archlinux.org/packages/?q=uniq)
- [yank](https://archlinux.org/packages/?q=yank)
- [column](https://archlinux.org/packages/?q=column)

---

## Installation

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
ln -svf $PWD/xsyn /usr/bin/xsyn

# Use it anywhere
xsyn sn void
	# null avoid eliminate empty vitiate annul quash nugatory invalid nullify evacuate vacancy invalidate emptiness nullity nothingness

xsyn void
	# vacancy emptiness nothingness empty null nullity invalid invalidate nugatory nullify vitiate avoid annul quash eliminate evacuate vacuum devoid nil useless
```

<!--
# Usage
xsyn void 7
	# ABOLISH	ABSENCE	BEGGING	DEADPAN	EXCRETE	INVALID	LACKING
	# MISSING	NULLIFY	REPRESS	RESCIND	SCHLOCK	SUBJECT	UNKNOWN
	# UNMOVED	UNNAMED	UNTRIED	URINATE	USELESS	VACUOUS	WANTING
```
-->

# TODO

- [ ] Makefile
- [ ] Pager mod
- [x] Fallback providers

---

## License

[MIT](LICENSE)
