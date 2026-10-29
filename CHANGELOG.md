# Changelog

## v3.15 – 29 Oct 2026
- New **Tool development feedback** panel at the bottom of the page: type an idea / bug / wrong-fact note, paste (Ctrl+V) or drop up to six screenshots, and it is emailed to Mitch with the job context (site, council, mode, version, browser, any errors logged in the session). Sent through a Google Apps Script mailer; until that is configured the panel opens an email in your mail program instead.

## v3.14 – 25 Oct 2026
- Layout plan: roads named on the plan but not yet in the cadastre (a new internal road such as "Blacksmith Court") are kept as frontages, with a note listing the lots taken as fronting them; road abbreviations CRT, CL, CRS, ESP, PROM, BLVD, LN, WY etc. are recognised.
- Layout plan: lots on a cul-de-sac bulb or bend take their frontage from the curved boundary facing the road label (previously "rear"/no frontage).
- Layout plan: a boundary dimension read as an area label (e.g. "20.02 m" inside a 653 m² lot) no longer overrides the measured lot area; "1" and "01" are treated as the same lot.
- Corner lots list both frontages in the lot table ("19m to Tina Street and 10.4m to Blacksmith Court (corner lot)").
- Figure 2 (zone map) now draws for Ipswich – the zone layer query carries the ePlan map token.
- Print: fixed the black strip at the top of page 2 and the thin white edges on the cover (Chromium was shrinking the print to fit the header logo's margin overhang).

## v3.13 – 25 Oct 2026
- Panels reordered: "Checks before plotting and pushing to Code Generator" is now step 8, the Code Table Generator hand-over is step 9.
- "Mapping sources checked" removed from the report; it is now a one-page PDF from a button in the checks panel.
- Table 3: "[Confirm]" sits on the Neighbourhood plan and Overlays header rows only; individual rows read "No change".
- Cover page prints black to all four edges.
- Ward / division looked up automatically (QLD administrative boundaries – BCC wards, other councils' divisions).
- Architect / building designer firm read from the plans (title block or email domain) for Appendix A and Figure 4.

## v3.12 – 25 Oct 2026
- **Cover letter**: new "Cover letter" (Word) and "PDF" buttons produce MB's DA cover letter to Council from the same job (fee, addressee, salutation, signatory title and applicant email are under "Document control…" in step 6; MB contact details are remembered in your browser). Dropping a cover-letter .docx in step 7 now replaces the letter template, not the report template.
- **PDF print views open in a new tab** (report, cover letter, preliminary check) so closing them never closes the tool; falls back to an in-page preview if pop-ups are blocked.
- Architectural plans: GFA read from the areas block (ignores parking-rate text like "1/100m² GFA"); parking "provided (required)"; landscape area in m².
- Civil / traffic engineer fields take the consultant's firm from the report (e.g. "Meliora Engineering") rather than a "prepared by…" sentence.
- Step 8 rewritten with a live link to the Code Table Generator on meliorace.com; bar buttons renamed ("Copy text", green "JSON file for Code Table Tool"); print-summary button removed.

## v3.11 – 23 Oct 2026
- Ipswich City Plan 2025 zoning and overlays now load automatically via the ePlan relay feed (115 layers); step 2 shows the feed age and warns if it is stale.
- Excluded the city-wide "OV12 Flood & Overland Flow Risk" layer (it returns a hit for every Ipswich site); flood status comes from the risk-category layers.
- Version and build date shown in the header.
- Preliminary overlay check: Ipswich building height/density and RAAF airspace notes.

## v3.9 / v3.10 – 22–23 Oct 2026
- Preliminary overlay check panel (one-page first look, print/PDF, copy as text).
- MB logo header and black theme.
- BCC building-work triggers updated from 2026 Council decisions (raising, partial/whole demolition, pre-1911); Dwelling house (small lot) code added automatically under 450 m²; expected-conditions line in QA; "Value of work" fact passed to the Code Table Generator.

## v3.7 – 21 Oct 2026
- Building work (BW) mode with council trigger lists and fees; MCU mode; State-dataset fallback for overlays; easement reading from survey plans.
