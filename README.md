# jwt_profile_client_jwt_profile_api
Service User Using JWT Profile to Invoke API Secured Using JWT Profile in ZITADEL
1. Install Python 3.9 or later.
2. Install project dependencies by running the following command in the project directory: pip install -r requirements.txt
3. Replace the values in the .env file with own values. 
4. Copy the contents of your api key file to a file named api_key_file.json in the root directory of the project.
5. Copy the contents of your service user key file to a file named client_key.json in the root directory of the project.
6. In the command line, run the JWT token generator script by running the following command: 
  `python3 jwt_profile_token_generator.py`
7. Set an environment variable called TOKEN to the access token that was generated. e.g., `TOKEN=<Access_Token_From_Previous_Step>`
8. Once you have obtained the access token from the script, you can use it to make API requests using curl commands.
- `curl -X GET http://localhost:5000/api/public`
- `curl -X GET -H "Authorization: Bearer $TOKEN" http://localhost:5000/api/private`
- `curl -X GET -H "Authorization: Bearer $TOKEN" http://localhost:5000/api/private-scoped`
