autoform-bs-daterangepicker
====================
This project forked from [daterangepicker](https://github.com/dangrossman/bootstrap-daterangepicker/) packaged for [Meteor](http://meteor.com).

What change ?

* Remove dependence from momentjs
* Replace depends to [baysao:bootstrap-daterangepicker](https://atmospherejs.com/baysao/bootstrap-daterangepicker)

### Installation

With Meteor 0.9.3 and above, install using:

```sh
$ meteor add baysao:autoform-bs-daterangepicker
```


### Usage

```js

SearchSchema = new SimpleSchema({

  searchRange: {
    type: [Date],
    label: "From - To",
    optional: false,
    autoform: {
      type: "bootstrap-daterangepicker",
      dateRangePickerValue: moment().add(1, 'days').format("DD/MM/YYYY") + " - " + moment().add(3, 'days').format("DD/MM/YYYY"),
      dateRangePickerOptions: {
        dateLimit: { days: 6 },
        minDate: moment().add(-150, 'days'),
        maxDate:moment().add(6, 'months'),
        startDate: moment().add(1, 'days'),
        endDate: moment().add(3, 'days'),
        timePicker: false,
        format: 'DD/MM/YYYY',
        timePickerIncrement: 30,
        timePicker12Hour: false,
        timePickerSeconds: false
      }
    }
  },

  ...

});

```
