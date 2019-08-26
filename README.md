# MLIR Support for D Programming Language 

## Backgroud

The Multi-Level Intermediate Representation(MLIR) is a project that aims to define a flexible and extensible intermediate representation(IR) that will unify the infrastructure required to execute high performance machine learning models in TensorFlow and simi- lar ML frameworks. To achieve its goals, MLIR introduces notions from the polyhedral domain as first class concepts and the notion of dialects. These dialects consist in a set of defined operations that makes the levels of optimizations more flexible than the usual source code, LLVM IR and machine code. Each dialect can be visualized as a new level of IR. Each new level enables some optimizations that may not be available at other levels. GPU is one of the Dialects available in MLIR today, this dialect provides middle-level abstractions for launching GPU kernels following a programming model similar to that of CUDA or OpenCL. Some other examples of dialects are Affine, Vector and LLVM IR.

## Introduction

The goal of this project is to provide LDC with a new level of abstraction to support the integration of the MLIR into the D ecosystem. This project will lead to the incor- poration of new optimizations into the D programming language. The addition of new optimizations will be possible due to the levels of intermediate representation provided by the MLIR infrastructure. Ultimately, we shall generate XLA for use with TensorFlow. Thus, although an MLIR representation will be useful specifically for Machine Learning programs written in D, other programs may also benefit from the MLIR features to gain performance due the polyhedral concept implemented by MLIR to use some analysis and optmizations such as loop optimizations across kernels (fusion, loop interchange, tiling, etc) and high-performance in matrix multiplication. To complete these tasks, this project aims to create a D Dialect of MLIR, which will be closer to the D source code. Conse- quently, we will be able to use language specific optimizations such as GC2Stack8 in D at dialect level. We shall ensure the necessary infrastructure to port this D dialect of MLIR to other dialects, so that more optimizations might be available to improve the runtime of D programs. This portabilitiy will

## Millestones

1. Compilation of D through the LLVM dialect of MLIR. 
2. A D dialect (for GC2Stack & others optmizations) and exposure and utilisation of other dialects (Affine, vector, etc.)
3.
4.
