# adobe-pdf-embed-api-tutorial

## Purpose

## Exercise 0: Prepare

### Get Client ID
1. Go to https://www.adobe.io/apis/documentcloud/dcsdk/pdf-embed.html
2. Click on Get Started (https://www.adobe.io/apis/documentcloud/dcsdk/gettingstarted.html)
3. Click on Get Started
4. Under Choose a service, select PDF Embed API.
5. Under Credentials Name, provide a unique name.
6. Under Application Domain, set the domain of where PDF Embed API will be used.
7. Click on Create Credentials.
8. Note down the Client ID. This will be used later.

### Get Documentation
You can access documentation (https://www.adobe.com/go/docsvcs_doc_pdfembed#://) for PDF Embed API.
 
## Exercise 1: Adding PDF Embed API to a Webpage

### Navigate PDF Embed API Demo
1. Navigate to https://www.adobe.io/apis/documentcloud/dcsdk/pdf-embed.html
2. Click Try the Demo.
3. Click the different Embed Modes on the left side bar.
4. Switch back Full Window.
5. Click on annotation tools in top right corner to explore annotations.
6. Click on search button to search in the document.
7. Click the ... menu to show the Download PDF and Print PDF options.
8. Click on Customize button on left sidebar.
9. Toggle different viewer components.
10. Click Generate Code.
11. Copy the this part of the script: `<script src="https://documentcloud.adobe.com/view-sdk/main.js"></script>` code
12. In the files, open the file exercise/index.html.
13. Find the part of the code `<!-- TODO: EXERCISE 1: INSERT EMBED API SCRIPT TAG -->`.
14. After this line, paste the script.
15. Go back to the Embed API Demo and copy `<div id="adobe-dc-view"></div>` code.
16. In index.html, search for `<!-- TODO: EXERCISE 1: INSERT PDF EMBED API CODE  -->`.
17. Paste the `<div id="adobe-dc-view"></div>` code.
18. Go back to the Embed API Demo and copy the following code and paste it into index.html: 
...
<script type="text/javascript">
	document.addEventListener("adobe_dc_view_sdk.ready", function(){ 
		var adobeDCView = new AdobeDC.View({clientId: "<YOUR_CLIENT_ID>", divId: "adobe-dc-view"});
		adobeDCView.previewFile({
			content:{location: {url: "https://documentcloud.adobe.com/view-sdk-demo/PDFs/Bodea Brochure.pdf"}},
			metaData:{fileName: "Bodea Brochure.pdf"}
		}, {});
	});
</script>
...
## Exercise 2: Accessing Analytics APIs

## Exercise 3: Add Interactivity Based on Events