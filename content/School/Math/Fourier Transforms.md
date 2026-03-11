If a function $f(x)$ satisfies the Dirichlet conditions, we can represent it in Fourier space using a Fourier transform

## Inverse Fourier Transform

$$
f(x)=\int_{-\infty}^{\infty} \tilde{g}(\omega)e^{ i\omega x } \, d\omega 
$$

## Fourier Transform

$$
\tilde{g}(\omega)=\frac{1}{2\pi}\int_{-\infty}^{\infty} f(x)e^{ -i\omega x } \, dx 
$$

# Odd and even Functions
- **If $f(x)$ is odd**, we can represent its Fourier transform using a Fourier sine transform;
## Fourier Sine Transform

$$
f_{s}(x)=\sqrt{ \frac{2}{\pi} }\int_{0}^{\infty} \tilde{g}_{s}(\omega)\sin(\omega x) \, d\omega 
$$

## Inverse Fourier Sine Transform

$$
\tilde{g}_{s}(\omega)=\sqrt{ \frac{2}{\pi} }\int_{0}^{\infty} f_{s}(x)\sin(\omega x) \, dx
$$

- **If $f(x)$ is even**, we can represent its Fourier transform using a Fourier cosine transform;
## Fourier Cosine Transform

$$
f_{c}(x)=\sqrt{ \frac{2}{\pi} }\int_{0}^{\infty} \tilde{g}_{c}(\omega)\cos(\omega x) \, d\omega 
$$

## Inverse Fourier Cosine Transform

$$
\tilde{g}_{c}(\omega)=\sqrt{ \frac{2}{\pi} }\int_{0}^{\infty} f_{c}(x)\cos(\omega x) \, dx
$$

# Relationship between the Fourier Transform and Its Derivatives

$$
F[f'(t)]=-i\omega  \tilde{f}(\omega)
$$

More generally:

$$
F\left[ \frac{d^nf}{dx^n} \right]=(-i\omega)^n \tilde{f}(\omega)
$$

# Convolution Theorem
