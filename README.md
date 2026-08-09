# Listas DNS para bloqueio de conteúdo

Este repositório reúne listas de domínios para bloqueio em servidores DNS, com foco em redes escolares, domésticas e corporativas.

## Formato das listas

Todas as entradas utilizam o formato `hosts`:

```text
0.0.0.0 exemplo.com
```

O endereço `0.0.0.0` impede que o domínio seja direcionado ao servidor original. Linhas iniciadas por `#` são comentários e podem ser ignoradas pelo servidor DNS.

## Listas disponíveis

| Arquivo | Conteúdo bloqueado |
| --- | --- |
| `Apostas` | Casas de apostas, cassinos e jogos de azar |
| `Bloqueios` | Torrents, IPTV e serviços de streaming não autorizados |
| `Games` | Jogos, lojas, plataformas e serviços relacionados |
| `Porn` | Sites e plataformas com conteúdo adulto |
| `Radio` | Rádios e agregadores de rádio on-line |
| `Social` | Redes sociais, mensageiros e aplicativos de relacionamento |
| `Streaming` | Serviços de vídeo e música por streaming |

## Como usar

Baixe ou informe ao seu servidor DNS o endereço bruto da lista desejada. Exemplo para a lista de conteúdo adulto:

```text
https://raw.githubusercontent.com/LuanNether/dns/main/Porn
```

Para outra categoria, substitua `Porn` pelo nome do arquivo correspondente. O servidor deve interpretar cada linha como uma entrada de arquivo `hosts`.

Também é possível baixar o repositório e importar os arquivos localmente:

```bash
git clone https://github.com/LuanNether/dns.git
```

## Lista de conteúdo adulto

O arquivo `Porn` contém mais de 950 mil domínios únicos. Sua base principal vem da lista pública mantida pelo [Block List Project](https://github.com/blocklistproject/Lists), complementada com domínios relevantes para o Brasil.

Não existe uma lista capaz de cobrir permanentemente todos os sites: novos domínios são registrados e endereços antigos mudam com frequência. Atualize a lista periodicamente para manter a proteção efetiva.

## Recomendações para escolas

O bloqueio por domínio deve fazer parte de uma política de proteção em camadas. Além destas listas, recomenda-se:

- impedir que os dispositivos utilizem servidores DNS externos;
- controlar ou bloquear DNS sobre HTTPS (DoH) e DNS sobre TLS (DoT);
- ativar o SafeSearch nos mecanismos de pesquisa;
- habilitar o modo restrito do YouTube;
- registrar tentativas de acesso para identificar domínios ainda não catalogados;
- criar uma lista de permissões para corrigir eventuais falsos positivos;
- programar atualizações periódicas das listas.

## Observações

- Um domínio presente na lista pode afetar todos os serviços e subdomínios associados, dependendo do servidor DNS utilizado.
- Algumas plataformas compartilham infraestrutura com outros serviços. Teste as listas antes de aplicá-las em toda a rede.
- As listas são fornecidas sem garantia de cobertura total e podem exigir ajustes para cada ambiente.

## Licença e fontes

Consulte as condições das fontes utilizadas antes de redistribuir as listas. A lista de conteúdo adulto do Block List Project é disponibilizada sob a licença indicada no cabeçalho do arquivo `Porn`.
