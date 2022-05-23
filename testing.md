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

## Ground Rules

* Only mock classes I own
* Don't mock/stub the object under test

## Mocks vs Stubs

### Stub

A stub is a stand in for another object. It's just there to make sure the rest
of the code can run. No verifications are preformed on stubs.

### Mock

A mock has the same purpose as a stub but also to verify a message was sent.
