# id-card-code
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>ID Card Alert</title>
  <script>
   <script>
  // Mapping of employee ID → message with name and number
  const employeeMessages = {
    "003": {
      name: "Aprajith R.",
      phone: "+91-8939865851"
    },
    "002": {
      name: "Prem J.",
      phone: "+91-6374536273"
    },
    "001": {
      name: "Ajay K.",
      phone: "+91-9361141218"
    }
    // Add more employee entries as needed
  };

  window.onload = () => {
    const urlParams = new URLSearchParams(window.location.search);
    const id = urlParams.get('id');
    const company = "Torqsoft Solutions"; // Change to your company name

    if (id && employeeMessages[id]) {
      const emp = employeeMessages[id];
      alert(`This ID belongs to ${emp.name}. Please call ${emp.phone} or return it to ${company}.`);

      // Display employee info on the page
      const infoDiv = document.createElement('div');
      infoDiv.innerHTML = `<h3>Employee Details</h3>
                           <p>Name: ${emp.name}</p>
                           <p>Phone: ${emp.phone}</p>`;
      document.body.appendChild(infoDiv);
    } else {
      alert("This ID card belongs to an employee of our company. Kindly return it to the front desk. Thank you!");
    }
  };
</script>
    }
  </style>
</head>
<body>
  <h2>Thanks for scanning!</h2>
  <p>If you’ve found this ID, please return it to the employee or to the company mentioned.</p>
</body>
</html>
