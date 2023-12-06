<div class="grid-container">
	<ul class="grid">
		<li class="article-container">
			<article>
				<img
					src="https://images.unsplash.com/photo-1550098612-4838745601bf?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=M3wzMjM4NDZ8MHwxfHJhbmRvbXx8fHx8fHx8fDE2OTg3NTQ1ODh8&ixlib=rb-4.0.3&q=80&w=400"
					alt=""
				/>
				<div>
					<h3>Why all fossil fuels must decline rapidly to stay below 1.5C</h3>
					<p>
						Lorem ipsum dolor, sit amet consectetur adipisicing elit. Exercitationem, nihil
						explicabo adipisci iste saepe reiciendis.
					</p>
				</div>
			</article>
		</li>
		<li class="article-container">
			<article>
				<img
					src="https://images.unsplash.com/photo-1550098612-4838745601bf?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=M3wzMjM4NDZ8MHwxfHJhbmRvbXx8fHx8fHx8fDE2OTg3NTQ1ODh8&ixlib=rb-4.0.3&q=80&w=400"
					alt=""
				/>
				<div>
					<h3>Why all fossil fuels must decline rapidly to stay below 1.5C</h3>
					<p>
						Lorem ipsum dolor, sit amet consectetur adipisicing elit. Exercitationem, nihil
						explicabo adipisci iste saepe reiciendis.
					</p>
				</div>
			</article>
		</li>
		<li class="article-container">
			<article>
				<img
					src="https://images.unsplash.com/photo-1550098612-4838745601bf?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=M3wzMjM4NDZ8MHwxfHJhbmRvbXx8fHx8fHx8fDE2OTg3NTQ1ODh8&ixlib=rb-4.0.3&q=80&w=400"
					alt=""
				/>
				<div>
					<h3>Why all fossil fuels must decline rapidly to stay below 1.5C</h3>
					<p>
						Lorem ipsum dolor, sit amet consectetur adipisicing elit. Exercitationem, nihil
						explicabo adipisci iste saepe reiciendis.
					</p>
				</div>
			</article>
		</li>
	</ul>
</div>

<style>
	*,
	*::before,
	*::after {
		box-sizing: border-box;
	}

	body {
		margin: 0;
		min-height: 100vh;
		padding: 1rem;
		background: lavender;
		font-family: Montserrat, sans-serif;
		line-height: 1.3;
	}

	img {
		display: block;
		width: 100%;
		aspect-ratio: 3 / 2;
		object-fit: cover;
	}

	.grid {
		width: 100%;
		display: grid;
		gap: 2rem;
	}
	.article-container {
		min-width: min(100%, 400px);
		max-width: 1200px;
		overflow: hidden;
		resize: both;
		border: 1px solid #eee;
		padding: 1rem;
		background-color: #c4c4e1;
	}

	.article-container {
		container-name: article;
		container-type: inline-size;
	}

	article {
		display: grid;
		gap: 1rem;
	}

	@container article (inline-size > 500px) {
		article {
			grid-template-columns: 1fr 2fr;
		}
	}

	@container article (inline-size > 800px) {
		article {
			grid-template-columns: 1fr 1fr;
			gap: 2rem;
			font-size: 1.2rem;
		}

		h3 {
			font-size: 2rem;
		}
	}

	.grid-container {
		width: 100%;
		container-name: layout;
		container-type: inline-size;
	}

	@container layout (inline-size > 1000px) {
		.grid {
			grid-template-columns: repeat(4, 1fr);
		}
		.article-container:first-child {
			grid-column: span 4;
		}

		.article-container:nth-child(2),
		.article-container:nth-child(3) {
			grid-column: span 2;
		}
	}
</style>
