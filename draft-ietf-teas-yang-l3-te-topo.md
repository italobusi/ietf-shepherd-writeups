# Document Shepherd Write-Up for draft-ietf-teas-yang-l3-te-topo

*Reviewed revision: -19 (Template version dated 9 October 2026).*

## Document History & Implementations

1.	Have the Chairs confirmed Working Group (WG) consensus for this document? Did they indicate any issues to be called out with regard to that rough consensus? If so, what were they?

    Please supply any additional information about the quality of the WG consensus from the Shepherd's view (e.g., whether the consensus represents the strong concurrence of a few individuals, with others being silent, or did it reach a broad agreement).

    > The working group last call was made in April 2024 on -16:
    > - https://mailarchive.ietf.org/arch/msg/teas/uKIxNQBTNkUMxmelf7Pj5r_cT14/
    >
    > There were three positive replies from co-authors. We may assume that the relative silence at this stage results from the document being stable for quite some time.
    >
    > The WG LC was officially closed on May 14, 2024:
    > - https://mailarchive.ietf.org/arch/msg/teas/gOkXirk7VnJHqdC296MGc9c97_U/
    >
    > The -17 and -18 versions of the document addressed the Routing Directorate (Rtgdir) and YANG Doctors early review comments.
    >
    > The -19 version updated the title of the document to address the only pending Rtgdir early review comment. The new title was discussed on the TEAS WG mailing list and in previous IETF TEAS WG meetings:
    > - https://mailarchive.ietf.org/arch/msg/teas/GadilieuaF4Tb38QMaVlxbOuuM8/

2.	Indicate any significant disagreement in the WG about whether or not this document falls within the current charter.

    > None.
    > The comments that were brought during the process were incorporated into the document with good consensus. I did not find controversy on any point, and the modifications that were more complex were taken to the working group for discussion.

3.	If anyone threatened an appeal or otherwise indicated extreme discontent, please summarize the areas of conflict in separate email messages to the responsible Area Director. 

    (NOTE: This should be in a separate email because this completed questionnaire will be publicly available.)

    > No one has threatened an appeal nor indicated extreme discontent.

4.	For protocol documents, indicate whether the document adheres to the WG implementation policy (if any). Also, indicate whether there are existing (or planned) implementations and, if so, where they are listed. ([RFC 7942][3] recommends they be reported in the document itself).

    > The document is silent on implementation status.

## Additional Reviews

5.	Have reviews for the document happened in other IETF WGs or external organizations that you are aware of? If so, please provide references to those reviews (if any).

    > None, although the MPLS WG has been aware of this work.

6.	Describe the results of formal expert reviews (e.g., media type, URI) that the document has undergone. Also, indicate whether any of the required reviews are missing.

    > The document has also been reviewed by the Routing Directorate:
    > - https://datatracker.ietf.org/doc/review-ietf-teas-yang-l3-te-topo-16-rtgdir-early-peng-2024-04-28/
    > 
    > The document has also been reviewed by the YANG Doctors twice:
    - https://datatracker.ietf.org/doc/> review-ietf-teas-yang-l3-te-topo-04-yangdoctors-early-jethanandani-2019-06-18/
    - https://datatracker.ietf.org/doc/> review-ietf-teas-yang-l3-te-topo-16-yangdoctors-early-andersson-2024-05-06/
    > 
    > All the review comments have been addressed in the -19 version.
    > 
    > No other reviews are missing at this stage.

7.	If the document contains a YANG module, does the document’s Datatracker page indicate that it has no errors and warnings?

    > The Datatracker page shows YANG validation with 0 errors and 0 warnings.

    Has a YANGDOCTOR review been done on a recent version, indicating that it is ready for publication?

    > Yes, the latest YANGDOCTOR review indicates that the YANG data model is ready with issues:
    > -https://datatracker.ietf.org/doc/review-ietf-teas-yang-l3-te-topo-16-yangdoctors-early-andersson-2024-05-06/

    Does the document use the various templates in [RFC 9907][4] (mainly, YANG module, Security, and IANA templates)?

    > ** Action: discuss offline with the authors **
    > 
    > Partially. 
    > The document follows the structure and includes all required elements for the YANG modules (Section 5 and Appendix A), IANA Considerations (Section 6), and Security Considerations (Section 7). However, the boilerplate text in Sections 6 and 7 still uses the wording from RFC 8407 rather than the updated templates in RFC 9907 (and the YANG module revision dates are still set to 2024-06-08).

8.	Describe all reviews and automated checks performed to validate sections of the document written in a formal language, such as XML, JSON code, ABNF/RBNF/BNF rules, ASN.1, CBOR CDDL, etc.

    > ** Action: discuss offline with the authors **

