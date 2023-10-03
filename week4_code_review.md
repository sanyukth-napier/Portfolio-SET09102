# Code review

This section documents your practical work from week 4 in which you attempt a series of 
code review challenges. For your portfolio, do the following:

1. Choose the code review challenge which best demonstrates your skills.
2. Copy the code into your portfolio using a Markdown
   [fenced code block](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks).
3. Provide some descriptive commentary that identifies the problems.
4. Show your improved version of the code in a second code block.
5. Explain in one or more paragraphs why your solution is a good one.

**DO**

* Use grammatically correct sentences and paragraphs for your commentary.
* Make clear reference to the code in your commentary. GitHub Markdown does not support
  line numbers and so you need to make sure that the reader knows which line you are
  referring to from your description.
* Refer to recognised principles or rules when describing your solution. "I thought it
  would be better that way" is not sufficient: you need to have specific reasons.

**DON'T**

* Include multiple examples. Make the decision about which example shows your best
  work and use that one.
* 

```

class Program
{
    public static void Main(string[] args)
    {
        // create a new invoice
        var invoice = new Invoice
        {
            InvoiceNo = 1,
            Customer = "John Doe",
            IssuedDate = new DateOnly(2023, 4, 1),
            Description = "Website Design",
            Amount = 1000,
            Tax = Amount * CURRENT_TAX_RATE
        };

        invoice.Save();

    }
}

```

## Problems
The code violates C# coding conventions.There is an undefined variable, The code attempts to calculate the tax using Amount * CURRENT_TAX_RATE, but there's no declaration 
or initialization of the Amount variable. The 'invoice.Amount' needs to be used  to access the 'Amount' property of the invoice object. The code is also missing class definitions. 
The code uses the Invoice class, but the definition of the Invoice class is not provided in the code snippet. The 'Save' method is also not defined is this code snippet. 
To follow standard conventions, the class should be defined with appropriate properties and methods.

## Improved Code

```

using System;

class Invoice
{
    // Properties of the Invoice class
    public int InvoiceNo { get; set; }        // Invoice number
    public string Customer { get; set; }      // Customer name
    public DateOnly IssuedDate { get; set; }  // Date when the invoice is issued
    public string Description { get; set; }   // Description of the invoice
    public decimal Amount { get; set; }       // Total invoice amount
    public decimal Tax { get; set; }          // Tax amount on the invoice

    // Method to save the invoice
    public void Save()
    {
        // Implementation to save the invoice
        Console.WriteLine($"Invoice {InvoiceNo} saved for {Customer}");
    }
}

class Program
{
    static void Main(string[] args)
    {
        // Create a new invoice
        var invoice = new Invoice
        {
            InvoiceNo = 1,                                        // Set invoice number
            Customer = "John Doe",                                // Set customer name
            IssuedDate = new DateOnly(2023, 4, 1),                // Set issuance date
            Description = "Website Design",                       // Set invoice description
            Amount = 1000,                                       // Set invoice amount
            
            // Calculate tax based on the invoice amount and current tax rate
            Tax = invoice.Amount * GetCurrentTaxRate()
        };

        // Call the Save method to save the invoice
        invoice.Save();
    }

    // Method to get the current tax rate (replace with actual logic)
    static decimal GetCurrentTaxRate()
    {
        // Implement logic to get the current tax rate
        return 0.1m; // Example: 10% tax rate
    }
}

 ```    