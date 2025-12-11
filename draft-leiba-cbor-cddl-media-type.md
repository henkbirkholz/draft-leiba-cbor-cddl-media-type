---
v: 3

title: IANA Registrations for the Concise Data Definition Language (CDDL)
docname: draft-leiba-cbor-cddl-media-type-latest
stand_alone: true
ipr: trust200902
area: ART
wg: COSE
kw: Internet-Draft
cat: std
submissiontype: IETF
pi:
  toc: yes
  sortrefs: yes
  symrefs: yes

author:
- ins: B. Leiba
  name: Barry Leiba
  organization: Futurewei Technologies
  email: barryleiba@computer.org
  uri: http://internetmessagingtechnology.org/
- ins: H. Birkholz
  name: Henk Birkholz
  org: Fraunhofer SIT
  abbrev: Fraunhofer SIT
  email: henk.birkholz@ietf.contact
  street: Rheinstrasse 75
  code: '64295'
  city: Darmstadt
  country: Germany

normative:
  RFC8610:

informative:
  RFC6838:

entity:
  SELF: "RFCthis"

--- abstract

When the Concise Data Definition Language (CDDL) was defined, media-type, content-format, CBOR tag, and a file name extension were not defined for CDDL Definitions in RFC 8610.
Correspondingly, this documents specifies a media type (including a file name extension), a content format, and a CBOR tag for CDDL Definitions as specified in RFC 8610.

--- middle

# Introduction

When the Concise Data Definition Language (CDDL) was defined, media-type, content-format, CBOR tag, and a file name extension were not defined for CDDL Definitions in {{RFC8610}}.
Correspondingly, this documents specifies a media type (including a file name extension, see {{tbl-mt-reg}}), a content format (see {{tbl-cf-reg}}), and a CBOR tag (see {{tbl-tag-reg}}) for CDDL Definitions as specified in {{RFC8610}}.

# IANA Considerations

## Media Type

IANA is requested to add "application/cddl" as a new media type for CDDL Definitions to the "Media Types" registry {{!IANA.media-types}} in the Standards Tree {{RFC6838}}:

| Name | Template | Reference |
|----- --|--------------------|---------------------------|
| `cddl` | `application/cddl` | {{RFC8610}} and {{&SELF}} |
{: #tbl-mt-reg title="CDDL Media Type"}

Type name:
: application

Subtype name:
: cddl

Required parameters:
: N/A

Optional parameters:
: N/A

Encoding considerations:
: text

Security considerations:
: See Security Considerations in RFC 8610.

Interoperability considerations:
: N/A

Published specification:
: {{&SELF}}

Applications that use this media type:
: Applications that need to describe the structure of data in representation formats such as CBOR and JSON.

Fragment identifier considerations:
: N/A

Additional information:
: Deprecated alias names for this type:i
  :  N/A

  Magic number(s):
  : N/A

  File extension(s):
  : cddl

  Macintosh file type code(s):
  : N/A

Person/email address to contact for further information:
: CBOR WG mailing list (cbor@ietf.org)

Intended usage:
: COMMON

Restriction on usage:
: none

Author:
: See Author's Addresses section

Change controller
: IETF

Provisional registration:
: no

## CoAP Content Format

IANA is requested to assign a Content-Format ID for CDDL Definitions in the "CoAP Content-Formats" registry, within the "Constrained RESTful Environments (CoRE) Parameters" registry group {{!IANA.core-parameters}}:

| Content-Type | Content Coding | ID | Reference |
|------------------|---|------|---------------------------|
| application/cddl | - | TBD1 | {{RFC8610}} and {{&SELF}} |
{: #tbl-cf-reg title="CDDL Content Format"}

If possible, TBD1 should be assigned in the 256...9999 range.

## CBOR Tag

IANA is requested to allocate a tag for CDDL Definitions in the "CBOR Tags" registry {{!IANA.cbor-tags}}, preferably with the specific value requested:

| Tag  | Data Item | Semantics |
| 4344 | text | CDDL Definition as defined in {{RFC8610}} |
{: #tbl-tag-reg title="CDDL CBOR Tag"}

--- back
