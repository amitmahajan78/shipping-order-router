✏️ Downloading the router

The Apollo Router is a high-performance graph router built in Rust. It's available as an executable binary that you can add to your project in a few steps:

Open a terminal window and navigate to the router directory in the FlyBy project.

cd router
So far, we only have the .env file in here with our environment variables.

📦 router
┣ 📄 .env

We'll download the Router by running the install command in the terminal.

router
curl -sSL https://router.apollo.dev/download/nix/latest | sh
Note: Visit the official documentation to explore alternate methods of downloading the Router.

Now when we check the contents of our router directory, we'll see that we have a new file also called router!

📦 router
┣ 📄 .env
┗ 📄 router

✏️ Running the router

Back in the same terminal window, run the command below. You'll need to replace the <APOLLO_KEY> and <APOLLO_GRAPH_REF> placeholder values with your supergraph's corresponding values from the router/.env file. This command starts up the router locally and tells the router which supergraph to connect to.

APOLLO_KEY=<APOLLO_KEY> APOLLO_GRAPH_REF=<APOLLO_GRAPH_REF> ./router --config config.yaml

We'll see a few lines of router output, and finally a message that our router is running on port 4000, ready to receive queries!

Let's copy this address, we'll need it to set our connection settings in Studio. This tells outside consumers of our API what endpoint they can use to query our schema.

GraphQL endpoint exposed at http://127.0.0.1:4000/ 🚀

for more detail follow: https://www.apollographql.com/tutorials/voyage-part1/08-router-configuration-and-uplink
