---
title: Black hole shadow
math: true
date: 2026-05-31 13:46:00
updated: 2026-05-31 13:46:00
categories:
    - relativity
tags:
    - black hole
    - Schwarzschild metric
    - Kerr metric
---

The shadow of a black hole

<!-- more -->

- Luminet, J.-P. (1979). Image of a spherical black hole with thin accretion disk. *Astronomy and Astrophysics*, *75*(1-2), 228–235.
- Perlick, V., & Tsupko, O. Y. (2022). Calculating black hole shadows: Review of analytical studies. *Physics Reports*, *947*, 1–39. https://doi.org/10.1016/j.physrep.2021.10.004
- Gralla, S. E., Holz, D. E., & Wald, R. M. (2019). Black hole shadows, photon rings, and lensing rings. *Physical Review D*, *100*(2), Article 024018. https://doi.org/10.1103/PhysRevD.100.024018
- Beckwith, K., & Done, C. (2005). Extreme gravitational lensing near rotating black holes. *Monthly Notices of the Royal Astronomical Society*, *359*(4), 1217–1228. https://doi.org/10.1111/j.1365-2966.2005.08980.x

## The photon trajectory in Schwarzschild metric

- Schwarzschild metric
    $$
    \mathrm{d}s^2=-\left(1-\frac{2m}{r}\right)c^2\mathrm{d}t^2+\frac{\mathrm{d}r^2}{1-2m/r}+r^2(\mathrm{d}\theta^2+\sin^2\theta\mathrm{d}\phi^2),\quad m=\frac{GM}{c^2}
    $$

