# Ecosystem
This project is used to collect the information of all open-source projects built with the OpenMMLab projects. The collected projects will be displayed in the official [OpenMMLab Homepage](https://openmmlab.com/codebase/ecosystem)

## File Structure
The data collected in this repo is used for internal analysis and homepage display. The repo has the following file structure:

```python
ecosystem
|-----README.md #
|-----projects_index.yaml # store the detailed information of each project
|-----unit_test.py # used for validity check.
```

## How to Contribute
If you want to add one project into the ecosystem, please edit the `project_index.yaml` and add the related information of the specific project.

The following keys are required to :
- `repo_url`: Github link of the project
- `paper_url`: Paper link of the project(Only add one if have > 1 papers), could be arxiv link or other
- `type`: Type of the ecosystem projects
- `mmrepos`: Which OpenMMLab projects have been adopted in this project
- `tags`: Tags of this project
- `summary`: One sentence summary of the project.