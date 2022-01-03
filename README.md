# Nodejs_Task

##Delete movie
app.delete("/movies/:id", async (request, response) => {
  const { id } = request.params;
  const result = await client
    .db("b251we")
    .collection("movies")
    .deleteOne({ id: id });
  response.send(result);
});

##Update movie
app.put("/movies/:id", async (request, response) => {
  const { id } = request.params;
  const data = request.body;
  const result = await client
    .db("b251we")
    .collection("movies")
    .updateOne({ id: id },{$set :});
  response.send(result);
});

