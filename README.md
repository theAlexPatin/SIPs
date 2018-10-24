# SIPs

Squarelink Improvement Proposals (SIPs) describe new improvements to Squarelink's protocol and features including core authentication protocols outlined in the White Paper, multi-currency wallet features, or developer experience features/toolsets.

Please throughly review the following before contributing:
- [Squarelink White Paper](https://squarelink.com/Squarelink.pdf)
- [Squarelink Developer Documentation](https://squarelink.com/docs)

# Contributing

 1. Review [SIP-1](SIPS/sip-1.md).
 2. Fork the repository by clicking "Fork" in the top right.
 3. Add your SIP to your fork of the repository.
 4. Submit a Pull Request to Squarelink's [SIPs repository](https://github.com/Squarelink-Inc/SIPs).

Your first PR should be a first draft of the final SIP. It must meet the formatting criteria enforced by the build (largely, correct metadata in the header). An editor will manually review the first PR for a new SIP and assign it a number before merging it. Make sure you include a `discussions-to` header with the URL to a discussion forum or open GitHub issue where people can discuss the SIP as a whole.

If your SIP requires images, the image files should be included in a subdirectory of the `assets` folder for that SIP as follow: `assets/sip-X` (for sip **X**). When linking to an image in the SIP, use relative links such as `../assets/sip-X/image.png`.

Once your first PR is merged, we have a bot that helps out by automatically merging PRs to draft SIPs. For this to work, it has to be able to tell that you own the draft being edited. Make sure that the 'author' line of your SIP contains either your Github username or your email address inside <triangular brackets>. If you use your email address, that address must be the one publicly shown on [your GitHub profile](https://github.com/settings/profile).

When you believe your SIP is mature and ready to progress past the draft phase, you should open a PR changing the state of your SIP to 'Final'. An editor will review your draft and ask if anyone objects to its being finalised. If the editor decides there is no rough consensus - for instance, because contributors point out significant issues with the SIP - they may close the PR and request that you fix the issues in the draft before trying again.

# SIP Status Terms
* **Draft** - an SIP that is undergoing rapid iteration and changes
* **Final** - an SIP that the Core Devs have decide to implement and release in a future hard fork or has already been released in a hard fork
* **Deferred** - an SIP that is not being considered for immediate adoption. May be reconsidered in the future for a subsequent hard fork.
