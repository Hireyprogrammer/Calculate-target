## Student Information

- **Name**: Abdinajib Mohamed Hassan
- **Class ID**: C1210027
- **Class Name**: CA211

--- 
# Target Calculation Excluding Specific Days

## Description

This project is designed to calculate the proportional distribution of an annual target across multiple months, excluding specific days of the week (in this case, Fridays). The task ensures that Fridays are excluded from the working days when distributing the target over a specified date range.

The function `calculateTotalTarget(startDate, endDate, totalAnnualTarget)` helps you calculate the number of working days, assign targets to each month, and sum up the total target, ensuring a correct distribution of the annual target while excluding non-working Fridays.

## How to Run the Code

1. Clone this repository:
   ```bash
   git clone <repository-link>
   cd <repository-name>
   ```

2. Ensure you have Node.js installed. Run the function in any JavaScript environment (like Node.js). For example:
   ```bash
   node index.js
   ```

3. Example of usage:
   ```js
   console.log(calculateTotalTarget('2024-01-01', '2024-03-31', 5220));
   ```

## Function Explanation

The function `calculateTotalTarget(startDate, endDate, totalAnnualTarget)` performs the following tasks:

1. **Date Handling**: 
   - Converts the input strings (`startDate`, `endDate`) into Date objects.
   - Iterates through the date range, incrementing by one day and counting non-Friday working days for each month.

2. **Working Days**:
   - Excludes Fridays (day index `5`) from the calculation to focus only on valid working days.

3. **Monthly Target Distribution**:
   - Distributes the total annual target evenly across 12 months.
   - Assigns targets only to the months that have valid working days (non-Friday days).

4. **Return Format**:
   - Returns an object containing:
     - `daysWorkedExcludingFridays`: Non-Friday working days for each month in the range.
     - `monthlyTargets`: Targets assigned to each month with valid working days.
     - `totalTarget`: The total distributed target.

## Example Output

For the call:
```js
calculateTotalTarget('2024-01-01', '2024-03-31', 5220);
```

The function will return:
```json
{
  "daysWorkedExcludingFridays": [27, 25, 26],
  "monthlyTargets": [435, 434.99999999999994, 435],
  "totalTarget": 1305
}
```

## Assumptions

- The input dates are in the format `YYYY-MM-DD`.
- The function currently excludes only Fridays from the working days.
- The total annual target is evenly distributed across 12 months, even though each month may have a different number of working days.

## Future Extensions

This function can be extended to exclude different non-working days by passing additional parameters, allowing dynamic exclusions based on business requirements.
