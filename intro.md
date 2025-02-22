# ModelEarth Engine

We're creating a NextJS content engine with built-in environmental impact tracking.
[Fork and clone this repo](https://github.com/modelearth/engine)

TO DO: Display the [Household CoolClimate json](public/static/json/household-coolclimate.json) as a widget. [Details](https://model.earth/community/projects/#widgets)

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/git/external?repository-url=https://github.com/modelearth/engine)


You could switch to the engine's TypeScript branch here.  

Maybe we should run `npm audit fix` first here to try avoid: npm WARN old lockfile

### Add Storybook

Please use our [localsite/engine-storybook](https://github.com/localsite/engine-storybook) repo if you are adding storybook.  Avoid pushing storybook to the "modelearth/engine" repo so we can continue to sync with the parent repo.  

Storybook will look into your project's dependencies during its install process and provide you with the best configuration available. ([More details](https://storybook.js.org/docs/react/get-started/install))  

	npx sb init

Run the NextJS install (creates node_modules folder): 

	npm install

Run the server:

	npm start

Open [http://localhost:3000](http://localhost:3000)

In another terminal window, launch storybook at: [http://localhost:6006](http://localhost:6006)

	npm run storybook


To add an existing control to Storybook:

1. Update the .storybook/main.js file to include the "components" folder:

stories: ['../stories/**/*.stories.mdx', '../stories/**/*.stories.@(js|jsx|ts|tsx)', '../components/**/*.stories.mdx', '../components/**/*.stories.@(js|jsx|ts|tsx)'],

2. Add "export" before the const declaration in PageFilter.js  
export const PageFilter = () => {

3. Add an adjacent .stores.*  file for each component.

<!--
Not these:

Run these locally to add Storybook, and choose "yes" for the eslint plugin.

	npx -y sb init --builder webpack5
	yarn add -D @storybook/addon-postcss

Continue with the [Storybook install steps](https://theodorusclarence.com/blog/nextjs-storybook-tailwind)

TO DO: Figure out how to run one script similar to the curl script at the end of the page above.  Tried running it instead of manually pasting the rest of the Storybook install steps. It correctly adds: "resolutions": { "webpack": "^5" }  
But the yarn test did not work.

To test, run the yarn commands reside in the [Storybook tutorial](https://storybook.js.org/tutorials/intro-to-storybook/react/en/get-started/). 
-->

<!--
Manually coping ".storybook" folder after generating in "taskbox" using tutorial steps allowed yarn to complete, but yarn test command still did not work.

The following also did not work, but took a screenshot of settings added in case they have an impact.
[Steps for adding storybook](https://nebulab.com/blog/nextjs-tailwind-storybook) to the following.
-->