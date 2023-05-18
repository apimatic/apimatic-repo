
# Order

## Structure

`Order`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Optional | - |
| `pet_id` | `Integer` | Optional | - |
| `quantity` | `Integer` | Optional | - |
| `ship_date` | `DateTime` | Optional | - |
| `status` | [`Status1Enum`](../../doc/models/status-1-enum.md) | Optional | Order Status |
| `complete` | `TrueClass\|FalseClass` | Optional | - |

## Example (as JSON)

```json
{
  "id": 112,
  "petId": 152,
  "quantity": 68,
  "shipDate": "2016-03-13T12:52:32.123Z",
  "status": "delivered"
}
```

