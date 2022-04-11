# Mulesoft API Specification Upload
To automatically publish **'api.yaml'** to Mulesoft Anypoint:
- Create a **Pull Request**
- Add the label **'publish'**
- Ensure the title of the Pull Request matches this format **[0-9].[0-9].[0-9]**

Ensure that the **--apiVersion** argument in **/.github/workflows/main.yml** matches your API major version number in your Semantic Version reference (i.e. 1.x.x).

Your API Specification will uploaded using the repository name as the name of the API and the title of the Pull Request as the API Version.

For more strictly managed API specifications, you may wish to change the versioning method from ${{ github.event.pull_request.title }} to 1.x.${{ github.run_id }}.
This change will result in a unique patch number allowing hard-coding of the major and minor versions in **main.yml** while ensuring that a number (not a letter character) is used for the patch reference.
This is ideal to minimise human error generating manual PR names.
Where granular control over the patch number is required, this is not suitable as there is no control over the number used as the patch reference.
