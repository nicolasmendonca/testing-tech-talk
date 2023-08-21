<script>
	import Heading from '../Heading.svelte'
	import Slide from '../deck/slide.svelte'
</script>

<Slide>
	<Slide animate id="test-integracion">
		<Heading>Test de Integración 🧩</Heading>
		<div class="text-left text-base font-sans">
			<p class="text-purple-400 font-semibold">
				Es aquel que verifica a nivel de implementación que nuestro código se comporta como nosotros
				esperamos.
			</p>
			<p>Ejemplos:</p>
			<ul>
				<li>Si le paso ciertos valores a una funcion espero que me devuelva cierto resultado</li>
				<li>
					Espero que esta función llame a <code
						class="border rounded-md text-sm text-orange-400 px-1">window.fetch</code
					>
				</li>
				<li>Espero que cierto componente reciba cierta prop</li>
			</ul>
		</div>
		<aside class="notes">
			A partir de aca, los tests automatizados requieren de una programación. Vamos a tener que
			estar escribiendo código para la funcionalidad por un lado, y para el test por el otro
		</aside>
	</Slide>
	<Slide animate id="test-integracion">
		<Heading>Test de Integración 🧩</Heading>
		<div class="text-left text-base font-sans">
			<p class="text-cyan-500 font-semibold">✅ Ventajas</p>
			<ol>
				<li>
					Nos permite fácilmente montar escenarios complicados para verificar que el código resuelva
					las cosas correctamente
				</li>
				<li>Corren en un ambiente aislado</li>
				<li>Son muy performantes</li>
				<li>
					Mejores aplicaciones
					<ul>
						<li>Cuando hacemos una lib que queremos compartir con los demas</li>
						<li>Cuando tenemos código que es dificil de llevar a un entorno real</li>
					</ul>
				</li>
			</ol>
		</div>
		<aside class="notes">
			<p>
				A partir de aca, los tests automatizados requieren de una programación. Vamos a tener que
				estar escribiendo código para la funcionalidad por un lado, y para el test por el otro
			</p>

			<ol>
				<li>
					Por ejemplo: si tengo una función que formatea currencies, y quiero saber cómo se comporta
					cuando recibe un valor nulo, o negativo, puedo saber exactamente el resultado de esos edge
					cases
				</li>
				<li>
					No necesitan que nosotros creemos un usuario, iniciemos sesion, etc. Nada en el ambiente
					va a modificar el comportamiento de mi test y mi función.
				</li>
			</ol>
		</aside>
	</Slide>
	<Slide animate id="test-integracion">
		<Heading>Test de Integración 🧩</Heading>
		<div class="text-left text-base font-sans">
			<p class="text-cyan-500 font-semibold">❌ Desventajas</p>
			<ol>
				<li>Al estar acoplados por diseño a la implementación, no toleran refactors.</li>
				<li>
					No demuestran realmente que nuestra feature va a funcionarle al usuario. Sólo nos sirve a
					nosotros al momento de desarrollar.
				</li>
			</ol>
		</div>
		<aside class="notes">
			<ol>
				<li>
					Si nosotros cambiamos el código fuente, tendremos que reescribir nuestros tests. Ejemplo
					enzyme.
				</li>
				<li>
					Aca es donde mucha gente se frustra con los tests. Qué sentido tiene escribir unit tests
					después de escribir mi código si lo probé de alguna forma manualmente.
				</li>
			</ol>
		</aside>
	</Slide>
</Slide>
