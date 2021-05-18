# New benchmark instances for the multi-depot heterogeneous dial-a-ride problem (MDHDARP)

Instances proposed by [Malheiros et al. (2021)](https://www.sciencedirect.com/science/article/abs/pii/S0305054820303130).

The instances were created considering only the characteristics of group I proposed by [Parragh (2011)](https://www.sciencedirect.com/science/article/pii/S0968090X10001075) and [Braekers et al. (2014)](https://www.sciencedirect.com/science/article/pii/S0191261514000800?casa_token=fwJPWO5MaYEAAAAA:ODUpniNRLLk2PJXecvN2-ebqKlTmgpR0kNjebdoHOjaqjmnv9TkOUcFleNPf38U1nYZP_J-FyDk). The new dataset containing 24 instances ranging from 9 to 16 vehicles, and 72 to 192 requests.

## Instance names

The name of each instance follow the format below:
`"a" + number_of_vehicles + "-" + number_of_requests + "hetIUY.txt"`

### Example:
a10-100hetIUY.txt: `number_of_vehicles = 10` and `number_of_requests = 100`

## Instance format

```
number_of_vehicles number_of_requests
```
- For each vehicle:
```
route_duration capacity_resource_1 capacity_resource_2 capacity_resource_3 capacity_resource_4
```

- Dummy vertex
```
id x_coord y_coord service_time max_ride_time demand_resource_1 demand_resource_2 demand_resource_3 demand_resource_4 earliest_tw latest_tw
```
- For each pickup vertex:
```
id x_coord y_coord service_time max_ride_time demand_resource_1 demand_resource_2 demand_resource_3 demand_resource_4 earliest_tw latest_tw
``` 

- For each delivery vertex:
```
id x_coord y_coord service_time max_ride_time demand_resource_1 demand_resource_2 demand_resource_3 demand_resource_4 earliest_tw latest_tw
```

- Dummy vertex
```
id x_coord y_coord service_time max_ride_time demand_resource_1 demand_resource_2 demand_resource_3 demand_resource_4 earliest_tw latest_tw
```
### Extra information

- Coordinates ranging from `-10` to `10`
- For a given request, its pickup and delivery vertices are paired as follows: `pickup_id, pickup_id + number_of_requests`
- For each request and each resource `pickup_demand + delivery_demand = 0`
- For each request, `max_ride_time = 30`, the maximum ride time of a request is set at its pickup vertex
- For each request, `service_time = 3`
- Each demand ranging from `-1` to `1`
- Dummy vertices can be used as depot for heterogeneous dial-a-ride problem (HDARP)
