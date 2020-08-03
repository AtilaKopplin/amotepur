# Estima��o de Propor��es {#proporc}

## Par�metros populacionais

Um caso especial de par�metro de interesse para muitos estudos ou pesquisas ocorre quando a vari�vel $y$ indica se uma determinada unidade populacional tem ou n�o uma determinada caracter�stica ou atributo, ou pertence a um determinado grupo especificado de unidades da popula��o. S�o exemplos desse tipo as investiga��es sobre:

* Migrantes entre os habitantes de determinada regi�o.
* Estabelecimentos agropecu�rios que se dedicam exclusivamente � produ��o leiteira numa determinada localidade.
* Estudantes do sexo feminino em escolas.
* Sondagens eleitorais, onde se deseja conhecer qual parcela dos eleitores pretende votar em determinado candidato.

Sendo uma vari�vel indicadora, a vari�vel $y$ ir� assumir para cada unidade da popula��o um de dois valores poss�veis: o valor $1$, se a unidade possui o atributo de interesse, ou o valor $0$, caso a unidade n�o possua o atributo. Para fins de apresenta��o, seja $A \subset U$ o subconjunto das unidades da popula��o $U$ que possuem o atributo de interesse. Ent�o, para cada unidade $i$ da popula��o, a vari�vel $y$ ser� definida como:

