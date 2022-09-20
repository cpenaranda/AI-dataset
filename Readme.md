# Artificial Inteligence Dataset: AI-dataset

This dataset has been created using the remote GPU virtualization [rCUDA](http://www.rcuda.net/). These systems follow a client-server architecture:

![architecture](../assets/architecture.svg)

On the client side, a library intercepts all CUDA functions. By each CUDA function, the library processes the request information and sends it to the server side over the network.

On the server side, a daemon is run. It receives the GPU request and sends it to the GPU. Once the GPU runs the CUDA function, the result is sent back to the application.

The remote GPU virtualization approach works transparently to the application, so the application doesn’t know if the GPU request is served remotely instead of locally.

The AI-dataset represents the transfers between client and server when different TensorFlow applications run.

## References
You can access results obtained with the [Smash benchmark](https://github.com/cpenaranda/smash) in this [paper](https://doi.org/10.1007/978-3-031-15471-3_21). Also, if you are using this repository in your research, you need to cite the paper:
> Peñaranda, C., Reaño, C., Silla, F. (2022). Smash: A Compression Benchmark with AI Datasets from Remote GPU Virtualization Systems. In: , et al. Hybrid Artificial Intelligent Systems. HAIS 2022. Lecture Notes in Computer Science(), vol 13469. Springer, Cham. https://doi.org/10.1007/978-3-031-15471-3_21

<details><summary>BibTeX</summary>

```
@InProceedings{penaranda2022smash,
  author="Pe{\~{n}}aranda, Cristian and Rea{\~{n}}o, Carlos and Silla, Federico",
  editor="Garc{\'i}a Bringas, Pablo and P{\'e}rez Garc{\'i}a, Hilde and Mart{\'i}nez de Pis{\'o}n, Francisco Javier and Villar Flecha, Jos{\'e} Ram{\'o}n and Troncoso Lora, Alicia and de la Cal, Enrique A. and Herrero, {\'A}lvaro and Mart{\'i}nez {\'A}lvarez, Francisco and Psaila, Giuseppe and Quinti{\'a}n, H{\'e}ctor and Corchado, Emilio",
  title="Smash: A Compression Benchmark with AI Datasets from Remote GPU Virtualization Systems",
  booktitle="Hybrid Artificial Intelligent Systems",
  year="2022",
  publisher="Springer International Publishing",
  address="Cham",
  pages="236--248",
  abstract="Remote GPU virtualization is a mechanism that allows GPU-accelerated applications to be executed in computers without GPUs. Instead, GPUs from remote computers are used. Applications are not aware of using a remote GPU. However, overall performance depends on the throughput of the underlying network connecting the application to the remote GPUs. One way to increase this bandwidth is to compress transmissions made within the remote GPU virtualization middleware between the application side and the GPU side.",
  isbn="978-3-031-15471-3"
}
```

</details>
