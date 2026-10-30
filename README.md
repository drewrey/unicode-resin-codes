# How the plastic resin codes got into Unicode

Research notes, started 2026-10-30. Background for the Weird Web October "Plastic"
pieces in `featured-future` (`/wwo/2026/plastic`, `/wwo/2026/plastic2`).

## The question

Did the plastics industry push to get its numbered recycling symbols
(♳ ♴ ♵ ♶ ♷ ♸ ♹) added to Unicode?

## Short answer

**No, not according to the record.** The Unicode proposals were written by two
character-encoding experts, Michael Everson (filing for Ireland's national body)
and Asmus Freytag. Nothing in the proposals, the comments on them, or the meeting
minutes shows the Society of the Plastics Industry (SPI) taking part.

**The industry's push was at the state level.** Starting in 1989, SPI lobbied
almost 40 US states to require the chasing-arrows code on plastic containers
(NPR/Frontline, 2020). Those state laws are part of what made the symbols look
established enough to encode. The Unicode background paper cites them directly:
"As of January 1995, 39 US states had adopted legislation regarding the use of
this resin identification code system." So the industry didn't lobby Unicode,
but its lobbying produced the evidence that Unicode relied on. *(That link is our
reading, not a claim made in any source.)*

**Unicode froze the old design.** In 2013 ASTM swapped the arrows for a plain
triangle so the code would stop looking like a promise that the item can be
recycled. Unicode still has the 1988 chasing-arrows version, and from 2002
through 2026 no Unicode document title mentions recycling, resin or plastic.

## Timeline

| Date | Event | Source |
|---|---|---|
| 1970 | Gary Anderson designs the universal recycling symbol (♲) for a contest run by a paper company. It is based on a Möbius strip and was never trademarked. | N2342 |
| 1974 | An industry insider writes: "There is serious doubt that [recycling plastic] can ever be made viable on an economic basis." | NPR 2020 |
| 1988 | SPI introduces the code: a number inside chasing arrows, codes 1–7. The Unicode papers call it "The Plastic Bottle Material Code System"; Wikipedia gives the name as the "Voluntary Plastic Container Coding System." | N2310/N2342; Wikipedia |
| 1989 → | Oil and plastics executives start "a quiet campaign to lobby almost 40 states to mandate that the symbol appear on all plastic — even if there was no way to economically recycle it." | NPR 2020 |
| early 1990s | Coy Smith, who ran a recycling business near San Diego, finds every container stamped with the arrows. "It totally undermined our credibility." Recyclers protest for years and lose. | NPR 2020 |
| Jan 1995 | 39 states have laws on the resin code. | N2310/N2342 |
| 1997-12-08 | Everson files **N1661**, "Proposal to encode two ecological symbols," for Ireland. | N2240; WG2 status list N1952 |
| 1999 (Sept?) | WG2 meeting 34 in Redmond asks for more justification. | N2240 |
| 2000-08-27 | **N2240**, Everson & Freytag: "Proposal to add 8 recycling characters to the UCS," i.e. U+2672 ♲ plus ♳–♹. On the user community: "Almost everyone is a part of the user community." On the rationale: "They are symbols of great utility." The usage example comes from a city recycling web page in Grande Prairie, Alberta. | N2240 |
| 2000-12-22 | **N2310** background paper. It separates SPI's plastic codes from the American Forest & Paper Association's paper symbols, cites the state laws, and suggests adding the abbreviations (PETE, HDPE…) inside the glyphs "to match legislative requirements and usage by the sponsoring authority and industry." | N2310 |
| 2001-03-14 | **N2329**, Alain LaBonté (official Canadian position) objects: English abbreviations inside the glyphs would conflict with French labeling in Canada, Québec, France, Belgium and Switzerland. Symbols should stay language-neutral. | N2329 |
| 2001-04-02 | **N2342** replaces N2310. It also covers glass, steel, aluminum, the Pitch-In "do not litter" figure and the Green Dot. The Green Dot is left out because it requires a license from its trademark owners. | N2342 |
| 2001-04 | **WG2 meeting 40**, Mountain View. Everson: "Text will NOT be added inside the Glyphs." The long polymer names go into lowercase annotations instead. Four more symbols are accepted: ♺ generic materials, ♻ black universal, ♼ recycled paper, ♽ partially-recycled paper. Glass and "do not litter" are put off and never added. | N2353 minutes; resolution M40.5 |
| 2002 | **Unicode 3.2** ships U+2672–267D (12 characters). | DerivedAge.txt |
| 2008 | ASTM International takes over administration of the code and issues ASTM D7611. | Wikipedia |
| 2010 | ♻ (U+267B) is included in the original Japanese-carrier emoji set (emoji version E0.6), which is how it reached phone keyboards. ♳–♹ never became emoji. | emoji-data.txt |
| 2013 | At EPA's recommendation, a revision to ASTM D7611 replaces the chasing arrows with a solid triangle. ASTM's stated aim was to refocus the code on identifying resin rather than signaling recyclability. *(Paraphrased from a search summary; the ASTM press release URL now redirects to a dead page.)* | Wikipedia |
| 2002–2026 | No Unicode L2 document title mentions recycling, resin or plastic. The glyphs still show chasing arrows. | L2 registers (titles only) |
| 2020 | Former SPI president Larry Thomas: "If the public thinks that recycling is working, then they are not going to be as concerned about the environment." On the codes: "The symbols start showing up on the containers." | NPR 2020 |

## What Unicode says today (NamesList.txt)

```
2672 ♲ UNIVERSAL RECYCLING SYMBOL
       * used as generic symbol for recycling or to indicate that material is recyclable
2673 ♳ RECYCLING SYMBOL FOR TYPE-1 PLASTICS   * polyethylene terephthalate
2674 ♴ RECYCLING SYMBOL FOR TYPE-2 PLASTICS   * high density polyethylene
2675 ♵ RECYCLING SYMBOL FOR TYPE-3 PLASTICS   * vinyl, polyvinyl chloride
2676 ♶ RECYCLING SYMBOL FOR TYPE-4 PLASTICS   * low density polyethylene
2677 ♷ RECYCLING SYMBOL FOR TYPE-5 PLASTICS   * polypropylene
2678 ♸ RECYCLING SYMBOL FOR TYPE-6 PLASTICS   * polystyrene
2679 ♹ RECYCLING SYMBOL FOR TYPE-7 PLASTICS   * other plastics
267A ♺ RECYCLING SYMBOL FOR GENERIC MATERIALS
267B ♻ BLACK UNIVERSAL RECYCLING SYMBOL
267C ♼ RECYCLED PAPER SYMBOL
267D ♽ PARTIALLY-RECYCLED PAPER SYMBOL
```

The character names still say "RECYCLING SYMBOL," and Unicode names can never
be changed. Meanwhile, "resin codes do not indicate whether a product is
recyclable" (Wikipedia, citing Nuñez).

## Angles worth using

- **The industry got into Unicode without lobbying it.** The states passed laws
  the industry asked for, and the encoding experts treated those laws as proof
  the symbols were widely used.
- **The 2001 fight was about language, not truth.** Canada objected to the
  English abbreviations. No one in the record asks whether a recycling symbol on
  plastic that can't be recycled is misleading.
- **The standard changed and the font didn't.** ASTM dropped the arrows in 2013,
  but ♳ still shows them on every system, and a Unicode name can't be changed.
- **The proposers saw the marketing side.** N2342 says glass bottlers' symbols
  are driven by "consistency in making environmental marketing claims or possibly
  a sort of 'symbol envy' of glass bottlers towards their competitors using
  plastics."

## Not yet verified / open leads

- The full text of N1661 (1997). The dkuug.dk link is dead and no copy turned up
  in the Wayback Machine. Only its title and that Ireland filed it are confirmed.
- UTC minutes from 2000–01 approving the characters. The WG2 minutes say "The
  Unicode Technical Committee has approved these four," but the UTC minutes
  themselves haven't been read.
- Current state-law counts: "36 states with RIC laws, 29 still require chasing
  arrows" comes from search summaries of packaginglaw.com and natlawreview.com,
  which haven't been read directly. The Plastics Industry Association publishes
  an annual state survey (2025 edition) that would settle it.
- California SB 343 (2021), on chasing arrows printed on items that can't be
  recycled. Not researched yet.
- The 2001 Irish comments (N2328, page 3), where the final glyphs come from.

## Sources

Local copies are in `sources/`.

- Everson & Freytag, *Proposal to add 8 recycling characters to the UCS*, WG2 N2240 / L2/00-292, 2000-08-27. <https://www.unicode.org/wg2/docs/n2240.pdf>
- Everson & Freytag, *Background information on Recycling Symbols*, WG2 N2310 / L2/01-005, 2000-12-22. <https://www.unicode.org/L2/L2001/01005-n2310-recycling.pdf>
- LaBonté, *Multilingual issues concerning recycling symbols and symbols in general*, WG2 N2329 / L2/01-119, 2001-03-14. <https://www.unicode.org/L2/L2001/01119-n2329.pdf>
- Everson & Freytag, *Background information on Recycling Symbols* (supersedes N2310), WG2 N2342 / L2/01-146, 2001-04-02. <https://www.unicode.org/L2/L2001/01146-N2342-Recycling.pdf>
- WG2 Meeting 40 minutes, N2353, 2001-09-09. <https://www.unicode.org/wg2/docs/n2353.pdf>
- WG2 Meeting 40 resolutions, 2001-04-05. <https://www.open-std.org/jtc1/SC22/WG20/docs/n825-res-wg2.pdf>
- WG2 status of proposals (lists N1661, filed by Ireland). <https://www.unicode.org/wg2/docs/n1952s.html>
- Everson's 1997-12-09 announcement of N1661 on the Unicode list. <https://unicode.org/mail-arch/unicode-ml/Archives-Old/UML011/0212.html>
- Unicode Character Database: DerivedAge.txt, NamesList.txt, emoji-data.txt. <https://www.unicode.org/Public/UCD/latest/ucd/>
- Laura Sullivan, "How Big Oil Misled The Public Into Believing Plastic Would Be Recycled," NPR/PBS Frontline, 2020-09-11. <https://www.npr.org/2020/09/11/897692090/how-big-oil-misled-the-public-into-believing-plastic-would-be-recycled>
- ASTM, "ASTM Plastics Committee Releases Major Revisions to Resin Identification Code (RIC) Standard." Old URL <https://newsroom.astm.org/node/3040/printable/print> now redirects to a dead page; find an archived copy.
- Wikipedia, "Resin identification code." <https://en.wikipedia.org/wiki/Resin_identification_code>
