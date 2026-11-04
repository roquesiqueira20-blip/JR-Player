JR Play Player
Player Android nativo para listas e mídias fornecidas pelo próprio usuário. O aplicativo não fornece canais nem conteúdo.
Estado desta versão do projeto
O módulo Android foi refeito em Kotlin com AndroidX Media3 ExoPlayer e interface em paisagem, com navegação por foco/controle remoto e identidade visual preta e dourada. Implementado no núcleo atual: importar arquivo M3U, buscar e importar M3U/M3U8 por URL HTTP/HTTPS, interpretar itens EXTINF e group-title, separar categorias de TV/filmes/séries por metadados disponíveis, busca, favoritos e histórico persistentes localmente, reprodução interna por Media3, botões do player e mensagens de erro.
Não implementado/garantido ainda: autenticação com backend (a tela de conexão por URL não simula login), EPG/XMLTV, temporadas/episódios estruturados, metadados editoriais de filme, Room/DataStore, zapping numérico/seleção avançada de faixas e teste funcional em aparelho/Android TV/Fire TV. A classificação filme/série é heurística baseada nos metadados da lista, que podem não existir ou estar incorretos. O suporte a codecs/formato depende do Android e da fonte.
Requisitos de build
Android Studio com JDK 17
Android SDK Platform 35 e Build Tools 35
Gradle 8.9+ (Android Gradle Plugin 8.7.3)
Compilar APK debug
Abra a pasta android/ no Android Studio, sincronize o Gradle e execute :app:assembleDebug. O APK, após build bem-sucedido, fica em android/app/build/outputs/apk/debug/app-debug.apk.
Também é possível compilar com ./gradlew :app:assembleDebug depois de gerar o wrapper pelo Android Studio.
Instalação e atualização
Instale o APK debug em Android 8.0/API 26 ou posterior; a Activity solicita orientação paisagem. Para atualizar, preserve o mesmo applicationId (com.jrplay.player) e assine builds de distribuição com a mesma chave release. Desinstalar remove os dados locais.
Privacidade e uso
As listas são guardadas localmente no dispositivo. Use somente URLs e conteúdo que você tem autorização para acessar. Uma URL M3U pode conter credenciais: não a compartilhe publicamente.
