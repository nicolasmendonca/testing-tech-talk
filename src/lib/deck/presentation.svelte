<script lang="ts">
	import Slide from './slide.svelte'
	import Code from './code.svelte'

	import PorQueTesteamos from '../slides/PorQueTesteamos.svelte'
	import QuePasaSiSoloHacemosTestsManual from '../slides/QuePasaSiSoloHacemosTestsManual.svelte'
	import TestEstatico from '../slides/TestEstatico.svelte'
	import Heading from '../Heading.svelte'
	import TestUnitario from '../slides/TestUnitario.svelte'
	import TestDeIntegracion from '../slides/TestDeIntegracion.svelte'
	import TestEndToEnd from '../slides/TestEndToEnd.svelte'
</script>

<Slide>
	<p class="capitalize">Intro a Testing 👷‍♂️</p>
	<aside class="notes">
		<ol>
			<li>Hablo desde mi experiencia</li>
			<li>Tuve discusiones con gente a favor y en contra de testing</li>
			<li>Hay más tipos de testing de los que comunmente se hablan</li>
		</ol>
	</aside>
</Slide>

<PorQueTesteamos />
<QuePasaSiSoloHacemosTestsManual />

<Slide>
	<Heading>Que otras opciones hay? 🤷‍♂️</Heading>
</Slide>
<TestEstatico />
<TestUnitario />
<Slide>
	<Slide animate id="unit-vs-integration">
		<Heading>Unit vs Integration tests</Heading>
		<div class="flex justify-center">
			<img src="https://i.redd.it/9zf0asd0c3n51.gif" alt="" />
		</div>
	</Slide>
	<Slide animate id="unit-vs-integration">
		<Heading>Unit vs Integration tests</Heading>
		<div class="flex justify-center">
			<img src="https://i.stack.imgur.com/yHGn1.gif" alt="" />
		</div>
	</Slide>
	<Slide animate id="unit-vs-integration">
		<Heading>Unit vs Integration tests</Heading>
		<div class="flex justify-center">
			<img src="https://media.tenor.com/jeMFXFn8UA4AAAAC/integration-test-fail.gif" alt="" />
		</div>
	</Slide>
	<Slide animate id="unit-vs-integration">
		<Heading>Unit vs Integration tests</Heading>
		<div class="flex justify-center">
			<img
				src="https://www.maxpou.fr/7ab5a8d1ef6b5cd3164ae2913b99cc79/unit-vs-integration-test.gif"
				alt=""
			/>
		</div>
	</Slide>
</Slide>
<TestDeIntegracion />
<TestEndToEnd />

<Slide>
	<Code id="code">
		{`
			pnpm init
		`}
	</Code>
</Slide>

<Slide>
	<Code id="code">
		{`
			"js/ts.implicitProjectConfig.checkJs": true,
		`}
	</Code>
</Slide>

<Slide>
	<Slide animate>
		<p>Si quisieramos testear una simple funcion</p>
		<Code id="code" lines>
			{`
function sum(a, b) {
  return a + b;
}
		`}
		</Code>
	</Slide>
	<Slide animate>
		<p>Si queremos usar node:test</p>
		<Code id="code" lines>
			{`
import test from 'node:test'

function sum(a, b) {
  return a + b;
}

test('sum adds two numbers', () => {
  expect(sum(1, 2)).toBe(3);
})
		`}
		</Code>
	</Slide>
	<Slide animate>
		<p>Si queremos hacer nuesto propio testing framework</p>
		<Code id="code" lines>
			{`
function test(description, callback) {
  try {
    callback();
  } catch (e) {
    throw new Error(\`Test failed: "\${description}" \n\${e.message}\`);
  }
}

const assert = {
  strictEqual(actual, expected) {
    if (actual !== expected)
      throw new Error(
        \`Values are not equal. Expected: \${expected} - Received: \${actual}\`
      );
  },
};

function sum(a, b) {
  return a + b;
}

test("sum function works", () => {
  assert.strictEqual(sum(3, 2), 3);
});

		`}
		</Code>
	</Slide>
</Slide>

<Slide>
	<ul>
		<li><a href="https://jestjs.io/">Jest</a></li>
		<li><a href="https://vitest.dev/">Vitest</a></li>
		<li><a href="https://nodejs.org/api/test.html">node:test (v18)</a></li>
	</ul>
</Slide>
