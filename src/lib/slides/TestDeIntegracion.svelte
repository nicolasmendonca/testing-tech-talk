<script>
	import Heading from '../Heading.svelte'
	import Slide from '../deck/slide.svelte'
</script>

<Slide>
	<Slide animate id="test-integracion">
		<Heading>Test de Integración 🧩</Heading>
		<div class="text-left text-base font-sans">
			<p class="text-purple-400 font-semibold">
				Es aquel que verifica la integración entre varios componentes o módulos.
			</p>
			<p>Ejemplos:</p>
			<ul>
				<li>Tests de componentes de react <b>a nivel de página</b></li>
				<li>Tests de backend a nivel <b>endpoints y respuestas</b></li>
			</ul>
			<p>
				Es el caso de <a href="https://testing-library.com/docs/react-testing-library/intro/"
					>React Testing Library</a
				>
				o de <a href="https://www.npmjs.com/package/supertest">Supertest</a>
			</p>
		</div>
	</Slide>
	<Slide animate id="test-integracion">
		<Heading>Test de Integración 🧩</Heading>
		<div class="text-left text-base font-sans">
			<p class="text-cyan-500 font-semibold">✅ Ventajas</p>
			<ol>
				<li>
					Consigue detectar una cantidad mayor de bugs, al estar más alejado de la implementación
					del código.
				</li>
				<li>Sigue permitiendo mockear los módulos usados</li>
			</ol>
		</div>
	</Slide>
	<Slide animate id="test-integracion">
		<Heading>Test de Integración 🧩</Heading>
		<div class="text-left text-base font-sans">
			<p class="text-cyan-500 font-semibold">❌ Desventajas</p>
			<ol>
				<li>
					Al estar más desacoplados de la implementación, no son específicos para detectar donde
					está la falla
				</li>
				<li>Son más costosos de correr a nivel de performance</li>
			</ol>
		</div>
	</Slide>
</Slide>
