# Blockchain_API
Task (Mandatory Submission) — Basic API Development & Deployment
The task below is mandatory for candidates to attempt
Create a single video giving a walk-through of the code written for this task and run it with various cases
Write a minimum of 3 test cases. Bonus points if you have any extra test cases covered
Upload the code on GitHub with instructions and the video embedded within a GitHub README.md file
**Objective:**
Build an API to monitor the status of multiple blockchains using their respective RPC endpoints, and implement additional tasks to enhance the development and deployment process.

**Context:**
You are working on a project that involves monitoring and managing the status of various blockchains. Each blockchain has its own RPC endpoint that provides information about its current status, including whether it's running and the current block height.

**Deliverables:**
1. Develop an API that can fetch and display the status of all configured blockchains.
    a. Implement CRUD operations for blockchains list to add new blockchains or update existing blockchains in database (any database or `preferably MongoDB`)
    b. Implement status endpoint to give required info of all blockchains
    
3. Implement additional tasks to streamline the development and deployment process.


**Additional Tasks:**
1. **Create Docker Image for your API code:**
   - Develop a script for creating a Docker image of your API.

3. **Deploy Your API:**
   - Take an vm instance with ubuntu OS (GCP/AWS/other), set up your coding environment and deploy your API server.
   Note: `http://{instance-ip}:{port}/status` should give the required response.

4. **Implement CI/CD:**
   - Develop a CI/CD script to automatically deploy your changes/updates to the server

5. **Point a sub-domain to your deployment:**
   - Buy a domain (e.g., Freenom/GoDaddy/other free domain provider).
   - Add a subdomain to your domain name (specifically it should look like blockchain-status.yourdomain.name )

6. **Add reverse proxy using nginx:**
   - Block your API server port from public access, allow only 80 (http) and 443(https) ports
   - proxy pass API requests only with subdomain on 80 or 443

7. **Secure the API with https:**
   - Ensure that your API can be accessed through an HTTPS URL.
   - Redirect http request to https using nginx

**Constraints and Requirements:**
1. Utilize the RPC API for each blockchain to fetch status information.
2. Ensure the API can handle concurrent requests for multiple blockchains.
3. Implement error handling to manage cases where a blockchain is not reachable or returns an error response.
4. Document the API endpoints and provide clear instructions on how to use the API.

**Note:** `code needs to be pushed to github and should be accessible to us to evaluate`

**Success Criteria:**
1. The API should provide a list of configured blockchains with their current status.
2. For each blockchain, display whether it's running (able to fetch data) or not.
3. Include the current block height of each blockchain in the API response.

If you completed required tasks API response should be accessible on
`http://your-instance-ip:port/status`

Example Response
```
{
  "success": true,
  "result": [
    {
      "name": "blockchain1",
      "status": "active",
      "height": 12345
    },
    {
      "name": "blockchain2",
      "status": "inactive",
      "height": 0
    }
  ]
}
```
Note: if you fully completed all tasks
API respsonse needs be accessible on `https://blockchain-status.yourdomain`

**Relevant Information:**
- Docker Documentation: [Docker Documentation](https://docs.docker.com/)
- GitHub Documentation: [GitHub Documentation](https://docs.github.com/)
- CI/CD Documentation: [Github CI/CD docs](https://docs.github.com/en/actions/automating-builds-and-tests/about-continuous-integration)
- Nginx Documentation: [Nginx Documentation](https://nginx.org/en/docs/)

**Blockchains List:**
Use below chains list for the 2nd task

- OmniFlix Devnet
   - ChainID: devnet-alpha-2
   - API: https://api.devnet-alpha.omniflix.network
   - RPC: https://rpc.devnet-alpha.omniflix.network
- OmniFlix Testnet
   - ChainID: flixnet-4
   - API: https://api.testnet.omniflix.network
   - RPC: https://rpc.testnet.omniflix.network
- OmniFlix Mainnet
   - ChainID: omniflixhub-1
   - API: https://rest.omniflix.network
   - RPC: https://rpc.omniflix.network
 
   - Do not hesitate to let us know in the Telegram group in case of any queries you have. The more the participation, the better it is for you to get visibility. (Telegram link in the Connect with L0x section below)
