---
layout: page
---
### YAML
#### RubyからYAML
    Entry.find(1).to_yaml

#### YAMLからRuby
    yaml = <<-YAML

### XML
#### RubyからXML
    Entry.find(1).to_xml

#### XMLからHash
    xml = <<-XML

### JSON
#### RubyからJSON
    Entry.find(1).to_json
    {key0: "value0", key1: "value1" }.to_json

#### JSONからHash
    ActiveSupport::JSON.decode('{title: "my title", body: "my body", id: 1 }')