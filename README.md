# Cadrastro
public static void main(String[] args) {
    CadastroPessoas cadastro = new CadastroPessoas();
    Scanner scanner = new Scanner(System.in);

    int opcao;
    do {
        System.out.println("Selecione uma opção:");
        System.out.println("1 - Inserir nome");
        System.out.println("2 - Buscar nome");
        System.out.println("3 - Excluir nome");
        System.out.println("4 - Exibir lista");
        System.out.println("5 - Sair");
        opcao = scanner.nextInt();

        switch (opcao) {
            case 1:
                System.out.print("Digite o nome a ser inserido: ");
                String nome = scanner.next();
                cadastro.inserirNome(nome);
                break;
            case 2:
                System.out.print("Digite o nome a ser buscado: ");
                nome = scanner.next();
                cadastro.buscarNome(nome);
                break;
            case 3:
                System.out.print("Digite o nome a ser excluído: ");
                nome = scanner.next();
                cadastro.excluirNome(nome);
                break;
            case 4:
                cadastro.exibirLista();
                break;
            case 5:
                System.out.println("Encerrando o programa...");
                break;
            default:
                System.out.println("Opção inválida! Tente novamente.");
        }

        System.out.println();
    } while (opcao != 5);

    scanner.close();
}
