
#teatro_svjotlo

začátek pro práci se signálem:
- AudioDeviceIn - vstup
- AudioSpect - spektrum od 0 dál
- Analyze - použitelnější signál

- Trail - vizualizace

pro další zpracování (usable data)
- EnvelopeMath trick:
	- signál z Analyze do Envelope a Math, z Envelope do Math
	- Envelope - Envelope Width 10
	- Math - combine CHOPS with Divide, 0 analyze, 1 envelop
- Trigger - vstup z Math, udělá boolovskej signál
	- Sustain - všechno krom Sustain Level na 0, Level na 1
	- Attack - všechno krom Peak Level na 0, Level na 1
	- Trigger - Threshold = tolerance (0.7)

- Null - prázná node, HUB
	- z Triggeru

