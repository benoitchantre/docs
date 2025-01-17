---
title: 为拉取请求配置提交变基
intro: '对于仓库中 {% data variables.product.product_location %} 上的所有拉取请求合并，您可以实施、允许或禁用提交变基。'
redirect_from:
  - /articles/configuring-commit-rebasing-for-pull-requests
  - /github/administering-a-repository/configuring-commit-rebasing-for-pull-requests
  - /github/administering-a-repository/configuring-pull-request-merges/configuring-commit-rebasing-for-pull-requests
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Repositories
shortTitle: 配置提交变基
---

{% data reusables.pull_requests.configure_pull_request_merges_intro %}

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.sidebar-settings %}
3. 在 {% ifversion fpt or ghec or ghes > 3.5 or ghae-issue-6069 %}“拉取请求”{% else %}“合并按钮”{% endif %} 下，选择 **Allow rebase merging（允许变基合并）**。 这将允许贡献者通过将其个人提交变基到基本分支来合并拉取请求。
{% ifversion default-merge-squash-commit-message %}
 ![Screenshot of Pull Request settings with allow rebase merging checkbox emphasized](/assets/images/help/repository/allow-rebase-merging.png){% endif %}{% ifversion ghes = 3.6  %} ![Screenshot of Pull Request settings with allow rebase merging checkbox emphasized](/assets/images/help/repository/allow-rebase-merging-no-dropdown.png){% endif %}
 {% ifversion ghes < 3.6  %}
 ![拉取请求变基提交](/assets/images/help/repository/pr-merge-rebase.png){% endif %}

如果您还选择了另一种合并方法，则贡献者在合并拉取请求时能够选择合并提交的类型。 {% data reusables.repositories.squash-and-rebase-linear-commit-history %}