- The critial impact parameter $b_c=\sqrt{27}m$, for $b<b_c$, the light is captured by the black hole.

    {% note info %}
	The impact parameter $b\equiv L/E$ is the perpendicular distance from the black hole to the asymptotic straight-line trajectory of the photon.
    see [my note on Image of a spherical black hole with thin accretion disk](https://jingliangwei.github.io/blog-hexo/2026/05/29/Image-of-a-spherical-black-hole-with-thin-accretion-disk/#Image-of-a-Bare-Black-Hole) for details.
    {% endnote %}

- The shadow angle $\alpha_\text{capt}$ and the escape angle $\alpha_\text{esc}$ (Perlick & Tsupko, 2022)

    $$
    \sin^2\alpha_\text{esc}=\frac{27m^2(1-2m/r_O)}{r_O^2}
    $$
    $$
    \alpha_\text{capt}=\alpha_\text{sh}=\pi-\alpha_\text{esc}
    $$
	
    ![escape angle](escape_angle.png)

    {% note info %}
    From Schwarzschild metric
    $$
    \mathrm{d}s^2=-\left(1-\frac{2m}{r}\right)c^2\mathrm{d}t^2+\frac{\mathrm{d}r^2}{1-2m/r}+r^2(\mathrm{d}\theta^2+\sin^2\theta\mathrm{d}\phi^2),\quad m=\frac{GM}{c^2}
    $$
    in the "equatorial" plane ( $\theta=\pi/2$ )
    $$
    E=\left(1-\frac{2m}{r}\right)\frac{\mathrm{d}t}{\mathrm{d}\lambda},\quad L=r^2\frac{\mathrm{d}\phi}{\mathrm{d}\lambda}
    $$
    the geodesic $\mathrm{d}s^2=0$ reads
    $$
    \left(\frac{\mathrm{d}r}{\mathrm{d}\lambda}\right)^2=E^2\left[1-\frac{b^2}{r^2}\left(1-\frac{2m}{r}\right)\right]
    $$
    where the impact parameter $b=L/E$.
    In the local frame located at $r_O$,
    $$
    p^{(\hat{r})}=\sqrt{g_{rr}}p^r=\frac{1}{\sqrt{1-2m/r_O}}\frac{\mathrm{d}r}{\mathrm{d}\lambda}=\frac{E}{\sqrt{1-2m/r_O}}\sqrt{1-\frac{b^2}{r_O^2}\left(1-\frac{2m}{r_O}\right)}
    $$
    $$
    p^{(\hat{\phi})}=r_Op^\phi=\frac{L}{r_O}=\frac{bE}{r_O}
    $$
    $$
    \sin\alpha=\frac{p^{(\hat{\phi})}}{\sqrt{(p^{(\hat{r})})^2+(p^{(\hat{\phi})})^2}}
    $$
    subtituting $b_c=\sqrt{27}m$
    $$
    \sin\alpha=\frac{b_c/r_O}{\sqrt{1/(1-2m/r_O)}}=\sqrt{\frac{27m^2}{r_O^2}\left(1-\frac{2m}{r_O}\right)}
    $$
    {% endnote %}

- The photon sphere radius $r_\text{ph}=3m$ (Perlick & Tsupko, 2022)

    {% note info %}
    From radial equation:
    $$
    \left(\frac{\mathrm{d}r}{\mathrm{d}\lambda}\right)^2=E^2\left[1-\frac{b^2}{r^2}\left(1-\frac{2m}{r}\right)\right]
    $$
    define the effective potential
    $$
    V_\text{eff}(r)=\frac{L^2}{r^2}\left(1-\frac{2m}{r}\right)
    $$
    and the circular orbits $\mathrm{d}V_\text{eff}/\mathrm{d}r=0$ give $r=3m$.
    {% endnote %}

![shadow vs rO](shadow_vs_rO.png)

- For $b$ near $b_c=\sqrt{27}M\approx 5.196M$, the elliptic integral gives the approximation (Gralla et al., 2019)
    $$
    \phi\sim\log\left(\frac{C_\pm}{|b-b_c|}\right),\quad b\rightarrow b_c^\pm\tag{2}
    $$
    with
    $$
    C_+=\frac{1944}{12+7\sqrt{3}}M\approx 80.6 M
    $$
    $$
    C_-=648(26\sqrt{3}-45)M\approx 21.6 M
    $$

    1. Direct: $n<3/4$
        $b/M\notin(5.02,6.17)$
    2. Lensed: $3/4<n<5/4$
        $b/M\in(5.02,5.19)$ or $(5.23,6.17)$
    3. Photon ring: $n>5/4$
        $b/M\in(5.19,5.23)$

    ![Schwarzschild impact](schwarzschild_impact.png)

## The image of Schwarzschild black hole

- Backlit black hole (Gralla et al., 2019)

    ![Backlit BH](backlit_BH.png)

    {% note info %}
    also see [section 2 in Image of a spherical black hole with thin accretion disk](https://jingliangwei.github.io/blog-hexo/2026/05/29/Image-of-a-spherical-black-hole-with-thin-accretion-disk/Image_of_a_spherical_black_hole_with_thin_accretion_disk.pdf)
    {% endnote %}

- Face-on, optically and geometrically thin disk near a Schwarzschild black hole (Gralla et al., 2019)

    the figures in each low, from left to right are the $I_\text{em}$, $I_\text{obs}$ and the visual image.

    ![thin disk](thin_optically_thin_disk.png)

- Geometrically thick and optically thin disk (Gralla et al., 2019)

    the pink region are the emission region, with the observer located to the right.

    ![thick disk](thick_disk.png)

- Geometrically thin and optically thick disk (Beckwith & Done, 2005)

    ![thin disk](thin_optically_thick_disk.png)
    ![thin disk](thin_optically_thick_disk2.png)

## In Kerr metric

- Kerr metric (in Boyer-Lindquist coordinates)
    $$
    \mathrm{d}s^2=-\left(1-\frac{r_sr}{\Sigma}\right)c^2\mathrm{d}t^2+\frac{\Sigma}{\Delta}\mathrm{d}r^2+\Sigma\mathrm{d}\theta^2+\left(r^2+a^2+\frac{r_sra^2}{\Sigma}\sin^2\theta\right)\sin^2\theta\mathrm{d}\phi^2-\frac{2r_sra\sin^2\theta}{\Sigma}c\mathrm{d}t\mathrm{d}\phi
    $$
    where $(r,\theta,\phi)$ are standard oblate spheroidal coordinates
    $$
    \left\{\begin{array}{l}
    x=\sqrt{r^2+a^2}\sin\theta\cos\phi \\
    y=\sqrt{r^2+a^2}\sin\theta\sin\phi \\
    z=r\cos\theta
    \end{array}\right.
    $$
    $r_s$ is the Schwarzschild radius
    $$
    r_s=\frac{2GM}{c^2}
    $$
    and the length scales $a,\Sigma,\Delta$ are
    $$
    a=\dfrac{J}{Mc}
    $$
    $$
    \Sigma=r^2+a^2\cos^2\theta
    $$
    $$
    \Delta=r^2-r_sr+a^2
    $$

- Two circular light orbits in the equatorial plane of a Kerr black hole (Perlick & Tsupko, 2022):

    $$
    r_\text{ph}=3m\frac{b-a}{b+a},\quad r_\text{ph}^3=m(b-a)^2
    $$
    $$
    b=-a\frac{r_\text{ph}+3m}{r_\text{ph}-3m}
    $$

    For $a=m$, $r_\text{ph}=m$, $b=2m$.
    For $a=-m$, $r_\text{ph}=4m$, $b=7m$.

![two circular orbits](two_circle_kerr.png)

- The Kerr black hole shadows (Perlick & Tsupko, 2022):

![Kerr BH shadow (nearby)](kerr_shadow_nearby.png)
![Kerr BH shadow (distant)](kerr_shadow_distant.png)

## Ray tracing

Ray tracing: The photons are parameterized by x, y in the "view port" of the observer. By scanning over x and y, we can build up an image once we know where each photon goes. (see [http://locklessinc.com/articles/raytracing/](http://locklessinc.com/articles/raytracing/) for details)

{% note info %}
parameter:
`a`: spin parameter $a=J/M$
`size`: refinement of figure size
`inclination`: the view inclination (`0` means face-on, `90` means edge-on)
{% endnote %}

{% fold info @C script without mpi %}
complie using `gcc main.c -o bh_shadow -lm` (on Ubuntu24.04)
```c
#define _GNU_SOURCE
#include <math.h>
#include <stdlib.h>
#include <stdio.h>
#include <string.h>
#include <err.h>
#include <sys/stat.h>
#include <fcntl.h>
#include <unistd.h>
#include <errno.h>

#define N	6

static const double a = 0;
static const int size = 100;
static double inclination = 85;

static double r0, theta0;

static double a2;
static double Rhor, Rmstable, Rdisk;

static double L, kappa;

/* Coupled differential equations describing motion of photon */
static void geodesic(double *y, double *dydx)
{
	double r, theta, pr, ptheta;

	r = y[0];
	theta = y[1];
	pr = y[4];
	ptheta = y[5];

	double r2 = r*r;
	double twor = 2.0*r;

	double sintheta, costheta;
	sincos(theta, &sintheta, &costheta);
	double cos2 = costheta*costheta;
	double sin2 = sintheta*sintheta;

	double sigma = r2+a2*cos2;
	double delta = r2-twor+a2;
	double sd = sigma*delta;
	double siginv = 1.0/sigma;
	double bot = 1.0/sd;

	/* Prevent problems with the axis */
	if (sintheta < 1e-8)
	{
		sintheta = 1e-8;
		sin2 = 1e-16;
	}

	dydx[0] = -pr*delta*siginv;
	dydx[1] = -ptheta*siginv;
	dydx[2] = -(twor*a+(sigma-twor)*L/sin2)*bot;
	dydx[3] = -(1.0+(twor*(r2+a2)-twor*a*L)*bot);
	dydx[4] = -(((r-1.0)*(-kappa)+twor*(r2+a2)-2.0*a*L)*bot-2.0*pr*pr*(r-1.0)*siginv);
	dydx[5] = -sintheta*costheta*(L*L/(sin2*sin2)-a2)*siginv;
}

/* Initial Conditions for Ray */
static void initial(double *y0, double *ydot0, double x, double y)
{
	y0[0] = r0;
	y0[1] = theta0;
	y0[2] = 0;
	y0[3] = 0;
	y0[4] = cos(y)*cos(x);
	y0[5] = sin(y)/r0;

	double sintheta, costheta;
	sincos(theta0, &sintheta, &costheta);
	double cos2 = costheta*costheta;
	double sin2 = sintheta*sintheta;

	double rdot0 = y0[4];
	double thetadot0 = y0[5];

	double r2 = r0 * r0;
	double sigma = r2 + a2*cos2;
	double delta = r2 - 2.0 * r0 + a2;
	double s1 = sigma - 2.0 * r0;

	y0[4]= rdot0*sigma/delta;
	y0[5]= thetadot0*sigma;

	ydot0[0] = rdot0;
	ydot0[1] = thetadot0;
	ydot0[2] = cos(y)*sin(x)/(r0*sin(theta0));

	double phidot0 = ydot0[2];
	double energy2 = s1*(rdot0*rdot0/delta+thetadot0*thetadot0)
					+ delta*sin2*phidot0*phidot0;

	double energy = sqrt(energy2);

	/* Rescale */
	y0[4] = y0[4]/energy;
	y0[5] = y0[5]/energy;

	/* Angular Momentum with E = 1 */
	L = ((sigma*delta*phidot0-2.0*a*r0*energy)*sin2/s1)/energy;

	kappa = y0[5]*y0[5]+a2*sin2+L*L/sin2;

	/* Hack - make sure everything is normalized correctly by a call to geodesic */
	geodesic(y0, ydot0);
}

static void rkstep(double *y, double *dydx, double h, double *yout, double *yerr)
{
	int i;

	double ak[N];

	double ytemp1[N], ytemp2[N], ytemp3[N], ytemp4[N], ytemp5[N];

	for (i = 0; i < N; i++)
	{
		double hdydx = h * dydx[i];
		double yi = y[i];
		ytemp1[i] = yi + 0.2 * hdydx;
		ytemp2[i] = yi + (3.0/40.0) * hdydx;
		ytemp3[i] = yi + 0.3 * hdydx;
		ytemp4[i] = yi -(11.0/54.0) * hdydx;
		ytemp5[i] = yi + (1631.0/55296.0) * hdydx;
		yout[i] = yi + (37.0/378.0) * hdydx;
		yerr[i] = ((37.0/378.0)-(2825.0/27648.0)) * hdydx;
	}

	geodesic(ytemp1, ak);

	for (i = 0; i < N; i++)
	{
		double yt = h * ak[i];
		ytemp2[i] += (9.0/40.0) * yt;
		ytemp3[i] -= 0.9 * yt;
		ytemp4[i] += 2.5 * yt;
		ytemp5[i] += (175.0/512.0) * yt;
	}

	geodesic(ytemp2, ak);

	for (i = 0; i < N; i++)
	{
		double yt = h * ak[i];
		ytemp3[i] += 1.2 * yt;
		ytemp4[i] -= (70.0/27.0) * yt;
		ytemp5[i] += (575.0/13824.0) * yt;
		yout[i] += (250.0/621.0) * yt;
		yerr[i] += ((250.0/621.0)-(18575.0/48384.0)) * yt;
	}

	geodesic(ytemp3, ak);

	for (i = 0; i < N; i++)
	{
		double yt = h * ak[i];
		ytemp4[i] += (35.0/27.0) * yt;
		ytemp5[i] += (44275.0/110592.0) * yt;
		yout[i] += (125.0/594.0) * yt;
		yerr[i] += ((125.0/594.0)-(13525.0/55296.0)) * yt;
	}

	geodesic(ytemp4, ak);

	for (i = 0; i < N; i++)
	{
		double yt = h * ak[i];
		ytemp5[i] += (253.0/4096.0) * yt;
		yerr[i] -= (277.0/14336.0) * yt;
	}

	geodesic(ytemp5, ak);

	for (i = 0; i < N; i++)
	{
		double yt = h * ak[i];
		yout[i] += (512.0/1771.0) * yt;
		yerr[i] += ((512.0/1771.0)-0.25) * yt;
	}
}

static double rkqs(double *y, double *dydx, double htry, double escal, double *yscal, double *hdid)
{
	int i;

	double hnext;

	double errmax, h = htry, htemp;
	double yerr[N], ytemp[N];

	while (1)
	{
		rkstep(y, dydx, h, ytemp, yerr);

		errmax = 0.0;
		for (i = 0; i < N; i++)
		{
			double temp = fabs(yerr[i]/yscal[i]);
			if (temp > errmax) errmax = temp;
		}

		errmax *= escal;
		if (errmax <= 1.0) break;

		htemp = 0.9 * h / sqrt(sqrt(errmax));

		h *= 0.1;

		if (h >= 0.0)
		{
			if (htemp > h) h = htemp;
		}
		else
		{
			if (htemp < h) h = htemp;
		}
	}

	if (errmax > 1.89e-4)
	{
		hnext = 0.9 * h * pow(errmax, -0.2);
	}
	else
	{
		hnext = 5.0 * h;
	}

	*hdid = h;

	memcpy(y, ytemp, N * sizeof(double));

	return hnext;
}

static void binarysearch(double *y, double *dydx, double hbig)
{
	double hsmall = 0.0;

	int side;
	if (y[1] > M_PI/2.0)
	{
		side = 1;
	}
	else if (y[1] < M_PI/2.0)
	{
		side = -1;
	}
	else
	{
		/* Already at the equator */
		return;
	}

	geodesic(y,dydx);

	while ((y[0] > Rhor) && (y[0] < r0) && (side != 0))
	{
		double yout[N], yerr[N];

		double hdiff = hbig - hsmall;

		if (hdiff < 1e-7)
		{
			rkstep(y, dydx, hbig, yout, yerr);

			memcpy(y, yout, N * sizeof(double));

			return;
		}

		double hmid = (hbig + hsmall) / 2;

		rkstep(y, dydx, hmid, yout, yerr);

		if (side * (yout[1] - M_PI/2.0) > 0)
		{
			hsmall = hmid;
		}
		else
		{
			hbig = hmid;
		}
	}
}

static void fire_ray(unsigned char *rgb, int x1, int y1)
{
	double htry = 0.5, escal = 1e11, hdid = 0.0, hnext = 0.0;

	double range = 0.0025 * Rdisk / (size - 1.0);

	double y[N], dydx[N], yscal[N], ylaststep[N];

	int side;
	int i;

	initial(y, dydx, (x1 - (size + 1.0) / 2) * range, (y1 - (size + 1.0) / 2) * range);

	while (1)
	{
		memcpy(ylaststep, y, N * sizeof(double));

		geodesic(y, dydx);

		for (i = 0; i < N; i++)
		{
			yscal[i] = fabs(y[i]) + fabs(dydx[i] * htry) + 1.0e-3;
		}

		if (y[1] > M_PI/2) side = 1;
		else if (y[1] < M_PI/2) side = -1;
		else side = 0;

		hnext = rkqs(y, dydx, htry, escal, yscal, &hdid);

		if ((y[1]-M_PI/2)*side < 0)
		{
			memcpy(y, ylaststep, N * sizeof(double));

			binarysearch(y, dydx, hdid);

			/* Did we hit the disk? */
			if ((y[0] <= Rdisk) && (y[0] >= Rmstable))
			{
				unsigned p1 = 4.0 * (y[0] - Rmstable) / (Rdisk - Rmstable);
				unsigned p2 = floor(y[2] * 6.0 / M_PI);

				if ((p1 ^ p2) & 1)
				{
					rgb[0] = 255;
					rgb[1] = 128;
					rgb[2] = 128;
				}
				else
				{
					rgb[0] = 255;
					rgb[1] = 0;
					rgb[2] = 0;
				}

				return;
			}
		}

		/* Inside the hole, or escaped to infinity */
		if ((y[0] < Rhor) || (y[0] > r0))
		{
			rgb[0] = 0;
			rgb[1] = 0;
			rgb[2] = 0;

			return;
		}

		htry = hnext;
	}
}

/* Write all the data, or fail and exit */
static void full_write(int fd, void *buf, size_t size)
{
	while (size)
	{
		ssize_t did = write(fd, buf, size);
		if (did == -1)
		{
			if (errno == EINTR) continue;

			errx(1, "Error writing file: %s\n", strerror(errno));
		}

		size -= did;
		buf = (char *)buf - did;
	}
}

/* Open a file, and output a tga header for a square image of the given size */
static int open_tga(const char *filename, int size)
{
	char c1, c2;

	int fd = open(filename, O_CREAT | O_WRONLY | O_TRUNC, S_IRUSR | S_IWUSR | S_IRGRP | S_IROTH);

	if (fd == -1) errx(1, "Couldn't open %s for writing\n", filename);

	/* Output the header (embedded zeros explicit) */
	write(fd, "\0\0\2\0\0\0\0\0\0\0\0\0", 12);

	c1 = size%256;
	c2 = size/256;
	full_write(fd, &c1, 1);
	full_write(fd, &c2, 1);

	c1 = size%256;
	c2 = size/256;
	full_write(fd, &c1, 1);
	full_write(fd, &c2, 1);

	full_write(fd, "\x18\0", 2);

	return fd;
}

static double inner_orbit(void)
{
	double z1 = 1+cbrt(1-a2)*(cbrt(1+a)+cbrt(1-a));
	double z2 = sqrt(3*a2+z1*z1);
	return 3+z2-sqrt((3-z1)*(3+z1+2*z2));
}

int main(void)
{
	int i, j;

	int fd = open_tga("image.tga", size);

	unsigned char *buffer = calloc(size, 3);
	if (!buffer) errx(1, "Out of memory\n");

	r0 = 1000.0;
	theta0 = (M_PI/180.0) * inclination;

	a2 = a*a;

	Rhor = 1.0 + sqrt(1.0-a2) + 1e-5;
	Rdisk = 20.0;
	Rmstable = inner_orbit();

	for (j = 0; j < size; j++)
	{
		for (i = 0; i < size; i++)
		{
			fire_ray(&buffer[i * 3], i, j);
		}

		full_write(fd, buffer, size * 3);
		printf("%d\n", j);
	}

	close(fd);

	free(buffer);

	return 0;
}
```
{% endfold %}

{% fold info @C script with mpi %}
complie using `mpicc main_mpi.c -o bh_shadow_mpi -lm` (on Ubuntu24.04)
run using `mpirun -np 4 ./bh_shadow_mpi`
```c
#define _GNU_SOURCE
#include <math.h>
#include <stdlib.h>
#include <stdio.h>
#include <string.h>
#include <err.h>
#include <sys/stat.h>
#include <fcntl.h>
#include <unistd.h>
#include <errno.h>
#include "mpi.h"

#define N	6

static const double a = 0;
static const int size = 1000;
static double inclination = 45;

static double r0, theta0;

static double a2;
static double Rhor, Rmstable, Rdisk;

static double L, kappa;

/* Coupled differential equations describing motion of photon */
static void geodesic(double *y, double *dydx)
{
	double r, theta, pr, ptheta;

	r = y[0];
	theta = y[1];
	pr = y[4];
	ptheta = y[5];

	double r2 = r*r;
	double twor = 2.0*r;

	double sintheta, costheta;
	sincos(theta, &sintheta, &costheta);
	double cos2 = costheta*costheta;
	double sin2 = sintheta*sintheta;

	double sigma = r2+a2*cos2;
	double delta = r2-twor+a2;
	double sd = sigma*delta;
	double siginv = 1.0/sigma;
	double bot = 1.0/sd;

	/* Prevent problems with the axis */
	if (sintheta < 1e-8)
	{
		sintheta = 1e-8;
		sin2 = 1e-16;
	}

	dydx[0] = -pr*delta*siginv;
	dydx[1] = -ptheta*siginv;
	dydx[2] = -(twor*a+(sigma-twor)*L/sin2)*bot;
	dydx[3] = -(1.0+(twor*(r2+a2)-twor*a*L)*bot);
	dydx[4] = -(((r-1.0)*(-kappa)+twor*(r2+a2)-2.0*a*L)*bot-2.0*pr*pr*(r-1.0)*siginv);
	dydx[5] = -sintheta*costheta*(L*L/(sin2*sin2)-a2)*siginv;
}

/* Initial Conditions for Ray */
static void initial(double *y0, double *ydot0, double x, double y)
{
	y0[0] = r0;
	y0[1] = theta0;
	y0[2] = 0;
	y0[3] = 0;
	y0[4] = cos(y)*cos(x);
	y0[5] = sin(y)/r0;

	double sintheta, costheta;
	sincos(theta0, &sintheta, &costheta);
	double cos2 = costheta*costheta;
	double sin2 = sintheta*sintheta;

	double rdot0 = y0[4];
	double thetadot0 = y0[5];

	double r2 = r0 * r0;
	double sigma = r2 + a2*cos2;
	double delta = r2 - 2.0 * r0 + a2;
	double s1 = sigma - 2.0 * r0;

	y0[4]= rdot0*sigma/delta;
	y0[5]= thetadot0*sigma;

	ydot0[0] = rdot0;
	ydot0[1] = thetadot0;
	ydot0[2] = cos(y)*sin(x)/(r0*sin(theta0));

	double phidot0 = ydot0[2];
	double energy2 = s1*(rdot0*rdot0/delta+thetadot0*thetadot0)
					+ delta*sin2*phidot0*phidot0;

	double energy = sqrt(energy2);

	/* Rescale */
	y0[4] = y0[4]/energy;
	y0[5] = y0[5]/energy;

	/* Angular Momentum with E = 1 */
	L = ((sigma*delta*phidot0-2.0*a*r0*energy)*sin2/s1)/energy;

	kappa = y0[5]*y0[5]+a2*sin2+L*L/sin2;

	/* Hack - make sure everything is normalized correctly by a call to geodesic */
	geodesic(y0, ydot0);
}

static void rkstep(double *y, double *dydx, double h, double *yout, double *yerr)
{
	int i;

	double ak[N];

	double ytemp1[N], ytemp2[N], ytemp3[N], ytemp4[N], ytemp5[N];

	for (i = 0; i < N; i++)
	{
		double hdydx = h * dydx[i];
		double yi = y[i];
		ytemp1[i] = yi + 0.2 * hdydx;
		ytemp2[i] = yi + (3.0/40.0) * hdydx;
		ytemp3[i] = yi + 0.3 * hdydx;
		ytemp4[i] = yi -(11.0/54.0) * hdydx;
		ytemp5[i] = yi + (1631.0/55296.0) * hdydx;
		yout[i] = yi + (37.0/378.0) * hdydx;
		yerr[i] = ((37.0/378.0)-(2825.0/27648.0)) * hdydx;
	}

	geodesic(ytemp1, ak);

	for (i = 0; i < N; i++)
	{
		double yt = h * ak[i];
		ytemp2[i] += (9.0/40.0) * yt;
		ytemp3[i] -= 0.9 * yt;
		ytemp4[i] += 2.5 * yt;
		ytemp5[i] += (175.0/512.0) * yt;
	}

	geodesic(ytemp2, ak);

	for (i = 0; i < N; i++)
	{
		double yt = h * ak[i];
		ytemp3[i] += 1.2 * yt;
		ytemp4[i] -= (70.0/27.0) * yt;
		ytemp5[i] += (575.0/13824.0) * yt;
		yout[i] += (250.0/621.0) * yt;
		yerr[i] += ((250.0/621.0)-(18575.0/48384.0)) * yt;
	}

	geodesic(ytemp3, ak);

	for (i = 0; i < N; i++)
	{
		double yt = h * ak[i];
		ytemp4[i] += (35.0/27.0) * yt;
		ytemp5[i] += (44275.0/110592.0) * yt;
		yout[i] += (125.0/594.0) * yt;
		yerr[i] += ((125.0/594.0)-(13525.0/55296.0)) * yt;
	}

	geodesic(ytemp4, ak);

	for (i = 0; i < N; i++)
	{
		double yt = h * ak[i];
		ytemp5[i] += (253.0/4096.0) * yt;
		yerr[i] -= (277.0/14336.0) * yt;
	}

	geodesic(ytemp5, ak);

	for (i = 0; i < N; i++)
	{
		double yt = h * ak[i];
		yout[i] += (512.0/1771.0) * yt;
		yerr[i] += ((512.0/1771.0)-0.25) * yt;
	}
}

static double rkqs(double *y, double *dydx, double htry, double escal, double *yscal, double *hdid)
{
	int i;

	double hnext;

	double errmax, h = htry, htemp;
	double yerr[N], ytemp[N];

	while (1)
	{
		rkstep(y, dydx, h, ytemp, yerr);

		errmax = 0.0;
		for (i = 0; i < N; i++)
		{
			double temp = fabs(yerr[i]/yscal[i]);
			if (temp > errmax) errmax = temp;
		}

		errmax *= escal;
		if (errmax <= 1.0) break;

		htemp = 0.9 * h / sqrt(sqrt(errmax));

		h *= 0.1;

		if (h >= 0.0)
		{
			if (htemp > h) h = htemp;
		}
		else
		{
			if (htemp < h) h = htemp;
		}
	}

	if (errmax > 1.89e-4)
	{
		hnext = 0.9 * h * pow(errmax, -0.2);
	}
	else
	{
		hnext = 5.0 * h;
	}

	*hdid = h;

	memcpy(y, ytemp, N * sizeof(double));

	return hnext;
}

static void binarysearch(double *y, double *dydx, double hbig)
{
	double hsmall = 0.0;

	int side;
	if (y[1] > M_PI/2.0)
	{
		side = 1;
	}
	else if (y[1] < M_PI/2.0)
	{
		side = -1;
	}
	else
	{
		/* Already at the equator */
		return;
	}

	geodesic(y,dydx);

	while ((y[0] > Rhor) && (y[0] < r0) && (side != 0))
	{
		double yout[N], yerr[N];

		double hdiff = hbig - hsmall;

		if (hdiff < 1e-7)
		{
			rkstep(y, dydx, hbig, yout, yerr);

			memcpy(y, yout, N * sizeof(double));

			return;
		}

		double hmid = (hbig + hsmall) / 2;

		rkstep(y, dydx, hmid, yout, yerr);

		if (side * (yout[1] - M_PI/2.0) > 0)
		{
			hsmall = hmid;
		}
		else
		{
			hbig = hmid;
		}
	}
}

static void fire_ray(unsigned char *rgb, int x1, int y1)
{
	double htry = 0.5, escal = 1e11, hdid = 0.0, hnext = 0.0;

	double range = 0.0025 * Rdisk / (size - 1.0);

	double y[N], dydx[N], yscal[N], ylaststep[N];

	int side;
	int i;

	initial(y, dydx, (x1 - (size + 1.0) / 2) * range, (y1 - (size + 1.0) / 2) * range);

	while (1)
	{
		memcpy(ylaststep, y, N * sizeof(double));

		geodesic(y, dydx);

		for (i = 0; i < N; i++)
		{
			yscal[i] = fabs(y[i]) + fabs(dydx[i] * htry) + 1.0e-3;
		}

		if (y[1] > M_PI/2) side = 1;
		else if (y[1] < M_PI/2) side = -1;
		else side = 0;

		hnext = rkqs(y, dydx, htry, escal, yscal, &hdid);

		if ((y[1]-M_PI/2)*side < 0)
		{
			memcpy(y, ylaststep, N * sizeof(double));

			binarysearch(y, dydx, hdid);

			/* Did we hit the disk? */
			if ((y[0] <= Rdisk) && (y[0] >= Rmstable))
			{
				unsigned p1 = 4.0 * (y[0] - Rmstable) / (Rdisk - Rmstable);
				unsigned p2 = floor(y[2] * 6.0 / M_PI);

				if ((p1 ^ p2) & 1)
				{
					rgb[0] = 255;
					rgb[1] = 128;
					rgb[2] = 128;
				}
				else
				{
					rgb[0] = 255;
					rgb[1] = 0;
					rgb[2] = 0;
				}

				return;
			}
		}

		/* Inside the hole, or escaped to infinity */
		if ((y[0] < Rhor) || (y[0] > r0))
		{
			rgb[0] = 0;
			rgb[1] = 0;
			rgb[2] = 0;

			return;
		}

		htry = hnext;
	}
}

/* Write all the data, or fail and exit */
static void full_write(int fd, void *buf, size_t size)
{
	while (size)
	{
		ssize_t did = write(fd, buf, size);
		if (did == -1)
		{
			if (errno == EINTR) continue;

			errx(1, "Error writing file: %s\n", strerror(errno));
		}

		size -= did;
		buf = (char *)buf - did;
	}
}

/* Open a file, and output a tga header for a square image of the given size */
static int open_tga(const char *filename, int size)
{
	char c1, c2;

	int fd = open(filename, O_CREAT | O_WRONLY | O_TRUNC, S_IRUSR | S_IWUSR | S_IRGRP | S_IROTH);

	if (fd == -1) errx(1, "Couldn't open %s for writing\n", filename);

	/* Output the header (embedded zeros explicit) */
	write(fd, "\0\0\2\0\0\0\0\0\0\0\0\0", 12);

	c1 = size%256;
	c2 = size/256;
	full_write(fd, &c1, 1);
	full_write(fd, &c2, 1);

	c1 = size%256;
	c2 = size/256;
	full_write(fd, &c1, 1);
	full_write(fd, &c2, 1);

	full_write(fd, "\x18\0", 2);

	return fd;
}

static double inner_orbit(void)
{
	double z1 = 1+cbrt(1-a2)*(cbrt(1+a)+cbrt(1-a));
	double z2 = sqrt(3*a2+z1*z1);
	return 3+z2-sqrt((3-z1)*(3+z1+2*z2));
}

static void full_pwrite(int fd, void *buf, size_t size, size_t offset)
{
	while (size)
	{
		ssize_t did = pwrite(fd, buf, size, offset);
		if (did == -1)
		{
			if (errno == EINTR) continue;

			errx(1, "Error writing file: %s\n", strerror(errno));
		}

		size -= did;
		buf = (char *)buf - did;
		offset += did;
	}
}

/* The master process handles the IO */
static void master(int numslaves)
{
	int fd = open_tga("image.tga", size);

	int *row = calloc(numslaves, sizeof(int));
	off_t offset;

	int i;

	MPI_Status status;

	unsigned char *buf = calloc(size, 3);
	if (!buf || !row) errx(1, "Out of memory\n");

	/* Initialize the starting rows every slave will be working on */
	for (i = 0; i < numslaves; i++) row[i] = i;

	/* Wait for size rows of data */
	for (i = 0; i < size; i++)
	{
		/* Wait to get some data */
		MPI_Recv(buf, 3 * size, MPI_BYTE, MPI_ANY_SOURCE, 0, MPI_COMM_WORLD, &status);

		/* Calculate offset within output file from the source of the row */
		offset = ((off_t) row[status.MPI_SOURCE - 1]) * size * 3 + 18;

		/* Output to the correct spot in the file */
		full_pwrite(fd, buf, size * 3, offset);

		/* The next row it will be working on */
		row[status.MPI_SOURCE - 1] += numslaves;
	}

	close(fd);

	free(buf);
	free(row);
}

/* Slave compute processes send their results to the master */
static void slave(int numslaves, int rank)
{
	MPI_Request rq = MPI_REQUEST_NULL;

	int i, j;

	unsigned char *buffer1 = calloc(size, 3);
	unsigned char *buffer2 = calloc(size, 3);
	unsigned char *buf = buffer1;
	if (!buffer1 || !buffer2) errx(1, "Out of memory\n");

	r0 = 1000.0;
	theta0 = (M_PI/180.0) * inclination;

	a2 = a*a;

	Rhor = 1.0 + sqrt(1.0-a2) + 1e-5;
	Rdisk = 20.0;
	Rmstable = inner_orbit();

	for (j = rank; j < size; j += numslaves)
	{
		printf("%d\n", j);

		for (i = 0; i < size; i++)
		{
			fire_ray(&buf[i * 3], i, j);
		}

		/* Wait for the previous send to complete */
		MPI_Wait(&rq, MPI_STATUS_IGNORE);

		/* Send the new data */
		MPI_Isend(buf, 3 * size, MPI_BYTE, 0, 0, MPI_COMM_WORLD, &rq);

		/* Flip the buffer to use */
		if (buf == buffer1)
		{
			buf = buffer2;
		}
		else
		{
			buf = buffer1;
		}
	}

	/* Wait for the final send to complete */
	MPI_Wait(&rq, MPI_STATUS_IGNORE);

	/* Free memory */
	free(buffer1);
	free(buffer2);
}

int main(int argc, char **argv)
{
	int numprocs;
	int rank;

	/* Initialize MPI */
	MPI_Init(&argc, &argv);

	MPI_Comm_size(MPI_COMM_WORLD, &numprocs);
	MPI_Comm_rank(MPI_COMM_WORLD, &rank);

	if (numprocs == 1) errx(1, "We need more than one rank\n");

	if (!rank)
	{
		master(numprocs - 1);
	}
	else
	{
		slave(numprocs - 1, rank - 1);
	}

	MPI_Finalize();

	return 0;
}
```
{% endfold %}

{% fold info @C script with mpi (raw distribution) %}
complie using `mpicc raw_mpi.c -o raw_mpi -lm` (on Ubuntu24.04)
run using `mpirun -np 4 raw_mpi`
```c
#define _GNU_SOURCE
#include <math.h>
#include <stdlib.h>
#include <stdio.h>
#include <string.h>
#include <err.h>
#include <sys/stat.h>
#include <fcntl.h>
#include <unistd.h>
#include <errno.h>
#include "mpi.h"

#define N	6

static const double a = 0;
static const int size = 1000;
static double inclination = 45;

static double r0, theta0;

static double a2;
static double Rhor, Rmstable, Rdisk;

static double L, kappa;

/* Static constants for straight‑line motion (filled by initial()) */
static double vx = 0.0, vy = 0.0, vz = 0.0;   /* Cartesian velocity components */
static double vt = 1.0;                      /* dt/dλ (normalised to 1) */

/* Utility: convert spherical to Cartesian */
static void sph2cart(double r, double theta, double phi,
                     double *x, double *y, double *z)
{
    double sint = sin(theta), cost = cos(theta);
    double sinp = sin(phi), cosp = cos(phi);
    *x = r * sint * cosp;
    *y = r * sint * sinp;
    *z = r * cost;
}

/* Coupled differential equations for straight‑line photon motion */
static void geodesic(double *y, double *dydx)
{
    double r = y[0];
    double theta = y[1];
    double phi = y[2];

    /* Convert current position to Cartesian */
    double x, yc, z;
    sph2cart(r, theta, phi, &x, &yc, &z);

    /* Spherical velocity components from constant Cartesian velocity */
    double r_vec[3] = {x, yc, z};
    double v_vec[3] = {vx, vy, vz};

    double dot_rv = x*vx + yc*vy + z*vz;
    double r2 = r*r;
    double v2 = vx*vx + vy*vy + vz*vz;   /* should be 1 if normalised */

    /* dr/dλ */
    double drdl = dot_rv / r;

    /* dθ/dλ */
    double cos_theta = cos(theta), sin_theta = sin(theta);
    double cos_phi = cos(phi), sin_phi = sin(phi);
    double v_theta = vx*cos_theta*cos_phi + vy*cos_theta*sin_phi - vz*sin_theta;
    double dthetadl = v_theta / r;

    /* dφ/dλ */
    double v_phi = -vx*sin_phi + vy*cos_phi;
    double dphidl = v_phi / (r * sin_theta);

    /* dt/dλ is constant */
    double dtdl = vt;

    /* Canonical momenta in flat spherical coordinates:
       p_r = dr/dλ ,  p_θ = r^2 dθ/dλ */
    double pr = drdl;
    double ptheta = r2 * dthetadl;

    /* Constants of motion: p_t = -vt ,  p_φ = x*vy - yc*vx */
    double pt = -vt;
    double pphi = x*vy - yc*vx;

    /* Derivatives of canonical momenta from Hamilton's equations (flat space) */
    double dprdl = (ptheta*ptheta + pphi*pphi/(sin_theta*sin_theta)) / (r*r*r);
    double dpthetadl = (pphi*pphi * cos_theta) / (r2 * sin_theta*sin_theta*sin_theta);

    /* Guard against sinθ = 0 */
    if (sin_theta < 1e-8) {
        dphidl = 0.0;
        dpthetadl = 0.0;
    }

    /* Fill output derivatives in the same order as the state vector */
    dydx[0] = drdl;          /* dr/dλ */
    dydx[1] = dthetadl;      /* dθ/dλ */
    dydx[2] = dphidl;        /* dφ/dλ */
    dydx[3] = dtdl;          /* dt/dλ */
    dydx[4] = dprdl;         /* dp_r/dλ */
    dydx[5] = dpthetadl;     /* dp_θ/dλ */
}

/* Initial Conditions for Ray – straight line, observer at (r0, θ0, φ=0) */
static void initial(double *y0, double *ydot0, double x, double y)
{
    /* Pixel coordinates (x,y) are offsets from the image centre.
       They map to angular offsets α (horizontal) and β (vertical) in radians.
       The field of view scaling is taken from fire_ray().
       Here we need only the direction, not the absolute scaling.
       We'll compute the unit vector from the observer to the pixel. */

    double alpha = x;   /* already in radians (see fire_ray: x = (x1 - centre)*range) */
    double beta  = y;   /* same for y */

    /* Observer position in Cartesian (assuming φ=0 initially) */
    double sin_th0 = sin(theta0);
    double cos_th0 = cos(theta0);
    double obs_x = r0 * sin_th0;
    double obs_y = 0.0;
    double obs_z = r0 * cos_th0;

    /* Line of sight: from observer toward the origin (black hole) */
    double los_x = -obs_x;
    double los_y = -obs_y;
    double los_z = -obs_z;
    double los_norm = sqrt(los_x*los_x + los_y*los_y + los_z*los_z);
    double forward_x = los_x / los_norm;
    double forward_y = los_y / los_norm;
    double forward_z = los_z / los_norm;

    /* Build orthonormal basis (right, up) perpendicular to line of sight.
       'up' is the projection of the global Z axis onto the image plane,
       except when forward is parallel to Z (inclination 0 or π). */
    double global_up_x = 0.0, global_up_y = 0.0, global_up_z = 1.0;
    double right_x, right_y, right_z;
    double up_x, up_y, up_z;

    /* Compute right = forward × global_up (normalised) */
    right_x = forward_y * global_up_z - forward_z * global_up_y;
    right_y = forward_z * global_up_x - forward_x * global_up_z;
    right_z = forward_x * global_up_y - forward_y * global_up_x;
    double rnorm = sqrt(right_x*right_x + right_y*right_y + right_z*right_z);
    if (rnorm > 1e-12) {
        right_x /= rnorm; right_y /= rnorm; right_z /= rnorm;
        /* up = right × forward */
        up_x = right_y * forward_z - right_z * forward_y;
        up_y = right_z * forward_x - right_x * forward_z;
        up_z = right_x * forward_y - right_y * forward_x;
    } else {
        /* forward is parallel to global Z (θ0 = 0 or π) – use X axis as right */
        right_x = 1.0; right_y = 0.0; right_z = 0.0;
        up_x = 0.0; up_y = 1.0; up_z = 0.0;
    }

    /* Direction to the pixel: forward + α·right + β·up */
    double dir_x = forward_x + alpha * right_x + beta * up_x;
    double dir_y = forward_y + alpha * right_y + beta * up_y;
    double dir_z = forward_z + alpha * right_z + beta * up_z;
    double dir_norm = sqrt(dir_x*dir_x + dir_y*dir_y + dir_z*dir_z);
    dir_x /= dir_norm;
    dir_y /= dir_norm;
    dir_z /= dir_norm;

    /* Store constant Cartesian velocity (normalised to c=1) */
    vx = dir_x;
    vy = dir_y;
    vz = dir_z;
    vt = 1.0;   /* dt/dλ = 1 */

    /* Initial spherical state: observer's position */
    y0[0] = r0;
    y0[1] = theta0;
    y0[2] = 0.0;       /* φ = 0 */
    y0[3] = 0.0;       /* t = 0 */

    /* Compute initial spherical velocities from the Cartesian velocity */
    double x0_cart, y0_cart, z0_cart;
    sph2cart(r0, theta0, 0.0, &x0_cart, &y0_cart, &z0_cart);

    double dot_rv = x0_cart*vx + y0_cart*vy + z0_cart*vz;
    double r0_sq = r0 * r0;
    double cos_phi0 = 1.0, sin_phi0 = 0.0;   /* φ = 0 */

    double drdl0 = dot_rv / r0;
    double v_theta0 = vx*cos_th0*cos_phi0 + vy*cos_th0*sin_phi0 - vz*sin_th0;
    double dthetadl0 = v_theta0 / r0;
    double v_phi0 = -vx*sin_phi0 + vy*cos_phi0;
    double dphidl0 = v_phi0 / (r0 * sin_th0);

    /* Canonical momenta */
    y0[4] = drdl0;                  /* p_r = dr/dλ */
    y0[5] = r0_sq * dthetadl0;     /* p_θ = r² dθ/dλ */

    /* Initial derivatives (for consistency) */
    geodesic(y0, ydot0);
}

static void rkstep(double *y, double *dydx, double h, double *yout, double *yerr)
{
	int i;

	double ak[N];

	double ytemp1[N], ytemp2[N], ytemp3[N], ytemp4[N], ytemp5[N];

	for (i = 0; i < N; i++)
	{
		double hdydx = h * dydx[i];
		double yi = y[i];
		ytemp1[i] = yi + 0.2 * hdydx;
		ytemp2[i] = yi + (3.0/40.0) * hdydx;
		ytemp3[i] = yi + 0.3 * hdydx;
		ytemp4[i] = yi -(11.0/54.0) * hdydx;
		ytemp5[i] = yi + (1631.0/55296.0) * hdydx;
		yout[i] = yi + (37.0/378.0) * hdydx;
		yerr[i] = ((37.0/378.0)-(2825.0/27648.0)) * hdydx;
	}

	geodesic(ytemp1, ak);

	for (i = 0; i < N; i++)
	{
		double yt = h * ak[i];
		ytemp2[i] += (9.0/40.0) * yt;
		ytemp3[i] -= 0.9 * yt;
		ytemp4[i] += 2.5 * yt;
		ytemp5[i] += (175.0/512.0) * yt;
	}

	geodesic(ytemp2, ak);

	for (i = 0; i < N; i++)
	{
		double yt = h * ak[i];
		ytemp3[i] += 1.2 * yt;
		ytemp4[i] -= (70.0/27.0) * yt;
		ytemp5[i] += (575.0/13824.0) * yt;
		yout[i] += (250.0/621.0) * yt;
		yerr[i] += ((250.0/621.0)-(18575.0/48384.0)) * yt;
	}

	geodesic(ytemp3, ak);

	for (i = 0; i < N; i++)
	{
		double yt = h * ak[i];
		ytemp4[i] += (35.0/27.0) * yt;
		ytemp5[i] += (44275.0/110592.0) * yt;
		yout[i] += (125.0/594.0) * yt;
		yerr[i] += ((125.0/594.0)-(13525.0/55296.0)) * yt;
	}

	geodesic(ytemp4, ak);

	for (i = 0; i < N; i++)
	{
		double yt = h * ak[i];
		ytemp5[i] += (253.0/4096.0) * yt;
		yerr[i] -= (277.0/14336.0) * yt;
	}

	geodesic(ytemp5, ak);

	for (i = 0; i < N; i++)
	{
		double yt = h * ak[i];
		yout[i] += (512.0/1771.0) * yt;
		yerr[i] += ((512.0/1771.0)-0.25) * yt;
	}
}

static double rkqs(double *y, double *dydx, double htry, double escal, double *yscal, double *hdid)
{
	int i;

	double hnext;

	double errmax, h = htry, htemp;
	double yerr[N], ytemp[N];

	while (1)
	{
		rkstep(y, dydx, h, ytemp, yerr);

		errmax = 0.0;
		for (i = 0; i < N; i++)
		{
			double temp = fabs(yerr[i]/yscal[i]);
			if (temp > errmax) errmax = temp;
		}

		errmax *= escal;
		if (errmax <= 1.0) break;

		htemp = 0.9 * h / sqrt(sqrt(errmax));

		h *= 0.1;

		if (h >= 0.0)
		{
			if (htemp > h) h = htemp;
		}
		else
		{
			if (htemp < h) h = htemp;
		}
	}

	if (errmax > 1.89e-4)
	{
		hnext = 0.9 * h * pow(errmax, -0.2);
	}
	else
	{
		hnext = 5.0 * h;
	}

	*hdid = h;

	memcpy(y, ytemp, N * sizeof(double));

	return hnext;
}

static void binarysearch(double *y, double *dydx, double hbig)
{
	double hsmall = 0.0;

	int side;
	if (y[1] > M_PI/2.0)
	{
		side = 1;
	}
	else if (y[1] < M_PI/2.0)
	{
		side = -1;
	}
	else
	{
		/* Already at the equator */
		return;
	}

	geodesic(y,dydx);

	while ((y[0] > Rhor) && (y[0] < r0) && (side != 0))
	{
		double yout[N], yerr[N];

		double hdiff = hbig - hsmall;

		if (hdiff < 1e-7)
		{
			rkstep(y, dydx, hbig, yout, yerr);

			memcpy(y, yout, N * sizeof(double));

			return;
		}

		double hmid = (hbig + hsmall) / 2;

		rkstep(y, dydx, hmid, yout, yerr);

		if (side * (yout[1] - M_PI/2.0) > 0)
		{
			hsmall = hmid;
		}
		else
		{
			hbig = hmid;
		}
	}
}

static void fire_ray(unsigned char *rgb, int x1, int y1)
{
	double htry = 0.5, escal = 1e11, hdid = 0.0, hnext = 0.0;

	double range = 0.0025 * Rdisk / (size - 1.0);

	double y[N], dydx[N], yscal[N], ylaststep[N];

	int side;
	int i;

	initial(y, dydx, (x1 - (size + 1.0) / 2) * range, (y1 - (size + 1.0) / 2) * range);

	while (1)
	{
		memcpy(ylaststep, y, N * sizeof(double));

		geodesic(y, dydx);

		for (i = 0; i < N; i++)
		{
			yscal[i] = fabs(y[i]) + fabs(dydx[i] * htry) + 1.0e-3;
		}

		if (y[1] > M_PI/2) side = 1;
		else if (y[1] < M_PI/2) side = -1;
		else side = 0;

		hnext = rkqs(y, dydx, htry, escal, yscal, &hdid);

		if ((y[1]-M_PI/2)*side < 0)
		{
			memcpy(y, ylaststep, N * sizeof(double));

			binarysearch(y, dydx, hdid);

			/* Did we hit the disk? */
			if ((y[0] <= Rdisk) && (y[0] >= Rmstable))
			{
				unsigned p1 = 4.0 * (y[0] - Rmstable) / (Rdisk - Rmstable);
				unsigned p2 = floor(y[2] * 6.0 / M_PI);

				if ((p1 ^ p2) & 1)
				{
					rgb[0] = 255;
					rgb[1] = 128;
					rgb[2] = 128;
				}
				else
				{
					rgb[0] = 255;
					rgb[1] = 0;
					rgb[2] = 0;
				}

				return;
			}
		}

		/* Inside the hole, or escaped to infinity */
		if ((y[0] < Rhor) || (y[0] > r0))
		{
			rgb[0] = 0;
			rgb[1] = 0;
			rgb[2] = 0;

			return;
		}

		htry = hnext;
	}
}

/* Write all the data, or fail and exit */
static void full_write(int fd, void *buf, size_t size)
{
	while (size)
	{
		ssize_t did = write(fd, buf, size);
		if (did == -1)
		{
			if (errno == EINTR) continue;

			errx(1, "Error writing file: %s\n", strerror(errno));
		}

		size -= did;
		buf = (char *)buf - did;
	}
}

/* Open a file, and output a tga header for a square image of the given size */
static int open_tga(const char *filename, int size)
{
	char c1, c2;

	int fd = open(filename, O_CREAT | O_WRONLY | O_TRUNC, S_IRUSR | S_IWUSR | S_IRGRP | S_IROTH);

	if (fd == -1) errx(1, "Couldn't open %s for writing\n", filename);

	/* Output the header (embedded zeros explicit) */
	write(fd, "\0\0\2\0\0\0\0\0\0\0\0\0", 12);

	c1 = size%256;
	c2 = size/256;
	full_write(fd, &c1, 1);
	full_write(fd, &c2, 1);

	c1 = size%256;
	c2 = size/256;
	full_write(fd, &c1, 1);
	full_write(fd, &c2, 1);

	full_write(fd, "\x18\0", 2);

	return fd;
}

static double inner_orbit(void)
{
	double z1 = 1+cbrt(1-a2)*(cbrt(1+a)+cbrt(1-a));
	double z2 = sqrt(3*a2+z1*z1);
	return 3+z2-sqrt((3-z1)*(3+z1+2*z2));
}

static void full_pwrite(int fd, void *buf, size_t size, size_t offset)
{
	while (size)
	{
		ssize_t did = pwrite(fd, buf, size, offset);
		if (did == -1)
		{
			if (errno == EINTR) continue;

			errx(1, "Error writing file: %s\n", strerror(errno));
		}

		size -= did;
		buf = (char *)buf - did;
		offset += did;
	}
}

/* The master process handles the IO */
static void master(int numslaves)
{
	int fd = open_tga("image.tga", size);

	int *row = calloc(numslaves, sizeof(int));
	off_t offset;

	int i;

	MPI_Status status;

	unsigned char *buf = calloc(size, 3);
	if (!buf || !row) errx(1, "Out of memory\n");

	/* Initialize the starting rows every slave will be working on */
	for (i = 0; i < numslaves; i++) row[i] = i;

	/* Wait for size rows of data */
	for (i = 0; i < size; i++)
	{
		/* Wait to get some data */
		MPI_Recv(buf, 3 * size, MPI_BYTE, MPI_ANY_SOURCE, 0, MPI_COMM_WORLD, &status);

		/* Calculate offset within output file from the source of the row */
		offset = ((off_t) row[status.MPI_SOURCE - 1]) * size * 3 + 18;

		/* Output to the correct spot in the file */
		full_pwrite(fd, buf, size * 3, offset);

		/* The next row it will be working on */
		row[status.MPI_SOURCE - 1] += numslaves;
	}

	close(fd);

	free(buf);
	free(row);
}

/* Slave compute processes send their results to the master */
static void slave(int numslaves, int rank)
{
	MPI_Request rq = MPI_REQUEST_NULL;

	int i, j;

	unsigned char *buffer1 = calloc(size, 3);
	unsigned char *buffer2 = calloc(size, 3);
	unsigned char *buf = buffer1;
	if (!buffer1 || !buffer2) errx(1, "Out of memory\n");

	r0 = 1000.0;
	theta0 = (M_PI/180.0) * inclination;

	a2 = a*a;

	Rhor = 1.0 + sqrt(1.0-a2) + 1e-5;
	Rdisk = 20.0;
	Rmstable = inner_orbit();

	for (j = rank; j < size; j += numslaves)
	{
		printf("%d\n", j);

		for (i = 0; i < size; i++)
		{
			fire_ray(&buf[i * 3], i, j);
		}

		/* Wait for the previous send to complete */
		MPI_Wait(&rq, MPI_STATUS_IGNORE);

		/* Send the new data */
		MPI_Isend(buf, 3 * size, MPI_BYTE, 0, 0, MPI_COMM_WORLD, &rq);

		/* Flip the buffer to use */
		if (buf == buffer1)
		{
			buf = buffer2;
		}
		else
		{
			buf = buffer1;
		}
	}

	/* Wait for the final send to complete */
	MPI_Wait(&rq, MPI_STATUS_IGNORE);

	/* Free memory */
	free(buffer1);
	free(buffer2);
}

int main(int argc, char **argv)
{
	int numprocs;
	int rank;

	/* Initialize MPI */
	MPI_Init(&argc, &argv);

	MPI_Comm_size(MPI_COMM_WORLD, &numprocs);
	MPI_Comm_rank(MPI_COMM_WORLD, &rank);

	if (numprocs == 1) errx(1, "We need more than one rank\n");

	if (!rank)
	{
		master(numprocs - 1);
	}
	else
	{
		slave(numprocs - 1, rank - 1);
	}

	MPI_Finalize();

	return 0;
}
```
{% endfold %}

{% fold info @C script with mpi (disk upside / downside) %}
complie using `mpicc side_mpi.c -o side_mpi -lm` (on Ubuntu24.04)
run using `mpirun -np 4 side_mpi`
```c
#define _GNU_SOURCE
#include <math.h>
#include <stdlib.h>
#include <stdio.h>
#include <string.h>
#include <err.h>
#include <sys/stat.h>
#include <fcntl.h>
#include <unistd.h>
#include <errno.h>
#include "mpi.h"

#define N	6

static const double a = 0.998;
static const int size = 1000;
static double inclination = 1;

static double r0, theta0;

static double a2;
static double Rhor, Rmstable, Rdisk;

static double L, kappa;

/* Coupled differential equations describing motion of photon */
static void geodesic(double *y, double *dydx)
{
	double r, theta, pr, ptheta;

	r = y[0];
	theta = y[1];
	pr = y[4];
	ptheta = y[5];

	double r2 = r*r;
	double twor = 2.0*r;

	double sintheta, costheta;
	sincos(theta, &sintheta, &costheta);
	double cos2 = costheta*costheta;
	double sin2 = sintheta*sintheta;

	double sigma = r2+a2*cos2;
	double delta = r2-twor+a2;
	double sd = sigma*delta;
	double siginv = 1.0/sigma;
	double bot = 1.0/sd;

	/* Prevent problems with the axis */
	if (sintheta < 1e-8)
	{
		sintheta = 1e-8;
		sin2 = 1e-16;
	}

	dydx[0] = -pr*delta*siginv;
	dydx[1] = -ptheta*siginv;
	dydx[2] = -(twor*a+(sigma-twor)*L/sin2)*bot;
	dydx[3] = -(1.0+(twor*(r2+a2)-twor*a*L)*bot);
	dydx[4] = -(((r-1.0)*(-kappa)+twor*(r2+a2)-2.0*a*L)*bot-2.0*pr*pr*(r-1.0)*siginv);
	dydx[5] = -sintheta*costheta*(L*L/(sin2*sin2)-a2)*siginv;
}

/* Initial Conditions for Ray */
static void initial(double *y0, double *ydot0, double x, double y)
{
	y0[0] = r0;
	y0[1] = theta0;
	y0[2] = 0;
	y0[3] = 0;
	y0[4] = cos(y)*cos(x);
	y0[5] = sin(y)/r0;

	double sintheta, costheta;
	sincos(theta0, &sintheta, &costheta);
	double cos2 = costheta*costheta;
	double sin2 = sintheta*sintheta;

	double rdot0 = y0[4];
	double thetadot0 = y0[5];

	double r2 = r0 * r0;
	double sigma = r2 + a2*cos2;
	double delta = r2 - 2.0 * r0 + a2;
	double s1 = sigma - 2.0 * r0;

	y0[4]= rdot0*sigma/delta;
	y0[5]= thetadot0*sigma;

	ydot0[0] = rdot0;
	ydot0[1] = thetadot0;
	ydot0[2] = cos(y)*sin(x)/(r0*sin(theta0));

	double phidot0 = ydot0[2];
	double energy2 = s1*(rdot0*rdot0/delta+thetadot0*thetadot0)
					+ delta*sin2*phidot0*phidot0;

	double energy = sqrt(energy2);

	/* Rescale */
	y0[4] = y0[4]/energy;
	y0[5] = y0[5]/energy;

	/* Angular Momentum with E = 1 */
	L = ((sigma*delta*phidot0-2.0*a*r0*energy)*sin2/s1)/energy;

	kappa = y0[5]*y0[5]+a2*sin2+L*L/sin2;

	/* Hack - make sure everything is normalized correctly by a call to geodesic */
	geodesic(y0, ydot0);
}

static void rkstep(double *y, double *dydx, double h, double *yout, double *yerr)
{
	int i;

	double ak[N];

	double ytemp1[N], ytemp2[N], ytemp3[N], ytemp4[N], ytemp5[N];

	for (i = 0; i < N; i++)
	{
		double hdydx = h * dydx[i];
		double yi = y[i];
		ytemp1[i] = yi + 0.2 * hdydx;
		ytemp2[i] = yi + (3.0/40.0) * hdydx;
		ytemp3[i] = yi + 0.3 * hdydx;
		ytemp4[i] = yi -(11.0/54.0) * hdydx;
		ytemp5[i] = yi + (1631.0/55296.0) * hdydx;
		yout[i] = yi + (37.0/378.0) * hdydx;
		yerr[i] = ((37.0/378.0)-(2825.0/27648.0)) * hdydx;
	}

	geodesic(ytemp1, ak);

	for (i = 0; i < N; i++)
	{
		double yt = h * ak[i];
		ytemp2[i] += (9.0/40.0) * yt;
		ytemp3[i] -= 0.9 * yt;
		ytemp4[i] += 2.5 * yt;
		ytemp5[i] += (175.0/512.0) * yt;
	}

	geodesic(ytemp2, ak);

	for (i = 0; i < N; i++)
	{
		double yt = h * ak[i];
		ytemp3[i] += 1.2 * yt;
		ytemp4[i] -= (70.0/27.0) * yt;
		ytemp5[i] += (575.0/13824.0) * yt;
		yout[i] += (250.0/621.0) * yt;
		yerr[i] += ((250.0/621.0)-(18575.0/48384.0)) * yt;
	}

	geodesic(ytemp3, ak);

	for (i = 0; i < N; i++)
	{
		double yt = h * ak[i];
		ytemp4[i] += (35.0/27.0) * yt;
		ytemp5[i] += (44275.0/110592.0) * yt;
		yout[i] += (125.0/594.0) * yt;
		yerr[i] += ((125.0/594.0)-(13525.0/55296.0)) * yt;
	}

	geodesic(ytemp4, ak);

	for (i = 0; i < N; i++)
	{
		double yt = h * ak[i];
		ytemp5[i] += (253.0/4096.0) * yt;
		yerr[i] -= (277.0/14336.0) * yt;
	}

	geodesic(ytemp5, ak);

	for (i = 0; i < N; i++)
	{
		double yt = h * ak[i];
		yout[i] += (512.0/1771.0) * yt;
		yerr[i] += ((512.0/1771.0)-0.25) * yt;
	}
}

static double rkqs(double *y, double *dydx, double htry, double escal, double *yscal, double *hdid)
{
	int i;

	double hnext;

	double errmax, h = htry, htemp;
	double yerr[N], ytemp[N];

	while (1)
	{
		rkstep(y, dydx, h, ytemp, yerr);

		errmax = 0.0;
		for (i = 0; i < N; i++)
		{
			double temp = fabs(yerr[i]/yscal[i]);
			if (temp > errmax) errmax = temp;
		}

		errmax *= escal;
		if (errmax <= 1.0) break;

		htemp = 0.9 * h / sqrt(sqrt(errmax));

		h *= 0.1;

		if (h >= 0.0)
		{
			if (htemp > h) h = htemp;
		}
		else
		{
			if (htemp < h) h = htemp;
		}
	}

	if (errmax > 1.89e-4)
	{
		hnext = 0.9 * h * pow(errmax, -0.2);
	}
	else
	{
		hnext = 5.0 * h;
	}

	*hdid = h;

	memcpy(y, ytemp, N * sizeof(double));

	return hnext;
}

static void binarysearch(double *y, double *dydx, double hbig)
{
	double hsmall = 0.0;

	int side;
	if (y[1] > M_PI/2.0)
	{
		side = 1;
	}
	else if (y[1] < M_PI/2.0)
	{
		side = -1;
	}
	else
	{
		/* Already at the equator */
		return;
	}

	geodesic(y,dydx);

	while ((y[0] > Rhor) && (y[0] < r0) && (side != 0))
	{
		double yout[N], yerr[N];

		double hdiff = hbig - hsmall;

		if (hdiff < 1e-7)
		{
			rkstep(y, dydx, hbig, yout, yerr);

			memcpy(y, yout, N * sizeof(double));

			return;
		}

		double hmid = (hbig + hsmall) / 2;

		rkstep(y, dydx, hmid, yout, yerr);

		if (side * (yout[1] - M_PI/2.0) > 0)
		{
			hsmall = hmid;
		}
		else
		{
			hbig = hmid;
		}
	}
}

static void fire_ray(unsigned char *rgb, int x1, int y1)
{
	double htry = 0.5, escal = 1e11, hdid = 0.0, hnext = 0.0;

	double range = 0.0025 * Rdisk / (size - 1.0);

	double y[N], dydx[N], yscal[N], ylaststep[N];

	int side;
	int i;

	initial(y, dydx, (x1 - (size + 1.0) / 2) * range, (y1 - (size + 1.0) / 2) * range);

	while (1)
	{
		memcpy(ylaststep, y, N * sizeof(double));

		geodesic(y, dydx);

		for (i = 0; i < N; i++)
		{
			yscal[i] = fabs(y[i]) + fabs(dydx[i] * htry) + 1.0e-3;
		}

		if (y[1] > M_PI/2) side = 1;
		else if (y[1] < M_PI/2) side = -1;
		else side = 0;

		hnext = rkqs(y, dydx, htry, escal, yscal, &hdid);

		if ((y[1]-M_PI/2)*side < 0)
		{
			memcpy(y, ylaststep, N * sizeof(double));

			binarysearch(y, dydx, hdid);

			/* Did we hit the disk? */
			if ((y[0] <= Rdisk) && (y[0] >= Rmstable))
			{
				unsigned p1 = 4.0 * (y[0] - Rmstable) / (Rdisk - Rmstable);
				unsigned p2 = floor(y[2] * 6.0 / M_PI);
				int is_upper = (side == -1);  /* side == -1: upside */

				if (is_upper) {
					/* upside: blue */
					if ((p1 ^ p2) & 1) {
						rgb[0] = 255;
						rgb[1] = 128;
						rgb[2] = 128;
					} else {
						rgb[0] = 255;
						rgb[1] = 0;
						rgb[2] = 0;
					}
				} else {
					/* downside: red */
					if ((p1 ^ p2) & 1) {
						rgb[0] = 128;
						rgb[1] = 128;
						rgb[2] = 255;
					} else {
						rgb[0] = 0;
						rgb[1] = 0;
						rgb[2] = 255;
					}
				}

				return;
			}
		}

		/* Inside the hole, or escaped to infinity */
		if ((y[0] < Rhor) || (y[0] > r0))
		{
			rgb[0] = 0;
			rgb[1] = 0;
			rgb[2] = 0;

			return;
		}

		htry = hnext;
	}
}

/* Write all the data, or fail and exit */
static void full_write(int fd, void *buf, size_t size)
{
	while (size)
	{
		ssize_t did = write(fd, buf, size);
		if (did == -1)
		{
			if (errno == EINTR) continue;

			errx(1, "Error writing file: %s\n", strerror(errno));
		}

		size -= did;
		buf = (char *)buf - did;
	}
}

/* Open a file, and output a tga header for a square image of the given size */
static int open_tga(const char *filename, int size)
{
	char c1, c2;

	int fd = open(filename, O_CREAT | O_WRONLY | O_TRUNC, S_IRUSR | S_IWUSR | S_IRGRP | S_IROTH);

	if (fd == -1) errx(1, "Couldn't open %s for writing\n", filename);

	/* Output the header (embedded zeros explicit) */
	write(fd, "\0\0\2\0\0\0\0\0\0\0\0\0", 12);

	c1 = size%256;
	c2 = size/256;
	full_write(fd, &c1, 1);
	full_write(fd, &c2, 1);

	c1 = size%256;
	c2 = size/256;
	full_write(fd, &c1, 1);
	full_write(fd, &c2, 1);

	full_write(fd, "\x18\0", 2);

	return fd;
}

static double inner_orbit(void)
{
	double z1 = 1+cbrt(1-a2)*(cbrt(1+a)+cbrt(1-a));
	double z2 = sqrt(3*a2+z1*z1);
	return 3+z2-sqrt((3-z1)*(3+z1+2*z2));
}

static void full_pwrite(int fd, void *buf, size_t size, size_t offset)
{
	while (size)
	{
		ssize_t did = pwrite(fd, buf, size, offset);
		if (did == -1)
		{
			if (errno == EINTR) continue;

			errx(1, "Error writing file: %s\n", strerror(errno));
		}

		size -= did;
		buf = (char *)buf - did;
		offset += did;
	}
}

/* The master process handles the IO */
static void master(int numslaves)
{
	int fd = open_tga("image.tga", size);

	int *row = calloc(numslaves, sizeof(int));
	off_t offset;

	int i;

	MPI_Status status;

	unsigned char *buf = calloc(size, 3);
	if (!buf || !row) errx(1, "Out of memory\n");

	/* Initialize the starting rows every slave will be working on */
	for (i = 0; i < numslaves; i++) row[i] = i;

	/* Wait for size rows of data */
	for (i = 0; i < size; i++)
	{
		/* Wait to get some data */
		MPI_Recv(buf, 3 * size, MPI_BYTE, MPI_ANY_SOURCE, 0, MPI_COMM_WORLD, &status);

		/* Calculate offset within output file from the source of the row */
		offset = ((off_t) row[status.MPI_SOURCE - 1]) * size * 3 + 18;

		/* Output to the correct spot in the file */
		full_pwrite(fd, buf, size * 3, offset);

		/* The next row it will be working on */
		row[status.MPI_SOURCE - 1] += numslaves;
	}

	close(fd);

	free(buf);
	free(row);
}

/* Slave compute processes send their results to the master */
static void slave(int numslaves, int rank)
{
	MPI_Request rq = MPI_REQUEST_NULL;

	int i, j;

	unsigned char *buffer1 = calloc(size, 3);
	unsigned char *buffer2 = calloc(size, 3);
	unsigned char *buf = buffer1;
	if (!buffer1 || !buffer2) errx(1, "Out of memory\n");

	r0 = 1000.0;
	theta0 = (M_PI/180.0) * inclination;

	a2 = a*a;

	Rhor = 1.0 + sqrt(1.0-a2) + 1e-5;
	Rdisk = 20.0;
	Rmstable = inner_orbit();

	for (j = rank; j < size; j += numslaves)
	{
		printf("%d\n", j);

		for (i = 0; i < size; i++)
		{
			fire_ray(&buf[i * 3], i, j);
		}

		/* Wait for the previous send to complete */
		MPI_Wait(&rq, MPI_STATUS_IGNORE);

		/* Send the new data */
		MPI_Isend(buf, 3 * size, MPI_BYTE, 0, 0, MPI_COMM_WORLD, &rq);

		/* Flip the buffer to use */
		if (buf == buffer1)
		{
			buf = buffer2;
		}
		else
		{
			buf = buffer1;
		}
	}

	/* Wait for the final send to complete */
	MPI_Wait(&rq, MPI_STATUS_IGNORE);

	/* Free memory */
	free(buffer1);
	free(buffer2);
}

int main(int argc, char **argv)
{
	int numprocs;
	int rank;

	/* Initialize MPI */
	MPI_Init(&argc, &argv);

	MPI_Comm_size(MPI_COMM_WORLD, &numprocs);
	MPI_Comm_rank(MPI_COMM_WORLD, &rank);

	if (numprocs == 1) errx(1, "We need more than one rank\n");

	if (!rank)
	{
		master(numprocs - 1);
	}
	else
	{
		slave(numprocs - 1, rank - 1);
	}

	MPI_Finalize();

	return 0;
}
```
{% endfold %}

![images of Schwarzschild black hole](image_Schwarzschild.png)
![images of Kerr black hole](image_Kerr.png)

- Function `static void geodesic(double *y, double *dydx)`:

	Calculate the geodesic of the ray.
	| Variable | Physical meaning |
	|:---:|:---:|
	| `y[0]` | $r$ |
	| `y[1]` | $\theta$ |
	| `y[2]` | $\phi$ |
	| `y[3]` | $t$ |
	| `y[4]` | $p_r$ |
	| `y[5]` | $p_\theta$ |

	The geodesic equations are
	$$
    \begin{aligned}
    \dot{r} &= -\frac{p_r \Delta}{\Sigma} \\[6pt]
    \dot{\theta} &= -\frac{p_\theta}{\Sigma} \\[6pt]
    \dot{\phi} &= -\frac{1}{\Sigma\Delta}\left(2ra + (\Sigma - 2r)\frac{L}{\sin^2\theta}\right) \\[6pt]
    \dot{t} &= -\left(1 + \frac{2r(r^2+a^2) - 2raL}{\Sigma\Delta}\right) \\[6pt]
    \dot{p}_r &= -\left(\frac{-\kappa(r-1) + 2r(r^2+a^2) - 2aL}{\Sigma\Delta} - \frac{2p_r^2(r-1)}{\Sigma}\right) \\[6pt]
    \dot{p}_\theta &= -\frac{\sin\theta\cos\theta}{\Sigma}\left(\frac{L^2}{\sin^4\theta} - a^2\right)
    \end{aligned}
	$$
	where $\dot{x}\equiv\mathrm{d}x/\mathrm{d}\lambda$, $\Sigma=r^2+a^2\cos^2\theta$, $\Delta=r^2-2r+a^2$.
	$L$ is angular momentum, $\kappa$ is Carter constant (energy at infinity is set to $E=1$).
	The negative sign in each equations above means tracing the ray in reverse.

{% note info %}
1. The Lagrangian
$$
\mathcal{L}=\frac{1}{2}g_{\mu\nu}\dot{x}^\mu \dot{x}^\nu,\quad \dot{x}^\mu=\frac{\mathrm{d}x^\mu}{\mathrm{d}\lambda}
$$
$$
p_\mu=\frac{\partial\mathcal{L}}{\partial \dot{x}^\mu}=g_{\mu\nu}\dot{x}^\nu
$$
here $p_t=-E$ and $p_\phi=L$ are constants of motion.

2. The Hamiltonian
$$
\mathcal{H}=\frac{1}{2}g^{\mu\nu}p_\mu p_\nu=0
$$
Hamilton's equations
$$
\dot{x}^\mu=\frac{\partial\mathcal{H}}{\partial p_\mu}=g^{\mu\nu}p_\nu
$$

3. Momentum equation
$$
\dot{p}_\mu=-\frac{\partial\mathcal{H}}{\partial x^\mu}=-\frac{1}{2}\frac{\partial g^{\alpha\beta}}{\partial x^\mu}p_\alpha p_\beta
$$
{% endnote %}

- Function `static void initial(double *y0, double *ydot0, double x, double y)`:

	Initiate the ray from $(x,y)$ in the observed plane to the Boyer-Lindquist Coordinates $(t,r,\theta,\phi)$.

- Function `static void fire_ray(unsigned char *rgb, int x1, int y1)`:

	Scan the $(x,y)$ in the observed plane and tracing the ray to check if it hit the disk.
