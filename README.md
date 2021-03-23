# CalculatePay
with corrections
function calculatePay() {
  var payRate = 15;
  numHours = 40;
  var grossPay = payRate * numHours;  
  var federalTaxes = grossPay * .08794;
  var stateTaxes = grossPay * .0476;
  var socialSecurity = grossPay * .062;
  var medicare = grossPay * .0145; 

  
  netPay = grossPay;
  netPay = netPay - stateTaxes;
  netPay = netPay - socialSecurity;
  netPay = netPay - medicare;
  netPay = netPay - federalTaxes;
  netPay = "$" + netPay.toFixed(2)
  document.write(netPay);
}

calculatePay();
