### Data Modelling
## _Single-entry Ledger_

```sh
public class Ledger
    {
        [ScaffoldColumn(false)]
        public int id { get; set; }
	
        public int customerId { get; set; }
	
        [DataType(DataType.Text)]
        [Required(ErrorMessage = "Please enter description"), MaxLength(30)]
        public string desc { get; set; }
	
        public string note { get; set; }
	
        [DefaultValue(0.00)]
        public float expense { get; set; }
	
        [DefaultValue(0.00)]
        public float income { get; set; }
	
        [DefaultValue(0.00)]
        public float balance { get; set; }
	
        [DataType(DataType.Date)]
        [Required(ErrorMessage = "*")]
        public DateTime date { get; set; }


        public void GetBalance(float expense, float income)
        {
            this.balance += income - expense;
        }

    }
```

#Explaination 
 - using Data Annotations for validation. like below.
 
	 ```sh
	 - [ScaffoldColumn(false)]
	 - [DataType(DataType.Text)]
	 - [Required(ErrorMessage = "msg")]
	 - [DefaultValue(0.00)]

	 ```

- Using GetBalance method for set "balance" attribute value means direct get balace value via this method as per below example.

```sh
  public void GetBalance(float expense, float income)
        {
            this.balance += income - expense;
        }
```
