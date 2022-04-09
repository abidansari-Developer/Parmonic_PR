### Design
##_Creating basic four microservices (GET, POST, PUT & DELETE) -- via Ledger for Transaction  _


```sh
// GET - Transaction by ID
			public async Task<Ledger> Get(int id)
			{
				Ledger objLedger = new Ledger();
				await Task.Run(() =>
				{
					Task.Delay(100).Wait();
					// Code omitted:
					//
					// Given a Transaction Id {id}, retrieves a LEDGER object corresponding
					// to the entry in the database with {id} as its Id.
				});

				return (objLedger);
			}
			```
			
```sh
// POST - Insert Transaction 
			public async Task<bool> Post(Ledger data)
			{
				await Task.Run(() =>
				{
					Task.Delay(100).Wait();
					// Code omitted:
					//
					// Insert data in the database.

				});
				return true;
			}
```
```sh
// PUT - Update Transaction 
			public async Task<bool> Put(int id, Ledger data)
			{
				await Task.Run(() =>
				{
					Task.Delay(100).Wait();
					// Code omitted:
					//
					// Update data in the database by using id.
				});
					return true;
			}
```
```sh
// DELETE - Insert Transaction 
//param - id

			public async Task<bool> Delete(int id)
			{
				await Task.Run(() =>
				{
					Task.Delay(100).Wait();
					// Code omitted:
					//
					// Delete data in the database by using id.
				});
					return true;
			}
```
##_Creating Other microservices _


```sh
//Get list of Transaction respect of customer-id
//Param - customerId

			public async Task <List<Ledger>> GetLedgersAsync(int customerId)
			{
				List<Ledger> lstLedger = new List<Ledger>();
				await Task.Run(() =>
				{
					Task.Delay(100).Wait();
					// Code omitted:
					//
					// lstLedger = get all transaction record from the database recpect of customer-Id.
				});
				return lstLedger;
			}
```
```sh
//Get History of Transaction
//Param - startDate
//Param - endDate

			public async Task <List<Ledger>> GetTransactionHistoryAsync(DateTime startDate, DateTime endDate)
			{
				List<Ledger> lstLedger = new List<Ledger>();
				await Task.Run(() =>
				{
					Task.Delay(100).Wait();
					// Code omitted:
					//
					// lstLedger = get history of transaction from the database based on start-date and end-date.
				});
				return lstLedger;
			}
```
```sh
//Get Balance enquiry 
//Param - customerid

			public async Task<List<Ledger>> GetBalanceEnquiryAsync(int customerId)
			{
				List<Ledger> lstLedger = new List<Ledger>();
				await Task.Run(() =>
				{
					Task.Delay(100).Wait();
					// Code omitted:
					//
					// lstLedger = get balance from the database based on customer-id.
				});
				return lstLedger;
			}
```