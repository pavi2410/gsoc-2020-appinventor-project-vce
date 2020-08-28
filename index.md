[GSoC Project Page](https://summerofcode.withgoogle.com/projects/#4749864480538624)

# About the Project
A Visible Component Extension or VCE is a type of extension which is able to provide Mock preview of what a component running on a real device would like. It leverages the existing mechanism set in place to write Mocks for the internal components.

# Background
## About Me
## My Experience with MIT App Inventor Open Source Project
## My Mentors
## My Exterience with Google Summer of Code 2020

# My contributions
- [PR #2223 @ mit-cml/appinventor-sources](https://github.com/mit-cml/appinventor-sources/pull/2223)
- [Branch with the new iFrame-based sandbox implementation](https://github.com/pavi2410/appinventor-sources/tree/mvce3) `WIP`
- [iFrame-based VCE SDK](https://gist.github.com/pavi2410/18195e3e6096aa257aa0341524d0da9e)

# Documentation
https://docs.google.com/document/d/17uMiZ5RuwC3u9J1e2oVUIGNPVHA8Mp2umDka6pXJ244/edit?usp=sharing `WIP`

# Sample Extensions I made for testing
- [SimpleLabel](https://github.com/pavi2410/vce-samples/tree/simplelabel) (mimicks the built-in Label component)
- [Cowsay](https://github.com/pavi2410/vce-samples/tree/cowsay) (this extension displays text said by cow)

## Code for the Mock for SimpleLabel extension
```js
class MockSimpleLabel extends MockVisibleExtension {
  static TYPE = "com.pavi2410.SimpleLabel"

  constructor(uuid) {
    super(MockSimpleLabel.TYPE, uuid)
    this.label = document.createElement('span')
    this.initComponent(this.label)
  }

  onCreateFromPalette() {
    this.changeProperty("Text", this.getName() || "NA");
  }

  onPropertyChange(propertyName, newValue) {
    switch (propertyName) {
      case 'Text': {
        this.el.innerText = newValue
        break
      }
    }

    super.onPropertyChange(propertyName, newValue)
  }
}

MockComponentRegistry.register(MockSimpleLabel.TYPE, MockSimpleLabel)
```

# Demo

# Technical Challenges
- Creating JavaScript sandbox to securely evaluate third-party extensions' Mock
- Getting GWT to work with dynamically loaded external JavaScript code

# Future Work
- Can't create more than one instance of a VCE `WIP`
- Reloading the page causes a runtime error, making VCE implementation useless `WIP`
- Implement callback messaging system with iframe
- Mock Container support
- More and more rigorous testing.
