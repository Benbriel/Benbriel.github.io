---
title: 'Apuntes IFS'
date: 2023-04-03
excerpt: "This is IFS"
category: IFS
---
Sure, here's the proof using LaTeX:

Let's say we have a crystal lattice with a basis defined by the set of lattice vectors $\mathbf{a}_1$, $\mathbf{a}_2$, and $\mathbf{a}_3$. The reciprocal lattice is defined by the set of lattice vectors $\mathbf{b}_1$, $\mathbf{b}_2$, and $\mathbf{b}_3$, where:

$$\mathbf{b}i = 2\pi \frac{\mathbf{a}{j} \times \mathbf{a}{k}}{\mathbf{a}i \cdot (\mathbf{a}{j} \times \mathbf{a}{k})} \qquad (i \neq j \neq k)$$

Now, let's take the reciprocal lattice and find its reciprocal. The reciprocal lattice vectors are defined as:

$$\mathbf{a}i = 2\pi \frac{\mathbf{b}{j} \times \mathbf{b}{k}}{\mathbf{b}i \cdot (\mathbf{b}{j} \times \mathbf{b}{k})} \qquad (i \neq j \neq k)$$

Substituting for the reciprocal lattice vectors $\mathbf{b}_i$ in the above equation, we get:

$$\mathbf{a}i = 2\pi \frac{\left(2\pi \frac{\mathbf{a}{k} \times \mathbf{a}{j}}{\mathbf{b}{i} \cdot (\mathbf{a}{k} \times \mathbf{a}{j})}\right) \times \left(2\pi \frac{\mathbf{a}{j} \times \mathbf{a}{k}}{\mathbf{b}{i} \cdot (\mathbf{a}{j} \times \mathbf{a}{k})}\right)}{\left(2\pi \frac{\mathbf{a}{j} \times \mathbf{a}{k}}{\mathbf{b}{i} \cdot (\mathbf{a}{j} \times \mathbf{a}{k})}\right) \cdot \left[\left(2\pi \frac{\mathbf{a}{k} \times \mathbf{a}{j}}{\mathbf{b}{i} \cdot (\mathbf{a}{k} \times \mathbf{a}{j})}\right) \times \left(2\pi \frac{\mathbf{a}{j} \times \mathbf{a}{k}}{\mathbf{b}{i} \cdot (\mathbf{a}{j} \times \mathbf{a}{k})}\right)\right]}$$

Simplifying the above equation, we get:

$$\mathbf{a}i = \frac{\mathbf{a}{j} \times \mathbf{a}{k}}{\mathbf{a}i \cdot (\mathbf{a}{j} \times \mathbf{a}{k})} \cdot \left(\frac{1}{2\pi}\right)^2$$

Multiplying both sides by $\mathbf{a}i \cdot (\mathbf{a}{j} \times \mathbf{a}_{k})$, we get:

$$\mathbf{a}i \cdot (\mathbf{a}{j} \times \mathbf{a}_{k}) = \frac{1}{2\pi}$$

This shows that the lattice vectors $\mathbf{a}_i$ are the reciprocal lattice vectors of the reciprocal lattice vectors $\mathbf{b}_i$, and hence the reciprocal of the reciprocal lattice is the original lattice.




Sure, I can help you with that.

Let's start by defining reciprocal lattice vectors. Given a Bravais lattice with basis vectors $\vec{a_1}$, $\vec{a_2}$, and $\vec{a_3}$, the reciprocal lattice vectors are defined as:

$$\vec{b_1} = 2\pi \frac{\vec{a_2}\times\vec{a_3}}{\vec{a_1}\cdot(\vec{a_2}\times\vec{a_3})}$$

$$\vec{b_2} = 2\pi \frac{\vec{a_3}\times\vec{a_1}}{\vec{a_1}\cdot(\vec{a_2}\times\vec{a_3})}$$

$$\vec{b_3} = 2\pi \frac{\vec{a_1}\times\vec{a_2}}{\vec{a_1}\cdot(\vec{a_2}\times\vec{a_3})}$$

