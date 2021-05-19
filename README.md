# astia2105
ASTIA 2105

* I started to write in another readme and found out here is the best place to put all of that [Original GIXAst/bingpu Readme](https://github.com/GuillaumeIsabelleX/gix-adaptive-style-transfer/blob/feat-cli-container-210110/bin-gpu/README.md#L1)

# Intentions

* A well organized distribution of used libraries with my enhancements that others can use (and so is myself)
* Write the stories bellow of each code writing activities that I had and their results and further intentions.

# Realities

* That folder is where I've done painfully most of my first AST learning, so it is messy.
* Only place where I am training the models
* Able to render(inference) using  

```sh
bash doit.sh <_RENDER_CONF.sh> <checkpoint1 checkpoint2>
```
* A New repo (that is getting better organized) where I build a Web API servicing for my stylistic model using containerized infrastructure. A bunch of scripts at different level of abstraction had enable me to understand better what the service and data model of stylization is.  So I feel ready refactoring a new unified repo.  Sounds great hein!  I also have so much writing for my thesis to do that I might keep working in this mess and clean it up from time to time... anyway, it's here:  [repo](https://github.com/GuillaumeAI/rwml__adaptive_style_transfer#intentions)
```sh
#Public
git clone https://github.com/GuillaumeAI/rwml__adaptive_style_transfer.git
#Access
git clone git@github.com:GuillaumeAI/rwml__adaptive_style_transfer.git

```
* A Web UI Experimentation of Etch a Sketch in which I have made few sub-projects that would not usually go there : 
```sh
git clone git@github.com:GuillaumeAI/x__etch-a-sketch__210224.git
```
* [gia-ast-util](https://github.com/GuillaumeAI/x__etch-a-sketch__210224/tree/master/gia-ast-util/gia-ast-util) is a set of tools to work with the Web api servicing requests and response from the /svr (rwroot) using nodejs. and [gia-lib-encoding-base64](https://github.com/GuillaumeAI/x__etch-a-sketch__210224/tree/master/gia-ast-util/gia-lib-encoding-base64) which is a library to deal with encoding in that context. (at least it made me understood it and made available to me )
```sh
npm i gia-ast-util --g
npm i gia-lib-encoding-base64 --save #if needed elsewhere
```
* And finally : [gia-ast](https://github.com/GuillaumeAI/x__etch-a-sketch__210224/tree/master/gia-ast), also a nodejs cli, that I am prototyping to interface thru CLI with CASMI-AST service.  Mostly to get inferences from various model being deployed.  I am starting to think about adding on some ways to compose multi stylistic model (which I invented) thru that interface but I don't know all the implementation details yet. for now It is :
```sh
#install
npm i gia-ast --g
#example use:
gia-ast myimage.jpg 91
gia-ast <image> <modelid>
# modelid correspond to a port range where it is deployer.  I assign one model by number and they match a 9000 + $modelid callable with something like http://localhost:9091/stylize
```
* I am in the verge of a [new gia-ast](https://github.com/GuillaumeAI/x__etch-a-sketch__210224/blob/master/gia-ast/x__yargs_cmd_210512_ast3s.js) prototype with a bit more argumentation capabilities to the cli. Nonetheless auto completion for available server port using the CASMI's API. I am also mastering [Yargs](https://yargs.js.org/) which helps implementing **commands** in the CLI. (like docker run, docker build, etc).  That is really helpful with a lot still to learn but worth the try.
* **About CASMI** : Well I was having thought on naming the server so here they are :  ...the Web API Model service (I really should find a name for it?? Cloud Applicative Model service interface (CAMSI)(CASMI: Cloud Applicative Servicing Model Interface, I like it.  It is now, set, the server infrastructure abstraction will be called CASMI, well it is in context of Adaptive Style Transfer.. so ASTCASMI or CASMIAST for Cloud Applicative Servicing Model Interface for Adaptive Style Transfer... Wow, that sound academic or poetic too much.  Anyway, I need a name so I will keep it.)
* 



