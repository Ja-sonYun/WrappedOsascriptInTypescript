# WrappedOsascriptInTypescript

Use osascript with typescript  

build with `npm build`  
run with `npm jxa`  

# Supported Applications

## Calendars

### glue
```typescript
export const accessCalendarOsascript = async <T extends AllOsascriptCalendarsAction>(
  action: T,
  param: OsascriptCalendarPropsType<T>
): Promise<OsascriptCalendarReturnType<T>>
```

| action | parameter | return |
| ------ | --------- | ------ |
| get_calendar_names | `{ }` | `Array<string>` |
| get_calendar_by_key | `{ key, value, request_field }` | object of requested fields |
| create_new_calendar | TODO | TODO |
| get_events_by_key | `{ key, value, until?, calendar_name, request_field, max_size? }` | list of events with requested fields |
| create_new_event | calendar name and object with possible keys and values | uid of new event |
| update_existing_event | calendar name and object with possible keys and new values | boolean |
| delete_existing_event | calendar name and uid | boolean |


# TODO

wrap glue codes with class
