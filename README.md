# Redimensionar imagens em lote no Linux com ImageMagick

Comandos para auxiliar no redimensionamento de imagens em massa e liberar espaço em disco.

Para testar o comando convert é necessário o imagemagick instalado, e caso vc não tenha segue uma imagem pronta para isso.

## Container com imagemagick  (Entrar na pasta /images/ do container)
    $docker run -v .:/images --rm -it v4tech/imagemagick /bin/sh

## Busca recursivamente e redimensiona imagens maiores que 1280
    $find meu_diretorio/ type f \( -iname \*.jpg -o -iname \*.JPG -o -iname \*.png -o -iname \*.PNG \) -exec convert \{} -verbose -resize '1280>' \{} \;