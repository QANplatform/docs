---
title: 'QAN API Methods'
description: 'Use APIs to interact with the QAN TestNet.'
---

# QAN API Methods

::lead
Use APIs to interact with the QAN TestNet.
::

## qan_accounts

::wrapper
#text
Returns a list of addresses owned by client.

### HTTP response status codes for "qan_accounts"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_accounts"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/accounts/" urlType="get"}
  :::tabPanel
  ```sh
  curl --request GET \
	--url /accounts/ \
	--header 'Accept: application/json, , application/problem+json'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'GET',
	headers: {Accept: 'application/json, , application/problem+json'}
};

fetch('/accounts/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"net/http"
	"io"
)

func main() {

	url := "/accounts/"

	req, _ := http.NewRequest("GET", url, nil)

	req.Header.Add("Accept", "application/json, , application/problem+json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {"Accounts":"array"}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

## qan_blobBaseFee

::wrapper
#text
Returns the expected base fee for blobs in the next block.

### HTTP response status codes for "qan_blobBaseFee"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_blobBaseFee"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/blobBaseFee/" urlType="get"}
  :::tabPanel
  ```sh
  curl --request GET \
	--url /blobBaseFee/ \
	--header 'Accept: application/json, , application/problem+json'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'GET',
	headers: {Accept: 'application/json, , application/problem+json'}
};

fetch('/blobBaseFee/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"net/http"
	"io"
)

