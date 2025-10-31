### If A and B are two real orthogonal matrices of same order and det A + det B = 0, show that A + B is a singular matrix.

$Given:$ $$A^tA \; = \; AA^t \; = \; B^tB \; = \; BB^t \; = \; I_n$$
$$det \, A + det \, B \; = \; 0$$
$$\therefore \quad det \, A = -det \, B \tag{1}$$
$To \; show:$
$$det\,(A\,+\,B)\;=\;0$$

$\text{We know that:}$
$AA^t \; = \; I_n$
$det \, (AA^t) \; = \; 1$
$det \, A \; det \, A^t \; = \; 1$
$(det \, A)^2 \; = \; 1$
$det \, A \; = \; \pm 1$
$\text{Similarly, }det \, B \; = \; \pm 1$

$\text{From (1),}$
$\text{when } det \, A \; = \; 1, \; det \, B \; = \; -1$
$\text{or when } det \, A \; = \; -1, \; det \, B \; = \; 1$


$det \, (A + B)$
$= \; det \, (AI_n+I_nB)$
$= \; det \, (AB^tB+AA^tB)$
$= \; det \, (A\,(B^t+A^t)\,B)$
$= \; det \, A \; det \, (B^t+A^t)$
$= \; - \, det \, (B^t+A^t)$
$= \; - \, det \, (B+A)^t$
$= \; - \, det \, (B+A)$
$= \; - \, det \, (A+B)$

$\therefore \quad det \, (A+B) \; = \; - \, det \, (A+B)$
$2 \, det \, (A+B) \; = \; 0$
$det \, (A+B) \; = \; 0$

$\therefore \quad A+B \text{ is singular.}$