9.	Does the document describe any protocol elements that are intended for human interpretation and understanding? If so, does the document contain an Internationalization Considerations section that describes how those protocol elements are suitable for international use?

    > ** Action: review offline with chairs **
    > 
    > No.
    > This document defines YANG data models for automated network management (NETCONF/RESTCONF) and does not introduce any new protocol elements intended for human interpretation or understanding. Therefore, an Internationalization Considerations section is not required.

## Document Shepherd Checks

10.	Confirm that (in your opinion) this document is clearly written, complete, technically accurate, correctly designed, and ready to be handed off to the responsible Area Director.

    > ** Action: review the document and discuss offline with the authors **

11.	Several IETF Areas have assembled [lists of common issues that their reviewers encounter][5]. Have such issues been identified and addressed? For which areas are subsequent reviews believed particularly important to happen?

    > ** Action: review offline with chairs **
    > 
    > Yes. Relevant items from the IESG Expert Topics list have been checked and addressed;
    > 
    > The YANG modules follow standard modeling conventions, use RFC 8340 tree diagrams, isolate non-NMDA state modules in Appendix A (RFC 8342), and properly augment L3 and TE topology models (RFC 8346, RFC 8795). Note that, as mentioned above, the boilerplate text in Sections 6 and 7 still follows RFC 8407 rather than the updated templates in RFC 9907.
    > 
    > Section 7 details the sensitivity of both writable and readable data nodes over secure transports (NETCONF/SSH and RESTCONF/HTTPS).
    > 
    > Example IPv4 addresses in Appendix B use the documentation block 203.0.113.0/24 (RFC 5737), the JSON example conforms to RFC 7951, namespace URNs are properly registered.
    > 

12.	What type of RFC publication is being requested ([Best Current Practice][6], [Proposed Standard, Internet Standard][7], [Informational, Experimental, or Historic][8])?

    > Proposed Standard

    Why is this the appropriate type of RFC?

    > This is appropriate because this is an implementable protocol specification that requests codepoints from the registry of IETF YANG models.

    > This is appropriate because the document defines normative YANG data models intended for interoperable implementation (augmenting existing Standards Track TE topology models) and registers new module names and XML namespaces with IANA.

13.	Will publication of this document change the status of any existing RFC(s)? If so, does the Datatracker status page for this document correctly list those RFCs on the Title page, in the Abstract, and in the Introduction of the document?

    > None

14.	If the document uses BCP 14 key words [9], does the document follow the guidance in the [IESG Statement on Clarifying the Use of BCP 14 Key Words][10]?
Is there any use of the BCP 14 key words that could be considered unclear or inappropriate? Please flag those.

    > ** Action: review the document and discuss offline with the authors **

15.	Confirm that reasonable efforts have been made to remind the WG (including the document authors, editors, and contributors) about the intellectual property rights (IPR) disclosure obligations described in [BCP 79][11].

    Please summarize any relevant discussion, including links to publicly available messages when applicable.

    > The document was polled for IPR before its adoption as WG document:
    > - https://mailarchive.ietf.org/arch/msg/teas/3gwmuJshAiaDMrff_2bSb9gAsb4
    > 
    > The -16 version of the document has also been polled for IPR before initiation of the WG LC:
    > - https://mailarchive.ietf.org/arch/msg/teas/M4BB0r67xXp73F-132tE2uoKH7M/
    > 
    > All listed authors responded to both IPR polls, and no IPR disclosures have been filed against this document.

16.	Confirm that each author, editor, and contributor has shown their willingness to be listed as such. If the total number of authors and editors on the front page is greater than five, please provide a justification.

    > ** Action: discuss offline with the authors since there are 6 authors on front page **
    > 
    > All listed authors and contributors have confirmed their willingness to be listed as such through their active participation and responses to the WG IPR polls.

