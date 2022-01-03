---
sidebar_label: Plugins
sidebar_position: 5
---

## What is a Plugin?

```ruby title="/app/models/blog/plan.rb"
module Blog
  class Plan
    def hello_docusaurus
      return 'hey now!'
    end

    def ten
      3 + 4
    end

    def tenn() = 'this'
  end
end
```
