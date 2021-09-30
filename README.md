# servovalve
Um projeto de uma servo válvula robusta
Copyright <2021> <Juliano Passaretti Filho juliano.passaretti@gmail.com>

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the
 Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the
 Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A
PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Uma válvula de 3 vias controlada por servo motor.

	A análise em fluxo é um procedimento de automação de procedimentos analíticos, no qual a amostra é introduzida em um fluído carregador que é trasportada até o detector. O fluxo contínuo pode auxiliar a separação de fases, formação de produtos de interesse em reações químicas controladas e diluição ou pré-concentração de analitos de interesse[1]–[3]⁠. Neste contexto, controlar e direcionar o encontro ou a separação de fluídos líquidos ou gasosos é uma necessidade real dentro de processos analíticos em fluxo. 
	Existem diversos tipos para o controle sistemas em fluxo com válvulas para o controle de fluídos como redutoras de pressão, purgadores de vapor e controle e desvio(bypass)[4]⁠. A válvula do tipo bypass são interessantes para o controle de fluídos, para o prenchimento de alças de amostragem, encontro do fluxo de reagente e amostra para derivação, passagem por bobinas de mistura de líquidos ou gases e direcionamento dos produtos da reação em fluxo para detectores[4], [5]⁠.
	O uso de dispositivos eletrônicos, como as válvulas solenoide, válvulas rotatórias e bombas solenoide em sistemas de análises em fluxo, permitiu que as soluções pudessem ser gerenciadas de forma eficiente, controlando os tempos e a sequência de adição[6]⁠. 
	A válvula de 3 vias, é um dos modelos mais simples empregado para esse tipo de procedimentos de controle bypass em fluxo[5]⁠. Essas válvulas tem um formato em Y ou T para promover a mistura, ou interrupção de fluxo de fluidos. A válvula tipo T promove diferentes tipos de encontros com diferentes reagentes e a mudança de posição com uma rotação de 90º permite   conectar até 3 reservatórios simuntamente ou interrupção de conexão  com uma rotação de 45º  (Figura 1). 
Figura 1: Posições de uma válvula bypass conectado simultaneamente 3 reservatórios com rotações de 90° ou interrupção de conexão com rotação de 45°.

	As válvulas de 3 vias podem ser usadas para sistemas em fluxo, para o controle de transporte de líquidos e gases. O controle de fluxo e conexão, com até 3 diferentes reservatórios, depende de  uma movimentação mecânica que transmita uma rotação para reservatório em T da válvula. Esse movimento pode ser executado com boa precisão usando servos motores[7], [8]⁠⁠. 
	Servo motores são motores de corrente contínua com circuitos de feedback embutidos para que as posições do eixo possam ser controladas com precisão. Esses motores têm três terminais: alimentação, aterramento e controle. O terminal de controle é conduzido com forma de onda PWM (Pulse Width Modulation), geralmente com um período de 20ms (50 Hz) e ângulos de posição entre 0 e 180° [6]⁠.	Válvulas controlados por servo motores podem ser usadas para controlar de sistemas de comutação para gases ou líquidos[7]–[10]⁠.
	Existem projetos opensource que usam válvulas de 3 vias hospitalares controladas com servo motores, usando impressão 3d ou suportes de baixo custo de acrílico[11]–[13]⁠. Entretanto esses projetos são manufaturados com materiais frágeis que podem comprometer o uso contínuo da válvula de 3 vias. Neste trabalho foi desenvolvido um suporte metálico com elevada resistência mecânica para o controle de uma válvula de 3 vias hospitalar, diminuindo a quantidade de componentes frágeis do sistema, e propiciando apenas troca da válvula ou o motor aumentando facilitando o uso contínuo do comutador.

Procedimentos	

	O desenvolvimento da válvula servo controlada, foi pautada escolhendo materiais mais rígidos para diminuir o desgaste e troca de componentes da estrutura do sistema e foi divido em a) Componentes estruturais eletromecânicos; b) Montagem do sistema eletromecânico; e c) Controle de servo motor com o Arduino Uno firmware e software de controle.

Componentes estruturais eletromecânicos

	Para o desenvolvimento do sistema foi usado um Servo Motor Mg995, 9,4 kgf cm, 4,8 V (SVM)(Towerpro, China). A válvula empregada para o comutador em fluxo foi uma torneira 3 vias (Luer Lock), polipropileno e estéril (VT) (Descarpak, Brasil). Para suportar a válvula foi utilizado um Perfil Alumínio U 12 x 12 x 40 mm (PU-A) e para girar a torneira da válvula foi usada um Perfil Alumínio U 12 x 12 x 20 mm (PU-B). Todo o sistema foi montada em um suporte em formato L projetado usando o software de desenho paramétrico FreeCAD V. 0.19.24276 (GNU - GPL)[14]⁠. O suporte foi projetado com dimensões 2d de 40 x 100 mm com cortes e ponto de dobra indicado (fp) na Figura 2-a , resultando em um suporte em formando um L 40 x 35 x 65 mm (SL) (Figura 2-b), a peça foi produzida em aço-carbono 2 mm e contada a laser na empresa Perfban Soluções em Corte e Dobra (Perfban, Brasil). A tabela 1 representa todos os componentes, incluindo o conjunto parafusos, porcas e arruelas, utilizados na montagem e os respectivos preços no mercado nacional em 2021.

