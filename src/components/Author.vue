<template>
	<div class="author">

		<g-image alt="Author image" class="author__image" src="~/assets/images/profile.jpg" width="180" height="180" blur="5" />

		<h1 v-if="showTitle" class="author__site-title">
			All about Food!!!
		</h1>

		<p class="author__intro">
			Delicious and authentic food around the world!
		</p>

		<p class="author__links">
			<a href="https://github.com/6110110144/gridsome">GitHub</a>
		</p>

	</div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<script>
export default {
	props: ['showTitle']
}
</script>

<style lang="scss">
.author {
	margin: 0 auto;
	max-width: 500px;
	text-align: center;
	padding: calc(var(--space) / 2) 0;

	&__image {
		border-radius: 100%;
		width: 90px;
		height: 90px;
		margin-bottom: 1em;
	}

	&__intro {
		opacity: .8;
	}

	&__site-title {
		font-size: 1.5em;
	}

	&__links {
		margin-top: -.5em;
		a {
			margin: 0 .5em;
		}
	}
}
</style>
