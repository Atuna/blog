```
{
  __type(name: "Tree") {
    name
    kind
    description
    fields {
      name
      description
    }
  }
}
```

查看所有的可用字段
```
{
  __schema {
    types {
      name,
      description
    }
  }
}
```

查看下Tree下entries的字段的类型
```
{
  __type(name: "Tree") {
    entries {
      type {
        name
        kind
        ofType {
          name
          kind
        }
      }
    }
  }
}

```

查看Tree下各个字段的类型
```
{
  __type(name: "Tree") {
    fields {
      name
      description
      type {
        name
        kind
        ofType {
          name
          kind
        }
      }
    }
  }
}
```

目前的GraphQL规范明确指出不能（无限）递归的获取数据
https://github.community/t/graphql-equivalent-of-repos-owner-repo-git-trees-tree-sha-recursive-1/14075
https://github.com/graphql/graphql-spec/issues/91



https://juejin.im/post/5c87b1776fb9a049ac7a0247