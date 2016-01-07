# REACT EASY SWIPE

Add swipe interactions to your react component.

## Demo
``


## Instalation
`npm install react-easy-swipe --save`

## Usage
```javascript
import React, {Component} from 'react';
import ReactDOM from 'react-dom';
import Swipe from './react-swipe';

class MyComponent extends Component {
  onSwipeStart() {
    console.log('Start swiping...');
  }

  onSwipeMove(position) {
    console.log(`Moved ${position.x} pixels horizontally`);
    console.log(`Moved ${position.y} pixels vertically`);
  }

  onSwipeEnd() {
    console.log('End swiping...');
  }

  render() {
    const boxStyle = {
      width: '100%',
      height: '300px',
      border: '1px solid black',
      background: '#ccc',
      padding: '20px',
      fontSize: '3em'
    };

    return (
      <Swipe
        onSwipeStart={this.onSwipeStart}
        onSwipeMove={this.onSwipeMove}
        onSwipeEnd={this.onSwipeEnd}>
          <div style={boxStyle}>Open the console and swipe me</div>
      </Swipe>
    );
  }
}

ReactDOM.render(<MyComponent/>, document.getElementById('root'));

```

## Properties

```javascript
{
  tagName: PropTypes.string,
  className: PropTypes.string,
  style: PropTypes.object,
  children: PropTypes.node,
  onSwipeUp: PropTypes.func,
  onSwipeDown: PropTypes.func,
  onSwipeLeft: PropTypes.func,
  onSwipeRight: PropTypes.func,
  onSwipeStart: PropTypes.func,
  onSwipeMove: PropTypes.func,
  onSwipeEnd: PropTypes.func
}
```

## Contributing

Please, feel free to contributing. You may file an issue or submit a pull request!

* Generated using [react-init](https://www.npmjs.com/package/react-init)

### TODOs
- [ ] write tests
- [ ] write docs
