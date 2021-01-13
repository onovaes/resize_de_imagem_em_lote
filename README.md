# Redimensionar imagens em lote no Linux com ImageMagick

## Rodando com docker (Entrar na pasta /images/ do container)
    docker run -v .:/images --rm -it v4tech/imagemagick /bin/sh

## Busca recursivamente e redimensiona imagens maiores que 1280
    find meu_diretorio/ type f \( -iname \*.jpg -o -iname \*.JPG -o -iname \*.png -o -iname \*.PNG \) -exec convert \{} -verbose -resize '1280>' \{} \;