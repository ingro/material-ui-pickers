# Material-UI picker
> Components, that implements material design date and time pickers for material-ui v1

## [Click here for demo](https://material-ui-pic.firebaseapp.com/)

### Recently updated?
Changelog available [here](https://github.com/dmtrKovalenko/material-ui-pickers/releases)

### Installation
Available as npm package
```sh
npm install material-ui-pickers -S
```

### Usage
Here is a quick example of how to use this package

```jsx
class App extends Component {
  state = {
    selectedDate: new Date(),
    selectedTime: new Date()
  }

  handleDateChange = date => {
    this.setState({ selectedDate: date })
  }

  handleTimeChange = time => {
    this.setState({ selectedTime: time })
  }

  render() {
    const { selectedDate, selectedTime } = this.state

    return (
      <div>
        <DatePicker
          value={selectedDate}
          onChange={this.handleDateChange}
        />

        <TimePicker
          value={selectedTime}
          onChange={this.handleDateChange}
        />
      </div>
    )
  }
}
```

### Props documentation
Here is a list of available props

#### Datepicker
Prop | Type | Default | Definition
------------ | ------------- | ------------- | -------------
value | string, number, Date object, Moment object | null | Datepicker value
format | string | 'MMMM Do' | Moment format string for input
autoOk | boolean | false | Auto accept date on selection
disableFuture | boolean | false | Disable future dates
animateYearScrolling | boolean | false | Will animate year selection (note that will work for browser supports scrollIntoView api)
openToYearSelection | boolean | false | Open datepicker from year selection
minDate | string, number, Date object, Moment object | '1900-01-01' | Minimum selectable date
maxDate | string, number, Date object, Moment object | '2100-01-01' | Maximum selectable date

#### Timepicker
Prop | Type | Default | Definition
------------ | ------------- | ------------- | -------------
value | string, number, Date object, Moment object | null | Timepicker value
format | string | 'MMMM Do' | Moment format string for input
autoOk | boolean | false | Auto accept time on selection

### Known Issues
1. 24 hour displaying for timepicker (now supporting only am/pm)
2. DateTime picker (wrapper above date and time)

They would be added/fixed in one of the nearest release :)

### Contributing
For information about how to contribute, see the [CONTRIBUTING](https://github.com/dmtrKovalenko/material-ui-pickers/blob/master/CONTRIBUTING.md) file.

### LICENSE
The project is licensed under the terms of [MIT license](https://github.com/dmtrKovalenko/material-ui-pickers/blob/master/LICENSE)
