<script>
	// Educational resources
	let resources = [
		{description: "Collated resources on Black Lives Matter and anti-racism", link: "https://blacklivesmatters.carrd.co/#educate"},
		{description: "8 Ways to Make Real Progress on Tech's Diversity Problem", link: "https://www.fastcompany.com/40528096/8-ways-to-make-real-progress-on-techs-diversity-problem"},
		{description: "A view into being a Black employee at a tech company", link: "https://medium.com/@marksluckie/what-it-s-actually-like-to-be-a-black-employee-at-a-tech-company-e32bb222818b"},
		{description: "Report on Black and Hispanic underrepresentation in tech", link: "https://www.brookings.edu/research/black-and-hispanic-underrepresentation-in-tech-its-time-to-change-the-equation/"}
	]

	// JSON object that gets mapped to fund items
	let funds = [
		{ title: "NAACP Legal Defense Fund", 
		summary: "The NAACP Legal Defense Fund is a non-profit organization that seeks \"structural changes to expand democracy, eliminate disparities, and achieve racial justice in a society that fulfills the promise of equality for all Americans.\"", 
		url: "https://www.naacpldf.org", 
		buttonText: "Donate to the NAACP LDF"},
		{ title: "Campaign Zero", 
		summary: "Non-profit seeking data-driven policy solutions from local, state, and federal lawmakers to take immediate action to end police violence.", 
		url: "https://www.joincampaignzero.org/", 
		buttonText: "Donate to Campaign Zero"},
		{ title: "Thurgood Marshall College Fund", 
		summary: "Non-profit that supports and provides opportunities for the Black College Community \"through scholarships, capacity builder and research initiatives, innovative programs, and strategic partnerships.\"", 
		url: "https://www.tmcf.org", 
		buttonText: "Code 2040"},
		{ title: "Thurgood Marshall College Fund", 
		summary: "Non-profit \"activating, connecting, and mobilizing the largest racial equity community in tech to dismantle the structural barriers that prevent the full participation and leadership of Black and Latinx technologists in the innovation economy.\"", 
		url: "http://www.code2040.org/", 
		buttonText: "Donate to Code 2040"},
		{ title: "My Brother's Keeper Alliance", 
		summary: "Focused on building safe and supportive communities for boys and young men of color where they feel valued and have clear pathways to opportunity and success.", 
		url: "https://www.obama.org/mbka/", 
		buttonText: "Donate to MBKA"},
		{ title: "Black Girls Code", 
		summary: "Providing coding lessons to young girls from underrepresented communities by reaching out to the community through workshops and after school programs. Black Girls CODE's ultimate goal is to train 1 million girls by 2040.", 
		url: "https://www.blackgirlscode.com", 
		buttonText: "Donate to Black Girls Code"},
		{ title: "Black Girls Code", 
		summary: "Established to cover funeral and burial expenses, mental and grief counseling, lodging and travel for all court proceedings, and to assist the Floyd family in the days to come as they continue to seek justice for George.", 
		url: "https://www.gofundme.com/f/georgefloyd", 
		buttonText: "Donate to the Floyd Family"},
		{ title: "NAACP", 
		summary: "The mission of the National Association for the Advancement of Colored People (NAACP) is to secure the political, educational, social, and economic equality of rights in order to eliminate race-based discrimination and ensure the health and well-being of all persons.", 
		url: "https://www.naacp.org", 
		buttonText: "Donate to the NAACP"},

	]
</script>

<main>
<h1>Educate. Donate. Act.</h1>
<div class="content">
	We at VandyHacks condemn the systemic racism and oppression gripping our society that senselessly murdered George Floyd, Breonna Taylor, Ahmaud Abery, and countless other Black people. These actions have shocked and saddened us, and we denounce unjust deaths at the hands of institutional racism.

	<br>
	<br>
	We believe that we must act against these forces, in whatever way that we can. While it is strange to speak as a hackathon organization, we believe we must work to support the organizations and people doing critical work. We believe in equal access to education, resources, and opportunities, especially in tech, and are taking action. 
	<br>
	<br>
	
	We do not have the solutions to injustice, but we can help support change-making organizations. Our action comes in the form of self-education, listening, and donations.

	<br>
	<br>
	
	<h2>Educate.</h2>
	<hr>

	Through self-education, we seek to better understand systemic racism. Some of the resources we are using are:
	<ul>
	{#each resources as resource}
		<li>
			<a href={resource.link} target="_blank">
				{resource.description}
			</a>
		</li>
	{/each}
	</ul>

	<hr>
	Through listening, we seek to learn from the experiences of members of our community. Please let us know your thoughts on how we can best support the community, and use what platform we have to spread resources and information. We want to continue this conversation and welcome any input on how we can make ourselves better and positively impact our current and future workspaces.

	<br>
	<br>

	<h2>Donate.</h2>
	<hr>
	We are matching donations up to a total of $1,000 to any organization fighting racism and anti-Blackness. As a result of restrictions on student organization accounts at Vanderbilt, VandyHacks will be donating all the matches to the NAACP Legal Defense Fund. We highly encourage anyone who has the means to donate what they can. Please send us the receipt at <a href="mailto:info@vandyhacks.org">info@vandyhacks.org</a> so that VandyHacks can match all of your donations. 

	<br>
	<br>

	Some of the organizations our members individually are donating to include:
	{#each funds as fund}
	<div class="fund">
		<h3>{fund.title}</h3>
		<div class="summary">
			{fund.summary}
		</div> 
		<a class="button button-primary" href={fund.url} target="_blank">{fund.buttonText}</a>
	</div>
	{/each}

	<br>
	<br>
	
	<h2>Act.</h2>
	<hr>
	There are many ways that you and I can be allies. Taking action by calling and writing letters to your representatives, participating in peaceful demonstrations, and signing petitions are ways that we can contribute. 
	
	<br>
	<br>
	- The VandyHacks Team
</div>
</main>

<style>
	main {
		color: white;
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
		font-family: "Lato";
	}

	h1 {
		color: white;
		font-weight: 100;
	}

	.content {
		text-align: left;
	}

	.fund {
		margin: 2em 0 0 0;
	}

	.button-primary {
		margin: .5em 0 0 0;
	}

	@media (min-width: 640px) {
		main {
			max-width: 50%;
			font-size: 1.5em;
		}
		h1 { 
			font-size: 3em;
			font-weight: 100;
		}

		h2 {
			font-size: 2em;
		}

		.button-primary {
			font-size: .75em;
		}
	}
</style>