# react-datepicker [![build status](https://travis-ci.org/trendmicro-frontend/react-datepicker.svg?branch=master)](https://travis-ci.org/trendmicro-frontend/react-datepicker) [![Coverage Status](https://coveralls.io/repos/github/trendmicro-frontend/react-datepicker/badge.svg?branch=master)](https://coveralls.io/github/trendmicro-frontend/react-datepicker?branch=master)

[![NPM](https://nodei.co/npm/@trendmicro/react-datepicker.png?downloads=true&stars=true)](https://nodei.co/npm/@trendmicro/react-datepicker/)

React DatePicker

Demo: https://trendmicro-frontend.github.io/react-datepicker

## Installation

1. Install the latest version of [react](https://github.com/facebook/react) and [react-datepicker](https://github.com/trendmicro-frontend/react-datepicker):

  ```
  npm install --save react @trendmicro/react-datepicker
  ```

2. At this point you can import `@trendmicro/react-datepicker` and its styles in your application as follows:

  ```js
  import DatePicker, { DateInput, TimeInput } from '@trendmicro/react-datepicker';

  // Be sure to include styles at some point, probably during your bootstraping
  import '@trendmicro/react-datepicker/dist/react-datepicker.css';
  ```

## Usage

### DatePicker

Initialize state in your React component:
```js
state = {
    date: moment().format('YYYY-MM-DD')
};
```

#### Controlled

```js
<DatePicker
    date={this.state.date}
    onSelect={date => {
        this.setState(state => ({ date: date }));
    }}
/>
```

#### Uncontrolled

```js
<DatePicker
    defaultDate={this.state.date}
    onSelect={date => {
        // Optional
    }}
/>
```

### DateInput

Initialize state in your React component:
```js
state = {
    // 2017-08-01
    value: moment().format('YYYY-MM-DD')
};
```

#### Controlled

```js
<DateInput
    value={this.state.value}
    onChange={value => {
        this.setState(state => ({ value: value }));
    }}
/>
```

#### Uncontrolled

```js
<DateInput
    defaultValue={this.state.value}
    onChange={value => {
        // Optional
    }}
/>
```

### TimeInput

Initialize state in your React component:
```js
state = {
    // 08:00:00
    value: moment().format('hh:mm:ss')
};
```

#### Controlled

```js
<TimeInput
    value={this.state.value}
    onChange={value => {
        this.setState(state => ({ value: value }));
    }}
/>
```

#### Uncontrolled

```js
<TimeInput
    defaultValue={this.state.value}
    onChange={value => {
        // Optional
    }}
/>
```

## Examples

### DatePicker
https://github.com/trendmicro-frontend/react-datepicker/tree/master/examples/DatePicker

### DateTimePicker
https://github.com/trendmicro-frontend/react-datepicker/tree/master/examples/DateTimePicker

### DateTimeRangePicker
https://github.com/trendmicro-frontend/react-datepicker/tree/master/examples/DateTimeRangePicker

## API

### Properties

#### DatePicker

Name | Type | Default | Description 
:--- | :--- | :------ | :----------
locale | string | 'en' |
date | object or string | null |
defaultDate | object or string | null |
minDate | object or string | null | The minimum selectable date. When set to null, there is no minimum.
maxDate | object or string | null | The maximum selectable date. When set to null, there is no maximum.
onSelect | function(date) | | Called when a date is selected.
navArrows | object | |
navArrows.prev | node | &lt;i className="fa fa-angle-left" /&gt; |
navArrows.next | node | &lt;i className="fa fa-angle-right" /&gt; |

#### DateInput

Name | Type | Default | Description 
:--- | :--- | :------ | :----------
locale | string | 'en' |
dateFormat | string | 'YYYY-MM-DD' |
value | object or string | null |
defaultValue | object or string | null |
minDate | object or string | null | The minimum selectable date. When set to null, there is no minimum.
maxDate | object or string | null | The maximum selectable date. When set to null, there is no maximum.
onChange | function(value) | | Called when the value changes.
renderIcon | function(props) | |

#### TimeInput

Name | Type | Default | Description 
:--- | :--- | :------ | :----------
value | string | '00:00:00' |
defaultValue | string | '00:00:00' |
onChange | function(value) | | Called when the value changes.
renderIcon | function(props) | |

## License

MIT
