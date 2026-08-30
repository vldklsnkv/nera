# Nera

Nera is a personal web concierge for Codex. It helps research products and services, compare realistic options, contact providers, negotiate within approved limits, prepare bookings or carts, and follow an outcome through to confirmation.

The plugin is designed for tasks that span several steps rather than a single search. A typical workflow is:

`find → compare → clarify → negotiate → prepare → approve → execute → verify`

Nera works through the user's authorized browser sessions and available connectors. It does not provide its own marketplace API, store account credentials, or bypass authentication and platform restrictions.

## What Nera can do

- Research services, products, prices, availability, fees, and cancellation terms.
- Compare a small set of viable options by total cost instead of headline price alone.
- Search authenticated websites and supported social platforms using the user's existing session.
- Review conversations, draft replies, and ask providers focused clarification questions.
- Negotiate non-binding terms within an explicitly approved budget and scope.
- Search Wolt Georgia, compare normalized prices and delivery costs, and prepare a reviewed cart.
- Find relevant Telegram communities, search visible history, and prepare an approved question.
- Search Unison doctors and appointment slots, then prepare an exact booking for confirmation.
- Monitor replies, availability, or booking status when the user asks for follow-up.

## Operating model

Nera chooses the narrowest mode that satisfies the request:

1. **Research** — inspect and report without typing into a composer.
2. **Draft** — prepare exact message text without sending it.
3. **Confirmed send** — send an approved message to an approved recipient.
4. **Bounded concierge dialogue** — continue factual, non-binding discussion with approved providers inside explicit limits.
5. **Confirmed booking** — perform a reviewed booking, reservation, or order only after final confirmation.

Requests such as “find”, “compare”, or “draft” do not authorize sending a message or completing a transaction. Before a booking, purchase, deposit, cancellation, or disclosure of sensitive data, Nera presents the exact action and asks for confirmation.

## Requirements and usage

Nera requires Codex with an installed browser-control capability. Authenticated tasks reuse the user's existing browser session; sign-in, MFA, CAPTCHA, and payment entry remain in the official browser UI.

After installing the plugin, start a new Codex task and invoke:

```text
Use $social-web-assistant:social-web-assistant to find and compare the best options for this request.
```

Other useful prompts include:

```text
Find three viable options, compare the all-in price, and recommend one.
Draft a short message asking about availability and cancellation terms.
Prepare the best appointment for review, but do not book it yet.
```

## Privacy and safety

- Credentials, cookies, browser profiles, passwords, MFA codes, and payment details are never read or stored by the plugin.
- Nera never bypasses CAPTCHA, rate limits, account challenges, access controls, or platform restrictions.
- Messages are sent only inside the approved recipient and purpose boundary.
- Binding commitments, payments, bookings, cancellations, and new personal-data disclosure always require a fresh checkpoint.
- Search results from social platforms may be ranked, incomplete, personalized, or limited to visible contacts and conversations. Nera reports those limits when they affect confidence.
- A clicked button or loading state is not treated as success; the final confirmation must be visible and verifiable.

## Project structure

The repository contains the Codex plugin manifest, the `social-web-assistant` skill, and its safety-oriented operating instructions. There is no standalone server and no credential database.

Nera is released under the MIT License. See [LICENSE](LICENSE) and [NOTICE.md](NOTICE.md).
