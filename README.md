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
We appreciate all contributions to add new projects into OpenMMLab ecosystem.
<!-- Please refer to [CONTRUBUTING.md](https://mmclassification.readthedocs.io/en/latest/community/CONTRIBUTING.html) for the contributing guideline. -->
If you want to add one project into the ecosystem, please edit the `project_index.yaml` and add the related information of the specific project.

The following keys are required to :
- `repo_url`: Github link of the project
- `paper_url`: Paper link of the project(Only add one if have > 1 papers, use `""` if no paper)
- `type`: Type of the ecosystem projects(Choose **one** from Type Table)
- `mmrepos`: Which OpenMMLab projects have been adopted in this project(Choose **one or more** from the MMRepos Table)
- `tags`: Tags of this project(<= 5 item)
- `summary`: One sentence summary of the project(Engi)

### Add New Project into YAML
Please add the information of the specific project with the following example:

```yaml
- repo_url: https://github.com/NVlabs/FAN # repo url
  paper_url: https://arxiv.org/abs/2204.12451 # paper url
  type: Official Implementation # type of the projects
  mmrepos: # used projects of OpenMMLab
    - mmdetection
    - mmsegmentation
  tags: # tags of this projects
    - ICML
    - Vision Transformer
  summary: # Engish/Chinese summary of this projects with one sentence
    zh: Official PyTorch implementation of Fully Attentional Networks
    en: 基于PyTorch的Fully Attentional Networks官方实现
```

### Type Table

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-0lax{text-align:left;vertical-align:top}
</style>
<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax">Chinese</th>
    <th class="tg-0lax">English</th>
    <th class="tg-0lax">Meaning</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">官方实现 </td>
    <td class="tg-0lax">Official Implementation </td>
    <td class="tg-0lax">论文的官方实现 </td>
  </tr>
  <tr>
    <td class="tg-0lax">第三方实现 </td>
    <td class="tg-0lax">Community Implementation </td>
    <td class="tg-0lax">论文的第三方实现 </td>
  </tr>
  <tr>
    <td class="tg-0lax">比赛代码 </td>
    <td class="tg-0lax">Competition </td>
    <td class="tg-0lax">比赛代码 </td>
  </tr>
  <tr>
    <td class="tg-0lax">算法框架 </td>
    <td class="tg-0lax">Library </td>
    <td class="tg-0lax">在 OpenMMLab 之上开发的第三方代码库 </td>
  </tr>
  <tr>
    <td class="tg-0lax">服务 </td>
    <td class="tg-0lax">Service </td>
    <td class="tg-0lax">第三方服务项目，例如 wandb </td>
  </tr>
  <tr>
    <td class="tg-0lax">教程 </td>
    <td class="tg-0lax">Tutorial&nbsp;&nbsp;</td>
    <td class="tg-0lax">基于OpenMMLab开发的教程 </td>
  </tr>
  <tr>
    <td class="tg-0lax">示例 </td>
    <td class="tg-0lax">Demo </td>
    <td class="tg-0lax">基于OpenMMLab设计的Demo </td>
  </tr>
  <tr>
    <td class="tg-0lax">其他 </td>
    <td class="tg-0lax">Others </td>
    <td class="tg-0lax">不在以上分类中的其他项目 </td>
  </tr>
</tbody>
</table>

### MMRepos

- [mmcv](https://github.com/open-mmlab/mmcv): OpenMMLab foundational library for computer vision.
- [mmclassification](https://github.com/open-mmlab/mmclassification): OpenMMLab image classification toolbox and benchmark.
- [mmdetection](https://github.com/open-mmlab/mmdetection): OpenMMLab detection toolbox and benchmark.
- [mmdetection3d](https://github.com/open-mmlab/mmdetection3d): OpenMMLab's next-generation platform for general 3D object detection.
- [mmrotate](https://github.com/open-mmlab/mmrotate): OpenMMLab rotated object detection toolbox and benchmark.
- [mmsegmentation](https://github.com/open-mmlab/mmsegmentation): OpenMMLab semantic segmentation toolbox and benchmark.
- [mmocr](https://github.com/open-mmlab/mmocr): OpenMMLab text detection, recognition, and understanding toolbox.
- [mmpose](https://github.com/open-mmlab/mmpose): OpenMMLab pose estimation toolbox and benchmark.
- [mmhuman3d](https://github.com/open-mmlab/mmhuman3d): OpenMMLab 3D human parametric model toolbox and benchmark.
- [mmselfsup](https://github.com/open-mmlab/mmselfsup): OpenMMLab self-supervised learning toolbox and benchmark.
- [mmrazor](https://github.com/open-mmlab/mmrazor): OpenMMLab model compression toolbox and benchmark.
- [mmfewshot](https://github.com/open-mmlab/mmfewshot): OpenMMLab fewshot learning toolbox and benchmark.
- [mmaction2](https://github.com/open-mmlab/mmaction2): OpenMMLab's next-generation action understanding toolbox and benchmark.
- [mmtracking](https://github.com/open-mmlab/mmtracking): OpenMMLab video perception toolbox and benchmark.
- [mmflow](https://github.com/open-mmlab/mmflow): OpenMMLab optical flow toolbox and benchmark.
- [mmediting](https://github.com/open-mmlab/mmediting): OpenMMLab image and video editing toolbox.
- [mmgeneration](https://github.com/open-mmlab/mmgeneration): OpenMMLab image and video generative models toolbox.
- [mmdeploy](https://github.com/open-mmlab/mmdeploy): OpenMMLab model deployment framework.

## License

This project is released under the [Apache 2.0 license](LICENSE).