---
category: minorAnalysis
---
* The `rb/xxe` query has been updated to add the following sinks for XML external entity expansion:
    1. Calls to parse XML using `LibXML` when its `default_substitute_entities` option is enabled.
    2. Uses of the Rails methods `ActiveSupport::XmlMini.parse`, `Hash.from_xml`, and `Hash.from_trusted_xml` when `ActiveSupport::XmlMini` is configured to use `LibXML` as its backend, and its `default_substitute_entities` option is enabled.