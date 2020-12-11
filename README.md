# Vaja3-casovno-sprozena-ADC-pretvorba-s-STM32F0-Discovery
2b)	Glede na vašo razvojno ploščico in razširitveno vezje z tipkami ter potenciometri, izberite ustrezni analogni vhod. Kateri pin je to? 
PC0
2e)	Glede na potenciometer na vaši ploščici izberite-obkljukajte ustrezni kanal/pin. Na zaslonu se vam mora usterzno pobarvati izbrani pin v zeleno barvo. Kaj se izpiše poleg pina? 
ADC_IN10
2i)	V Clock Configuration spremenimo APB1 Timer clock (MHz) na 16 MHz (pritisnemo ENTER). Kaj opazite? 
Urni takt se najprej spremeni na 96 MHz, če postopek ponovimo se postavi na 16 MHz ter spremeni še par ostalih urnih taktov.
2l)	V razdelku TIM1, pod Counter Settings, bi radi časovniku spremenili frekvenco na 1 kHz, zato moramo frekvenco ABP1 Timer Clock preskalirati v polju Prescaler (PSC – 16 bit value). Koliko znaša ta vrednost? 
16.000
3f)	Branje vrednosti želimo prikazati z utripanjem zelene LED diode na STM32f0 ploščici. Uporabite metodo TogglePin iz HAL knjižnice in zapišite ukaz:
HAL_GPIO_TogglePin(GPIOC, GPIO_PIN_9);

Komentar:
Vrednost potenciometra preberemo s pomočjo timerjev, ki določajo kdaj bo STM prebral vrednost. To vrednost shranimo kot osem bitni intiger in ga lahko opazujemo s pomočjo debuga.
