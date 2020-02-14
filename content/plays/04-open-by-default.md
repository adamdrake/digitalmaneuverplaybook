---
title: "04 - Open by Default"
---

Try to use as much open-source software as possible, and to contribute as much as possible back to the open source community.

Most of the software we use nowadays, including Linux, Docker, Kubernetes, Nginx, most modern programming langauges like Go, Python, Rust, Java, etc. are all open source.

Although large organizations and especially the Department of Defense have had varying levels of acceptance over the years, resulting in many myths about the use of open source software in DoD, the current messaging is very supportive and clear.

Here are some facts:

1. Open-source software is encouraged by the US Government and the Department of Defense
1. Open-source software is COTS
1. Open-source software does not have any issues with information assurance or security checks simply due to the fact that it is open source

Consider some of the common myths and misconceptions addressed in the [DoD CIO's Open Source FAQ](https://dodcio.defense.gov/Open-Source-Software-FAQ/):

**Q: Is this related to "open source intelligence"?**

No. In the Intelligence Community(IC), the term "open source" typically refers to overt, publicly available sources (as opposed to covert or classified sources).  Thus, Open Source Intelligence (OSINT) is form of intelligence collection management that involves finding, selecting, and acquiring information from publicly available sources and analyzing it to produce actionable intelligence.

In software, "Open Source" refers to software where the human-readable source code is available to the users of the software. (see above)

**Q: Isn’t using open source software forbidden by DoD Information Assurance Policy?**

No. This misconception comes from a misinterpretation of DoD Instruction 8500.2, “Information Assurance (IA) Implementation”, Enclosure 4, control DCPD-1.

The control in question reads:

DCPD-1 Public Domain Software Controls Binary or machine executable public domain software products and other software products with limited or no warranty such as those commonly known as freeware or shareware are not used in DoD information systems unless they are necessary for mission accomplishment and there are no alternative IT solutions available. Such products are assessed for information assurance impacts, and approved for use by the DAA. The assessment addresses the fact that such software products are difficult or impossible to review, repair, or extend, given that the Government does not have access to the original source code and there is no owner who could make such repairs on behalf of the Government.

This control is intended to limit the use of certain kinds of “binary or machine executable” software when “the Government does not have access to the original source code”. As clarified in the 2009 DoD CIO Memorandum, this control does not prohibit the use of open source software, since with open source software the government does have access to the original source code.

In the Desktop Application STIG version 3, release 1 (09 March 2007); in its section 2.4, it clearly states that DCPD-1 does not apply to open source software, for this very reason. The STIG first notes that "DoD has clarified policy on the use of open source software to take advantage of the capabilities available in the Open Source community as long as certain prerequisites are met. DoD no longer requires that operating system software be obtained through a valid vendor channel and have a formal support path, if the source code for the operating system is publicly available for review". It notes in particular that three cases for software are acceptable:

    A utility that has publicly available source code is acceptable.
    A commercial product that incorporates open source software is acceptable because the commercial vendor provides a warranty.
    Vendor supported open source software is acceptable.

The DISA STIG also notes "4. A utility that comes compiled and has no warranty is not acceptable." Thus, a program must come with either source code or a warranty; if it has neither, then special dispensation is required, since it difficult to review, repair, or extend the program either directly or via someone else.
General information about OSS

**Q: Is open source software commercial software? Is it COTS?**

Open source software that has at least one non-governmental use, and has been or is available to the public, is commercial software. If it is already available to the public and is used unchanged, it is usually COTS.

U.S. law governing federal procurement (U.S. Code Title 41, Chapter 7, Section 403) defines "commercial item" as including "Any item, other than real property, that is of a type customarily used by the general public or by non-governmental entities for purposes other than governmental purposes (i.e., it has some non-government use), and (i) Has been sold, leased, or licensed to the general public; or (ii) Has been offered for sale, lease, or license to the general public ...". Thus, as long as the software has at least one non-governmental use, software released (or offered for release) to the public is a commercial item for procurement purposes.

Similarly, U.S. Code Title 41, Chapter 7, Section 431 defines the term "Commercially available off-the-shelf (COTS) item"; software is COTS if it is (a) a "commercial item", (b) sold in substantial quantities in the commercial marketplace, and (c) is offered to the Government, without modification, in the same form in which it is sold in the commercial marketplace. Thus, OSS available to the public and used unchanged is normally COTS.

These definitions in U.S. law govern U.S. acquisition regulations, namely the Federal Acquisition Regulation (FAR) and the Defense Federal Acquisition Regulation Supplement (DFARS). DFARS 252.227-7014 Rights in Noncommercial Computer Software and Noncommercial Computer Software Documentation defines "Commercial computer software" as "software developed or regularly used for non-governmental purposes which: (i) Has been sold, leased, or licensed to the public; (ii) Has been offered for sale, lease, or license to the public; (iii) Has not been offered, sold, leased, or licensed to the public but will be available for commercial sale, lease, or license in time to satisfy the delivery requirements of this contract; or (iv) Satisfies a criterion expressed in paragraph (a)(1)(i), (ii), or (iii) of this clause and would require only minor modification to meet the requirements of this contract."

There are many other reasons to believe OSS is commercial software:

    OSS is increasingly commercially developed and supported.
    OSS projects typically seek financial gain in the form of improvements. U.S. Code Title 17, section 101 (part of copyright law) explicitly defines the term “financial gain” as including “receipt, or expectation of receipt, of anything of value, including the receipt of other copyrighted works.”
    OSS licenses and projects clearly approve of commercial support

**Q: Why is it important to understand that open source software is commercial software?**

It is important to understand that open source software is commercial software, because there are many laws, regulations, policies, and so on regarding commercial software. Failing to understand that open source software is commercial software would result in failing to follow the laws, regulations, policies, and so on regarding commercial software.

In particular, U.S. law (10 USC 2377) requires a preference for commercial items for procurement of supplies or services. 10 USC 2377 requires that the head of an agency shall ensure that procurement officials in that agency, to the maximum extent practicable:

    "acquire commercial items or nondevelopmental items other than commercial items to meet the needs of the agency;
    require prime contractors and subcontractors at all levels under the agency contracts to incorporate commercial items or nondevelopmental items other than commercial items as components of items supplied to the agency;
    modify requirements in appropriate cases to ensure that the requirements can be met by commercial items or, to the extent that commercial items suitable to meet the agency’s needs are not available, nondevelopmental items other than commercial items;
    state specifications in terms that enable and encourage bidders and offerors to supply commercial items or, to the extent that commercial items suitable to meet the agency’s needs are not available, nondevelopmental items other than commercial items in response to the agency solicitations;
    revise the agency’s procurement policies, practices, and procedures not required by law to reduce any impediments in those policies, practices, and procedures to the acquisition of commercial items; and
    require training of appropriate personnel in the acquisition of commercial items."

Similarly, it requires preliminary market research to determine "whether there are commercial items or, to the extent that commercial items suitable to meet the agency’s needs are not available, nondevelopmental items other than commercial items available" that "(A) meet the agency’s requirements; (B) could be modified to meet the agency’s requirements; or (C) could meet the agency’s requirements if those requirements were modified to a reasonable extent." This market research should occur "before developing new specifications for a procurement by that agency; and before soliciting bids or proposals for a contract in excess of the simplified acquisition threshold."

An agency that failed to consider open source software, and instead only considered proprietary software, would fail to comply with these laws, because it would unjustifiably exclude a significant part of the commercial market. This is particularly the case where future modifications by the U.S. government may be necessary, since OSS by definition permits modification. 