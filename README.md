# llmvet SDK for Workshop

This SDK provides llmvet, a local code-review tool for LLM/agent harnesses.
It shows diffs in the browser, lets reviewers leave inline comments, and prints
a prompt for agents to consume. The SDK sets LLMVET_HOST to the workshop's
external IP so the printed URL can be opened directly in a browser.

---

## Reference workshop

A minimal workshop:

```yaml
# workshop.yaml
name: llmvet-review
base: ubuntu@24.04
sdks:
  - name: llmvet
    channel: latest/stable
```

This workshop makes llmvet's web UI reachable at the workshop's external IP.

---

## Using the SDK

### Prerequisites, project layout

1. No prerequisite SDKs are required.
2. No specific project layout is needed. Run llmvet from any git working tree
   with uncommitted changes.
3. On launch, the SDK installs the llmvet binary on PATH and sets LLMVET_HOST
   to the workshop's external IP address. When llmvet runs, it prints a URL
   using that IP which can be opened directly in a browser on the host.

### Running a review

```bash
workshop shell
cd /path/to/your/repo
llmvet
# prints "Open http://<external-ip>:<port>/ to review"
# copy the URL directly into your browser
```

### Verify from the command line

```bash
workshop shell
llmvet --version
```

---

## Plugs (resources this SDK consumes)

This SDK doesn't define any plugs.

## Slots (resources this SDK provides)

This SDK doesn't define any slots.

---

## Documentation and guidance

- [llmvet upstream documentation](https://github.com/bjornt/llmvet#readme)
- [Workshop documentation](https://ubuntu.com/workshop/docs/)

---

## Community and support

- llmvet community:
  [GitHub Issues](https://github.com/bjornt/llmvet/issues)
- Workshop forum:
  [Discourse](https://discourse.ubuntu.com/)
- Please review our
  [Code of Conduct](https://ubuntu.com/community/ethos/code-of-conduct) before
  participating.

---

## Contributions

All contributions, including code, documentation updates, and issue reports,
are welcome!

- See `CONTRIBUTING.md` for guidelines.
- Open issues or pull requests on the official repository.

---

## License and copyright

Copyright 2026 Canonical Ltd.

Licensed under the [Apache-2.0 License](https://www.apache.org/licenses/LICENSE-2.0).

llmvet is licensed under the
[Apache License 2.0](https://github.com/bjornt/llmvet/blob/main/LICENSE).
