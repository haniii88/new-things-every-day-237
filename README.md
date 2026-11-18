function dailyLog232() {
  const energyUsage = [
    { period: "Morning", kwh: 12.5 },
    { period: "Afternoon", kwh: 18.2 },
    { period: "Evening", kwh: 22.8 },
    { period: "Night", kwh: 9.4 }
  ];

  const total = energyUsage.reduce(
    (sum, item) => sum + item.kwh,
    0
  );

  const average = total / energyUsage.length;

  const highest = energyUsage.reduce(
    (max, item) => item.kwh > max.kwh ? item : max
  );

  console.log("Daily Energy Consumption Report");
  console.log("--------------------------------");
  console.log(`Total Usage: ${total.toFixed(2)} kWh`);
  console.log(`Average Usage: ${average.toFixed(2)} kWh`);
  console.log(`Highest Usage: ${highest.period} (${highest.kwh} kWh)`);
}

dailyLog232();
