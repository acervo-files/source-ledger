# Source ledger

Every archive Acervo has assessed, and what we decided.

Acervo is a local-first tool for searching archives of public-record
documents. Which archives it carries is a decision, not a technical
accident — this file records those decisions so that they can be
checked rather than taken on trust.

Each entry states the reasoning in plain language first, with the
governing instrument cited alongside it. A consolidated list of those
instruments appears at the end.

## What the statuses mean

| Status | Meaning |
|---|---|
| **Carried** | Assessed and included. |
| **Paused** | Assessed and built, then held back pending an open question. |
| **Declined** | Assessed and turned down. Not carried. |
| **Under review** | Assessment open, or awaiting a reply from the archive. |

## What we assess

Before any code is written for a source, we work through:

- **Copyright status of the records** — public domain, an open licence, or still protected
- **Terms of use** — what the publisher permits, in writing
- **Access channel** — whether the material can be reached as an honest, self-identifying visitor that respects robots.txt. If it cannot, we do not take it
- **Privacy** — whether making the records name-searchable would harm the people named in them, private individuals above all
- **Third-party rights** — material sitting inside a public record that belongs to someone other than the publisher
- **Removability** — whether the source can be removed from the product completely, on a legitimate request

A source has to pass all six. Several have not.

## The ledger

| Source | Jurisdiction | Status |
|---|---|---|
| PURSUE — U.S. Department of War | United States | Carried |
| FBI Vault | United States | Carried |
| CIA Reading Room | United States | Carried |
| AARO | United States | Carried |
| National Archives and Records Administration | United States | Carried |
| The National Archives — MoD UFO files (DEFE 24, DEFE 31) | United Kingdom | Paused |
| GEIPAN — CNES | France | Declined (case files) · Under review (catalogue) |
| Library and Archives Canada | Canada | Declined |
| Transport Canada — Civil Aviation Daily Occurrence Reporting System (CADORS) | Canada | Declined (as a UAP source) · Under review (as an official-records source) |

### Carried

**PURSUE · FBI Vault · CIA Reading Room · AARO** — United States.

Work produced by the U.S. federal government is not protected by
copyright inside the United States, so anyone may reproduce these
records freely. Each of the four is published by the originating agency
itself, as a public reading room or a disclosure catalogue.

> Copyright protection "is not available for any work of the United
> States Government" — 17 U.S.C. § 105.

One qualification applies to AARO. A minority of that material was
produced under contract by a federally funded research and development
centre rather than by agency staff. Section 105 reaches works of
government *employees*; a contractor can hold copyright in what it
produces. We therefore treat that subset as carrying narrower rights
than the rest, and handle it accordingly.

**National Archives and Records Administration** — United States.

Carried through the archive's own published bulk-distribution product,
rather than its API. Per-record use restrictions are honoured
individually: where a record is not cleanly marked as unrestricted, we
link back to NARA instead of copying the file.

### Paused

**The National Archives** — United Kingdom. Ministry of Defence UFO desk
files, series DEFE 24 and DEFE 31.

These are Crown copyright, not public domain. They are released under
the Open Government Licence v3.0, which permits reuse on condition of
attribution — and every document we hold carries that attribution.

> Crown copyright subsists in work made by an officer or servant of the
> Crown in the course of their duties — Copyright, Designs and Patents
> Act 1988, s. 163.

Assessed, built and tested, then held back. The distinction that stopped
us is between the *record* and the *scan of the record*: the open licence
covers the underlying information, while the archive separately operates
a commercial licensing arm for its own digitised images. We are seeking
written confirmation before carrying it. Until that arrives, it is not
shipped.

### Declined

We would have been glad to carry both of the following. Neither passed.

**GEIPAN — CNES** — France.

French law has no equivalent to the U.S. rule. What it offers instead is
a statutory right to reuse public information — but that right expressly
stops where a third party holds the rights in the material.

> The right of reuse does not extend to public information "sur lesquels
> des tiers détiennent des droits de propriété intellectuelle" — Code des
> relations entre le public et l'administration, art. L321-2; the reuse
> right itself is at art. L321-1.

The case files rest on photographs and reports supplied by witnesses and
licensed to the agency alone. Those rights sit with the witnesses, which
places the files outside the reuse right we would otherwise rely on.

The metadata catalogue is a closer question. The published terms forbid
extraction, while L321-1 grants a right of reuse. Resolving that tension
by asserting the statute against an explicit written prohibition did not
meet our threshold for proceeding. A formal reuse request is pending
with the agency, and the catalogue stays under review until it is
answered.

