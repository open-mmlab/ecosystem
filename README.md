# Ecosystem

English | [简体中文](/README_zh-CN.md)

This project is used to collect the information of all open-source projects built with the OpenMMLab projects. The collected projects will be displayed in the official [OpenMMLab Homepage(WIP)](https://openmmlab.com/codebase/ecosystem)

## File Structure

The data collected in this repo is used for internal analysis and homepage display. The repo has the following file structure:

```python
ecosystem
|-----.pre-commit-config.yaml # configuration of the pre-commit hooks
|-----LICENSE #  license of the project
|-----projects_index.yaml # store the detailed information of each project
|-----README.md # readme file
```

## How to Contribute

We appreciate all contributions to add new projects into OpenMMLab ecosystem.

<!-- Please refer to [CONTRUBUTING.md](https://mmclassification.readthedocs.io/en/latest/community/CONTRIBUTING.html) for the contributing guideline. -->

### Workflow

1. fork and pull the latest OpenMMLab repository (ecosystem)
2. checkout a new branch (do not use master branch for PRs)
3. commit your changes
4. create a PR

### Add New Project into YAML

If you want to add one project into the ecosystem, please edit the `project_index.yaml` and add the related information of the specific project.

The following keys are required to :

- `repo_url`: Github link of the project
- `paper_url`: Paper link of the project(Only add one if have > 1 papers, use `""` if no paper)
- `type`: Type of the ecosystem projects(Choose **one** from Type Table)
- `mmrepos`: Which OpenMMLab projects have been adopted in this project(Choose **one or more** from the MMRepos Table, please pay attention to capitalization)
- `tags`: Tags of this project(\<= 5 item)
- `summary`: One sentence summary of the project(English and Chinese)

Please add the information of the specific project with the following example:

```yaml
- repo_url: https://github.com/NVlabs/FAN # repo url
  paper_url: https://arxiv.org/abs/2204.12451 # paper url
  type: Official Implementation # type of the projects
  mmrepos: # used projects of OpenMMLab
    - MMDetection
    - MMSegmentation
  tags: # tags of this projects
    - ICML
    - Vision Transformer
  summary: # Engish/Chinese summary of this projects with one sentence
    zh: Official PyTorch implementation of Fully Attentional Networks
    en: 基于PyTorch的Fully Attentional Networks官方实现
```

### Validity Check

We use [pre-commit hook](https://pre-commit.com/) that checks and formats for `trailing whitespaces`, `check-yaml`, and use our [openmmlab pre-commit hook](https://github.com/open-mmlab/pre-commit-hooks) for `check-ecosystem-validity`.
The config for a pre-commit hook is stored in [.pre-commit-config](https://github.com/open-mmlab/ecosystem/blob/master/.pre-commit-config.yaml).

After you clone the repository, you will need to install initialize pre-commit hook.

```shell
pip install -U pre-commit
```

From the repository folder

```shell
pre-commit install
```

After this on every commit check code linters and formatter will be enforced.

```{important}
Before you create a PR, make sure that your code lints and is formatted by yapf.
```

### Type Table

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax">Chinese</th>
    <th class="tg-0lax">English</th>
    <th class="tg-0lax">含义</th>
    <th class="tg-0lax">Meaning</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">官方实现 </td>
    <td class="tg-0lax">Official Implementation </td>
    <td class="tg-0lax">论文的官方实现 </td>
    <td class="tg-0lax">Official Implementation of the Research Work </td>
  </tr>
  <tr>
    <td class="tg-0lax">第三方实现 </td>
    <td class="tg-0lax">Community Implementation </td>
    <td class="tg-0lax">论文的第三方实现 </td>
    <td class="tg-0lax">Community Implementation of the Research Work </td>
  </tr>
  <tr>
    <td class="tg-0lax">比赛代码 </td>
    <td class="tg-0lax">Competition </td>
    <td class="tg-0lax">比赛代码 </td>
    <td class="tg-0lax">Open-source Code of the Competition </td>
  </tr>
  <tr>
    <td class="tg-0lax">算法框架 </td>
    <td class="tg-0lax">Library </td>
    <td class="tg-0lax">在 OpenMMLab 之上开发的第三方代码库 </td>
    <td class="tg-0lax">Algorithm Library Built on OpenMMLab </td>
  </tr>
  <tr>
    <td class="tg-0lax">服务 </td>
    <td class="tg-0lax">Service </td>
    <td class="tg-0lax">第三方服务项目，例如 wandb </td>
    <td class="tg-0lax">Service Project, e.g., wandb </td>
  </tr>
  <tr>
    <td class="tg-0lax">教程 </td>
    <td class="tg-0lax">Tutorial&nbsp;&nbsp;</td>
    <td class="tg-0lax">基于OpenMMLab开发的教程 </td>
    <td class="tg-0lax">Tutorial Built on OpenMMLab </td>
  </tr>
  <tr>
    <td class="tg-0lax">示例 </td>
    <td class="tg-0lax">Demo </td>
    <td class="tg-0lax">基于OpenMMLab设计的Demo </td>
    <td class="tg-0lax">Demo Built on OpenMMLab </td>
  </tr>
  <tr>
    <td class="tg-0lax">其他 </td>
    <td class="tg-0lax">Others </td>
    <td class="tg-0lax">不在以上分类中的其他项目 </td>
    <td class="tg-0lax">Projects not in the above Types </td>
  </tr>
</tbody>
</table>

### MMRepos

- [MMCV](https://github.com/open-mmlab/mmcv): OpenMMLab foundational library for computer vision.
- [MMClassification](https://github.com/open-mmlab/mmclassification): OpenMMLab image classification toolbox and benchmark.
- [MMDetection](https://github.com/open-mmlab/mmdetection): OpenMMLab detection toolbox and benchmark.
- [MMDetection3D](https://github.com/open-mmlab/mmdetection3d): OpenMMLab's next-generation platform for general 3D object detection.
- [MMRotate](https://github.com/open-mmlab/mmrotate): OpenMMLab rotated object detection toolbox and benchmark.
- [MMSegmentation](https://github.com/open-mmlab/mmsegmentation): OpenMMLab semantic segmentation toolbox and benchmark.
- [MMOCR](https://github.com/open-mmlab/mmocr): OpenMMLab text detection, recognition, and understanding toolbox.
- [MMPose](https://github.com/open-mmlab/mmpose): OpenMMLab pose estimation toolbox and benchmark.
- [MMHuman3D](https://github.com/open-mmlab/mmhuman3d): OpenMMLab 3D human parametric model toolbox and benchmark.
- [MMSelfSup](https://github.com/open-mmlab/mmselfsup): OpenMMLab self-supervised learning toolbox and benchmark.
- [MMRazor](https://github.com/open-mmlab/mmrazor): OpenMMLab model compression toolbox and benchmark.
- [MMFewShot](https://github.com/open-mmlab/mmfewshot): OpenMMLab fewshot learning toolbox and benchmark.
- [MMAction2](https://github.com/open-mmlab/mmaction2): OpenMMLab's next-generation action understanding toolbox and benchmark.
- [MMTracking](https://github.com/open-mmlab/mmtracking): OpenMMLab video perception toolbox and benchmark.
- [MMFlow](https://github.com/open-mmlab/mmflow): OpenMMLab optical flow toolbox and benchmark.
- [MMEditing](https://github.com/open-mmlab/mmediting): OpenMMLab image and video editing toolbox.
- [MMGeneration](https://github.com/open-mmlab/mmgeneration): OpenMMLab image and video generative models toolbox.
- [MMDeploy](https://github.com/open-mmlab/mmdeploy): OpenMMLab model deployment framework.

## License

This project is released under the [Apache 2.0 license](LICENSE).
