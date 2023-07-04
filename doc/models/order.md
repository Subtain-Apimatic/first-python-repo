
# Order

## Structure

`Order`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `long\|int` | Optional | - |
| `pet_id` | `long\|int` | Optional | - |
| `quantity` | `int` | Optional | - |
| `ship_date` | `datetime` | Optional | - |
| `status` | [`Status1Enum`](../../doc/models/status-1-enum.md) | Optional | Order Status |
| `complete` | `bool` | Optional | - |

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

