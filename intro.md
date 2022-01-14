# ModelEarth Engine

We're creating a NextJS CMS fork with built-in environmental impact tracking
[Fork and clone this repo](https://github.com/modelearth/engine)

TO DO: Display the [Household CoolClimate json](public/static/json/household-coolclimate.json) as a widget. [Details](https://model.earth/community/projects/#widgets)

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/git/external?repository-url=https://github.com/modelearth/engine)



Run to add Storybook ([source](https://theodorusclarence.com/blog/nextjs-storybook-tailwind))

	npx -y sb init --builder webpack5

Say yes to eslint plugin.

	yarn add -D @storybook/addon-postcss


AVOID: Tried running this for the rest (from the bottom source). Adds: "resolutions": { "webpack": "^5" }  
But yarn test did not work.

	curl -s https://raw.githubusercontent.com/theodorusclarence/expansion-pack/main/storybook/trigger.sh | bash -s

But unable to run yarn commands in the [Storybook tutorial](https://storybook.js.org/tutorials/intro-to-storybook/react/en/get-started/). So manually copied ".storybook" folder after generating in "taskbox" using tutorial steps. Allows yarn to complete, but yarn test command still did not work.

<!--
The following also did not work, but took a screenshot of settings added in case they have an impact.
[Steps for adding storybook](https://nebulab.com/blog/nextjs-tailwind-storybook) to the following.
-->