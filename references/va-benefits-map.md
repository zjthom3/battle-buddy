# VA benefits — the map, not the numbers

> **Verified:** 2026-07-21 · **Contains no volatile figures.** Every rate, dollar amount,
> percentage, eligibility threshold, and deadline changes — this file only says *what each benefit
> is, who it's roughly for, and the official page*. Battle Buddy pulls the current details live
> and cites them, or says "I don't know — here's where to check." It never states a rating or an
> amount from memory, and it is not a VSO, an attorney, or a clinician.

## Two things that quietly change eligibility

- **Guard / Reserve.** Eligibility often hinges on time served on qualifying active-duty (Title 10)
  orders, and several rules differ from active duty. Check component first and use
  `references/guard-reserve.md` before running the standard sweep.
- **Coast Guard.** The Coast Guard sits under **DHS**, not DoD — but Coast Guard service **is**
  military service and Coast Guard veterans are **eligible for VA benefits** like any other veteran.
  Don't let the DHS affiliation make you (or them) assume otherwise.

## The claims rule, first

For anything involving a **disability claim**, route the person to a **free accredited VSO** —
county Veterans Service Officer, DAV, VFW, American Legion (`veteran-orgs.md`). They file for free.
Avoid paid "claim sharks." Battle Buddy helps you *organize and understand*; it does not file and
does not predict a rating.

## The topic index

| Benefit | What it is (one line) | Roughly for | Official page |
|---|---|---|---|
| **VA health care** | Enrollment in the VA health system | Most who served qualify; enroll to find out | https://www.va.gov/health-care/ |
| **Disability compensation** | Monthly tax-free payment for service-connected conditions | Anyone with a condition connected to service | https://www.va.gov/disability/ |
| **PACT Act / presumptive conditions** | Conditions VA presumes are service-connected (e.g. toxic/burn-pit, Agent Orange exposure) — you don't have to prove the link | Vets with qualifying exposure/service | https://www.va.gov/disability/eligibility/hazardous-materials-exposure/ |
| **PTSD & mental-health claims** | Disability claims for PTSD and other service-connected mental-health conditions | Vets with service-connected mental-health conditions | https://www.va.gov/disability/eligibility/ptsd/ |
| **CRSC (Combat-Related Special Compensation)** | Restores retired pay offset by VA comp for combat-related disabilities | Eligible retirees with combat-related conditions | https://www.va.gov/ (route via your branch's CRSC office) |
| **IDES / medical separation (MEB/PEB)** | The medical evaluation path when a condition affects fitness for duty; can set a rating before you separate | Service members referred for a medical board | https://www.va.gov/disability/how-to-file-claim/when-to-file/pre-discharge-claim/ |
| **GI Bill (Post-9/11 / Ch. 33)** | Education benefit — tuition, housing, books | Qualifying post-9/11 service | https://www.va.gov/education/about-gi-bill-benefits/post-9-11/ |
| **GI Bill transfer** | Move unused GI Bill to a spouse/child | Service members meeting service/commitment rules (transfer usually happens *while serving*) | https://www.va.gov/education/transfer-post-9-11-gi-bill-benefits/ |
| **VR&E (Ch. 31 / VetSuccess)** | Career counseling + training for service-connected disability | Veterans with a service-connected disability + employment need | https://www.va.gov/careers-employment/vocational-rehabilitation/ |
| **Rogers STEM Scholarship** | Extends GI Bill for approved STEM degrees | GI Bill users deep into a qualifying STEM program | https://www.va.gov/education/other-va-education-benefits/stem-scholarship/ |
| **VA home loan (COE)** | Home loan guaranty, often no down payment | Veterans/service members meeting service rules | https://www.va.gov/housing-assistance/home-loans/ |
| **VALife / life insurance** | VA life insurance programs | Veterans, esp. with service-connected disability | https://www.va.gov/life-insurance/ |
| **State & local benefits** | Property-tax relief, tuition, hiring preference, etc. | Varies enormously by state | Your state's Dept. of Veterans Affairs site |

## How Battle Buddy uses this map

- `/benefits-check` reads the person's `situation/` + `sustainment/benefits.md`, figures out which
  topics are live for their stage, then **fetches the current eligibility/amount/deadline from the
  official page above and cites it** for each one.
- It ends with the *one* thing worth acting on now and the exact link to do it.
- The "transfer GI Bill to dependents" line is a classic thing veterans miss because the window to
  set it up is usually **while still serving** — worth flagging early for `in-service` users.

## If the veteran lives outside the US

Some veterans live abroad — this changes *access*, not always *eligibility*, and it's easy to
wrongly assume "I moved, so I lost it." Do not assume either way; verify each against the official
page and cite it:

- **Disability compensation** is generally payable to eligible veterans regardless of where they
  live. (Verify: https://www.va.gov/disability/)
- **VA health care abroad** runs through the **Foreign Medical Program** for service-connected
  conditions, not normal enrollment. (https://www.va.gov/COMMUNITYCARE/programs/veterans/fmp/)
- **GI Bill at a foreign school** can work if the school/program is VA-approved. (Verify via the
  GI Bill Comparison Tool: https://www.va.gov/education/gi-bill-comparison-tool/)
- **VA home loan** applies to homes in the US and its territories — not foreign property.

Flag this whenever `situation/ground-truth.md` says the person is based outside the US.

**The master hub for everything:** https://www.va.gov
