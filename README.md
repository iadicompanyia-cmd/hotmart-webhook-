const express = require('express');
const app = express();

app.use(express.json());

app.post('/api/hotmart-webhook', (req, res) => {
  console.log('Recebido da Hotmart:', req.body);
  res.sendStatus(200);
});

app.get('/', (req, res) => {
  res.send('Webhook ativo!');
});

app.listen(3000, () => {
  console.log('Servidor rodando na porta 3000');
});
