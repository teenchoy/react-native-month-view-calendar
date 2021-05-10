# React Native Month View Calendar

<p>
<img src="screenshots/1.png?raw=1" width="200" />
&nbsp;
<img src="screenshots/2.png?raw=1" width="200" />
</p>

## Install

```
npm install --save react-native-month-view-calendar
```

### Basic usage
```js
import { MonthViewCalendar } from 'react-native-month-view-calendar';
import { View, ScrollView } from 'react-native'

const Component = () => {
  const eventsForCalendar = [
  	{
  	  title: 'My awesome event',
  	  date: new Date(),
  	},
  ];

  return (
    <ScrollView>
      <MonthViewCalendar
        events={eventsForCalendar}
        renderEvent={(event, i) => {
          return (
            <Text key={i} numberOfLines={1}>{event.title}</Text>
          )
        }}
      />
    </ScrollView>
  );
}
```
### Props

| Properties | Default | Description|
| --- | --- | ---|
|date            |new Date()|Date from which the calendar will be built|
|dayTextStyles   |{}|Styles for label day(numer of day), can be array or object|
|events          || Array of events|
|headerTextStyles|{}|Styles for label week day name, can be array or object|
|weekDays        |['S', 'M', 'T', 'W', 'T', 'F', 'S']|Array with name of the day of the week|
|renderEvent     ||Function required to render event information. Example (event, index) => <Event key={index} />|

### Event object
```js
{
  /// your props
  date: new Date(),
}
```