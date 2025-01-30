# Interval Basis with graded Smith Normal Form
We have a family of maps of $\mathbb{F}$-vector spaces $\mathcal{M} = (M_i , \varphi_i)_i$

Fix the standard grading on $\mathbb{F[x]}$. Build a graded $\mathbb{F[x]}$-module $\alpha(\mathcal{M}) := \bigoplus_i M_i$, with this given grading, i.e. such that $x^pM_i \subseteq M_{i+p}$. In particular, we define that $x$ acts on a homogenous element $m_i$ by $\varphi_i(m_i)$.  

In other words, if we fix the obvious basis for $\bigoplus_i M_i$, we can write the $\varphi_i$'s together as a map $\Phi : \bigoplus_i M_i \rightarrow \bigoplus_i M_i$. So, on any element $m \in \alpha(\mathcal{M})$, multiplication by polynomial $p(x) \in \mathbb{F}(x)$ acts as $p(x) \cdot m = p(\Phi)(m)$. 

$\alpha(\mathcal{M})$ must fit in the following exact sequence  
$\ker\mu \ \overset{i}{\hookrightarrow} \mathbb{F}[x]^g \  \overset{\mu}{\twoheadrightarrow} \ \alpha(\mathcal{M})$  
which amounts to giving a *presentation* of $\alpha(\mathcal{M})$.
Fixing $g$ generators of the free module, saying the module is *given* amounts to giving homogenous generators of the syzygy module, i.e. a set of homogenous elements of the free module that span Im $i$. Then $\alpha(\mathcal{M}) \cong \mathbb{F}[x]^g \ / \ \text{Im } i \cong \mathbb{F}[x]^g \ / \ \ker \mu$.

As per [Corbet, Kerber](https://d-nb.info/1166945936/34), from the $\varphi_i$'s one can build these *homogenous* generators of Im $i$, $\langle r_1 , \dots , r_s \rangle$. They can be stored as a $g \ \times \ s$ matrix $S$ representing map $i$. 
It then holds  
$\alpha(\mathcal{M}) \cong \mathbb{F}[x]^g \ / \ \text{Im }S \cong \mathbb{F}[x]^g \ / \ \langle r_1, \dots r_s \rangle$   
In particular, by the procedure in the paper one obtains a matrix $S$ with the same size as $\Phi$, i.e. where $g = s = \dim \bigoplus_i M_i$.  
In general, this presentation is far from minimal, in the sense that several pairs of generator-relation can be discarded while maintaining the module fixed.

The graded Smith Normal Form in [Skraba, Vejdemo-Johansson](https://arxiv.org/pdf/1302.2015.pdf) computes a *graded* primary decomposition over $\mathbb{F}[x]$ of this module, changing basis for generators and syzygies to obtain new (homogenous) relations $r'_1 , \dots , r'_{g}$ that are,  up to reordering, diagonal. Of these, some are zero, corresponding to free generators of the module. Others are units (invertible in $\mathbb{F}[x]$, i.e. non-zero scalars), which correspond to surplus generators which should be discarded. Finally others are elements of positive degree, corresponding to torsion elements. Then    
$\alpha(\mathcal{M}) \cong \mathbb{F}[x]^g \ / \ \left( \langle r'_1 \rangle \oplus \dots \oplus \langle r'_g\rangle \right) \ \overset{?}{\cong} \ \mathbb{F}[x] \ / \ \langle r'_1\rangle \oplus \dots \oplus \mathbb{F}[x] \ / \ \langle r'_g\rangle \ \cong \ \mathbb{F}[x]^d \oplus \bigoplus_{\deg r'_i > 0} \mathbb{F}[x] \ / \ \langle r'_i\rangle \left( \oplus \bigoplus_{r'_j \text{ unit}} 0 \right)$ 

Additionally, I think we can modify the gSNF to work on scalars in $\mathbb{F}$ instead of polynomials, keeping track of degree by knowing the degree of relations and generators.
