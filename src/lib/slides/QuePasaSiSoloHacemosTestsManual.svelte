<script>
	import Heading from '../Heading.svelte'
	import Slide from '../deck/slide.svelte'
</script>

<Slide>
	<Slide animate id="tipos-de-test">
		<div class="font-sans h-full flex-col justify-evenly">
			<Heading>Qué pasa si sólo hacemos test manual? ✋</Heading>
		</div>
	</Slide>
	<Slide animate id="tipos-de-test">
		<div class="font-sans h-full flex-col justify-evenly">
			<Heading>Qué pasa si sólo hacemos test manual? ✋</Heading>

			<div class="text-left text-base">
				<p class="text-cyan-500 font-semibold">✅ Ventajas</p>
				<ol class="text-base">
					<li>Verifica que nuestras features cumplen los requisitos en un entorno real.</li>
					<li>Entry level. Podemos delegar esta tarea.</li>
					<li>El tiempo de verificación es menor, por lo que se considera "barato".</li>
				</ol>
			</div>
		</div>
		<aside class="notes">
			<ol>
				<li>
					En definitiva el único que puede determinar si una feature funciona es el usuario final.
				</li>
				<li>No hace falta prácticamente preparación técnica para poder realizar un test manual</li>
			</ol>
		</aside>
	</Slide>
	<Slide animate id="tipos-de-test">
		<div class="font-sans h-full flex-col justify-evenly">
			<Heading>Qué pasa si sólo hacemos test manual? ✋</Heading>

			<div class="text-left text-base">
				<p class="text-cyan-500 font-semibold">❌ Desventajas</p>
				<ol class="text-base">
					<li>
						Debemos "recordar" qué partes del código afectan a qué funcionalidades y qué pantallas.
					</li>
					<li>
						Esa tarea nos convierte en los únicos "guardianes" de la feature. Tomamos una
						responsabilidad personal de un producto que nos excede.
					</li>
					<li>
						<strong class="text-purple-400">Tiene un costo lineal 📉</strong>. Vamos a tener que
						estar corroborando si la feature funciona por cada cambio durante todo el ciclo de vida
						del proyecto.
					</li>
				</ol>
			</div>
		</div>

		<aside class="notes">
			<ol>
				<li>
					Esa responsabilidad nos convierte en "dueños" de la feature. Por lo cual sómos los únicos
					que reconoceríamos un potencial problema durante code review. Somos los únicos que
					podríamos "atajar" un problema durante code review
				</li>
				<li>
					Nosotros no venimos incluidos con el producto ni nos casamos con el mismo. Lo tenemos que
					soltar.
				</li>
				<li>
					Aca entra el concepto de "costo de un test", que en el caso de test manual implica el
					sueldo del tester. El costo de oportunidad de su tiempo. El tiempo que esta gastando
					testeando una feature lo esta perdiendo en hacer otra cosa. Hay un sacrificio lineal
				</li>
			</ol>
		</aside>
	</Slide>
</Slide>
