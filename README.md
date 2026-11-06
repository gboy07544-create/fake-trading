// Simple realistic price simulator (random walk)
let price = 100;
function tick() {
  const drift = 0.0001;
  const volatility = 0.02;
  const shock = (Math.random() - 0.5) * volatility;
  price = price * (1 + drift + shock);
  return price;
}
