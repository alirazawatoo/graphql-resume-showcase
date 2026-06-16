# GraphQL Resume Showcase

A React and Apollo client that renders resume details from a GraphQL API and submits new experience entries through a mutation.

## Data flow

`Resume` runs the `resume` query, renders profile and position data, and opens `CreatePosition` for validated position, description, and starting-year input. After a successful mutation, Apollo updates the cached position list without a full reload.

The GraphQL server is not included in this repository. Configure the Apollo endpoint used by the application before starting the client.

## Local setup

```bash
npm install
npm start
```

## GraphQL operations

- Query: resume `id`, `name`, `address`, and position records.
- Mutation: create a position with `position`, `description`, and `year`.
- Client behavior: append the returned position to Apollo cache.

## Boundaries

- The historical Heroku URL is not treated as a verified deployment.
- The mutation is available from the UI without a demonstrated authentication or authorization layer.
- Error rendering is intentionally minimal and the test file is only a basic React smoke test.
