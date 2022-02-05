# Testing

## Object Under Test

When using RSpec, use a named subject for the object under test. Example:

```ruby
RSpec.describe String do
  subject(:string) { "this is a string" }

  describe "#length" do
    it "returns the length of the string" do
      expect(string.length).to eq(16)
    end
  end
end
```

## Three Phases of a Test

Divide each test into the following three phases:

* Setup
* Execution
* Expectation
