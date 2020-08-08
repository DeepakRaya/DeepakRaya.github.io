---
layout: post
include: true
title:  "The compressive sensing problem, various considrations and applications in general"
date:   2020-08-07 10:00:00
mathjax: true
---
* TOC
{:toc}

## The compressive sensing problem:
If only few degrees of freedom are left after the compression of a signal, why not sense the signal more efficiently, i.e. take considerably less number of measurements than the actual size of the
signal, and reconstruct the orginal signal from the measurements when required(e.g. at the Receiver end).
#### Well, what advantage will this provide?
It reduces the complexity of sensing device or sensors, without loss in the performance of the required output. 
## The Compressive sensing Paradigm:
Reconstruction of a sparse vector $$\mathbf{x}\, \in \,\mathcal{R}^{N}$$, from the linear measurements  $$\mathbf{y \,=\, Ax} \,\in \,\mathcal{R}^m$$ , $$m\,<\,N$$;
 