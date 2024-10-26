# Currency Converter

This project is a **React-based Currency Converter** that allows users to convert between different currencies using real-time exchange rates.

## Features
- Convert between multiple currencies.
- Swap functionality to switch the source and target currencies.
- Real-time exchange rate fetching using **ExchangeRate-API**.
- Built with **React** and **Vite**.
- Styled using **Tailwind CSS**.

## Components & Hooks

### 1. `useCurrencyInfo` Hook
- **Purpose:** Fetches and stores currency conversion rates based on the selected currency.
- **Usage:** const currencyInfo = useCurrencyInfo(from);
- **Returns:** An object containing conversion rates.



```javascript
const currencyInfo = useCurrencyInfo(from); // Example usage
```

### 2. `InputBox` Component
- Purpose: Handles input and dropdown for currency and amount.
- Props:
 - `label` (string): Label for the input field.
 - `amount` (number): Value of the amount field.
 - `onAmountChange` (function): Handler for amount changes.
 - `onCurrencyChange` (function): Handler for currency changes.
 - `currencyOptions` (array): List of available currencies.
 - `selectCurrency` (string): Selected currency value.
 - `amountDisable` (bool): Disables amount input.
 - `currencyDisable` (bool): Disables currency dropdown.

 ```javascript
<InputBox
  label="From"
  amount={amount}
  currencyOptions={options}
  onCurrencyChange={setFrom}
  onAmountChange={setAmount}
  selectCurrency={from}
/>
```

### 3. `App` Component
- **Purpose:** Main component handling the currency conversion logic.

- **State Variables:**
  - `amount`: Stores the amount to be converted.
  - `from`: The currency from which the conversion is happening.
  - `to`: The currency to which the conversion is happening.
  - `convertedAmount`: Stores the result after conversion.

- **Functions:**
  - `swap`: Switches the "from" and "to" currencies.
  - `convert`: Converts the amount using fetched rates.

---

## Setup Instructions

### 1. Clone the Repository:
```bash
git clone https://github.com/Babita00/currency-converter.git
cd currency-converter
```
### 2. Install Dependencies:
```bash
npm install
```
### 3. Run the APP:
```bash
npm run dev
```
## How it Works
1. **User Input:**  
   Enter the amount and select the desired currencies using the `InputBox` components.

2. **Convert:**  
   Click the **Convert** button to calculate the converted amount using real-time exchange rates.

3. **Swap:**  
   Use the **Swap** button to instantly switch the source and target currencies.



## API Used

**ExchangeRate-API**  
**API Endpoint:**  
`https://v6.exchangerate-api.com/v6/YOUR_API_KEY/latest/{currency}`

> **Note:** Replace `YOUR_API_KEY` with your actual API key to access the service.

## Technologies Used

- **React**: For building the user interface and managing component-based state.
- **Vite**: As the development environment for fast and optimized builds.
- **Tailwind CSS**: For styling the application with utility-first CSS.

## Troubleshooting

### Issue: Currency Options Not Loading
- **Solution**: Check if the API response contains conversion rates. Ensure the API request is successfully fetching data, and handle any errors or empty responses.

### Issue: Amount Not Updating Correctly on Swap
- **Solution**: Confirm the amount state is updating correctly by calling `swap()` and ensuring the state refreshes immediately after the swap operation.

---

Happy coding!










