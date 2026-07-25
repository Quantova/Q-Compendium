# Quantova Developer Content

This repository holds the developer documentation and tutorials for [Quantova](https://quantova.org), a post quantum Layer 1 blockchain.

The content is Markdown organized by topic. Each topic is a folder that contains an `index.md`. The files are consumed by the Quantova website and rendered with the docs and tutorial layouts.

## Repository layout

```
public/
  content/
    developers/
      docs/                          # Reference documentation
        intro-to-quantova/
        post-quantum-cryptography/
        accounts/
        qorus-consensus/
          committee-sortition/
          finality/
        blocks/
        transactions/
        fees/
        qvm/
        smart-contracts/
          quanta/
        standards/
          qasset/
          qcollectible/
        qns/
        staking/
        governance/
        nodes-and-clients/
          run-a-node/
        apis/
          gateway/
        chain-specs/
        development-networks/
      tutorials/                      # Step by step guides
        deploy-your-first-qasset/
        run-a-quantova-node/
```

## Conventions

One folder per topic. A page lives at `…/<topic>/index.md`. For example, `quantova.org/developers/docs/qorus-consensus/` is built from `public/content/developers/docs/qorus-consensus/index.md`.

Frontmatter. Every `index.md` starts with YAML frontmatter that carries `title`, `description`, and `lang` for docs. Tutorials add `published`, `skill`, and `tags`.

Internal links are root relative, for example `/developers/docs/accounts/`.

## Links

Website, https://quantova.org

## Contributing

See CONTRIBUTING.md. In short, edit or add an `index.md` under the right topic folder, keep the frontmatter, use root relative links, and open a pull request.

## License

See LICENSE.md. Documentation is copyright 2026 Quantova Inc.
