# Yet Another PlantText dockerfile

I was having trouble with the stdin/stdout approach from

https://hub.docker.com/r/think/plantuml/

But I liked the idea. So I cooked up a variation that you invoke thusly:

    docker run --rm -it -v `pwd`:/src plantuml -tsvg /src/planttext.txt

This doesn't use the `-p` argument and seems to work more reliably.

You can build the image using:

    docker build -t plantuml .

-sjs