$$
\displaystyle y_i = I(i \in A) =
\begin{cases} 
1, \text { se a unidade} \textit{ i } \text{possui o atributo de interesse} \\ 
0, \text{ caso contr�rio}   
\end{cases}
(\#eq:eqpro1)
$$

O total populacional da vari�vel $y$ coincide com a contagem do n�mero de unidades populacionais que possuem o atributo de interesse, ou que pertencem ao subconjunto $A$, e pode ser representado como:

$$
Y = \displaystyle \sum_{i \in U} y_i = N_A  (\#eq:eqpro2)
$$
onde $N_A$ representa o n�mero de unidades populacionais que possuem o atributo de interesse.

Um exemplo cl�ssico do uso de vari�veis indicadoras ocorre quando se quer tabular frequ�ncias de respostas a uma pergunta categ�rica numa pesquisa ou censo. Considere uma pergunta cujas respostas podem ser um dos valores inteiros de $1$ a $C$, onde $C$ representa o n�mero de categorias de resposta da pergunta. Por exemplo, para a pergunta 'Qual � o sexo do morador', h� duas categorias de resposta $(C= 2)$: 1 (=Feminino) e 2 (=Masculino). Logo, para contar o n�mero de pessoas por sexo na popula��o, seria necess�rio criar duas vari�veis indicadoras: $y_{1i} = I[Sexo(i) = 1]$ e $y_{2i} = I[Sexo(i) = 2]$. Estas contagens poderiam ser representadas por $N_1$ para as pessoas do sexo Feminino, e $N_2$ para as pessoas do sexo Masculino, que seriam obtidos como dois totais populacionais:


$$
\displaystyle Y_1 = \sum_{i \in U} y_{1i} = N_1 \\ Y_2 = \sum_{i \in U} y_{2i} = N_2
$$


Como j� adiantado no Cap�tulo \@ref(visger), quando a vari�vel $y$ � do tipo indicadora, a *m�dia populacional* dada por: 

$$
\overline {Y} = \displaystyle \frac{1}{N} \sum_{i \in U} y_i = \frac {Y}{N} = \frac {N_A} {N} = p \, \, (\#eq:eqpro3)
$$

corresponde � *propor��o* $p$ de unidades da popula��o que t�m o atributo de interesse. O par�metro populacional *propor��o* � aqui representado pela letra $p$ min�scula, j� que a letra $P$ mai�scula j� foi usada para denotar *probabilidade*.

Uma *propor��o* pode assumir valores variando entre $0$, quando nenhuma unidade da popula��o tem o atributo investigado, at� $1$, quando todas as unidades possuem esse atributo. Muitas vezes � interessante expressar a *propor��o* sob forma de porcentagem podendo ent�o variar de 0% at� 100%.

Como $y$ s� pode receber valores $0$ ou $1$, a express�o da sua *vari�ncia* populacional pode ser simplificada:

$$ \hspace{-1.0cm}
S^2_y = \displaystyle \frac {1}{N-1} \left( \sum_{i \in U} y^2_i - N \overline{Y}^2 \right) = \frac{1}{N-1} \left(Np-Np^2 \right) = \frac{N}{N-1} p \left(1-p\right) (\#eq:eqpro4)
$$ 

A *vari�ncia* populacional de $y$ pode tamb�m ser definida como $\sigma^2_y = p (1-p)$. Tanto $S^2_y$ como $\sigma^2_y$ representam a dispers�o da distribui��o dos valores de $y$ na popula��o. Para popula��es com um grande n�mero de unidades $(N \displaystyle \rightarrow \infty)$, � f�cil verificar que as duas quantidades s�o praticamente iguais, pois pode-se considerar $S^2_y \displaystyle \doteq p(1-p) = \sigma^2_y$.

Outra medida importante para avaliar a dispers�o de uma vari�vel � o seu *Coeficiente de Varia��o* ou *CV*, definido como a raz�o entre o *Desvio Padr�o* de $y$ e sua m�dia:

$$
CV_y = \frac {\sqrt {\sigma^2_y}} {\overline Y} = \sqrt {{p(1-p) / p^2}} = \sqrt {(1-p)/p}\quad  (\#eq:eqpro5) 
$$

**(#exm:exmprop1)** Seja uma escola de ensino fundamental onde se deseja estudar a composi��o dos estudantes por sexo. Vamos supor que a escola tenha um total de 1.000 estudantes, dos quais 480 s�o do sexo feminino. Pode-se definir a vari�vel $y$ de interesse como:
$$
\displaystyle y_i =  \begin{cases} 1, \,\, \text {se o estudante for do sexo feminino} \\ 0, \,\, \text {caso contr�rio} \end{cases}
$$

O total de meninas da escola ser� o total da vari�vel $y$, dado por: 
$$
 Y = N_A = \displaystyle \sum_{i \in U} y_i = 1+1+0+1+...+0+1+1 = 480 
$$
A *m�dia* da vari�vel $y$, que neste caso � tamb�m a *propor��o* de meninas entre os estudantes da escola, � igual a:
$$
\overline Y = \frac Y N = \frac {N_A}{N} = p = \frac {480} {1.000}=0,48 \text { ou }  48\text{%}
$$

A *vari�ncia* da vari�vel $y$, medida por $S^2_y$ � igual a:
$$
S^2_y = \frac N {N-1}p(1-p) = \frac{1.000}{999} \times 0,48 \times 0,52 \doteq 0,24985
$$

e quando medida por $\sigma^2_y$ fica igual a
$$
\sigma^2_y = p(1-p) = 0,48 \times 0,52 = 0,2496
$$

Finalmente, o *coeficiente de varia��o* de $y$ � igual a:
$$
CV_y = \sqrt {\frac {1-p}{p}} = \sqrt \frac{0,52}{0,48} \doteq 1,041
$$

Podemos obter os resultados acima utilizando um *script* escrito em R.


```r
# Alunos da escola
N=1000
# Meninas
Na=480
# Propor��o de meninas
(p=Na/N)
```

```
## [1] 0.48
```

```r
# Vari�ncia
(S2y=N/(N-1)*p*(1-p))
```

```
## [1] 0.2498498
```

```r
(Sigma2y=p*(1-p))
```

```
## [1] 0.2496
```

```r
# Coeficiente de varia��o
(CVy=sqrt((1-p)/p))
```

```
## [1] 1.040833
```

Nas duas se��es seguintes tratamos do problema da estima��o desses par�metros populacionais a partir dos dados de amostras aleat�rias simples retiradas da popula��o de interesse com e sem reposi��o, respectivamente.


## Estima��o sob Amostragem Aleat�ria Simples Com Reposi��o - *AASC*

Seja $s$ uma *AASC* de tamanho $n$ selecionada de uma popula��o composta de $N$ unidades, onde se observa uma vari�vel indicadora $y$ como definida na se��o anterior. Pode-se obter estimadores para os par�metros populacionais de $y$ adaptando os estimadores gerais de total e m�dia apresentados no cap�tulo anterior.

O total de unidades da amostra com o atributo de interesse, $n_A$, ser� dado pela soma amostral:

$$
t_y = \displaystyle \sum_{i \in\ s} y_i = n_A \,\, (\#eq:eqpro6) 
$$
O total de unidades na popula��o com o atributo de interesse, $N_A$, � estimado usando:

$$
\widehat Y_{AASC} = N \times t_y / n = N \times n_A / n = \widehat N_A (\#eq:eqpro7)
$$
Como indicado no cap�tulo anterior, este estimador � n�o viciado sob AASC para qualquer vari�vel $y$, logo � ENV tamb�m quando $y$ � do tipo indicadora, como aqui definido.

A *propor��o amostral* de unidades que possuem o atributo de interesse � dada pela *m�dia amostral*:

$$
\displaystyle \overline y = \frac {1}{n} \sum_{i \in s} y_i = \frac {n_A}{n} =  \widehat p \,\, (\#eq:eqpro8) 
$$

Pode-se facilmente verificar que $\widehat p$ � um *estimador n�o viciado* para a *propor��o* populacional $p$, pois:

$$
\displaystyle E_{AASC} (\widehat p) = E_{AASC} (\overline y) = \overline Y = p \,\, (\#eq:eqpro9) 
$$

A *vari�ncia da propor��o amostral* sob AASC � dada por:

$$
\displaystyle V_{AASC} (\widehat p) = \frac {\sigma^2_y}{n} = \frac {p(1-p)}{n} \,\, (\#eq:eqpro10) 
$$

A *vari�ncia amostral* de $y$ � dada por:

$$
\displaystyle s^2_y = \frac {n}{n-1} \widehat p (1 - \widehat p) (\#eq:eqpro11) 
$$

Sob AASC, a *vari�ncia amostral *$s^2_y$ � um estimador n�o viciado para a *vari�ncia populacional* $\sigma^2_y$. Assim se obtem um estimador n�o viciado para a vari�ncia do estimador $\widehat p$ como:

$$
\displaystyle \widehat {V}_{AASC} (\widehat p) = \frac {\widehat p (1 - \widehat p)}{n-1} \,\, (\#eq:eqpro12) 
$$
O total de unidades na popula��o que possuem o atributo de interesse, e respectivo estimador, s�o obtidos por:
$$
N_A= Np\:\:\text{e}\:\: \widehat N_A=N\widehat p 
$$

A vari�ncia da estimativa de $N_A$ e seu estimador s�o dadas por:
$$
V_{AASC}(\widehat N_A)=N^2\frac {p(1-p)} {n}\:\:\text{e}\:\:\widehat V_{AASC}(\widehat N_A)=N^2\frac {\widehat p(1- \widehat p)} {n-1}
$$

A Tabela \@ref(tab:tabprop1) re�ne os resultados principais da estima��o de contagens e propor��es sob *AASC*.

<center>
<table>
<caption>(#tab:tabprop1)Par�metros e respectivos estimadores sob AASC</caption>
</table>
----------
Par�metro                                              Estimador                                                            
------------------------------------------------------ ----------------------------------------------------------------------------------
$\displaystyle N_A = \sum_{i \in U} y_i$               $\displaystyle\widehat N_A= N\times n_A/n = N\times \widehat p$

$\displaystyle p = N_A /N$                             $\displaystyle\widehat{p}=\displaystyle n_A / n$

$\displaystyle\sigma^2_y = p (1-p)$                    $\displaystyle s^2_y=\displaystyle\frac{n}{n-1}\widehat p (1-\widehat p)$

$\displaystyle V_{AASC}(\widehat N_A)=N^2{p(1-p)}/{n}$ $\displaystyle\widehat V_{AASC}(\widehat N_A)=N^2\widehat{p}(1-\widehat{p})/(n-1)$

$\displaystyle V_{AASC} (\widehat p) ={p(1-p)}/{n}$    $\displaystyle\widehat V_{AASC}(\widehat{p})=\widehat{p} (1-\widehat{p})/(n-1)$

----------
</center>


## Estima��o sob Amostragem Aleat�ria Simples Sem Reposi��o - *AAS*

No caso de uma amostra $s$ obtida por sele��o do tipo *AAS*, as express�es da soma amostral $t_y$, da propor��o amostral $\widehat p$ e da vari�ncia amostral $s^2_y$ t�m a mesma forma j� apresentada acima para amostras obtidas por *AASC*. Em consequ�ncia, tamb�m s�o id�nticos os estimadores para o total populacional $N_A$ e a propor��o populacional $p$. Entretanto, uma diferen�a � que no caso da *AAS* a vari�ncia amostral $s^2_y$ � um estimador n�o viciado para $S^2_y$ e n�o para $\sigma^2_y$. Tamb�m s�o diferentes as express�es para as vari�ncias dos estimadores amostrais e seus correspondentes estimadores n�o viciados.

Foi visto no Cap�tulo \@ref(aas) que as vari�ncias dos estimadores do total e da m�dia s�o dadas pelas express�es:

$$
V_{AAS} (\widehat Y) = N^2 \left( \frac 1 n - \frac {1}{N} \right) {S^2_y} \,\, (\#eq:eqpro13) 
$$

$$
V_{AAS} (\overline y) = \left( \frac 1 n - \frac {1}{N} \right) {S^2_y} \,\, (\#eq:eqpro14) 
$$

Ent�o, no caso de vari�veis $y$ do tipo indicadoras, tem-se que as vari�ncias do estimador do total e da propor��o populacionais s�o dadas por:

$$
V_{AAS} (\widehat {N} _A) = N^2 \left( \frac 1 n - \frac {1}{N} \right) \frac{N}{N-1} p(1-p) \,\, (\#eq:eqpro15) 
$$

$$
V_{AAS} (\widehat p) = \left( \frac 1 n - \frac {1}{N} \right) \frac{N}{N-1} p(1-p) \,\, (\#eq:eqpro16) 
$$

Note que para popula��es onde o n�mero de unidades $N$ � suficientemente grande, tem-se que $V_{AAS} (\widehat p) \doteq \displaystyle\frac {p (1 - p)}{n}$, resultando numa equival�ncia aproximada entre os desempenhos da *AAS* e da *AASC* na estima��o da propor��o populacional. Intuitivamente, isso ocorre porque a probabilidade de sele��o repetida sob *AASC* tende a ser muito pequena no caso de popula��es muito grandes.

Utilizando $s^2_y$ como estimador n�o viciado para $S^2_y$ chega-se aos estimadores para as vari�ncias dos estimadores de total e propor��o:

$$
\widehat V_{AAS} (\widehat {N} _A) = N^2 \left( \frac 1 n - \frac {1}{N} \right) \frac {n\widehat p (1 - \widehat p)} {n-1} \,\,(\#eq:eqpro17) 
$$

$$
\widehat V_{AAS} (\widehat p) = \left( \frac 1 n - \frac {1}{N} \right) \frac {n\widehat p (1 - \widehat p)} {n-1} \,\,(\#eq:eqpro18) 
$$

A Tabela \@ref(tab:tabprop2) re�ne os resultados principais da estima��o de contagens e propor��es sob *AAS*.

<center>

<table>
<caption>(#tab:tabprop2)Par�metros e respectivos estimadores sob AAS</caption>
</table>

----------
Par�metro                                                                             Estimador 
------------------------------------------------------------------------------------- --------------------------------------------------------------------------------------------------------------------------
$\displaystyle N_A=\sum_{i \in U} y_i$                                                $\displaystyle\widehat N_A = N \times n_A / n = N \times\widehat p$

$\displaystyle p = N_A/N$                                                             $\displaystyle\widehat{p} = n_A/n$

$\displaystyle S^2_y =\frac{N}{N-1}p(1-p)$                                            $\displaystyle s^2_y =\displaystyle\frac{n}{n-1} \widehat p (1 - \widehat p)$

$\displaystyle V_{AAS}(\widehat N_A)= N^2\left(\frac1 n-\frac1 N\right)S^2_y$         $\displaystyle\widehat V_{AAS}(\widehat N_A)=N^2\left(\frac 1 n-\frac {1}{N}\right)\frac{n\widehat p (1-\widehat p)}{n-1}$

$\displaystyle V_{AAS}(\widehat p)=\displaystyle\left(\frac1 n-\frac1 N\right)S^2_y$  $\displaystyle\widehat V_{AAS}(\widehat p)=\left(\frac 1 n-\frac{1}{N}\right)\frac{n\widehat p(1-\widehat p)} {n-1}$
----------
</center>
 

## Distribui��o amostral exata de estimadores de propor��o sob AASC e AAS

Na *AASC* as unidades amostrais s�o selecionadas com igual probabilidade e com reposi��o a cada sorteio. Ent�o as vari�veis aleat�rias $Y_k$ que correspondem aos valores observados na amostra a cada sorteio $k$,  $k=1, \dots, n$, s�o independentes e identicamente distribu�das com probabilidades definidas por:

$$ \hspace{-1.0cm}
\begin{align} \displaystyle P(Y_k = 1) = P(y_{i_k} \text{ ter o atributo de interesse}) = \frac {N_A} {N} = p \\ P(Y_k = 0) = P(y_{i_k} \text{ n�o ter o atributo de interesse}) = 1 - \frac {N_A} {N} = 1-p \end{align}\,\, (\#eq:eqpro19) 
$$

Dessa maneira fica configurada uma distribui��o de **_Bernoulli$(p)$_** para cada uma dessas vari�veis:
$$
\begin{array}{c | c c} 
 {v} & \ 1 & 0 \\
\hline \text{$P(Y_k = v)$} & p & 1-p  \\
\end{array}
$$
Ainda sob *AASC*, a soma amostral $t_y = n_A$, que representa o n�mero de unidades na amostra com o atributo de interesse, � ent�o dada pela soma de $n$ vari�veis aleat�rias IID com distribui��o **_Bernoulli$(p)$_**. Portanto, sob *AASC* a vari�vel aleat�ria $t_y = n_A$ segue uma distribui��o **_Binomial$(n,p)$_**. Imediatamente tem-se que:

$$
E_{AASC}(n_A) = n p {\quad \text e \quad} V_{AASC}(n_A) = n p (1-p) \,\, (\#eq:eqpro20) 
$$

Seguindo o mesmo racioc�nio, pode-se ter o valor esperado e a vari�ncia de $\widehat p$:

$$
\displaystyle E_{AASC} (\widehat p) = E_{AASC} \left(\frac{n_A}{n}\right) = p  {\quad\text e \quad} V_{AASC}(\widehat p) = \frac {p (1-p)} {n} \,\, (\#eq:eqpro21) 
$$

Outro resultado importante � que nesse caso se pode obter a distribui��o de probabilidades exata de $\widehat p$, pois:

$$ \hspace{-0,4cm}
\displaystyle P \left(\widehat p = \frac v n \right) = P(n_A = v) = \binom{n} {v} p^v (1-p)^{n-v} ,\quad \forall\, v=0, 1, 2, ..., n  (\#eq:eqpro22) 
$$


Esta distribui��o corresponde apenas a uma transforma��o escalar da distribui��o **_Binomial$(n,p)$_**, onde a contagem de sucessos ($n_A$) � dividida pelo n�mero de sorteios ($n$).

Sob *AAS*, a distribui��o da contagem de sucessos ($n_A$) tem uma distribui��o de probabilidades 
**_Hipergeom�trica$(N, N_A, n)$_**. Isto ocorre porque sob *AAS* os $n$ sorteios s�o feitos da popula��o sem reposi��o, e portanto, a cada nova unidade sorteada, o n�mero de unidades remanescentes na popula��o com o atributo de interesse varia, dependendo do n�mero dessas unidades j� selecionadas.

O n�mero total de amostras aleat�rias simples sem reposi��o de tamanho $n$ que podem ser selecionadas de uma popula��o com $N$ unidades � dado por $\binom{N}{n}$; o n�mero dessas amostras com exatamente $v$ unidades com a caracter�stica em estudo, e $n-v$ unidades sem essa caracter�stica, pode se calculado por $\binom{N_A}{v}\binom{N-N_A}{n-v}$. Sendo assim, a distribui��o de probabilidades da vari�vel aleat�ria $t_y = n_A$ � dada por:

$$
\displaystyle P \left(n_A = v \right) = \frac {\binom{N_A} {v} \binom{N-N_A} {n-v}}{\binom{N} {n}} , \quad \forall\, v=0, 1, 2, ..., min(n;N_A) \,\, (\#eq:eqpro23) 
$$

e assim fica tamb�m determinada a distribui��o exada de probabilidades do estimador $\widehat p$, que � a mesma $n_A$, com os valores poss�veis da propor��o amostral divididos pelo tamanho da amostra $n$.

Consequentemente tem-se que o valor esperado de unidades com o atributo de interesse na amostra e sua vari�ncia ser�o dados por:

$$
\displaystyle E_{AAS}(n_A)=n\frac{N_A}N=np \quad\text e\quad V_{AAS}(n_A)=np(1-p)\frac{N-n}{N-1} \,\, (\#eq:eqpro24)
$$

Para o estimador, $\widehat p=n_A/n$, da propor��o de unidades com o atributo de interesse na popula��o tem-se:

$$
\displaystyle E_{AAS}(\widehat p)=p \quad\text e\quad V_{AAS}(\widehat p)=\left(\frac1n-\frac1N\right)S^2_y\,\, (\#eq:eqpro25)
$$

## Intervalos de confian�a para propor��es na Amostragem Aleat�ria Simples

Foi visto que na *Amostragem Aleat�ria Simples*, tanto com ou sem reposi��o, s�o conhecidas as distribui��es exatas para o estimador $\widehat p$. Portanto, � poss�vel obter os limites inferior e superior para intervalos de confian�a para a propor��o $p$, com um n�vel de signific�ncia $\alpha$ fixado. Para isso, no caso de *AASC*, � necess�rio resolver o sistema de equa��es determinando os valores de $\widehat p_I$ e $\widehat p_S$ que satisfa�am:

$$
\begin{cases} 
\displaystyle \sum _{v=0}^{n_A} \binom {n}{v} \widehat p_S^v (1 - \widehat p_S)^{n-v} = \alpha / 2 
\\\\ 
\displaystyle \sum _{v=n_A}^n \binom {n}{v} \widehat p_I^v (1 - \widehat p_I)^{n-v} = \alpha / 2 (\#eq:eqpro26) 
\end{cases}
$$
No caso da *AAS*, o sistema a ser resolvido � baseado na distribui��o Hipergeom�trica como se segue:

$$
\begin{cases} 
\displaystyle \sum_ {v=0}^{n_A}\frac {\binom{N\widehat p_S}{v} \binom{N-N\widehat p_S} {n-v}}{\binom{N}{n}} = \alpha / 2
\\\\ 
\displaystyle \sum_ {v=n_A}^{n}\frac {\binom{N\widehat p_I}{v} \binom{N - N \widehat p_I} {n-v}} {\binom{N}{n}} = \alpha / 2 (\#eq:eqpro27) 
\end{cases}  
$$

Em ambos os casos $1 - \alpha$ � o *n�vel de confian�a* desejado. Por exemplo, para intervalos de 95% de confian�a, deve-se usar $\alpha= 0,05$.

A solu��o desses sistemas costumava ser trabalhosa, exigindo aplica��o de m�todos iterativos que consumiam quantidade razoavelmente grande de recursos computacionais. Atualmente, com o avan�o dos m�todos computacionais, esse problema pode facilmente ser resolvido, por exemplo, com o uso do R. Uma maneira � utilizar as fun��es *qbinom* e *qhyper* que podem calcular os quantis das distribui��es Binomial e Hipergeom�trica para $\alpha /2$ e $1 -\alpha /2$.

Al�m disso h� outros programas j� prontos facilmente utiliz�vies como, por exemplo, as fun��es *binconf* e *confCI* inclu�das, respectivamente nos pacotes *Hmisc* e *prevalence* do R. Essas fun��es estimam intervalos de confian�a para v�rios m�todos al�m do mostrado acima, como o da aproxima��o Normal, apresentado na pr�xima se��o, al�m de outras abordagens.
H�, tamb�m, no pacote *survey* uma fun��o espec�fica, *svyciprop*, para calcular intervalos de confian�a para propor��es. Uma caracter�stica interessante do pacote *survey* � que � poss�vel determinar a utiliza��o do fator de corre��o para popula��es finitas, quando a sele��o � sem reposi��o.

**(#exm:exmprop2)** Voltando ao exemplo da escola com $N=1.000$ alunos, suponha que foi selecionada uma amostra aleat�ria simples de tamanho $n=125$ e foi investigado o sexo de cada um desses alunos, sendo que 60 s�o do sexo feminino. Constuir um intervalo de aproximadamente 95% de confian�a para a propor��o de alunos do sexo feminino, utilizando os v�rios m�todos  da linguagem R sugeridos acima.



















