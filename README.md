 <h1>DIO - Trilha Java Básico</h1>
<p>Desafio de Controle de Fluxo: o sistema recebe dois números inteiros via terminal e imprime uma contagem entre eles. Se o primeiro número for maior que o segundo, uma exceção personalizada é lançada.</p>
<h2>Requisitos:</h2>
<ul>
<li>Imprimir números entre o primeiro e o segundo parâmetro.</li>
<li>Se o primeiro parâmetro for maior, lançar a exceção <code>ParametrosInvalidosException</code>.</li>
</ul>
<h2>Como executar:</h2>
<ol>
<li>Clone o repositório: <code>git clone https://github.com/seuusuario/DIO-Trilha-Java-Basico.git</code></li>
<li>Compile: <code>javac Contador.java ParametrosInvalidosException.java</code></li>
<li>Execute: <code>java Contador</code></li>
<li>Informe os parâmetros quando solicitado.</li>
</ol>
<h2>Código</h2>
<h3>Classe Contador.java</h3>
<pre><code>import java.util.Scanner;
public class Contador {
    public static void main(String[] args) {
        Scanner terminal = new Scanner(System.in);
        System.out.println("Digite o primeiro parâmetro:");
        int parametroUm = terminal.nextInt();
        System.out.println("Digite o segundo parâmetro:");
        int parametroDois = terminal.nextInt();
        try {
            contar(parametroUm, parametroDois);
        } catch (ParametrosInvalidosException exception) {
            System.out.println("O segundo parâmetro deve ser maior que o primeiro");
        }
    }
    static void contar(int parametroUm, int parametroDois) throws ParametrosInvalidosException {
        if (parametroUm > parametroDois) {
            throw new ParametrosInvalidosException();
        }
        int contagem = parametroDois - parametroUm;
        for (int i = 1; i <= contagem; i++) {
            System.out.println("Imprimindo o número " + i);
        }
    }
}</code></pre>
<h3>Classe ParametrosInvalidosException.java</h3>
<pre><code>public class ParametrosInvalidosException extends Exception {
    public ParametrosInvalidosException() {
        super("O segundo parâmetro deve ser maior que o primeiro");
    }
}</code></pre>
<h2>Autor do Desafio</h2>
<p>Gleyson Sampaio</p>
<p>Acesse <a href="https://www.dio.me" target="_blank">DIO</a> para mais informações.</p>
