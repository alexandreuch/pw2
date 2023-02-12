# PW

npm install express nodemon esm
"start": "npx nodemon -r esm index.js"

import express from "express"
const app = express()
const PORT = 4444
app.use("/sum/:num1/:num2", (req,res)=>{
    res.send(`${parseInt(req.params.num1) + parseInt(req.params.num2)}`)
})
app.listen(PORT, () => {
    console.log(`Escutando a porta ${PORT}`)
})
