---
layout: species
title: Species
description: Codes for taxa in ESAS.
permalink: /species/
---

The source file for the table below can be found in [`_data/vocabularies/species.tsv`](https://github.com/ices-tools-dev/esas/blob/main/_data/vocabularies/species.tsv).

Data providers can express species data in [Observation]({{ '/tables/#observation' | relative_url }}) in two ways:

- Using an ESAS code in `SpeciesCode`. Set `SpeciesCodeType` to `"ESAS"` for that record.
- Using a WoRMS Aphia ID in `SpeciesCode`. Set `SpeciesCodeType` to `"ERID"` for that record.

Downloads will always include a link to WoRMS.
