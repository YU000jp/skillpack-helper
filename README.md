# @yu000jp/skillpack-helper

## Use Cases

Use this package in a downstream repository when you want to:

- validate `skillpack.manifest.json`
- generate `SKILL.md`
- build deterministic bundle output
- run skill pack management from `npm scripts`

## Install

```bash
npm i -D @yu000jp/skillpack-helper
```

## Use In a Repository

Add scripts like these to the consuming repo:

```json
{
  "scripts": {
    "skillpack:validate": "skillpack-helper validate ./packs",
    "skillpack:build": "skillpack-helper build ./packs --out ./dist",
    "skillpack:pack": "skillpack-helper pack ./packs --out ./bundle.json"
  }
}
```

Run the CLI directly when needed:

```bash
npx skillpack-helper create ./packs/example --name example-pack
npx skillpack-helper update ./packs/example
npx skillpack-helper validate ./packs
npx skillpack-helper build ./packs --out ./dist
npx skillpack-helper pack ./packs --out ./bundle.json
npx skillpack-helper explain ./packs/example
```

## Command Reference

- `create`: scaffold a new pack
- `update`: regenerate `SKILL.md`
- `validate`: check a pack or pack tree
- `build`: write deterministic bundle output
- `pack`: write JSON bundle output
- `explain`: print a normalized view of a pack

## Schema

- [`schema/skillpack.manifest.schema.json`](./schema/skillpack.manifest.schema.json)
- `@yu000jp/skillpack-helper/schema/skillpack.manifest.schema.json`
