<template>
	<a :href="'https://github.com/' + name" target="_blank">
		<div id="contributor">
			<img :src="imageURL" :alt="name" />
			<span>{{ name }}</span>
		</div>
	</a>
</template>
<script>
export default {
	name: 'Contributor',
	introduction: 'Render each contributor in the list of contributors in the component page.',
	description: `
The Contributor component renders an image and the name of the contributor.
`,
	token: `
<div id="contributor">
	<img :src="imageURL" :alt="name" />
	<span>{{ name }}</span>
</div>
`,
	props: {
		imageURL: {
			type: String,
			required: true,
			default: '',
			note: 'Circular icon of the contributor.'
		},
		name: {
			type: String,
			required: true,
			default: '',
			note: 'Name of the contributor.'
		}
	}
};
</script>
<style lang="scss" scoped>
#contributor {
	display: flex;
	flex-direction: column;
	align-items: center;
	margin: 10px;

	img {
		margin: 10px;
		border-radius: 50%;
		max-height: 40px;
	}

	span {
		text-align: center;
		color: #000;
	}
	span:active, span:visited {
		color: #000;
		text-decoration: none;
	}
}
</style>
