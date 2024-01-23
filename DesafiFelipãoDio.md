function calcularNivelHeroi(vitorias, derrotas) {
    const saldoVitorias = vitorias - derrotas;

    let nivel;
    if (vitorias < 10) {
        nivel = "Ferro";
    } else if (vitorias >= 51 && vitorias <= 80) {
        nivel = "Ouro";
    } else if (vitorias >= 91 && vitorias <= 100) {
        nivel = "Lendário";
    } else {
        nivel = "Classificação não definida";
    }

    const mensagem = `O Herói tem um saldo de ${saldoVitorias}. Está no nível de ${nivel}`;
    
    return mensagem;
}

// Exemplo de uso:
const quantidadeVitorias = 75;
const quantidadeDerrotas = 20;

const mensagemResultado = calcularNivelHeroi(quantidadeVitorias, quantidadeDerrotas);
console.log(mensagemResultado);
