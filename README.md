Questão 1:
Usar getters e setters é considerado boa prática porque permite encapsular os dados, protegendo os atributos internos da classe contra acessos ou modificações indevidas. Com setters, é possível validar ou transformar os dados antes de atribuí-los, garantindo a integridade do objeto. Já os getters permitem controlar o formato ou o que será exposto do atributo.
Exemplo:
public class Produto {
    private double preco;

    public Produto(double preco) {
        setPreco(preco); // usa o setter
    }

    public double getPreco() {
        return preco;
    }

    public void setPreco(double preco) {
        if (preco < 0) {
            throw new IllegalArgumentException("O preço não pode ser negativo.");
        }
        this.preco = preco;
    }
}

Questão 2:
a) Título, autor, editora, ano de publicação, gênero, número de páginas, status, código, etc.
b) Porque ela representa, de forma simplificada e genérica, as características e comportamentos essenciais de um livro real dentro do contexto do sistema, ocultando detalhes irrelevantes para o funcionamento do programa.
c) 
emprestar(): altera o status do livro para "emprestado", caso esteja disponível.
devolver(): marca o livro como "disponível" novamente.
reservar(): define o status como "reservado", se o livro não estiver emprestado.
