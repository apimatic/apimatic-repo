# Store

Access to Petstore orders

```ruby
store_controller = client.store
```

## Class Name

`StoreController`

## Methods

* [Place Order](../../doc/controllers/store.md#place-order)
* [Get Order by Id](../../doc/controllers/store.md#get-order-by-id)
* [Delete Order](../../doc/controllers/store.md#delete-order)
* [Get Inventory](../../doc/controllers/store.md#get-inventory)


# Place Order

Place an order for a pet

```ruby
def place_order(body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`Order`](../../doc/models/order.md) | Body, Required | order placed for purchasing the pet |

## Response Type

[`Order`](../../doc/models/order.md)

## Example Usage

```ruby
body = Order.new(
  nil,
  nil,
  nil,
  nil,
  nil,
  nil
)

result = store_controller.place_order(body)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Invalid Order | `APIException` |


# Get Order by Id

For valid response try integer IDs with value >= 1 and <= 10. Other values will generated exceptions

```ruby
def get_order_by_id(order_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `order_id` | `Integer` | Template, Required | ID of pet that needs to be fetched<br>**Constraints**: `>= 1`, `<= 10` |

## Response Type

[`Order`](../../doc/models/order.md)

## Example Usage

```ruby
order_id = 62

result = store_controller.get_order_by_id(order_id)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Invalid ID supplied | `APIException` |
| 404 | Order not found | `APIException` |


# Delete Order

For valid response try integer IDs with positive integer value. Negative or non-integer values will generate API errors

```ruby
def delete_order(order_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `order_id` | `Integer` | Template, Required | ID of the order that needs to be deleted<br>**Constraints**: `>= 1` |

## Response Type

`void`

## Example Usage

```ruby
order_id = 62

store_controller.delete_order(order_id)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Invalid ID supplied | `APIException` |
| 404 | Order not found | `APIException` |


# Get Inventory

Returns a map of status codes to quantities

```ruby
def get_inventory
```

## Response Type

`Hash of Integer`

## Example Usage

```ruby
result = store_controller.get_inventory
```

