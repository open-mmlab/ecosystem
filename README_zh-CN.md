# Ecosystem
[English](/README.md) | 简体中文

本项目用于收录使用了OpenMMLab体系的开源项目，所有收录的项目将会在[OpenMMLab生态项目(WIP)](https://openmmlab.com/codebase/ecosystem)进行展示。

## 文件结构

本项目中的数据与文档按如下方式组织：

```python
ecosystem
|-----.pre-commit-config.yaml # configuration of the pre-commit hooks
|-----LICENSE #  license of the project
|-----projects_index.yaml # store the detailed information of each project
|-----README.md # readme file
```

## 如何贡献代码

我们非常感谢所有为生态项目贡献数据和信息的Contributor。

<!-- We appreciate all contributions to add new projects into OpenMMLab ecosystem. -->
<!-- Please refer to [CONTRUBUTING.md](https://mmclassification.readthedocs.io/en/latest/community/CONTRIBUTING.html) for the contributing guideline. -->

### 工作流

1. fork and pull the latest OpenMMLab repository (ecosystem)
2. checkout a new branch (do not use master branch for PRs)
3. commit your changes
4. create a PR

### 在YAML文件增加一个项目

如果你想在把某个项目加入OpenMMLab生态体系，请编辑 `project_index.yaml`并添加具体项目的相关信息

下面的信息是必须要提供的
- `repo_url`: 项目的Github/Gitee链接。
- `paper_url`: 项目涉及的论文的链接(如果有多篇论文，添加一篇即可，如果没有论文则赋值为`""`。)
- `type`: 项目类型(请从下边的类别列表中选 **一个**)
- `mmrepos`: 使用到了哪些OpenMMLab的开源算法库(从MMRepos Table下面 **选一个或多个** 请注意大小写)
- `tags`: 为项目的增加Tag(不超过5个)
- `summary`: 项目的一句话总结(English and Chinese)

请参考如下的例子添加一个项目的相关信息
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

### 格式检查与合法性检查
我们使用 [pre-commit hook](https://pre-commit.com/) 来检查格式`trailing whitespaces`, `check-yaml`, 使用 [openmmlab pre-commit hook](https://github.com/open-mmlab/pre-commit-hooks) 的 `check-ecosystem-validity`来检查字段的合法性.
相关的配置文件定义在 [.pre-commit-config](https://github.com/open-mmlab/ecosystem/blob/master/.pre-commit-config.yaml).

当你克隆了项目之后，你需要安装pre-commit hook.
```shell
pip install -U pre-commit
```

在项目内执行
```shell
pre-commit install
```

每一次commit的时候，pre-commit会进行格式检查和合法性检查
```{important}
每次创建PR时，请确保代码的格式和合法性通过了检查
```

### 项目类型列表

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