# Edifesf2 — Amazon Silk para Fire TV Stick

O aplicativo consulta o primeiro endereço válido no arquivo:

`https://raw.githubusercontent.com/edifesf1/r/refs/heads/main/link.txt`

Em seguida, tenta abrir o endereço no Amazon Silk (`com.amazon.cloud9`). **Assim que o navegador é aberto, o aplicativo Edifesf2 encerra sua própria Activity e remove sua tarefa**, para que sair do Silk não retorne à tela do Edifesf2. Se o Silk não estiver disponível, tenta abrir o navegador padrão e também encerra o app após o navegador abrir.

## Gerar o APK pelo GitHub Actions

1. Crie/abra o repositório `Edifesf2` no GitHub.
2. Extraia este ZIP e envie todos os arquivos e pastas para a raiz do repositório, incluindo `.github`.
3. Faça commit na branch `main`.
4. Abra **Actions** e selecione **Gerar APK Edifesf2**.
5. Quando a execução terminar, baixe o artefato **Edifesf2-APK**.
6. Extraia o artefato para obter `app-debug.apk`.

O workflow também roda automaticamente quando há push para `main`.

## Formato de link.txt

O app usa a primeira linha não vazia que não comece com `#`. Exemplo:

`https://exemplo.com/pagina`

## Observações

O aplicativo encerra sua tela depois de iniciar o navegador. O modo de tela cheia dentro do Silk depende dos recursos e configurações do próprio Silk/Fire OS; o APK não consegue garantir que o Silk esconda todas as suas barras. Este projeto usa o ícone já incluído no PlayerFire original.
