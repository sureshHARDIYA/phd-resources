# Challenges

`GraphQL` provides a enormous power to the client to craft very complex queries; however, unmanaged queries can have sophisticated security implications. For instance, a malicious actor could submit an expensive, nested query to overload a `GraphQL` server, database and network. Lack of right protections can open up to a DoS attack \cite{r17}.

## Circular relationship complexity:

Consider **many-to-many** relationship schema and a query to create circular relationship complexity. Allowing such queries increases response objects exponentially and ultimately crashes the server. There are certain ways to mitigate this issue including Cross-Origin Resource Sharing (CORS) \cite{r18}; limiting size of query string; limiting maximum depth of query string\footnote{https://github.com/stems/graphql-depth-limit}; limiting amount of resources to fetch in one request - fetching **100000** texts as in \ref{listing2} is not-trivial, hence pagination with limited resources is recommended; and performing query cost analysis\footnote{https://github.com/pa-bru/graphql-cost-analysis} before execution and rejecting request with higher complexity.

```
type ThreadDefinition {
  title: String
  text(first: Int, after: String): [MessageDefinition]
}

type MessageDefinition {
  text: String
  thread: ThreadDefinition
}

type Query {
  thread(id: ID!): ThreadDefinition
}
```

```
query complicatedQuery {
  thread(id: "ID") {
    text(first: 100000) {
      thread {
        text(first: 100000) {
          thread {
              # ...repeat 100000 (n) times ...
            }
          }
        }
      }
    }
  }
}
```

## Schema Duplication:

Creation of `GraphQL` based backend, which acts as a database abstraction layer, involves a plethora of similar but not-quite-identical code especially schema definition. It requires i) schema definition based on the choice of the database being used (this project uses mongoDB, so schema are based on mongoose \footnote{https://mongoosejs.com/}); and ii) schema definition for a `GraphQL` endpoint. This creates redundancy of schema on one hand and requires synchronization between two independent sources of truth. There are a number of emerging solutions in the `GraphQL` echosystem including [`PostGraphile`](https://www.graphile.org/postgraphile/)- generates GraphQL schema from \texttt{PostgreSQL} database; Prisma\footnote{https://www.prisma.io/} - allows to generate queries and mutations. In addition to these, various other transformation libraries are being developed by the community to support various database systems. Removal of duplicate schema from our prototype and usage of the similar \texttt{mongoDB} schema to a `GraphQL` schema is subjective to future work.