**Library and Archives Canada** — Canada.

Again no public-domain rule for government works. Canadian Crown
copyright is measured from first publication, so a record written inside
a department in the 1950s and never published has not started its clock
and remains protected today. Age does not help.

> Copyright in works "prepared or published by or under the direction or
> control of Her Majesty" subsists for fifty years following the year of
> first publication — Copyright Act, R.S.C. 1985, c. C-42, s. 12.

No reuse licence covering this material is available either.

The decisive objection is privacy, and it is not one a licence could
cure. OCR, full-text search and semantic indexing are the whole point of
Acervo — and applied to these records they would turn scanned files into
a name-searchable database of private individuals. Canadian law has
already addressed almost exactly this: the Federal Court found against
an operator who republished records that were themselves already public,
because making them searchable and indexable created a new harm to the
people named in them.

> *A.T. v. Globe24h.com*, 2017 FC 114, applying the Personal Information
> Protection and Electronic Documents Act, S.C. 2000, c. 5.

Worth recording: the access channel here was the cleanest of any
difficult source we have assessed. The refusal was purely legal.

**Transport Canada — Civil Aviation Daily Occurrence Reporting System
(CADORS)** — Canada.

We assessed CADORS, Transport Canada's register of civil aviation
occurrences, because among the occurrences it records are sightings of
objects that were not identified.

We want to be clear about why we said no, because it is not our usual
reason. The licensing here is excellent. Transport Canada publishes
CADORS as open data under the Open Government Licence – Canada,
refreshed daily, and that licence expressly permits commercial use. It
is the most permissive instrument we have encountered outside the
United States, and on the question that has stopped us elsewhere — may
we lawfully reuse this — the answer was largely yes.

We declined on fit. This is a database of aviation safety occurrences,
and the portion concerning unidentified objects is very small.
Transport Canada itself explains that the label it uses "should not be
interpreted to mean something of extraterrestrial origin" — the same
category covers weather balloons, meteors, drones, kites and birds.
When we read what the records actually say, the overwhelming majority
describe an object that was identified. What remained was a residue of
brief entries, on the order of one to seven a year across a quarter of
a century, each a few sentences long. Volume alone would not have
stopped us — we already carry sources of sixteen and fourteen records.
The difference is that those are documents, and these are sentences:
one of those sixteen files carries more text than this entire category.

Two further things weighed against it. These are short operational
notes rather than documents, and this archive exists to hold documents.
And CADORS is a living system: Transport Canada describes its contents
as preliminary and subject to change, and points to a different body as
the authoritative source. We are built to hold stable material
faithfully, and we would rather not hold a moving official record
badly.

We also could not establish with certainty that the descriptive text —
the part that would have made this worth having — falls inside the open
licence, as distinct from the structured data that plainly does. Where
we cannot say with evidence that we are in the clear, we do not
proceed, even when we could.

None of this is a criticism of CADORS. It is a well-run safety system
doing exactly what it was built to do, published openly and maintained
daily. It is simply not a record of unidentified phenomena, whatever
its category label suggests.

We are keeping the wider question open. Our decision here is about
CADORS as a source of UAP material, and that is the only thing we
assessed. As a body of official aviation records it is openly licensed
and well maintained, and that is a different question we have not yet
put to ourselves. We would rather say so than let a narrow "no" read as
a broad one.

> Open Government Licence – Canada; Copyright Act, R.S.C. 1985, c. C-42,
> s. 12; Personal Information Protection and Electronic Documents Act,
> S.C. 2000, c. 5.

If the open release later covers the descriptive text explicitly, or if
Canada establishes the dedicated public reporting service its Chief
Science Advisor has recommended, we would look again.

## Legal instruments referenced

- **United States** — Copyright Act, 17 U.S.C. § 105 (works of the United States Government)
- **United Kingdom** — Copyright, Designs and Patents Act 1988, s. 163 (Crown copyright); Open Government Licence v3.0
- **France** — Code des relations entre le public et l'administration, arts. L321-1 and L321-2 (reuse of public information)
- **Canada** — Copyright Act, R.S.C. 1985, c. C-42, s. 12 (Crown copyright); Personal Information Protection and Electronic Documents Act, S.C. 2000, c. 5; *A.T. v. Globe24h.com*, 2017 FC 114

## A note on these decisions

These are our decisions about what Acervo will carry, on our own reading
of the instruments cited above and our own threshold for proceeding.
They are not legal advice, and they are not a judgement about the
archives themselves. In more than one case we have declined material
that others may be perfectly entitled to use differently.
