let makanan = [
  {
    id: "1",
    namaMakanan: "Rendang",
    keteranganMakanan: "Makanan Khas Padang",
    gambar: "https://raw.githubusercontent.com/MuhammadHudaibi/json-mobpro1/master/rendang.jpg"
  },
  {
    id: "2",
    namaMakanan: "Tahu Sumedang",
    keteranganMakanan: "Makanan Khas Sumedang",
    gambar: "https://raw.githubusercontent.com/MuhammadHudaibi/json-mobpro1/master/tahu.jpg"
  }
];

// Endpoint GET
app.get('/makanan', (req, res) => {
  res.json(makanan);
});

// Endpoint POST
app.post('/makanan', (req, res) => {
  const newMakanan = {
    id: (makanan.length + 1).toString(),  // Generate ID baru
    namaMakanan: req.body.namaMakanan,
    keteranganMakanan: req.body.keteranganMakanan,
    gambar: req.body.gambar
  };
  makanan.push(newMakanan);
  res.status(201).json(newMakanan);
});

// Endpoint DELETE
app.delete('/makanan/:id', (req, res) => {
  const id = req.params.id;
  makanan = makanan.filter(m => m.id !== id);
  res.status(204).send();
});
