datafilenamekey_list_from_cohort
################################
Takes a cohort id as a required parameter and returns cloud storage paths to files associated with all the samples in that cohort. Authentication is required. User must have READER or OWNER permissions on the cohort.

**Example**

$ python isb_curl.py "https://api-dot-isb-cgc.appspot.com/_ah/api/cohort_api/v1/datafilenamekey_list_from_cohort?cohort_id={YOUR_COHORT_ID}"

**Request**

HTTP request

GET https://api-dot-isb-cgc.appspot.com/_ah/api/cohort_api/v1/datafilenamekey_list_from_cohort``

**Parameters**

.. csv-table::
	:header: "**Parameter name**", "**Value**", "**Description**"
	:widths: 50, 10, 50

	cohort_id,string,Required.
	pipeline,string,Optional.
	platform,string,Optional.
	token,string,Optional.


Response

If successful, this method returns a response body with the following structure:

.. code-block:: javascript

  {
    "count": string,
    "datafilenamekeys": [string]
  }

.. csv-table::
	:header: "**Parameter name**", "**Value**", "**Description**"
	:widths: 50, 10, 50

	count, string, "Number of data file cloud storage paths returned."
	datafilenamekeys[], list, "List of cloud storage file paths associated with each sample."