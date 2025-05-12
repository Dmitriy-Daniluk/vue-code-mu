<template>
	<table>
		<thead>
			<tr>
				<th>Name</th>
				<th>Surname</th>
				<th>Actions</th>
			</tr>
		</thead>
		<tbody>
			<tr v-for="user in users" :key="user.id">
				<td>
					<template v-if="!user.isEdit">
						{{ user.name }}
					</template>
					<template v-else>
						<input v-model="user.name" />
					</template>
				</td>
				<td>
					<template v-if="!user.isEdit">
						{{ user.surn }}
					</template>
					<template v-else>
						<input v-model="user.surn" />
					</template>
				</td>
				<td>
					<template v-if="!user.isEdit">
						<button @click="edit(user)">Edit</button>
					</template>
					<template v-else>
						<button @click="save(user)">Save</button>
					</template>
				</td>
			</tr>
		</tbody>
	</table>
</template>

<script>
export default {
	data() {
		return {
			users: [
				{ id: 1, name: 'name1', surn: 'surn1', isEdit: false },
				{ id: 2, name: 'name2', surn: 'surn2', isEdit: false },
				{ id: 3, name: 'name3', surn: 'surn3', isEdit: false },
			],
		};
	},
	methods: {
		edit(user) {
			user.isEdit = true;
		},
		save(user) {
			user.isEdit = false;
		},
	},
};
</script>
