<template>
	<strong>№1. Дан абзац и кнопка. Сделайте так, чтобы абзац тогглился по нажатию на кнопку.</strong>
	<button @click="toggleVisibility">Тогглить абзац</button>
	<p v-show="isVisible">Абзац для тогглинга</p>
	<ul>
  <li><strong>№2. Отличия директив v-show и v-if:</strong>
    <ul>
      <li><strong>v-if</strong> выполняет условную отрисовку элемента. Если условие ложно, элемент не отрисовывается в DOM, и события не активны.</li>
      <li><strong>v-show</strong> всегда отрисовывает элемент, скрывая его с помощью CSS (через свойство `display: none`). События остаются привязанными, но элемент не виден.</li>
    </ul>
  </li>
  
  <li><strong>№3. Когда лучше использовать директиву v-show, а когда v-if:</strong>
    <ul>
      <li><strong>v-show</strong> лучше использовать, когда нужно часто переключать видимость элемента, так как переключение состояния быстрее (изменяется только CSS).</li>
      <li><strong>v-if</strong> лучше использовать, когда элемент должен быть создан и уничтожен в зависимости от условия, особенно если условие меняется редко.</li>
    </ul>
  </li>
  
  <li><strong>№4. Ограничения директивы v-show:</strong>
    <ul>
      <li>Директиву <strong>v-show</strong> нельзя использовать на элементе <code>&lt;template&gt;</code>.</li>
      <li>Она не работает с <strong>v-else</strong>, то есть нельзя использовать их вместе для одного элемента.</li>
    </ul>
  </li>
</ul>

</template>

<script>
export default {
	data() {
		return {
			isVisible: true
		}
	},
	methods: {
		toggleVisibility() {
			this.isVisible = !this.isVisible;
		}
	}
}
</script>
