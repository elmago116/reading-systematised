---
title: Open Policy Agent - Homepage | Open Policy Agent
source: https://www.openpolicyagent.org/
author:
published:
created: 2026-04-02
description:
tags:
  - op/doc/tool
  - tech/Ai/agents
  - tech/ai
DOI:
Type: http://dx.doi.org/10.1590/2175-623668636
year:
---
![OPA Logo](https://www.openpolicyagent.org/assets/images/logo-text-dark-20ab84c6b2ba2433801b16fa43fe6550.png)

## OPA is a policy engine that streamlines policy management across your stack for improved development, security and audit capability.

```json
data.json{}
```
[Edit](https://www.openpolicyagent.org/#edit)

```json
input.json{

  "account": {

    "state": "open"

  },

  "user": {

    "risk_score": "low"

  },

  "transaction": {

    "amount": 950

  }

}
```
[Edit](https://www.openpolicyagent.org/#edit)

```json
# Run your first Rego policy!

package payments

default allow := false

allow if {

    input.account.state == "open"

    input.user.risk_score in ["low", "medium"]

    input.transaction.amount <= 1000

}

# Open in the Rego Playground to see the full example.
```
[Edit](https://www.openpolicyagent.org/#edit) [Open in Playground](https://play.openpolicyagent.org/?state=eyJpIjoie1xuICBcImFjY291bnRcIjoge1xuICAgIFwic3RhdGVcIjogXCJvcGVuXCJcbiAgfSxcbiAgXCJ1c2VyXCI6IHtcbiAgICBcInJpc2tfc2NvcmVcIjogXCJsb3dcIlxuICB9LFxuICBcInRyYW5zYWN0aW9uXCI6IHtcbiAgICBcImFtb3VudFwiOiA5NTBcbiAgfVxufSIsImQiOiJ7fSIsInAiOiIjIFJ1biB5b3VyIGZpcnN0IFJlZ28gcG9saWN5IVxucGFja2FnZSBwYXltZW50c1xuXG5kZWZhdWx0IGFsbG93IDo9IGZhbHNlXG5cbmFsbG93IGlmIHtcblx0aW5wdXQuYWNjb3VudC5zdGF0ZSA9PSBcIm9wZW5cIlxuXHRpbnB1dC51c2VyLnJpc2tfc2NvcmUgaW4gW1wibG93XCIsIFwibWVkaXVtXCJdXG5cdGlucHV0LnRyYW5zYWN0aW9uLmFtb3VudCA8PSAxMDAwXG59XG5cbiMgT3BlbiBpbiB0aGUgUmVnbyBQbGF5Z3JvdW5kIHRvIHNlZSB0aGUgZnVsbCBleGFtcGxlLlxuIn0=)

Open Policy Agent is a [Cloud Native Computing Foundation](https://www.cncf.io/) Graduated project.

![Productivity icon](https://www.openpolicyagent.org/assets/images/productivity-e966195af4635efbf03aba59a0e8106b.png)

**Developer Productivity:** OPA helps teams focus on delivering business value by decoupling policy from application logic. Security & platform teams centrally manage shared policies, while developer teams extend them as needed within the policy system.

![Performance icon](https://www.openpolicyagent.org/assets/images/performance-96543736340717309b3bc0e3b7a7fa46.png)

**Performance:** Rego, our domain-specific policy language, is built for speed. By operating on pre-loaded, in-memory data, OPA acts as a fast policy decision point for your applications.

![Audit icon](https://www.openpolicyagent.org/assets/images/audit-80b596c42f179c3e249be2b36d2a007a.png)

**Audit & Compliance:** OPA generates comprehensive audit trails for every policy decision. This detailed history supports auditing and compliance efforts and enables decisions to be replayed for analysis or debugging.

![](https://www.youtube.com/watch?v=Icl0_b5Llqc)

Interested to see more? Checkout the [Maintainer Track Session](https://www.youtube.com/watch?v=XtA-NKoJDaI) from KubeCon.

## Context-aware, Expressive, Fast, Portable

OPA is a general-purpose policy engine that unifies policy enforcement across the stack. OPA provides a high-level declarative language that lets you specify policy for a wide range of use cases. You can use OPA to enforce policies in applications, proxies, Kubernetes, CI/CD pipelines, API gateways, and more.

The examples below are interactive! Use the **Evaluate** button to see output for the given rego and input. Then edit the rego or the input (or both) to see how the output changes.

- API
- Envoy
- Kubernetes
- GenAI

Applications can directly integrate with OPA using our [SDKs](https://www.openpolicyagent.org/ecosystem) or [REST API](https://www.openpolicyagent.org/docs/rest-api). This is great when your application needs to make domain specific runtime decisions.

```json
policy.regopackage application.authz

# Only owner can update the pet's information. Ownership

# information is provided as part of the request data from

# the application.

default allow := false

allow if {

    input.method == "PUT"

    some petid

    input.path = ["pets", petid]

    input.user == input.owner

}
```
[Edit](https://www.openpolicyagent.org/#edit)

```json
input.json{

  "role": "staff",

  "owner": "bob@example.com",

  "path": [

    "pets",

    "pet113-987"

  ],

  "user": "alice@example.com"

}
```
[Edit](https://www.openpolicyagent.org/#edit)

```json
data.json{}
```
[Edit](https://www.openpolicyagent.org/#edit)

[Open in OPA Playground](https://play.openpolicyagent.org/?state=eyJpIjoie1xuICBcInJvbGVcIjogXCJzdGFmZlwiLFxuICBcIm93bmVyXCI6IFwiYm9iQGV4YW1wbGUuY29tXCIsXG4gIFwicGF0aFwiOiBbXG4gICAgXCJwZXRzXCIsXG4gICAgXCJwZXQxMTMtOTg3XCJcbiAgXSxcbiAgXCJ1c2VyXCI6IFwiYWxpY2VAZXhhbXBsZS5jb21cIlxufSIsImQiOiJ7fSIsInAiOiJwYWNrYWdlIGFwcGxpY2F0aW9uLmF1dGh6XG5cbiMgT25seSBvd25lciBjYW4gdXBkYXRlIHRoZSBwZXQncyBpbmZvcm1hdGlvbi4gT3duZXJzaGlwXG4jIGluZm9ybWF0aW9uIGlzIHByb3ZpZGVkIGFzIHBhcnQgb2YgdGhlIHJlcXVlc3QgZGF0YSBmcm9tXG4jIHRoZSBhcHBsaWNhdGlvbi5cbmRlZmF1bHQgYWxsb3cgOj0gZmFsc2VcblxuYWxsb3cgaWYge1xuXHRpbnB1dC5tZXRob2QgPT0gXCJQVVRcIlxuXHRzb21lIHBldGlkXG5cdGlucHV0LnBhdGggPSBbXCJwZXRzXCIsIHBldGlkXVxuXHRpbnB1dC51c2VyID09IGlucHV0Lm93bmVyXG59XG4ifQ==)

### Rego Playground

Write your first Rego Policy

[Play with Rego](https://play.openpolicyagent.org/)

Talk to other users and maintainers

[Join us on Slack](https://slack.openpolicyagent.org/)

Get involved with our project

[Get started](https://www.openpolicyagent.org/docs/contributing)