func main() {

	url := "/blobBaseFee/"

	req, _ := http.NewRequest("GET", url, nil)

	req.Header.Add("Accept", "application/json, , application/problem+json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {"BaseFee":"12345"}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

## qan_blockNumber

::wrapper
#text
Returns the latest block number of the blockchain.

### HTTP response status codes for "qan_blockNumber"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_blockNumber"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/blockNumber/" urlType="get"}
  :::tabPanel
  ```sh
  curl --request GET \
	--url /blockNumber/ \
	--header 'Accept: application/json, , application/problem+json'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'GET',
	headers: {Accept: 'application/json, , application/problem+json'}
};

fetch('/blockNumber/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"net/http"
	"io"
)

func main() {

	url := "/blockNumber/"

	req, _ := http.NewRequest("GET", url, nil)

	req.Header.Add("Accept", "application/json, , application/problem+json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {"BlockNumber":"latest"}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

## qan_call

::wrapper
#text
Executes a new message call immediately without creating a transaction on the block chain.

### HTTP response status codes for "qan_call"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_call"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/call/" urlType="post"}
  :::tabPanel
  ```sh
  curl --request POST \
	--url /call/ \
	--header 'Accept: application/json, , application/problem+json' \
	--header 'Content-Type: application/json' \
	--data '
{
  "BlockNumber": "string",
  "Transaction": {
    "Data": "string",
    "From": "string",
    "Gas": "string",
    "GasPrice": "string",
    "To": "string",
    "Value": "string"
  }
}
'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'POST',
	headers: {
		Accept: 'application/json, , application/problem+json',
		'Content-Type': 'application/json'
	},
	body: JSON.stringify({
		BlockNumber: 'string',
		Transaction: {
			Data: 'string',
			From: 'string',
			Gas: 'string',
			GasPrice: 'string',
			To: 'string',
			Value: 'string'
		}
	})
};

fetch('/call/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"strings"
	"net/http"
	"io"
)

func main() {

	url := "/call/"

	payload := strings.NewReader("{\"BlockNumber\":\"string\",\"Transaction\":{\"Data\":\"string\",\"From\":\"string\",\"Gas\":\"string\",\"GasPrice\":\"string\",\"To\":\"string\",\"Value\":\"string\"}}")

	req, _ := http.NewRequest("POST", url, payload)

	req.Header.Add("Accept", "application/json, , application/problem+json")
	req.Header.Add("Content-Type", "application/json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {"Data":"0xcafebabe"}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

## qan_chainId

::wrapper
#text
Returns the current network/chain ID, used to sign replay-protected transaction introduced in EIP-155.

### HTTP response status codes for "qan_chainId"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_chainId"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/chainId/" urlType="get"}
  :::tabPanel
  ```sh
  curl --request GET \
	--url /chainId/ \
	--header 'Accept: application/json, , application/problem+json'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'GET',
	headers: {Accept: 'application/json, , application/problem+json'}
};

fetch('/chainId/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"net/http"
	"io"
)

func main() {

	url := "/chainId/"

	req, _ := http.NewRequest("GET", url, nil)

	req.Header.Add("Accept", "application/json, , application/problem+json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {"ChainId":"1"}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

## qan_estimateGas

::wrapper
#text
Returns an estimation of gas for a given transaction.

### HTTP response status codes for "qan_estimateGas"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_estimateGas"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/estimateGas/" urlType="post"}
  :::tabPanel
  ```sh
  curl --request POST \
	--url /estimateGas/ \
	--header 'Accept: application/json, , application/problem+json' \
	--header 'Content-Type: application/json' \
	--data '
{
  "Object": {
    "Balance": "string",
    "Code": "integer",
    "Nonce": "string",
    "State": "string",
    "StateDiff": "string"
  },
  "Transaction": {
    "Data": "string",
    "From": "string",
    "Gas": "string",
    "GasPrice": "string",
    "To": "string",
    "Value": "string"
  }
}
'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'POST',
	headers: {
		Accept: 'application/json, , application/problem+json',
		'Content-Type': 'application/json'
	},
	body: JSON.stringify({
		Object: {
			Balance: 'string',
			Code: 'integer',
			Nonce: 'string',
			State: 'string',
			StateDiff: 'string'
		},
		Transaction: {
			Data: 'string',
			From: 'string',
			Gas: 'string',
			GasPrice: 'string',
			To: 'string',
			Value: 'string'
		}
	})
};

fetch('/estimateGas/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"strings"
	"net/http"
	"io"
)

func main() {

	url := "/estimateGas/"

	payload := strings.NewReader("{\"Object\":{\"Balance\":\"string\",\"Code\":\"integer\",\"Nonce\":\"string\",\"State\":\"string\",\"StateDiff\":\"string\"},\"Transaction\":{\"Data\":\"string\",\"From\":\"string\",\"Gas\":\"string\",\"GasPrice\":\"string\",\"To\":\"string\",\"Value\":\"string\"}}")

	req, _ := http.NewRequest("POST", url, payload)

	req.Header.Add("Accept", "application/json, , application/problem+json")
	req.Header.Add("Content-Type", "application/json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {"EstimatedGas":"string"}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

## qan_feeHistory

::wrapper
#text
Returns the collection of historical gas information.

### HTTP response status codes for "qan_feeHistory"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_feeHistory"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/feeHistory/" urlType="post"}
  :::tabPanel
  ```sh
  curl --request POST \
	--url /feeHistory/ \
	--header 'Accept: application/json, , application/problem+json' \
	--header 'Content-Type: application/json' \
	--data '
{
  "BlockCount": "integer",
  "NewestBlock": "string",
  "RewardPercentiles": "array"
}
'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'POST',
	headers: {
		Accept: 'application/json, , application/problem+json',
		'Content-Type': 'application/json'
	},
	body: JSON.stringify({BlockCount: 'integer', NewestBlock: 'string', RewardPercentiles: 'array'})
};

fetch('/feeHistory/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"strings"
	"net/http"
	"io"
)

func main() {

	url := "/feeHistory/"

	payload := strings.NewReader("{\"BlockCount\":\"integer\",\"NewestBlock\":\"string\",\"RewardPercentiles\":\"array\"}")

	req, _ := http.NewRequest("POST", url, payload)

	req.Header.Add("Accept", "application/json, , application/problem+json")
	req.Header.Add("Content-Type", "application/json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {"BaseFeePerGas":"array","GasUsedRatio":"array","OldestBlock":"string","Reward":"array"}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

## qan_gasPrice

::wrapper
#text
Returns the current gas price on the network in wei.

### HTTP response status codes for "qan_gasPrice"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_gasPrice"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/gasPrice/" urlType="get"}
  :::tabPanel
  ```sh
  curl --request GET \
	--url /gasPrice/ \
	--header 'Accept: application/json, , application/problem+json'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'GET',
	headers: {Accept: 'application/json, , application/problem+json'}
};

fetch('/gasPrice/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"net/http"
	"io"
)

func main() {

	url := "/gasPrice/"

	req, _ := http.NewRequest("GET", url, nil)

	req.Header.Add("Accept", "application/json, , application/problem+json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {"GasPrice":"12345"}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

## qan_getAccount

::wrapper
#text
Retrieves account details by specifying an address and a block number/tag.

### Parameters for "qan_getAccount"

::parameters{in="Path parameters"}
  ::parameter{name="Address" type="string" :required="true"}
  The account address for which the information is to be retrieved
  ::
  ::parameter{name="BlockReference" type="string" :required="true"}
  The block number in hexadecimal or decimal format or the string latest, earliest, pending, safe or finalized (safe and finalized tags are only supported on Ethereum, Gnosis, Arbitrum, Arbitrum Nova and Avalanche C-chain), see the default block parameter description in the official Ethereum documentation
  ::
::

### HTTP response status codes for "qan_getAccount"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_getAccount"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/getAccount/{Address}/{BlockReference}/" urlType="get"}
  :::tabPanel
  ```sh
  curl --request GET \
	--url /getAccount/%7BAddress%7D/%7BBlockReference%7D/ \
	--header 'Accept: application/json, , application/problem+json'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'GET',
	headers: {Accept: 'application/json, , application/problem+json'}
};

fetch('/getAccount/%7BAddress%7D/%7BBlockReference%7D/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"net/http"
	"io"
)

func main() {

	url := "/getAccount/%7BAddress%7D/%7BBlockReference%7D/"

	req, _ := http.NewRequest("GET", url, nil)

	req.Header.Add("Accept", "application/json, , application/problem+json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {"Balance":"string","CodeHash":"string","Nonce":"string","StorageRoot":"string"}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

## qan_getBalance

::wrapper
#text
Returns the balance of the account of given address.

### Parameters for "qan_getBalance"

::parameters{in="Path parameters"}
  ::parameter{name="Address" type="string" :required="true"}
  A 20 bytes long hexadecimal value representing an Ethereum address
  ::
::

::parameters{in="Query parameters"}
  ::parameter{name="BlockNumber" type="string"}
  The block number in hexadecimal or decimal format or the string latest, earliest, pending, safe or finalized (safe and finalized tags are only supported on Ethereum, Gnosis, Arbitrum, Arbitrum Nova and Avalanche C-chain), see the default block parameter description in the official Ethereum documentation
  ::
::

### HTTP response status codes for "qan_getBalance"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_getBalance"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/getBalance/{Address}/" urlType="get"}
  :::tabPanel
  ```sh
  curl --request GET \
	--url /getBalance/%7BAddress%7D/ \
	--header 'Accept: application/json, , application/problem+json'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'GET',
	headers: {Accept: 'application/json, , application/problem+json'}
};

fetch('/getBalance/%7BAddress%7D/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"net/http"
	"io"
)

func main() {

	url := "/getBalance/%7BAddress%7D/"

	req, _ := http.NewRequest("GET", url, nil)

	req.Header.Add("Accept", "application/json, , application/problem+json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {"Balance":"0xcafebabe"}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

## qan_getBlockByHash

::wrapper
#text
Returns information of the block matching the given block hash.

### Parameters for "qan_getBlockByHash"

::parameters{in="Path parameters"}
  ::parameter{name="Hash" type="string" :required="true"}
  The hash (32 bytes) of the block
  ::
  ::parameter{name="TransactionDetailFlag" type="boolean" :required="true"}
  The method returns the full transaction objects when this value is true otherwise, it returns only the hashes of the transactions
  ::
::

### HTTP response status codes for "qan_getBlockByHash"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_getBlockByHash"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/getBlockByHash/{Hash}/{TransactionDetailFlag}/" urlType="get"}
  :::tabPanel
  ```sh
  curl --request GET \
	--url /getBlockByHash/%7BHash%7D/%7BTransactionDetailFlag%7D/ \
	--header 'Accept: application/json, , application/problem+json'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'GET',
	headers: {Accept: 'application/json, , application/problem+json'}
};

fetch('/getBlockByHash/%7BHash%7D/%7BTransactionDetailFlag%7D/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"net/http"
	"io"
)

func main() {

	url := "/getBlockByHash/%7BHash%7D/%7BTransactionDetailFlag%7D/"

	req, _ := http.NewRequest("GET", url, nil)

	req.Header.Add("Accept", "application/json, , application/problem+json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {"Block":""}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

## qan_getBlockByNumber

::wrapper
#text
Returns information of the block matching the given block number.

### Parameters for "qan_getBlockByNumber"

::parameters{in="Path parameters"}
  ::parameter{name="BlockNumber" type="string" :required="true"}
  The block number in hexadecimal or decimal format or the string latest, earliest, pending, safe or finalized (safe and finalized tags are only supported on Ethereum, Gnosis, Arbitrum, Arbitrum Nova and Avalanche C-chain), see the default block parameter description in the official Ethereum documentation
  ::
  ::parameter{name="TransactionDetailFlag" type="boolean" :required="true"}
  The method returns the full transaction objects when this value is true otherwise, it returns only the hashes of the transactions
  ::
::

### HTTP response status codes for "qan_getBlockByNumber"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_getBlockByNumber"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/getBlockByNumber/{BlockNumber}/{TransactionDetailFlag}/" urlType="get"}
  :::tabPanel
  ```sh
  curl --request GET \
	--url /getBlockByNumber/%7BBlockNumber%7D/%7BTransactionDetailFlag%7D/ \
	--header 'Accept: application/json, , application/problem+json'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'GET',
	headers: {Accept: 'application/json, , application/problem+json'}
};

fetch('/getBlockByNumber/%7BBlockNumber%7D/%7BTransactionDetailFlag%7D/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"net/http"
	"io"
)

func main() {

	url := "/getBlockByNumber/%7BBlockNumber%7D/%7BTransactionDetailFlag%7D/"

	req, _ := http.NewRequest("GET", url, nil)

	req.Header.Add("Accept", "application/json, , application/problem+json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {"Block":""}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

## qan_getBlockReceipts

::wrapper
#text
Returns all transaction receipts for a given block.

### Parameters for "qan_getBlockReceipts"

::parameters{in="Path parameters"}
  ::parameter{name="BlockNumber" type="string" :required="true"}
  The block number in hexadecimal or decimal format or the string latest, earliest, pending, safe or finalized (safe and finalized tags are only supported on Ethereum, Gnosis, Arbitrum, Arbitrum Nova and Avalanche C-chain), see the default block parameter description in the official Ethereum documentation
  ::
::

### HTTP response status codes for "qan_getBlockReceipts"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_getBlockReceipts"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/getBlockReceipts/{BlockNumber}/" urlType="get"}
  :::tabPanel
  ```sh
  curl --request GET \
	--url /getBlockReceipts/%7BBlockNumber%7D/ \
	--header 'Accept: application/json, , application/problem+json'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'GET',
	headers: {Accept: 'application/json, , application/problem+json'}
};

fetch('/getBlockReceipts/%7BBlockNumber%7D/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"net/http"
	"io"
)

func main() {

	url := "/getBlockReceipts/%7BBlockNumber%7D/"

	req, _ := http.NewRequest("GET", url, nil)

	req.Header.Add("Accept", "application/json, , application/problem+json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {"TransactionReceipts":"array"}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

## qan_getBlockTransactionCountByHash

::wrapper
#text
Returns the number of transactions for the block matching the given block hash.

### Parameters for "qan_getBlockTransactionCountByHash"

::parameters{in="Path parameters"}
  ::parameter{name="Hash" type="string" :required="true"}
  The hash of the block
  ::
::

### HTTP response status codes for "qan_getBlockTransactionCountByHash"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_getBlockTransactionCountByHash"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/getBlockTransactionCountByHash/{Hash}/" urlType="get"}
  :::tabPanel
  ```sh
  curl --request GET \
	--url /getBlockTransactionCountByHash/%7BHash%7D/ \
	--header 'Accept: application/json, , application/problem+json'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'GET',
	headers: {Accept: 'application/json, , application/problem+json'}
};

fetch('/getBlockTransactionCountByHash/%7BHash%7D/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"net/http"
	"io"
)

func main() {

	url := "/getBlockTransactionCountByHash/%7BHash%7D/"

	req, _ := http.NewRequest("GET", url, nil)

	req.Header.Add("Accept", "application/json, , application/problem+json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {"TransactionCount":"string"}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

## qan_getBlockTransactionCountByNumber

::wrapper
#text
Returns the number of transactions for the block matching the given block number.

### Parameters for "qan_getBlockTransactionCountByNumber"

::parameters{in="Path parameters"}
  ::parameter{name="BlockNumber" type="string" :required="true"}
  The block number in hexadecimal or decimal format or the string latest, earliest, pending, safe or finalized (safe and finalized tags are only supported on Ethereum, Gnosis, Arbitrum, Arbitrum Nova and Avalanche C-chain), see the default block parameter description in the official Ethereum documentation
  ::
::

### HTTP response status codes for "qan_getBlockTransactionCountByNumber"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_getBlockTransactionCountByNumber"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/getBlockTransactionCountByNumber/{BlockNumber}/" urlType="get"}
  :::tabPanel
  ```sh
  curl --request GET \
	--url /getBlockTransactionCountByNumber/%7BBlockNumber%7D/ \
	--header 'Accept: application/json, , application/problem+json'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'GET',
	headers: {Accept: 'application/json, , application/problem+json'}
};

fetch('/getBlockTransactionCountByNumber/%7BBlockNumber%7D/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"net/http"
	"io"
)

func main() {

	url := "/getBlockTransactionCountByNumber/%7BBlockNumber%7D/"

	req, _ := http.NewRequest("GET", url, nil)

	req.Header.Add("Accept", "application/json, , application/problem+json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {"TransactionCount":"string"}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

## qan_getCode

::wrapper
#text
Returns the compiled bytecode of a smart contract.

### Parameters for "qan_getCode"

::parameters{in="Path parameters"}
  ::parameter{name="Address" type="string" :required="true"}
  The address of the smart contract from which the bytecode will be obtained
  ::
::

::parameters{in="Query parameters"}
  ::parameter{name="BlockNumber" type="string"}
  The block number in hexadecimal or decimal format or the string latest, earliest, pending, safe or finalized (safe and finalized tags are only supported on Ethereum, Gnosis, Arbitrum, Arbitrum Nova and Avalanche C-chain), see the default block parameter description in the official Ethereum documentation
  ::
::

### HTTP response status codes for "qan_getCode"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_getCode"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/getCode/{Address}/" urlType="get"}
  :::tabPanel
  ```sh
  curl --request GET \
	--url /getCode/%7BAddress%7D/ \
	--header 'Accept: application/json, , application/problem+json'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'GET',
	headers: {Accept: 'application/json, , application/problem+json'}
};

fetch('/getCode/%7BAddress%7D/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"net/http"
	"io"
)

func main() {

	url := "/getCode/%7BAddress%7D/"

	req, _ := http.NewRequest("GET", url, nil)

	req.Header.Add("Accept", "application/json, , application/problem+json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {"Bytecode":"string"}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

## qan_getFilterChanges

::wrapper
#text
Polling method for a filter, which returns an array of events that have occurred since the last poll.

### Parameters for "qan_getFilterChanges"

::parameters{in="Path parameters"}
  ::parameter{name="FilterId" type="string" :required="true"}
  The filter id that is returned from eth_newFilter, eth_newBlockFilter or eth_newPendingTransactionFilter
  ::
::

### HTTP response status codes for "qan_getFilterChanges"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_getFilterChanges"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/getFilterChanges/{FilterId}/" urlType="get"}
  :::tabPanel
  ```sh
  curl --request GET \
	--url /getFilterChanges/%7BFilterId%7D/ \
	--header 'Accept: application/json, , application/problem+json'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'GET',
	headers: {Accept: 'application/json, , application/problem+json'}
};

fetch('/getFilterChanges/%7BFilterId%7D/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"net/http"
	"io"
)

func main() {

	url := "/getFilterChanges/%7BFilterId%7D/"

	req, _ := http.NewRequest("GET", url, nil)

	req.Header.Add("Accept", "application/json, , application/problem+json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {"Result":""}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

## qan_getFilterLogs

::wrapper
#text
Returns an array of all logs matching filter with given id.

### Parameters for "qan_getFilterLogs"

::parameters{in="Path parameters"}
  ::parameter{name="Id" type="string" :required="true"}
  The filter ID
  ::
::

### HTTP response status codes for "qan_getFilterLogs"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_getFilterLogs"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/getFilterLogs/{Id}/" urlType="get"}
  :::tabPanel
  ```sh
  curl --request GET \
	--url /getFilterLogs/%7BId%7D/ \
	--header 'Accept: application/json, , application/problem+json'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'GET',
	headers: {Accept: 'application/json, , application/problem+json'}
};

fetch('/getFilterLogs/%7BId%7D/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"net/http"
	"io"
)

func main() {

	url := "/getFilterLogs/%7BId%7D/"

	req, _ := http.NewRequest("GET", url, nil)

	req.Header.Add("Accept", "application/json, , application/problem+json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {"Logs":"array"}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

## qan_getLogs

::wrapper
#text
Returns an array of all logs matching a given filter object.

### HTTP response status codes for "qan_getLogs"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_getLogs"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/getLogs/" urlType="post"}
  :::tabPanel
  ```sh
  curl --request POST \
	--url /getLogs/ \
	--header 'Accept: application/json, , application/problem+json' \
	--header 'Content-Type: application/json' \
	--data '
{
  "Address": "string",
  "BlockHash": "string",
  "FromBlock": "string",
  "ToBlock": "string",
  "Topics": "array"
}
'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'POST',
	headers: {
		Accept: 'application/json, , application/problem+json',
		'Content-Type': 'application/json'
	},
	body: JSON.stringify({
		Address: 'string',
		BlockHash: 'string',
		FromBlock: 'string',
		ToBlock: 'string',
		Topics: 'array'
	})
};

fetch('/getLogs/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"strings"
	"net/http"
	"io"
)

func main() {

	url := "/getLogs/"

	payload := strings.NewReader("{\"Address\":\"string\",\"BlockHash\":\"string\",\"FromBlock\":\"string\",\"ToBlock\":\"string\",\"Topics\":\"array\"}")

	req, _ := http.NewRequest("POST", url, payload)

	req.Header.Add("Accept", "application/json, , application/problem+json")
	req.Header.Add("Content-Type", "application/json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {"Logs":"array"}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

## qan_getProof

::wrapper
#text
Returns the account and storage values of the specified account including the Merkle-proof.

### HTTP response status codes for "qan_getProof"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_getProof"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/getProof/" urlType="post"}
  :::tabPanel
  ```sh
  curl --request POST \
	--url /getProof/ \
	--header 'Accept: application/json, , application/problem+json' \
	--header 'Content-Type: application/json' \
	--data '
{
  "Address": "string",
  "BlockNumber": "string",
  "StorageKeys": "array"
}
'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'POST',
	headers: {
		Accept: 'application/json, , application/problem+json',
		'Content-Type': 'application/json'
	},
	body: JSON.stringify({Address: 'string', BlockNumber: 'string', StorageKeys: 'array'})
};

fetch('/getProof/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"strings"
	"net/http"
	"io"
)

func main() {

	url := "/getProof/"

	payload := strings.NewReader("{\"Address\":\"string\",\"BlockNumber\":\"string\",\"StorageKeys\":\"array\"}")

	req, _ := http.NewRequest("POST", url, payload)

	req.Header.Add("Accept", "application/json, , application/problem+json")
	req.Header.Add("Content-Type", "application/json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {"AccountProof":"string","Address":"string","Balance":"string","CodeHash":"string","Nonce":["string","null"],"StorageHash":"string","StorageProof":"array"}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

## qan_getStorageAt

::wrapper
#text
Returns the value from a storage position at a given address.

### HTTP response status codes for "qan_getStorageAt"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_getStorageAt"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/getStorageAt/" urlType="post"}
  :::tabPanel
  ```sh
  curl --request POST \
	--url /getStorageAt/ \
	--header 'Accept: application/json, , application/problem+json' \
	--header 'Content-Type: application/json' \
	--data '
{
  "Address": "string",
  "BlockNumber": "string",
  "Position": "string"
}
'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'POST',
	headers: {
		Accept: 'application/json, , application/problem+json',
		'Content-Type': 'application/json'
	},
	body: JSON.stringify({Address: 'string', BlockNumber: 'string', Position: 'string'})
};

fetch('/getStorageAt/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"strings"
	"net/http"
	"io"
)

func main() {

	url := "/getStorageAt/"

	payload := strings.NewReader("{\"Address\":\"string\",\"BlockNumber\":\"string\",\"Position\":\"string\"}")

	req, _ := http.NewRequest("POST", url, payload)

	req.Header.Add("Accept", "application/json, , application/problem+json")
	req.Header.Add("Content-Type", "application/json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {"Value":"string"}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

## qan_getTransactionByBlockHashAndIndex

::wrapper
#text
Returns information about a transaction given a blockhash and transaction index position.

### Parameters for "qan_getTransactionByBlockHashAndIndex"

::parameters{in="Path parameters"}
  ::parameter{name="blockHash" type="string" :required="true"}
  ::
  ::parameter{name="index" type="string" :required="true"}
  An integer of the transaction index position
  ::
::

### HTTP response status codes for "qan_getTransactionByBlockHashAndIndex"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_getTransactionByBlockHashAndIndex"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/getTransactionByBlockHashAndIndex/{blockHash}/{index}/" urlType="get"}
  :::tabPanel
  ```sh
  curl --request GET \
	--url /getTransactionByBlockHashAndIndex/%7BblockHash%7D/%7Bindex%7D/ \
	--header 'Accept: application/json, , application/problem+json'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'GET',
	headers: {Accept: 'application/json, , application/problem+json'}
};

fetch('/getTransactionByBlockHashAndIndex/%7BblockHash%7D/%7Bindex%7D/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"net/http"
	"io"
)

func main() {

	url := "/getTransactionByBlockHashAndIndex/%7BblockHash%7D/%7Bindex%7D/"

	req, _ := http.NewRequest("GET", url, nil)

	req.Header.Add("Accept", "application/json, , application/problem+json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {"Transaction":""}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

## qan_getTransactionByBlockNumberAndIndex

::wrapper
#text
Returns information about a transaction given a block number and transaction index position.

### Parameters for "qan_getTransactionByBlockNumberAndIndex"

::parameters{in="Path parameters"}
  ::parameter{name="blockNumber" type="string" :required="true"}
  The block number in hexadecimal or decimal format or the string latest, earliest, pending, safe or finalized (safe and finalized tags are only supported on Ethereum, Gnosis, Arbitrum, Arbitrum Nova and Avalanche C-chain), see the default block parameter description in the official Ethereum documentation
  ::
  ::parameter{name="index" type="string" :required="true"}
  An integer of the transaction index position
  ::
::

### HTTP response status codes for "qan_getTransactionByBlockNumberAndIndex"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_getTransactionByBlockNumberAndIndex"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/getTransactionByBlockNumberAndIndex/{blockNumber}/{index}/" urlType="get"}
  :::tabPanel
  ```sh
  curl --request GET \
	--url /getTransactionByBlockNumberAndIndex/%7BblockNumber%7D/%7Bindex%7D/ \
	--header 'Accept: application/json, , application/problem+json'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'GET',
	headers: {Accept: 'application/json, , application/problem+json'}
};

fetch('/getTransactionByBlockNumberAndIndex/%7BblockNumber%7D/%7Bindex%7D/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"net/http"
	"io"
)

func main() {

	url := "/getTransactionByBlockNumberAndIndex/%7BblockNumber%7D/%7Bindex%7D/"

	req, _ := http.NewRequest("GET", url, nil)

	req.Header.Add("Accept", "application/json, , application/problem+json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {"Transaction":""}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

## qan_getTransactionByHash

::wrapper
#text
Returns the information about a transaction from a transaction hash.

### Parameters for "qan_getTransactionByHash"

::parameters{in="Path parameters"}
  ::parameter{name="hash" type="string" :required="true"}
  The hash of a transaction
  ::
::

### HTTP response status codes for "qan_getTransactionByHash"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_getTransactionByHash"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/getTransactionByHash/{hash}/" urlType="get"}
  :::tabPanel
  ```sh
  curl --request GET \
	--url /getTransactionByHash/%7Bhash%7D/ \
	--header 'Accept: application/json, , application/problem+json'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'GET',
	headers: {Accept: 'application/json, , application/problem+json'}
};

fetch('/getTransactionByHash/%7Bhash%7D/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"net/http"
	"io"
)

func main() {

	url := "/getTransactionByHash/%7Bhash%7D/"

	req, _ := http.NewRequest("GET", url, nil)

	req.Header.Add("Accept", "application/json, , application/problem+json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {"Transaction":""}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

## qan_getTransactionCount

::wrapper
#text
Returns the number of transactions sent from an address.

### Parameters for "qan_getTransactionCount"

::parameters{in="Path parameters"}
  ::parameter{name="Address" type="string" :required="true"}
  The address from which the transaction count to be checked
  ::
  ::parameter{name="BlockNumber" type="string" :required="true"}
  The block number in hexadecimal or decimal format or the string latest, earliest, pending, safe or finalized (safe and finalized tags are only supported on Ethereum, Gnosis, Arbitrum, Arbitrum Nova and Avalanche C-chain), see the default block parameter description in the official Ethereum documentation
  ::
::

### HTTP response status codes for "qan_getTransactionCount"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_getTransactionCount"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/getTransactionCount/{Address}/{BlockNumber}/" urlType="get"}
  :::tabPanel
  ```sh
  curl --request GET \
	--url /getTransactionCount/%7BAddress%7D/%7BBlockNumber%7D/ \
	--header 'Accept: application/json, , application/problem+json'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'GET',
	headers: {Accept: 'application/json, , application/problem+json'}
};

fetch('/getTransactionCount/%7BAddress%7D/%7BBlockNumber%7D/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"net/http"
	"io"
)

func main() {

	url := "/getTransactionCount/%7BAddress%7D/%7BBlockNumber%7D/"

	req, _ := http.NewRequest("GET", url, nil)

	req.Header.Add("Accept", "application/json, , application/problem+json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {"TransactionCount":"string"}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

## qan_getTransactionReceipt

::wrapper
#text
Returns the receipt of a transaction by transaction hash.

### Parameters for "qan_getTransactionReceipt"

::parameters{in="Path parameters"}
  ::parameter{name="Hash" type="string" :required="true"}
  The hash of a transaction
  ::
::

### HTTP response status codes for "qan_getTransactionReceipt"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_getTransactionReceipt"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/getTransactionReceipt/{Hash}/" urlType="get"}
  :::tabPanel
  ```sh
  curl --request GET \
	--url /getTransactionReceipt/%7BHash%7D/ \
	--header 'Accept: application/json, , application/problem+json'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'GET',
	headers: {Accept: 'application/json, , application/problem+json'}
};

fetch('/getTransactionReceipt/%7BHash%7D/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"net/http"
	"io"
)

func main() {

	url := "/getTransactionReceipt/%7BHash%7D/"

	req, _ := http.NewRequest("GET", url, nil)

	req.Header.Add("Accept", "application/json, , application/problem+json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {"TransactionReceipt":""}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

## qan_getUncleCountByBlockHash

::wrapper
#text
Returns the number of uncles for the block matching the given block hash.

### Parameters for "qan_getUncleCountByBlockHash"

::parameters{in="Path parameters"}
  ::parameter{name="Hash" type="string" :required="true"}
  The hash of the block to get uncles for
  ::
::

### HTTP response status codes for "qan_getUncleCountByBlockHash"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_getUncleCountByBlockHash"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/getUncleCountByBlockHash/{Hash}/" urlType="get"}
  :::tabPanel
  ```sh
  curl --request GET \
	--url /getUncleCountByBlockHash/%7BHash%7D/ \
	--header 'Accept: application/json, , application/problem+json'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'GET',
	headers: {Accept: 'application/json, , application/problem+json'}
};

fetch('/getUncleCountByBlockHash/%7BHash%7D/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"net/http"
	"io"
)

func main() {

	url := "/getUncleCountByBlockHash/%7BHash%7D/"

	req, _ := http.NewRequest("GET", url, nil)

	req.Header.Add("Accept", "application/json, , application/problem+json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {"UncleCount":"string"}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

## qan_getUncleCountByBlockNumber

::wrapper
#text
Returns the number of uncles for the block matching the given block number.

### Parameters for "qan_getUncleCountByBlockNumber"

::parameters{in="Path parameters"}
  ::parameter{name="BlockNumber" type="string" :required="true"}
  The block number in hexadecimal or decimal format or the string latest, earliest, pending, safe or finalized (safe and finalized tags are only supported on Ethereum, Gnosis, Arbitrum, Arbitrum Nova and Avalanche C-chain), see the default block parameter description in the official Ethereum documentation
  ::
::

### HTTP response status codes for "qan_getUncleCountByBlockNumber"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_getUncleCountByBlockNumber"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/getUncleCountByBlockNumber/{BlockNumber}/" urlType="get"}
  :::tabPanel
  ```sh
  curl --request GET \
	--url /getUncleCountByBlockNumber/%7BBlockNumber%7D/ \
	--header 'Accept: application/json, , application/problem+json'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'GET',
	headers: {Accept: 'application/json, , application/problem+json'}
};

fetch('/getUncleCountByBlockNumber/%7BBlockNumber%7D/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"net/http"
	"io"
)

func main() {

	url := "/getUncleCountByBlockNumber/%7BBlockNumber%7D/"

	req, _ := http.NewRequest("GET", url, nil)

	req.Header.Add("Accept", "application/json, , application/problem+json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {"UncleCount":"string"}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

## qan_maxPriorityFeePerGas

::wrapper
#text
Get the priority fee needed to be included in a block.

### HTTP response status codes for "qan_maxPriorityFeePerGas"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_maxPriorityFeePerGas"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/maxPriorityFeePerGas/" urlType="get"}
  :::tabPanel
  ```sh
  curl --request GET \
	--url /maxPriorityFeePerGas/ \
	--header 'Accept: application/json, , application/problem+json'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'GET',
	headers: {Accept: 'application/json, , application/problem+json'}
};

fetch('/maxPriorityFeePerGas/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"net/http"
	"io"
)

func main() {

	url := "/maxPriorityFeePerGas/"

	req, _ := http.NewRequest("GET", url, nil)

	req.Header.Add("Accept", "application/json, , application/problem+json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {"MaxPriorityFeePerGas":"string"}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

## qan_newBlockFilter

::wrapper
#text
Creates a filter in the node, to notify when a new block arrives.

### HTTP response status codes for "qan_newBlockFilter"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_newBlockFilter"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/newBlockFilter/" urlType="get"}
  :::tabPanel
  ```sh
  curl --request GET \
	--url /newBlockFilter/ \
	--header 'Accept: application/json, , application/problem+json'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'GET',
	headers: {Accept: 'application/json, , application/problem+json'}
};

fetch('/newBlockFilter/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"net/http"
	"io"
)

func main() {

	url := "/newBlockFilter/"

	req, _ := http.NewRequest("GET", url, nil)

	req.Header.Add("Accept", "application/json, , application/problem+json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {"FilterId":"string"}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

## qan_newFilter

::wrapper
#text
Creates a filter object, based on filter options, to notify when the state changes (logs).

### HTTP response status codes for "qan_newFilter"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_newFilter"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/newFilter/" urlType="post"}
  :::tabPanel
  ```sh
  curl --request POST \
	--url /newFilter/ \
	--header 'Accept: application/json, , application/problem+json' \
	--header 'Content-Type: application/json' \
	--data '
{
  "FilterObject": {
    "Address": "string",
    "FromBlock": "string",
    "ToBlock": "string",
    "Topics": "array"
  }
}
'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'POST',
	headers: {
		Accept: 'application/json, , application/problem+json',
		'Content-Type': 'application/json'
	},
	body: JSON.stringify({
		FilterObject: {Address: 'string', FromBlock: 'string', ToBlock: 'string', Topics: 'array'}
	})
};

fetch('/newFilter/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"strings"
	"net/http"
	"io"
)

func main() {

	url := "/newFilter/"

	payload := strings.NewReader("{\"FilterObject\":{\"Address\":\"string\",\"FromBlock\":\"string\",\"ToBlock\":\"string\",\"Topics\":\"array\"}}")

	req, _ := http.NewRequest("POST", url, payload)

	req.Header.Add("Accept", "application/json, , application/problem+json")
	req.Header.Add("Content-Type", "application/json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {"FilterId":"string"}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

## qan_newPendingTransactionFilter

::wrapper
#text
Creates a filter in the node to notify when new pending transactions arrive.

### HTTP response status codes for "qan_newPendingTransactionFilter"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_newPendingTransactionFilter"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/newPendingTransactionFilter/" urlType="get"}
  :::tabPanel
  ```sh
  curl --request GET \
	--url /newPendingTransactionFilter/ \
	--header 'Accept: application/json, , application/problem+json'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'GET',
	headers: {Accept: 'application/json, , application/problem+json'}
};

fetch('/newPendingTransactionFilter/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"net/http"
	"io"
)

func main() {

	url := "/newPendingTransactionFilter/"

	req, _ := http.NewRequest("GET", url, nil)

	req.Header.Add("Accept", "application/json, , application/problem+json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {"FilterId":"string"}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

## qan_sendRawTransaction

::wrapper
#text
Creates new message call transaction or a contract creation for signed transactions.

### HTTP response status codes for "qan_sendRawTransaction"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_sendRawTransaction"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/sendRawTransaction/" urlType="post"}
  :::tabPanel
  ```sh
  curl --request POST \
	--url /sendRawTransaction/ \
	--header 'Accept: application/json, , application/problem+json' \
	--header 'Content-Type: application/json' \
	--data '{"Data":"string"}'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'POST',
	headers: {
		Accept: 'application/json, , application/problem+json',
		'Content-Type': 'application/json'
	},
	body: JSON.stringify({Data: 'string'})
};

fetch('/sendRawTransaction/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"strings"
	"net/http"
	"io"
)

func main() {

	url := "/sendRawTransaction/"

	payload := strings.NewReader("{\"Data\":\"string\"}")

	req, _ := http.NewRequest("POST", url, payload)

	req.Header.Add("Accept", "application/json, , application/problem+json")
	req.Header.Add("Content-Type", "application/json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {"TransactionHash":"string"}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

## qan_subscribe

::wrapper
#text
Starts a subscription to a specific event.

### HTTP response status codes for "qan_subscribe"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_subscribe"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/subscribe/" urlType="post"}
  :::tabPanel
  ```sh
  curl --request POST \
	--url /subscribe/ \
	--header 'Accept: application/json, , application/problem+json' \
	--header 'Content-Type: application/json' \
	--data '
{
  "Data": "null",
  "Flag": "boolean",
  "SubscriptionName": "string"
}
'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'POST',
	headers: {
		Accept: 'application/json, , application/problem+json',
		'Content-Type': 'application/json'
	},
	body: JSON.stringify({Data: 'null', Flag: 'boolean', SubscriptionName: 'string'})
};

fetch('/subscribe/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"strings"
	"net/http"
	"io"
)

func main() {

	url := "/subscribe/"

	payload := strings.NewReader("{\"Data\":\"null\",\"Flag\":\"boolean\",\"SubscriptionName\":\"string\"}")

	req, _ := http.NewRequest("POST", url, payload)

	req.Header.Add("Accept", "application/json, , application/problem+json")
	req.Header.Add("Content-Type", "application/json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {"SubscriptionId":"string"}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

## qan_syncing

::wrapper
#text
Returns an object with the sync status of the node if the node is out-of-sync and is syncing. Returns null when the node is already in sync.

### HTTP response status codes for "qan_syncing"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_syncing"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/syncing/" urlType="get"}
  :::tabPanel
  ```sh
  curl --request GET \
	--url /syncing/ \
	--header 'Accept: application/json, , application/problem+json'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'GET',
	headers: {Accept: 'application/json, , application/problem+json'}
};

fetch('/syncing/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"net/http"
	"io"
)

func main() {

	url := "/syncing/"

	req, _ := http.NewRequest("GET", url, nil)

	req.Header.Add("Accept", "application/json, , application/problem+json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {"SyncStatus":""}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

## qan_uninstallFilter

::wrapper
#text
Uninstalls a filter with the given filter id.

### Parameters for "qan_uninstallFilter"

::parameters{in="Path parameters"}
  ::parameter{name="FilterId" type="string" :required="true"}
  The filter ID that needs to be uninstalled. It should always be called when watch is no longer needed. Additionally, Filters timeout when they aren't requested with eth_getFilterChanges for a period of time
  ::
::

### HTTP response status codes for "qan_uninstallFilter"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_uninstallFilter"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/uninstallFilter/{FilterId}/" urlType="get"}
  :::tabPanel
  ```sh
  curl --request GET \
	--url /uninstallFilter/%7BFilterId%7D/ \
	--header 'Accept: application/json, , application/problem+json'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'GET',
	headers: {Accept: 'application/json, , application/problem+json'}
};

fetch('/uninstallFilter/%7BFilterId%7D/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"net/http"
	"io"
)

func main() {

	url := "/uninstallFilter/%7BFilterId%7D/"

	req, _ := http.NewRequest("GET", url, nil)

	req.Header.Add("Accept", "application/json, , application/problem+json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {"Result":"boolean"}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

## qan_unsubscribe

::wrapper
#text
Cancels an existing subscription so that no further events are sent.

### Parameters for "qan_unsubscribe"

::parameters{in="Path parameters"}
  ::parameter{name="SubscriptionId" type="string" :required="true"}
  A subscription ID that was previously generated in a eth_subscribe RPC request
  ::
::

### HTTP response status codes for "qan_unsubscribe"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_unsubscribe"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/unsubscribe/{SubscriptionId}/" urlType="get"}
  :::tabPanel
  ```sh
  curl --request GET \
	--url /unsubscribe/%7BSubscriptionId%7D/ \
	--header 'Accept: application/json, , application/problem+json'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'GET',
	headers: {Accept: 'application/json, , application/problem+json'}
};

fetch('/unsubscribe/%7BSubscriptionId%7D/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"net/http"
	"io"
)

func main() {

	url := "/unsubscribe/%7BSubscriptionId%7D/"

	req, _ := http.NewRequest("GET", url, nil)

	req.Header.Add("Accept", "application/json, , application/problem+json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {"Result":"boolean"}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

## qan_xlinkValid

::wrapper
#text
### HTTP response status codes for "qan_xlinkValid"

<table>
  <thead>
    <tr>
      <th>Status Code</th>
      <th>Description</th>
    </tr>
   </thead>
  <tbody>
    <tr>
      <td>200</td>
      <td>OK</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Bad Request</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Not Found</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Unprocessable Entity</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Internal Server Error</td>
    </tr>
  </tbody>
</table>

#code
### Code samples for "qan_xlinkValid"
::codeBlock{h4="Request examples" :tabs='["cURL", "JavaScript", "Go"]' url="/xlinkValid/" urlType="get"}
  :::tabPanel
  ```sh
  curl --request GET \
	--url /xlinkValid/ \
	--header 'Accept: application/json, , application/problem+json'
  ```
  :::

  :::tabPanel
  ```js
  const options = {
	method: 'GET',
	headers: {Accept: 'application/json, , application/problem+json'}
};

fetch('/xlinkValid/', options)
	.then(response => response.json())
	.then(response => console.log(response))
	.catch(err => console.error(err));
  ```
  :::

  :::tabPanel
  ```go
  package main

import (
	"fmt"
	"net/http"
	"io"
)

func main() {

	url := "/xlinkValid/"

	req, _ := http.NewRequest("GET", url, nil)

	req.Header.Add("Accept", "application/json, , application/problem+json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(string(body))

}
  ```
  :::

::
::codeBlock{h4="Response examples" contentType="application/json" :tabs='[200,400,404,422,500]'}
  :::tabPanel{contentType="application/json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

  :::tabPanel{contentType="application/problem+json"}
  ```js
  {}
  ```
  :::

::
::

