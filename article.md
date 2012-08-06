# Millores en les referències creuades amb prettyref

En articles anteriors hem vist l'ús i algunes millores en les referencies creuades. En aquest article veurem què ens pot aportar el paquet [prettyref->http://www.ctan.org/tex-archive/macros/latex/contrib/prettyref] a l'hora d'inserir referencies a seccions, figures, taules o equacions.

El paquet, que es crida al preàmbul amb <code>\usepackage{prettyref}</code>, només té un requisit i es que quan fem les etiquetes posem un codi per identificar cada element separat per dos punts de l'etiqueta. Per exemple: una equació es pot etiquetar amb <code>\label{eq:segongrau}</code>, una secció amb <code>\label{sec:nomseccio}</code>, una taula amb <code>\label{tau:nomdelataula}</code>, etc.

[prettyref->http://www.ctan.org/tex-archive/macros/latex/contrib/prettyref], que admet l'ús simultani de <code>\ref, \pageref i \autoref</code>, permet redefinir el comandament <code>\newrefformat{eq}{Equació \ref{#1} de la pàgina \pageref{#1}}</code> perquè quan escrivim el comandament per fer les referències creuades ens aparegui un text complet i ben adreçat:
<code>
\newrefformat{eq}{Equació \ref{#1} de la pàgina \pageref{#1}}
\newrefformat{lem}{Lema \ref{#1}}
\newrefformat{teo}{Teorema \ref{#1} de la pàgina \pageref{#1}}
%\newrefformat{cap}{Capítol \ref{#1}}
\newrefformat{sec}{Secció \ref{#1}}
\newrefformat{tau}{Taula \ref{#1} de la pàgina \pageref{#1}}
\newrefformat{fig}{Figura \ref{#1} de la pàgina \pageref{#1}}
</code>

Al document tex adjunt hom pot estudiar el codi i veure'n el resultat, un cop processat, al PDF adjunt.

Es poden trobar les versions actualitzades dels document a [github->https://github.com/jqueralt/prettyref]

