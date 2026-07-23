# Data Dictionary

## leads.json

- `lead_id`: Unique identifier for the customer lead.
- `customer_name`: Customer name.
- `budget_egp`: Maximum stated budget in EGP; can be null when unknown.
- `budget_flexibility`: Whether the customer has a fixed budget or can stretch it.
- `preferred_locations`: Ordered list of preferred locations.
- `property_types`: Acceptable property types.
- `bedrooms`: Minimum/target number of bedrooms; null when unknown.
- `bathrooms`: Minimum/target number of bathrooms; null when unknown.
- `minimum_area_sqm`: Minimum desired property area; null when unknown.
- `purpose`: Purchase intent.
- `preferred_payment_plan`: Preferred payment method.
- `availability_timeline`: Desired purchase/availability timeline.
- `must_have_features`: Features required for a valid match.
- `nice_to_have_features`: Features that improve a match but are not mandatory.
- `notes`: Free-text context that may require reasoning.
- `status`: Lead status.

## properties.json

- `property_id`: Unique identifier for the property.
- `title`: Human-readable property name.
- `location`: Property location.
- `property_type`: Apartment, villa, townhouse, or duplex.
- `price_egp`: Listed price in EGP.
- `bedrooms`: Number of bedrooms.
- `bathrooms`: Number of bathrooms.
- `area_sqm`: Property area in square meters.
- `availability`: `available`, `reserved`, or `sold`.
- `payment_plan`: `cash` or `installments`.
- `features`: Property features.
- `ready_to_move`: Whether the property is ready to move in.

## Design Notes

This is a synthetic dataset created specifically for the Agent Design Lab.
It is intentionally designed to contain:
- Exact matches.
- Flexible-budget matches.
- Alternative-location/type matches.
- Unavailable properties.
- Early-stage leads.
- Missing-information cases.
- Cases where the next action depends on previous tool results.
