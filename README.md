# Kickciety Database Project

Welcome to the **Kickciety Database Project** readme! This project involves the creation of a database named `KICKCIETY` for managing a fictional membership-based organisation. Below is a brief overview of the project structure, including tables, data insertion, views, queries, and advanced features like triggers and events.

## Tables Created

1. **BASES**: Stores information about different bases including their ID, name, location, type, and price.
2. **MEMBERS**: Contains member details such as ID, name, phone number, package, assigned base, and payment key.
3. **PAYMENTS**: Records payments made by members including member ID, amount, and base ID.
4. **SIGN_UPS\<LOCATION>**: Tracks sign-ups per month for each base location.
5. **BASE_OF_THE_YEAR**: Summarizes sign-ups and revenue for each base.
   
## Constraints Added

- Primary keys and foreign keys were added to ensure data integrity among tables.

```sql
ALTER TABLE MEMBERS
  ADD CONSTRAINT MEMBER_IDPK1 PRIMARY KEY (MEMBER_ID);

ALTER TABLE PAYMENTS
  ADD CONSTRAINT PAYMENTSFK1 FOREIGN KEY (MEMBER_ID) REFERENCES MEMBERS (MEMBER_ID);
```

## Views Created

1. **SIGN_UPS_BY_MONTH**: A view showing sign-ups by month across all base locations.
2. **SIGN_UPS_COMBINED**: Combines sign-ups from different base locations into a single view.

## Queries Executed

- Various queries were executed to retrieve and analyze data from the database, including total sign-ups by month, combined sign-ups by location, member names from specific bases, total payments from selected locations, and base with the highest revenue in a particular month.

## Advanced Features Implemented

1. **Triggers**: An example trigger was created to update the total sign-ups for the London base whenever a new member is added to the database with London as their base.
2. **Events**: An event was created to calculate revenue monthly for the year 2023.

## Usage

To use this project, simply execute the provided SQL scripts in your preferred database management system.

## Contributors

- This project was created by Phoebe Musuka

## License

This project is licensed under the MIT License.
