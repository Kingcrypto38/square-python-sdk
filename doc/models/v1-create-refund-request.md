
# V1 Create Refund Request

V1CreateRefundRequest

## Structure

`V1 Create Refund Request`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `payment_id` | `str` | Required | The ID of the payment to refund. If you are creating a `PARTIAL`<br>refund for a split tender payment, instead provide the id of the<br>particular tender you want to refund. |
| `type` | [`str (V1 Create Refund Request Type)`](../../doc/models/v1-create-refund-request-type.md) | Required | - |
| `reason` | `str` | Required | The reason for the refund. |
| `refunded_money` | [`V1 Money`](../../doc/models/v1-money.md) | Optional | - |
| `request_idempotence_key` | `str` | Optional | An optional key to ensure idempotence if you issue the same PARTIAL refund request more than once. |

## Example (as JSON)

```json
{
  "payment_id": "payment_id2",
  "type": "FULL",
  "reason": "reason2",
  "refunded_money": {
    "amount": 214,
    "currency_code": "SRD"
  },
  "request_idempotence_key": "request_idempotence_key6"
}
```