Now, let's consider a plane described by the Miller indices $(h,k,l)$. The normal to this plane is given by:

$$\vec{n} = h\vec{b_1} + k\vec{b_2} + l\vec{b_3}$$

If we take the dot product of $\vec{r}$ with $\vec{n}$, where $\vec{r}$ is the position vector of a point in the plane, we get:

$$\vec{r}\cdot\vec{n} = 2\pi(hx+ky+lz)$$

where $(x,y,z)$ are the fractional coordinates of the point.

Now, let's consider two points in the plane with fractional coordinates $(x_1,y_1,z_1)$ and $(x_2,y_2,z_2)$. The vector between these two points is:

$$\vec{r_{12}} = (x_2-x_1)\vec{a_1} + (y_2-y_1)\vec{a_2} + (z_2-z_1)\vec{a_3}$$

If we take the dot product of $\vec{r_{12}}$ with $\vec{n}$, we get:

$$\vec{r_{12}}\cdot\vec{n} = 2\pi(h(x_2-x_1)+k(y_2-y_1)+l(z_2-z_1))$$

But $(x_2-x_1)$, $(y_2-y_1)$, and $(z_2-z_1)$ are integers, since they represent the difference between two fractional coordinates in the same plane. Therefore, $\vec{r_{12}}\cdot\vec{n}$ is an integer multiple of $2\pi$, which means that the angle between $\vec{r_{12}}$ and $\vec{n}$ is a multiple of $2\pi$. In other words, $\vec{r_{12}}$ is perpendicular to $\vec{n}$, which means that the two points are in the same plane.

Therefore, we have shown that any two points in a plane described by the Miller indices $(h,k,l)$ are in the same plane.



To prove that if $(n_1, n_2, n_3)$ belongs to a Bravais lattice, then $n_1 h + n_2 k + n_3 l = 1$, for h, k, l Miller Indices, we can use the following steps:
1.
Let $\vec{a_1}$, $\vec{a_2}$, and $\vec{a_3}$ be the primitive translation vectors of the Bravais lattice, such that any point in the lattice can be written as $\vec{R} = n_1 \vec{a_1} + n_2 \vec{a_2} + n_3 \vec{a_3}$, where $n_1$, $n_2$, and $n_3$ are integers.
2.
Let $\vec{b_1}$, $\vec{b_2}$, and $\vec{b_3}$ be the reciprocal lattice vectors, such that $\vec{b_i} \cdot \vec{a_j} = 2\pi\delta_{ij}$, where $\delta_{ij}$ is the Kronecker delta.
3.
Let $\vec{G} = h\vec{b_1} + k\vec{b_2} + l\vec{b_3}$ be a reciprocal lattice vector with Miller indices h, k, and l.
4.
We can show that $\vec{G} \cdot \vec{R} = 2\pi(n_1h + n_2k + n_3l)$, using the fact that $\vec{b_i} \cdot \vec{a_j} = 2\pi\delta_{ij}$.
5.
Since $\vec{G} \cdot \vec{R}$ is a scalar, it must be an integer multiple of $2\pi$ if $\vec{R}$ belongs to the Bravais lattice.
6.
Therefore, we have $n_1h + n_2k + n_3l$ is an integer.
7.
Since $\vec{G}$ is a reciprocal lattice vector, we can choose $h$, $k$, and $l$ such that $|\vec{G}|^2 = h^2 + k^2 + l^2$ is minimized.
8.
From step 6, we know that $n_1h + n_2k + n_3l$ is an integer. If it is not equal to 1, we can choose a different set of Miller indices that satisfy $n_1h + n_2k + n_3l = 1$ and have a smaller value of $|\vec{G}|^2$.
9.
Therefore, we have proved that if $(n_1, n_2, n_3)$ belongs to a Bravais lattice, then $n_1 h + n_2 k + n_3 l = 1$, for h, k, l Miller Indices.