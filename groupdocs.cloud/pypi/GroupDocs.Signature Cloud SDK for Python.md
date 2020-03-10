Use this REST API to [search, verify & create signatures](https://products.groupdocs.cloud/signature/python) of 6 different types for a [lot of file formats](https://wiki.groupdocs.cloud/signaturecloud/getting-started/supported-document-formats/) from within your Python cloud apps.

## Cloud Document Signing Features

- Supports application of several types of document signatures.
- Create and apply [highly configurable](https://wiki.groupdocs.cloud/signaturecloud/developer-guide/common-resources/signature-options-objects/) signatures.
- Specify pages (even, odd, specific etc.) to apply the signature on.
- Configure page padding options.
- Specify font, color, alignment & other appearance settings for the signature.
- Apply crop settings for the signature background.
- Setting to repeat the signature string to fill the specified area.
- Configure alignment of text string along the barcode type signature.
- Support for various types of brushes to perform signature formatting.
- Apply signature to password-protected documents.
- Perform document signature verification.
- Get or set the time at which the document was digitally signed.
- Option to search some type of signatures from the document.

## Signature Supported File Formats

The following file formats are supported for the barcode, image, QR-code, stamp and text type of signatures:
**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX
**Microsoft Excel:** XLSX, XLS, XLSB, XLSM, XLTX, XLTM
**Microsoft PowerPoint:** PPT, PPTX, PPTM, PPS, PPSM, PPSX, POTX, POTM
**OpenOffice:** ODT, OTT, ODS, OTS, ODP, OTP
**Image:** BMP, GIF, JPG, JPEG, PNG, SVG, TIF, TIFF, WEBP, DJVU
**Metafile:** WMF
**CorelDraw:** CDR, CMX
**Adobe Photoshop:** PSD
**Adobe Acrobat:** PDF

## Digital Signature Supported Formats

**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX
**Microsoft Excel:** XLSX, XLS, XLSB, XLSM, XLTX, XLTM
**OpenOffice:** ODS, OTS
**Adobe Acrobat:** PDF

## FormField Signature Supported Formats

**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX
**Microsoft Excel:** XLSX, XLS, XLSB, XLSM, XLTX, XLTM
**OpenOffice:** ODS, OTS, ODP
**Adobe Acrobat:** PDF

## Metadata Signature Supported Formats

**Microsoft Word:** DOC, DOCM, DOCX, DOT, DOTM, DOTX
**Microsoft Excel:** XLSX, XLS, XLSB, XLSM, XLTX, XLTM
**Microsoft PowerPoint:** PPT, PPTX, PPTM, PPS, PPSM, PPSX, POTX, POTM
**OpenOffice:** ODT, OTT, ODS, OTS, ODP, OTP
**Image:** JPG, JPEG, PNG, SVG, TIF, TIFF
**Adobe Photoshop:** PSD
**Adobe Acrobat:** PDF

## Supported Signature Types

- Text
- Image
- Barcode
- QR-code
- Digital
- Stamp

## Platform Independence

GroupDocs.Signature Cloud's platform independent document manipulation API is a true REST API that can be used from any platform. You can use it with any language or platform that supports REST, be it the web, desktop, mobile, or the cloud. The API integrates with other cloud services to provide you the flexibility you require for processing documents. It is suitable for the most types of businesses, documents, or content.

## Dependencies

- Python 2.7 or 3.4+

## Installation

Install `groupdocs-signature-cloud` with [PIP](https://pypi.org/project/pip/) from [PyPI](https://pypi.org/) by:

`pip install groupdocs-signature-cloud`

Or clone repository and install it via [Setuptools](http://pypi.python.org/pypi/setuptools):

`python setup.py install`

Please create an account at [GroupDocs for Cloud](https://dashboard.groupdocs.cloud/#/apps) and get your application information.

The complete source code is available at the [GitHub Repository](https://github.com/groupdocs-signature-cloud/groupdocs-signature-cloud-python) for other common usage scenarios.

## Getting Started

Please follow the [installation procedure](https://pypi.org/project/groupdocs-signature-cloud/#installation) and then run following:

```python
# Import module
import groupdocs_signature_cloud

# Get your app_sid and app_key at https://dashboard.groupdocs.cloud (free registration is required).
app_sid = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
app_key = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"

# Create instance of the API
api = groupdocs_signature_cloud.InfoApi.from_keys(app_sid, app_key)

try:
    # Retrieve supported file-formats
    response = api.get_supported_file_formats()

    # Print out supported file-formats
    print("Supported file-formats:")
    for format in response.formats:
        print('{0} ({1})'.format(format.file_format, format.extension)) 
except groupdocs_signature_cloud.ApiException as e:
    print("Exception when calling get_supported_file_formats: {0}".format(e.message))
```

## Use Python SDK to Search Barcode Signature in a Spreadsheet at Provided URL

```python
# Import module
from groupdocs_signature_cloud.rest import ApiException
from Common_Utilities.Utils import Common_Utilities
from groupdocs_signature_cloud.models.cells_search_barcode_options_data import CellsSearchBarcodeOptionsData
from groupdocs_signature_cloud.models.requests.post_search_barcode_from_url_request import PostSearchBarcodeFromUrlRequest

class Search_Signature_Barcode_From_Url:

    @staticmethod
    def Post_Search_Signature_Barcode_From_Url():

        try:
            # Getting instance of the API
            api = Common_Utilities.Get_SignatureApi_Instance();

            Url = "https://www.dropbox.com/s/o9k7gweapq8k15l/SignedForVerificationAll.xlsx?dl=1"
            password = ""

            options = CellsSearchBarcodeOptionsData()

            # set barcode properties
            options.barcode_type_name ="Code39Standard"
            options.text = "12345678"
            # set match type
            options.match_type ="Contains"
            #set pages for search
            options.document_page_number = 1

            request = PostSearchBarcodeFromUrlRequest(Url, options, password, Common_Utilities.storage_name)

            response = api.post_search_barcode_from_url(request)

            print("Searched Count: " + str(len(response.signatures)));

        except ApiException as e:
            print("Exception when calling SignatureApi: {0}".format(e.message))
```

## Licensing

GroupDocs.Signature Cloud Python SDK licensed under [MIT License](http://github.com/groupdocs-signature-cloud/groupdocs-signature-cloud-python/LICENSE).

[Product Page](https://products.groupdocs.cloud/signature/python) | [Documentation](https://wiki.groupdocs.cloud/signaturecloud/) | [API Reference](https://apireference.groupdocs.cloud/signature/) | [Code Samples](https://github.com/groupdocs-signature-cloud/groupdocs-signature-cloud-python) | [Blog](https://blog.groupdocs.cloud/category/signature/) | [Free Support](https://forum.groupdocs.cloud/c/signature) | [Free Trial](https://dashboard.groupdocs.cloud/#/apps)