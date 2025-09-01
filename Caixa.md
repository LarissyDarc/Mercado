package app;

public class Sistemadecaixa {
	 // Atributos
    private double saldoInicial;
    private double saldoAtual;

    // Construtor
    public Sistemadecaixa (double saldoInicial) {
        this.saldoInicial = saldoInicial;
        this.saldoAtual = saldoInicial;
    }

    // Métodos
    public void registrarEntrada(double valor) {
        if(valor > 0) {
            saldoAtual += valor;
            System.out.println("Entrada registrada: R$ " + valor);
        } else {
            System.out.println("Valor inválido para entrada!");
        }
    }

    public void registrarSaida(double valor) {
        if(valor > 0 && valor <= saldoAtual) {
            saldoAtual -= valor;
            System.out.println("Saída registrada: R$ " + valor);
        } else if(valor > saldoAtual) {
            System.out.println("Saldo insuficiente para a saída!");
        } else {
            System.out.println("Valor inválido para saída!");
        }
    }

    public void exibirSaldo() {
        System.out.println("Saldo atual: R$ " + saldoAtual);
    }
}
