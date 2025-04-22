<h1>BANK API</h1>
<h3>Overview</h3>
<p>This project implements a RESTful API service to fetch bank and branch details using in-memory data storage. The API supports queries to retrieve information about banks and their branches, designed for simplicity and efficiency.The API includes two main endpoints:</p>
<ul>
<li>GET /banks - Retrieves a list of all banks.</li>
<li>GET /banks/{bank_id}/branches - Retrieves all branches of a specific bank by bank_id</li>
</ul>
<h2>Method Used</h2>
<h3>Technologies</h3>
<ul>
<li><b>Backend Framework: <u>Flask</u></b> Used to implement the RESTful API.</li>
<li><b>Unit Tests:</b>It ensures that the endpoints return the correct status code and response data.</li>
<li><b>Deployment: </b>Vercel (I chose Vercel for deployment instead of Heroku, as Heroku’s free tier requires a payment method, which I approached cautiously).</li>
</ul>
<h3>Implementation</h3>
<ol>
<li>
<b>API Endpoints:</b>
<ul>
<li><u>GET /banks</u>: Returns a list of all banks.</li>
<li><u>GET /banks/{bank_id}/branches</u>: Returns the list of branches for a specified bank.
</li>
</ul>
</li>
<li><b>Error Handling:</b> A custom 404 error handler is used to return appropriate error messages in case of invalid requests or URLs.</li>
<li><b>Unit Tests:</b>
<ul>
<li>Tests in test_app.py verify:
<ul>
<li>Fetching all banks.</li>
<li>Fetching branches for a specific bank.</li>
<li>Handling requests for non-existing bank IDs.</li>
</ul>
</li>
</ul>
</li>
</ol>
<h3>Deployment</h3>
<p>The API was deployed on Vercel due to limitations in Heroku's free tier, which requires a payment method. To avoid adding payment details for cautious reasons, I chose Vercel instead. It provided a simpler and more convenient deployment process.</p>
<b>Vercel Deployment Link: </b> https://bank-api-blush.vercel.app/
</ul>
<h3>Time Taken</h3>
<p>I dedicated 2–3 days with 8–12 hours of focused work each day to build, test, and deploy the API efficiently.</p>
<h3>Challenges</h3>
<p>Faced deployment issues on Heroku due to payment requirements, so I switched to Vercel. This experience helped me gain valuable insights into deployment and error handling.</p>
