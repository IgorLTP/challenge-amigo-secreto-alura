# Challenge do Amigo Secreto da Alura
O desafio do amigo secreto da Alura.

# Função para adicionar um nome à lista
```
function adicionarAmigo() {
    const nomeInput = document.getElementById("amigo");
    const nome = nomeInput.value.trim();
    if (nome && !amigos.includes(nome)) {
        amigos.push(nome);
        atualizarListaAmigos();
        nomeInput.value = "";
```
# Função para atualizar a exibição da lista de amigos
```function atualizarListaAmigos() {
    const lista = document.getElementById("listaAmigos");
    lista.innerHTML = "";
    amigos.forEach(amigo => {
        const li = document.createElement("li");
        li.textContent = amigo;
        lista.appendChild(li);
    });
}
```
# Função para sortear um único amigo secreto
```
function sortearAmigo() {
    if (amigos.length === 0) {
        alert("Adicione pelo menos 1 amigo para sortear!");
        return;
    }
    const sorteado = amigos[Math.floor(Math.random() * amigos.length)];
    exibirResultado(sorteado);
}
```
# Função para exibir o resultado na tela
```
function exibirResultado(sorteado) {
    const listaResultado = document.getElementById("resultado");
    listaResultado.innerHTML = "";
    const li = document.createElement("li");
    li.textContent = `Sorteado: ${sorteado}`;
    listaResultado.appendChild(li);
}
```
