<script>
	import Heading from '../Heading.svelte'
	import Slide from '../deck/slide.svelte'
</script>

<Slide>
	<Slide animate id="test-estatico">
		<Heading>Test Estatico ✍️</Heading>
		<div class="text-base font-sans">
			<p>
				Se refiere a todo tipo de test que pueda correrse <strong
					class="font-semibold text-purple-400">sin ejecutar nuestro código</strong
				>.
			</p>
			<ul>
				<li><a href="https://www.typescriptlang.org/">Typescript</a></li>
				<li><a href="https://eslint.org/">Eslint</a></li>
				<li>
					Herramientas de análisis estático (ej: <a
						href="https://www.sonarsource.com/products/sonarqube/">Sonarqube</a
					>, <a href="https://codeclimate.com/">Code Climate</a>,
					<a href="https://www.codacy.com/">Codacy</a>)
				</li>
			</ul>
		</div>
	</Slide>
	<Slide animate id="test-estatico">
		<Heading>Test Estatico ✍️</Heading>
		<div class="text-left text-base font-sans">
			<p class="text-cyan-500 font-semibold">✅ Ventajas</p>
			<ol>
				<li>El feedback loop es instantáneo</li>
				<li>No requiere procesamiento intenso</li>
				<li>Es preciso al identificar el problema</li>
			</ol>
		</div>
		<aside class="notes">
			<ul>
				<li>
					No necesitamos salir del editor para saber que el código tiene fallas o que la feature no
					va a funcionar
				</li>
				<li>
					El editor lo corre continuamente. Lo podemos correr en un pre-commit hook, un pre-push, en
					un pull request, o incluso al deployar
				</li>
				<li>
					En el caso de TS nuestras features son explícitas con lo que necesitan para funcionar y lo
					que retornan
				</li>
				<li>Sabemos exactamente cuál es y donde ocurre</li>
			</ul>
		</aside>
	</Slide>
	<Slide animate id="test-estatico">
		<Heading>Test Estatico ✍️</Heading>
		<div class="text-left text-base font-sans">
			<p class="text-cyan-500 font-semibold">❌ Desventajas</p>
			<ol>
				<li>Requiere un setup inicial</li>
				<li>Requiere un consenso en el equipo</li>
				<li>Impacta en el tiempo de desarrollo del feature</li>
			</ol>
		</div>
		<aside class="notes">
			<ul>
				<li>Lo tenemos que instalar y configurar</li>
				<li>
					Tanto con typescript como con eslint nos tenemos que poner de acuerdo con cuáles son las
					reglas que queremos adoptar.
				</li>
				<li>
					Nuestro tiempo de desarrollo aumenta, pero una feature concluída está más asegurada.
				</li>
			</ul>
		</aside>
	</Slide>
</Slide>
