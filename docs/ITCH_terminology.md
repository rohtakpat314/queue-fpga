- **Add:** joins the back and takes the next ticket
- **Execute:** removes shares and keeps the ticket in place (shares_execute_of_A < shares_of_A)
- **Cancel:** remove shares, keep ticket
- **Delete:** remove an order
- **Replace:** delete old order id, append a new id at the back with a new ticket identifier

**Shares ahead of (watched order):** shares ahead = total # of shares ahead of the watched order, for every ticket and its quantity of shares preceding the watched order

## Message

- **Add (A):** new order joins the back, takes the next ticket
- **Add with MPID (F):** same add, extra field is which firm sent it, queue does not use this information
- **Execute (E):** shares come off that order, ticket stays
- **Execute with Price (C):** same share reduction, fill price can differ from displayed price, remaining shares keep their place
- **Cancel (X):** shares come off order, ticket stays
- **Delete (D):** whole order leaves
- **Replace (U):** old id leaves, new id joins back with new ticket
