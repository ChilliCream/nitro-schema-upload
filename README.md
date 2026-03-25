# Nitro Schema Upload

A GitHub Action that uploads GraphQL schemas to the Nitro registry.

## Usage

```yaml
- uses: ChilliCream/nitro-schema-upload@v16
  with:
    tag: <tag>
    schema-file: ./schema.graphql
    api-id: <api-id>
    api-key: <api-key>
```

## Inputs

| Name          | Required | Description                                             |
| ------------- | -------- | ------------------------------------------------------- |
| `tag`         | Yes      | The tag of the schema version                           |
| `schema-file` | Yes      | The path to the graphql file with the schema definition |
| `api-id`      | Yes      | The ID of the API                                       |
| `api-key`     | Yes      | API key for authentication                              |
| `cloud-url`   | No       | The URL of the Nitro registry                           |

The action automatically attaches source metadata from the GitHub Actions runtime.

If you self-host Nitro or use a dedicated hosted instance, you can specify the `cloud-url` input to point to your instance.
