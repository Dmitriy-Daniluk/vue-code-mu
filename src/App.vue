<template>
	<!-- Ссылка на страницы -->
	<ul>
		<template v-for="href in hrefs" :key="href.href">
			<li><a :href="href.href">{{ href.text }}</a></li>
		</template>
	</ul>

	<!-- Таблица с продуктами -->
	<table>
		<template v-for="product in products" :key="product.name">
			<tr>
				<td>{{ product.name }}</td>
				<td>{{ product.price }}</td>
				<td>{{ product.quantity }}</td>
			</tr>
		</template>
	</table>
</template>

<script>
export default {
	data() {
		return {
			hrefs: [
				{ href: '1.html', text: 'text1' },
				{ href: '2.html', text: 'text2' },
				{ href: '3.html', text: 'text3' },
			],
			products: [
				{ name: 'product1', price: 100, quantity: 5 },
				{ name: 'product2', price: 200, quantity: 4 },
				{ name: 'product3', price: 300, quantity: 3 },
			],
		};
	},
};
</script>
