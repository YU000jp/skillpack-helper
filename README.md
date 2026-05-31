# @yu000jp/skillpack-helper

CLI tool for managing AI skill packs in downstream repositories.

```bash
npm i -D @yu000jp/skillpack-helper
```

```json
{
  "scripts": {
    "skillpack:validate": "skillpack-helper validate ./packs",
    "skillpack:build": "skillpack-helper build ./packs --out ./dist",
    "skillpack:pack": "skillpack-helper pack ./packs --out ./bundle.json"
  }
}
```

```bash
npx skillpack-helper create ./packs/example --name example-pack
npx skillpack-helper update ./packs/example
npx skillpack-helper validate ./packs
npx skillpack-helper build ./packs --out ./dist
npx skillpack-helper pack ./packs --out ./bundle.json
npx skillpack-helper explain ./packs/example
```

Schema:

- `schema/skillpack.manifest.schema.json`
