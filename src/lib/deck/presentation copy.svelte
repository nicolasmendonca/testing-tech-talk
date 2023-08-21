<script lang="ts">
	import Slide from './slide.svelte'
	import Code from './code.svelte'
	import Markdown from './markdown.svelte'
</script>

<Slide>
	<p class="capitalize">Svelte deck 🔥</p>
</Slide>

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

<Slide>
	<Slide>
		<p class="capitalize">Vertical slide 1</p>
	</Slide>
	<Slide>
		<p class="capitalize">Vertical slide 2</p>
	</Slide>
</Slide>

<Slide id="animate" animate>
	<p class="capitalize">Animate elements</p>
</Slide>

<Slide id="animate" animate>
	<p class="capitalize">Animate elements</p>
	<p class="capitalize">Across slides</p>
</Slide>

<Slide id="list" animate>
	<ul>
		<li>React</li>
		<li>Solid</li>
		<li>Svelte</li>
		<li>Vue</li>
	</ul>
</Slide>

<Slide id="list" animate>
	<ul>
		<li>Svelte</li>
		<li>React</li>
		<li>Solid</li>
		<li>Vue</li>
	</ul>
</Slide>

<Slide id="list" animate>
	<ul>
		<li>Svelte ❤️</li>
		<li>React</li>
		<li>Solid</li>
		<li>Vue</li>
	</ul>
</Slide>

<Slide>
	<p class="capitalize">Code Blocks</p>
</Slide>

<Slide animate>
	<Code id="code" lines="1|3">
		{`
			<Slide animate>
				<!-- .. -->
			</Slide>
		`}
	</Code>
</Slide>

<Slide animate>
	<Code id="code" lines="2|4">
		{`
			<Slide animate>
				<Code lines>
					<!-- ... -->
				</Code>
			</Slide>
		`}
	</Code>
</Slide>

<Slide animate>
	<Code id="code" lines="3-5|1-7">
		{`
			<Slide animate>
				<Code lines>
					{code\`
						...
					\`}
				</Code>
			</Slide>
		`}
	</Code>
</Slide>

<Slide id="boxes" animate>
	<p class="capitalize">Cool transitions</p>
	<div class="flex gap-2 place-content-center">
		<div data-id="box-1" class="w-[100px] h-[100px] bg-gray-400" />
		<div data-id="box-2" class="w-[100px] h-[100px] bg-gray-400" />
		<div data-id="box-3" class="w-[100px] h-[100px] bg-gray-400" />
	</div>
</Slide>

<Slide id="boxes" animate>
	<p class="capitalize">Moving boxes</p>
	<div class="flex gap-2 place-content-center">
		<div data-id="box-1" class="w-[200px] h-[200px] bg-red-400" />
		<div data-id="box-2" class="w-[200px] h-[200px] bg-green-400" />
		<div data-id="box-3" class="w-[200px] h-[200px] bg-blue-400" />
	</div>
	<p class="capitalize">Cool transitions</p>
</Slide>

<Slide id="boxes" animate>
	<p>Moving boxes</p>
	<div class="flex gap-2 place-content-center">
		<div data-id="box-1" class="w-[200px] h-[200px] bg-gray-400" />
		<img src="https://i.giphy.com/media/ToMjGpnXBTw7vnokxhu/giphy.webp" alt="Whoa" />
		<div data-id="box-3" class="w-[200px] h-[200px] bg-gray-400" />
	</div>
	<p>Whoa!</p>
</Slide>

<Markdown>
	{`
		## Markdown ❤️
		You can use **HTML** or **Markdown** for slides.
	`}
</Markdown>

<Markdown name="example.md" external />

<Slide>
	<p class="capitalize">Get started 😎</p>
</Slide>
