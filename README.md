Here's the combined and neatly ordered `README.md` that includes both the general OSINT Postman collection details and the specific BGPView API setup:

```markdown
# Postman Collection for OSINT Data Gathering

This repository contains a Postman collection for querying various Open Source Intelligence (OSINT) APIs. The collection is designed to help you gather public information through API calls for research and investigation purposes.

## Features
- **API Requests**: A collection of commonly used OSINT-related API requests.
- **Environment Variables**: Customizable variables for API tokens, base URLs, and query parameters to make testing and data gathering easier.
- **Modular Design**: Easily expandable by adding more APIs and requests.

## Setup Instructions

### Step 1: Clone the Repository
```bash
gh repo clone arknet-cyber/osint-postman-collection
cd osint-postman-collection
```

# OSINT Postman Collection using BGPView API

This repository contains a Postman collection for gathering OSINT (Open Source Intelligence) data using the BGPView API. The collection includes multiple requests for investigating IP addresses, Autonomous System Numbers (ASNs), DNS records, and other network-related data.

## Collection Overview

The collection is divided into the following sections:
1. **Email Investigation**: (To be expanded)
2. **IP Investigation**:
   - **Basic IP Info**: Fetch basic details about an IP address.
   - **IP Info Detailed**: Retrieve detailed information about a specific IP address.
   - **IP Prefix**: Get details on the IP prefix associated with an IP address.
3. **DNS Investigation**:
   - **ASN Info**: Fetch details about an Autonomous System Number (ASN).
   - **ASN Prefixes**: Retrieve prefixes associated with an ASN.
   - **ASN Peers**: Get information about peers of an ASN.
   - **ASN Upstream**: Get upstream connections of an ASN.
   - **ASN Downstreams**: Get downstream connections of an ASN.
   - **ASN IXS**: Fetch information on Internet Exchange Points (IXPs) connected to an ASN.
   - **IX ID**: Retrieve details based on an IX ID.
   - **Search Term**: Search for data using a specific term (e.g., "digitalocean").

## Setup Instructions

### Step 2: Import the Postman Collection
1. Open Postman.
2. Click on the **Import** button.
3. Select the `osint_postman_collection.json` file from this repository.
4. Import the collection into your Postman workspace.

### Step 3: Setup Environment Variables
Before using the collection, configure the following environment variables in Postman:

- `base_url`: The base URL for the BGPView API (e.g., `https://api.bgpview.io`).
- `ip_address`: The target IP address for queries.
- `token`: Your API token (if required by the service).
- `asn_number`: The Autonomous System Number (ASN) for investigation.

Example environment setup:
```bash
base_url = https://api.bgpview.io
ip_address = 8.8.8.8
asn_number = 15169
```

### Step 4: Make API Requests
Select the appropriate environment in Postman, and you can start sending requests from the collection.

## Available Endpoints

### IP Investigation

- **Basic IP Info**: 
  - URL: `{{base_url}}/{{ip_address}}?token={{token}}`
  - Description: Fetches basic information about the given IP address.

- **IP Info Detailed**: 
  - URL: `{{base_url}}/ip/{{ip_address}}`
  - Description: Fetches detailed information for a specific IP address.

- **IP Prefix**: 
  - URL: `{{base_url}}/prefix/{{ip_address}}/24`
  - Description: Retrieves information about the prefix associated with the IP.

### DNS Investigation

- **ASN Info**: 
  - URL: `{{base_url}}/asn/{{asn_number}}`
  - Description: Fetches basic details about the given ASN.

- **ASN Prefixes**: 
  - URL: `{{base_url}}/asn/{{asn_number}}/prefixes`
  - Description: Retrieves the list of prefixes associated with the ASN.

- **ASN Peers**: 
  - URL: `{{base_url}}/asn/{{asn_number}}/peers`
  - Description: Lists the peers of the ASN.

- **ASN Upstreams**: 
  - URL: `{{base_url}}/asn/{{asn_number}}/upstreams`
  - Description: Lists the upstream connections of the ASN.

- **ASN Downstreams**: 
  - URL: `{{base_url}}/asn/{{asn_number}}/downstreams`
  - Description: Lists the downstream connections of the ASN.

- **ASN IXS**: 
  - URL: `{{base_url}}/asn/{{asn_number}}/ixs`
  - Description: Retrieves the Internet Exchange Points (IXPs) connected to the ASN.

- **IX ID**: 
  - URL: `{{base_url}}/ix/ix_id`
  - Description: Fetches information based on an IX ID.

- **Search Term**: 
  - URL: `{{base_url}}/search?query_term=digitalocean`
  - Description: Searches for information based on a query term (e.g., "digitalocean").

## Expanding the Collection
Feel free to extend the collection by adding more OSINT APIs, endpoints, and investigative queries to suit your needs.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
```

This format integrates the general setup and specific steps for the BGPView API OSINT collection in a clean, logical order. Let me know if further adjustments are needed!
