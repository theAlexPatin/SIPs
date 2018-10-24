---
SIP: 1
title: SIP Purpose and Guidelines
status: Accepted
author: Alex Patin <apatin@seas.harvard.edu>
        https://github.com/Squarelink-Inc/SIPs/blob/master/SIPS/SIP-1.md
created: 2018-10-24
---

## What is an SIP?

SIP stands for Squarelink Improvement Proposal. An SIP is a design document providing information to the Squarelink community, or describing a new feature for Squarelink or its processes or environment. The SIP should provide a concise technical specification of the feature and a rationale for the feature. The SIP author is responsible for building consensus within the community and documenting dissenting opinions.

## SIP Rationale

We intend SIPs to be the primary mechanisms for proposing new features, for collecting community technical input on an issue, and for documenting the design decisions that have gone into Squarelink. Because the SIPs are maintained as text files in a versioned repository, their revision history is the historical record of the feature proposal.

For Squarelink implementers, SIPs are a convenient way to track the progress of their implementation. Ideally each implementation maintainer would list the SIPs that they have implemented. This will give end users a convenient way to know the current status of a given implementation or library.

## SIP Work Flow

Parties involved in the process are you, the champion or *SIP author*, and the [*SIP editors*](#SIP-editors).

:warning: Before you begin, vet your idea, this will save you time. Ask the Squarelink community first if an idea is original to avoid wasting time on something that will be be rejected based on prior research (searching the Internet does not always do the trick). It also helps to make sure the idea is applicable to the entire community and not just the author. Just because an idea sounds good to the author does not mean it will work for most people in most areas where Squarelink is used. Examples of appropriate public forums to gauge interest around your SIP include [the Squarelink subreddit](https://reddit.com/r/squarelink) and [the Issues section of this repository](https://github.com/Squarelink-Inc/SIPs/issues). In particular, [the Issues section of this repository](https://github.com/Squarelink-Inc/SIPs/issues) is an excellent place to discuss your proposal with the community and start creating more formalized language around your SIP.

Your role as the champion is to write the SIP using the style and format described below, shepherd the discussions in the appropriate forums, and build community consensus around the idea.

### Statuses

- **Proposed**
- **Active**
- **Accepted**

## What belongs in a successful SIP?

Each SIP should have the following parts:

- Preamble - RFC 822 style headers containing metadata about the SIP, including the SIP number, a short descriptive title (limited to a maximum of 44 characters), and the author details. See [below](https://github.com/Squarelink-Inc/SIPs/blob/master/SIPS/SIP-1.md#SIP-header-preamble) for details.
- Simple Summary - “If you can’t explain it simply, you don’t understand it well enough.” Provide a simplified and layman-accessible explanation of the SIP.
- Abstract - a short (~200 word) description of the technical issue being addressed.
- Motivation (*optional*) - The motivation is critical for SIPs that want to change the Ethereum protocol. It should clearly explain why the existing specification is inadequate to address the problem that the SIP solves. SIP submissions without sufficient motivation may be rejected outright.
- Specification - The technical specification should describe the syntax and semantics of any new feature.
- Rationale - The rationale fleshes out the specification by describing what motivated the design and why particular design decisions were made. It should describe alternate designs that were considered and related work. The rationale may also provide evidence of consensus within the community, and should discuss important objections or concerns raised during discussion.
- Backwards Compatibility - All SIPs that introduce backwards incompatibilities must include a section describing these incompatibilities and their severity. The SIP must explain how the author proposes to deal with these incompatibilities. SIP submissions without a sufficient backwards compatibility treatise may be rejected outright.
- Test Cases - Test cases for an implementation are mandatory for SIPs that are affecting consensus changes. Other SIPs can choose to include links to test cases if applicable.
- Implementations - The implementations must be completed before any SIP is given status “Final”, but it need not be completed before the SIP is merged as draft. While there is merit to the approach of reaching consensus on the specification and rationale before writing code, the principle of “rough consensus and running code” is still useful when it comes to resolving many discussions of API details.
- Copyright Waiver - All SIPs must be in the public domain. See the bottom of this SIP for an example copyright waiver.

## SIP Formats and Templates

SIPs should be written in [markdown] format.
Image files should be included in a subdirectory of the `assets` folder for that SIP as follow: `assets/SIP-X` (for SIP **X**). When linking to an image in the SIP, use relative links such as `../assets/SIP-X/image.png`.

## SIP Header Preamble

Each SIP must begin with an RFC 822 style header preamble, preceded and followed by three hyphens (`---`). The headers must appear in the following order. Headers marked with "*" are optional and are described below. All other headers are required.

` SIP:` <SIP number> (this is determined by the SIP editor)

` title:` <SIP title>

` author:` <a list of the author's or authors' name(s) and/or username(s), or name(s) and email(s). Details are below.>

` * discussions-to:` \<a url pointing to the official discussion thread\>

 - :x: `discussions-to` can not be a Github `Pull-Request`.

`* review-period-end:` YYYY-MM-DD

` type:` <Standards Track (Core, Networking, Interface, ERC)  | Informational | Meta>

` * category:` <Core | Networking | Interface | ERC>

` created:` <date created on, in ISO 8601 (yyyy-mm-dd) format>

` * requires:` <SIP number(s)>

` * replaces:` <SIP number(s)>

` * superseded-by:` <SIP number(s)>

` * resolution:` \<a url pointing to the resolution of this SIP\>

#### Author header

The author header optionally lists the names, email addresses or usernames of the authors/owners of the SIP. Those who prefer anonymity may use a username only, or a first name and a username. The format of the author header value must be:

Random J. User &lt;address@dom.ain&gt;

or

Random J. User (@username)

if the email address or GitHub username is included, and

Random J. User

if the email address is not given.

The created header records the date that the SIP was assigned a number. Both headers should be in yyyy-mm-dd format, e.g. 2001-08-14.

SIPs may have a requires header, indicating the SIP numbers that this SIP depends on.

SIPs may also have a superseded-by header indicating that an SIP has been rendered obsolete by a later document; the value is the number of the SIP that replaces the current document. The newer SIP must have a Replaces header containing the number of the SIP that it rendered obsolete.

Headers that permit lists must separate elements with commas.

## Auxiliary Files

SIPs may include auxiliary files such as diagrams. Such files must be named SIP-XXXX-Y.ext, where “XXXX” is the SIP number, “Y” is a serial number (starting at 1), and “ext” is replaced by the actual file extension (e.g. “png”).

## Transferring SIP Ownership

It occasionally becomes necessary to transfer ownership of SIPs to a new champion. In general, we'd like to retain the original author as a co-author of the transferred SIP, but that's really up to the original author. A good reason to transfer ownership is because the original author no longer has the time or interest in updating it or following through with the SIP process, or has fallen off the face of the 'net (i.e. is unreachable or isn't responding to email). A bad reason to transfer ownership is because you don't agree with the direction of the SIP. We try to build consensus around an SIP, but if that's not possible, you can always submit a competing SIP.

If you are interested in assuming ownership of an SIP, send a message asking to take over, addressed to both the original author and the SIP editor. If the original author doesn't respond to email in a timely manner, the SIP editor will make a unilateral decision (it's not like such decisions can't be reversed :)).

## SIP Editors

The current SIP editors are

` * Alex Patin (@theAlexPatin)`

## SIP Editor Responsibilities

For each new SIP that comes in, an editor does the following:

- Read the SIP to check if it is ready: sound and complete. The ideas must make technical sense, even if they don't seem likely to get to final status.
- The title should accurately describe the content.
- Check the SIP for language (spelling, grammar, sentence structure, etc.), markup (Github flavored Markdown), code style

If the SIP isn't ready, the editor will send it back to the author for revision, with specific instructions.

Once the SIP is ready for the repository, the SIP editor will:

- Assign an SIP number (generally the PR number or, if preferred by the author, the Issue # if there was discussion in the Issues section of this repository about this SIP)

- Merge the corresponding pull request

- Send a message back to the SIP author with the next step.

Many SIPs are written and maintained by developers with write access to the Squarelink codebase. The SIP editors monitor SIP changes, and correct any structure, grammar, spelling, or markup mistakes we see.

The editors don't pass judgment on SIPs. We merely do the administrative & editorial part.

## History

This document was derived heavily from [Bitcoin's BIP-0001] written by Amir Taaki which in turn was derived from [Python's PEP-0001]. In many places text was simply copied and modified. Although the PEP-0001 text was written by Barry Warsaw, Jeremy Hylton, and David Goodger, they are not responsible for its use in the Ethereum Improvement Process, and should not be bothered with technical questions specific to Ethereum or the SIP. Please direct all comments to the SIP editors.
