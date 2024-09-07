```markdown
# ViewDNS Postman Collection

This repository contains a Postman collection for querying various services provided by the ViewDNS API. The collection includes multiple requests for investigating IP history, DNS records, traceroutes, and other domain and IP-related information.

## Features
- **API Requests**: Common OSINT-related API requests using the ViewDNS API.
- **Environment Variables**: Customizable environment variables for API tokens, base URLs, domains, and IP addresses to make querying easier.
- **Modular Design**: Easily expandable by adding more ViewDNS API endpoints.

## Setup Instructions

### Step 1: Clone the Repository
```bash
git clone https://github.com/YOUR_USERNAME/viewdns-postman-collection.git
cd viewdns-postman-collection
```

### Step 2: Import the Postman Collection
1. Open Postman.
2. Click on the **Import** button.
3. Select the `viewdns_postman_collection.json` file from this repository.
4. Import the collection into your Postman workspace.

### Step 3: Setup Environment Variables
Before using the collection, configure the following environment variables in Postman:

- `base_url`: The base URL for the ViewDNS API (e.g., `https://api.viewdns.info`).
- `domain`: The target domain for queries (e.g., `example.com`).
- `ip`: The target IP address for IP-related queries (e.g., `8.8.8.8`).
- `api_key`: Your API key for accessing the ViewDNS API.

Example environment setup:
```bash
base_url = https://api.viewdns.info
domain = example.com
ip = 8.8.8.8
api_key = your_api_key_here
```

### Step 4: Make API Requests
Select the appropriate environment in Postman, and you can start sending requests from the collection.

## Available Endpoints

### 1. IP History
- **URL**: `{{base_url}}/iphistory/?domain={{domain}}&apikey={{api_key}}&output=json`
- **Description**: Fetches the IP history for a given domain.

### 2. Traceroute
- **URL**: `{{base_url}}/traceroute/?domain={{domain}}&apikey={{api_key}}&output=json`
- **Description**: Executes a traceroute for a given domain.

### 3. Email Lookup
- **URL**: `{{base_url}}/freeemail/?domain={{domain}}&apikey={{api_key}}&output=json`
- **Description**: Checks if the domain is associated with free email services.

### 4. DNS Record Lookup
- **URL**: `{{base_url}}/dnsrecord/?domain={{domain}}&recordtype=A&apikey={{api_key}}&output=json`
- **Description**: Fetches DNS records for a given domain. The default record type is `A`.

### 5. Chinese Firewall Test
- **URL**: `{{base_url}}/chinesefirewall/?domain={{domain}}&recordtype=A&apikey={{api_key}}&output=json`
- **Description**: Tests if a domain is blocked by the Great Firewall of China.

### 6. Spam DB Lookup
- **URL**: `{{base_url}}/spamdblookup/?ip={{ip}}&apikey={{api_key}}&output=json`
- **Description**: Looks up the given IP address in various spam databases.

### 7. IP Location
- **URL**: `{{base_url}}/iplocation/?ip={{ip}}&apikey={{api_key}}&output=json`
- **Description**: Retrieves location details for a given IP address.

## Expanding the Collection
You can add more API requests and endpoints provided by ViewDNS to expand the capabilities of the collection.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
```

This `viewdns.md` provides a structured README for the Postman collection, outlining the available endpoints, setup steps, and usage of environment variables. Let me know if you need any further adjustments!