Figura 2. Suporte L 40 x 35 x 65 mm (SL)  a) Pontos de corte e dobra da chapa de aço-carbono .  2Mm; b) Representação do modelo tridimensional 3d(SL).





Montagem do sistema eletromecânico

	Na Figura 3 estão representados os componentes eletromecânicos montados em 2 peças suporte SL. Na parte superior (SL1) foi fixado o motor SVM com parafusos P-A, e ligado ao eixo de transmissão de movimento de um suporte circular ao perfil PU-B, fixado com parafusos P-B e P-D. A parte superior da válvula VT foi cortada e fixada ao perfil PU-B com parafuso P-C. Na parte inferior o perfil PU-A foi fixado com parafusos P-A a segunda peça suporte (SL2), O perfil PU-A, foi cortado com uma janela de 10 mm no centro, para o encaixe da válvula VT fixada no servo motor. Os suportes inferior e superior foram fixados com o parafuso P-E.

Figura 3.Válvula VT controlada por servo motor; SMV – Sevo motor; SL1- Suporte L superior. SL2 -Suporte inferior; VT – Válvula de 3 vias; PU-B – perfil U fixada ao eixo de VT; PU-A - perfil U encaixada a válvula VT e fixada em SL2.

Controle de servo motor com o Arduino Uno, firmware e software de controle

	O controle do servo motor (SVM) foi feito usando um Arduino Uno (Arduino, Itália) conforme representado no diagrama da Figura 4. O Arduino Uno (Figura 4-a) está ligado ao servo motor (SVM) (Figura 4-b) na porta digital 9. O servo motor (SVM) foi alimentado com uma fonte 5 volts, 10 A, 50-60 HZ (CAI, China) (Figura 4-c).
Figura 4: Diagrama do SVM ligado ao microcontrolador; a) Arduino UNO; b) Servo motor SVM e c) fonte de alimentação 5 V.
	
	O código do firmware está contido no anexo Tabela 1A, desenvolvido em C e C++ e gravado com Arduino IDE 1.8.16 (GNU-GPL). O código usa as bibliotecas arduino servo 1.1.8 (GNU-GPL) para o controle PWM do motor, e Software Serial (Someserial 1..12) (GNU-GPL) para modificar a posição da válvula (aberto, fechado ou troca de fluxo).
Referências
 
[1]	J. Ruzicka, G. D. Marshall, and G. D. Christian, “Variable flow rates and a sinusoidal flow pump for flow injection analysis,” Anal. Chem., vol. 62, no. 17, pp. 1861–1866, 1990.
[2]	J. Ruzicka and G. D. Marshall, “Sequential injection: a new concept for chemical sensors, process analysis and laboratory assays,” Anal. Chim. Acta, vol. 237, pp. 329–343, 1990.
[3]	B. F. dos Reis, “Análise química por injeção em fluxo: vinte anos de desenvolvimento,” Quim. Nova, vol. 19, no. 1, pp. 51–58, 1996.
[4]	M. Guidi, P. H. Seeberger, and K. Gilmore, “How to approach flow chemistry,” Chem. Soc. Rev., vol. 49, no. 24, pp. 8910–8932, 2020, doi: 10.1039/c9cs00832b.
[5]	S. D. Kolev and I. D. McKelvie, “Advances in flow injection analysis and related techniques,” 2008.
[6]	M. Y. Kamogawa and J. C. Miranda, “Uso de hardware de código fonte aberto ‘Arduino’ para acionamento de dispositivo solenoide em sistemas de análises em fluxo,” Quim. Nova, vol. 36, no. 8, pp. 1232–1235, 2013, doi: 10.1590/S0100-40422013000800023.
[7]	J. Prieto Barranco and C. Goberna Selma, “Servo-Positioner for a Micro-Regulating Valve,” 8740181, 2005.
[8]	Moon Hee-soo, “3-way valve system using servo motor,” KR20110019455A, 2009.
[9]	L. Holder-Pearson, T. Lerios, and J. G. Chase, “Physiologic-Range Three/Two-way Valve for Respiratory Circuits,” HardwareX, p. e00234, Sep. 2021, doi: 10.1016/j.ohx.2021.e00234.
[10]	G. Yan, Z. Jin, T. Zhang, and P. Zhao, “Position Control Study on Pump-Controlled Servomotor for Steam Control Valve,” Processes, vol. 9, no. 2, p. 221, Jan. 2021, doi: 10.3390/pr9020221.
[11]	H. as Águas, “Válvula de 3 vias Controlada por Servomotor,” 2021. https://www.c2o.pro.br/hackaguas/apa.html (accessed Sep. 28, 2021).
[12]	Thingiverse, “Three way valve servo controller,” 2020. https://www.thingiverse.com/thing:4632273 (accessed Feb. 28, 2021).
[13]	T. Pulsar, “Adding an actuated flow selector valve to our syringe pump,” 2015. https://www.thepulsar.be/article/adding-an-actuated-flow-selector-valve-to-our-syringe-pump/ (accessed Sep. 28, 2021).
[14]	F. Machado, N. Malpica, and S. Borromeo, “Parametric CAD modeling for open source scientific hardware: Comparing OpenSCAD and FreeCAD Python scripts,” PLoS One, vol. 14, no. 12, p. e0225795, 2019.
 
 
