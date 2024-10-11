# apiAtiv

const express = require('express');
const app = express();
const port = 3000;
 
app.use(express.json());
 
app.post('/veiculos', (req,res) => {
    const { marca, modelo, ano, proprietario, cor } =req.body;
 
});
 
 
 
// Inserir
app.post('/veiculos', (req, res) => {
    const { marca, modelo, ano, proprietario, cor } = req.body;
 
});
 
 
 
// Atualizar por Id
app.put('/veiculos/:id', (req, res) => {
    const { id } = req.params;
    const { marca, modelo, ano, proprietario, cor } = req.body;
});
 
 
// Deletar por Id
app.delete('/veiculos/:id', (req, res) => {
    const { id } = req.params;
 
});
 
 
 
// Deletar por modelo
app.delete('/veiculos/:modelo', (req, res) => {
    const { modelo } = req.params;
    veiculos = veiculos.filter(v=>v.modelo !==modelo);
    res.send({ message: `Todos os veículos do modelo ${modelo} foram deletados` });
});
 
 
 
 
 
// Mostrar todos
app.get('/veiculos', (req, res) => {
    res.send(veículos);
});
 
// Mostrar por id
app.get('/veiculos/:id', (req, res) => {
    res.send(veiculos);
});
 
// Mostrar por ano
app.get('/veiculos/:ano', (req, res) => {
    res.send(veiculos);
});
 
 
app.listen(port, () => {
    console.log(`Exemplo de app sendo "escutado" na porta ${port}`);
});
 
 
