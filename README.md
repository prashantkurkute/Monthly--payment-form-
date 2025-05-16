<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Monthly Payment Form</title>
<style>
  body { font-family: Arial, sans-serif; padding: 20px; }
  label { display: block; margin-top: 10px; }
  input, select { width: 100%; padding: 8px; margin-top: 5px; }
  button { margin-top: 15px; padding: 10px 20px; }
</style>
</head>
<body>
<h2>Monthly Payment Form</h2>
<form id="paymentForm">
  <label for="name">Name</label>
  <input type="text" id="name" required />

  <label for="toPay">To Pay Name</label>
  <input type="text" id="toPay" required />

  <label for="month">Select Month</label>
  <select id="month" required>
    <option value="">Select Month</option>
    <option>January</option><option>February</option><option>March</option>
    <option>April</option><option>May</option><option>June</option>
    <option>July</option><option>August</option><option>September</option>
    <option>October</option><option>November</option><option>December</option>
  </select>

  <label for="amount">Amount</label>
  <input type="number" id="amount" required />

  <button type="submit">Submit Payment</button>
</form>

<script>
  document.getElementById('paymentForm').addEventListener('submit', function(e){
    e.preventDefault();
    alert('Payment submitted for ' + document.getElementById('name').value);
    this.reset();
  });
</script>
</body>
</html>