17.	Please list any remaining I-D nits in the version of the document you reviewed that you feel are actual errors. Simply running the [idnits tool][12] is not enough; please review the ["Content Guidelines" on authors.ietf.org][13]. Idnits may display false positives; please flag those and please briefly explain as needed.
    (NOTE: No need to provide explanation for common false positives that are self-explanatory such as the existence of a newer version of referenced I-D)

    > ** Action: discuss offline with the authors **
    > 
    > The automated `idnits` check reports 0 errors and 0 warnings. However, a manual review against the IETF Content Guidelines and {{RFC8407}} identified the following actual issues that the authors should address before IESG evaluation:
    > 
    > 1. **Outdated YANG module metadata:** In all four YANG modules (Sections 5.1, 5.2, A.1, and A.2), the `Copyright` year (`2024`) and the `revision` date (`2024-06-08`) are outdated and should be updated to `2026` (and aligned with the document submission date).
    > 2. **Decommissioned URL in YANG `contact` blocks:** All four YANG modules reference `<http://tools.ietf.org/wg/teas/>`. Since `tools.ietf.org` is decommissioned, this must be updated to `<https://ietf.org>`.
    > 3. **Inconsistent author affiliations and emails:** Inside the YANG `contact` statements, the email addresses and affiliations for Igor Bryskin, Vishnu Pavan Beeram, and Tarek Saad still list previous employers (`huawei.com`, `juniper.net`, `cisco.com`) and do not match the front page or the Authors' Addresses section.
    > 4. **Security Considerations (Section 7):** Contains a double-slash typo (`//l3t:l3-termination-point-attributes`) in two subtree paths and refers to "The YANG module" in the singular despite defining four modules (NMDA and non-NMDA state modules).
    > 5. **References updates (Section 8):**
    >     * `[I-D.ietf-teas-rfc8776-update]` has recently been published as **RFC 10056** and should be updated accordingly (including inside the YANG `import` reference clauses).
    >     * `[I-D.ietf-teas-yang-te-mpls-topology]` should be updated from `-04` to `-05`.

### Document References

18.	List any informative references that should be normative or vice-versa? If so, please list those.

    See the [IESG Statement on Normative and Informative References][14].

    > None.
    > All normative and informative references in Section 8 are appropriately categorized in accordance with the [IESG Statement on Normative and Informative References][14].

19.	List any normative references that are not freely available to anyone. Does the community have sufficient access to review these references?

    > The document only references IETF RFCs and Internet Drafts which are freely available to anyone.

20.	List any normative downward references (see [RFC 3967][15] and [BCP 97][16]) that are not already listed in the [DOWNREF registry][17].

    > ** Action: review the document and discuss offline with the authors **
    > 
    > None.
    > All normative references are to Standards Track documents or BCPs.

21.	List any normative references to documents that are not ready to be submitted to the IESG for publication or are otherwise in an unclear state. For each, indicate the plan for their completion, if known.

    > ** Action: review the document and discuss offline with the authors **
    > 
    > None.
    > The document only has normative references to published IETF RFCs (noting that [I-D.ietf-teas-rfc8776-update] has just been published as RFC 10056, and the authors have been asked to update the reference in the next revision).

### IANA Considerations

22.	Describe your review of the IANA considerations section, especially its consistency with the body of the document.

    Confirm that all IANA requested actions are associated with the appropriate reservations in IANA registries.

    Confirm that any referenced IANA registries have been clearly identified.

    Confirm that each newly created IANA registry specifies its initial contents, allocation procedures, and a reasonable name (see [RFC 8126][18]).

    > ** Action: discuss offline with the authors **
    > 
    > I have reviewed Section 6 (IANA Considerations) and confirmed that it is fully consistent with the YANG modules defined in Section 5 and Appendix A.
    >
    > All requested IANA actions are properly associated with existing registries and clearly identified, following the template in RFC 9907.
    >
    > No new IANA registries are created by this document.

23.	List any new IANA registries that require Designated Expert Review for future allocations (Expert Review, Specification Required). If any, please confirm that the document includes guidelines for Designated Experts. Are these instructions to the Designated Expert clear?

    > N/A: there are no new IANA registries proposed in this document.

[1]: https://www.ietf.org/about/groups/iesg/ 
[2]: https://www.rfc-editor.org/rfc/rfc4858.html 
[3]: https://www.rfc-editor.org/rfc/rfc7942.html 
[4]: https://www.rfc-editor.org/rfc/rfc9907.html
[5]: https://wiki.ietf.org/group/iesg/ExpertTopics 
[6]: https://www.rfc-editor.org/rfc/rfc2026.html#section-5 
[7]: https://www.rfc-editor.org/rfc/rfc2026.html#section-4.1 
[8]: https://www.rfc-editor.org/rfc/rfc2026.html#section-4.2 
[9]: https://datatracker.ietf.org/doc/bcp14/ 
[10]: https://datatracker.ietf.org/doc/statement-iesg-statement-on-clarifying-the-use-of-bcp-14-key-words/
[11]: https://www.rfc-editor.org/info/bcp79 
[12]: https://author-tools.ietf.org/idnits3/ 
[13]: https://authors.ietf.org/en/content-guidelines-overview 
[14]: https://www.ietf.org/about/groups/iesg/statements/normative-informative-references/
[15]: https://www.rfc-editor.org/rfc/rfc3967.html 
[16]: https://www.rfc-editor.org/info/bcp97 
[17]: https://datatracker.ietf.org/doc/downref/ 
[18]: https://www.rfc-editor.org/rfc/rfc8126.html 
