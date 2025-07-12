# id-card-code
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>ID Card Alert</title>
  <script>
    // Mapping of employee ID → message with name and number
    const employeeMessages = {
      "101": {
        name: "Aprajith R.",
        phone: "‪+91-9876543210‬"
      },
      "102": {
        name: "Sneha M.",
        phone: "‪+91-9123456789‬"
      },
      "103": {
        name: "Rajesh K.",
        phone: "‪+91-9988776655‬"
      }
      // Add more employee entries as needed
    };

    window.onload = () => {
      const urlParams = new URLSearchParams(window.location.search);
      const id = urlParams.get('id');
      const company = "Torqsoft Solutions"; // Change to your company name

      if (id && employeeMessages[id]) {
        const emp = employeeMessages[id];
        alert(This ID belongs to ${emp.name}. Please call ${emp.phone} or return it to ${company}.);
  } else {
        alert("This ID card belongs to an employee of our company. Kindly return it to the front desk. Thank you!");
      }
    };
  </script>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      padding: 40px;
    }
  </style>
</head>
<body>
  <h2>Thanks for scanning!</h2>
  <p>If you’ve found this ID, please return it to the employee or to the company mentioned.</p>
</body>
</html>
