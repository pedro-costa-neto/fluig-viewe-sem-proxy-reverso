# Corrigir o erro "Erro ao gerar a visualização do arquivo" no Fluig Viewe sem a necessidade de configurar um Proxy Reverso

O problema ocorre devido o servidor não reconhecer a DNS, para solucionar a mensagem “Erro ao gerar a visualização do arquivo. Caso possua permissão, utilize a opção de download do documento.” apresentada no momento da visualização dos documentos no Fluig ECM, é necessário fazer uma alteração no arquivo hosts.

### Caminho do arquivo no Windows

Abrir o arquivo hosts que está localizado no caminho “C:\Windows\System32\drivers\etc” com o bloco de notas ou outro editor de texto da sua preferência.

### Caminho do arquivo no Linux (CentOS/Ubuntu)

Abrir o arquivo hosts que está localizado no caminho “/etc” com o vim ou outro editor de texto da sua preferência.

Adicionar uma nova linha no final do arquivo com o número do IP do servidor onde o Fluig está instalado e na frente a DNS que está redirecionando para o servidor do Fluig.

Exemplo:

    # localhost name resolution is handled within DNS itself.
    # 127.0.0.1			localhost
    # ::1				localhost
    111.111.1.2			fluig.minhadns.com.br

### Documentos técnica disponibilizada pela Totvs sobre o problema

Configuração do Fluig Viewer: [https://tdn.totvs.com/pages/releaseview.action?pageId=235327464](https://tdn.totvs.com/pages/releaseview.action?pageId=235327464)

Configuração do Proxy Reverso: [https://tdn.totvs.com/pages/releaseview.action?pageId=257623455](https://tdn.totvs.com/pages/releaseview.action?pageId=257623455)
