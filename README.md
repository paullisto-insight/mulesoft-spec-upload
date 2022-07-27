# Mulesoft API Specification Upload

To automatically publish **'api.yaml'** to Mulesoft Anypoint:
- Create a **Release**
- Ensure the that the Tag of the Release matches this format **[0-9].[0-9].[0-9]**
- Add a Name, Description and Publish.

Ensure that the **--apiVersion** argument in **/.github/workflows/main.yml** matches your API major version number in your Semantic Version reference (i.e. 1.x.x).

Your API Specification will uploaded using the repository name as the name of the API and the Tag_Name of the Release as the API Version.
