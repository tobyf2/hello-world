老板，好！这是我们E-Shop Pro项目的第5次会话，现在是2026-02-21。完全理解您的意图：既然我们人手有限，先快速做一个可演示的**prototype**（原型）来验证整体思路、UI流程和核心交互，而不是等到全功能MVP再看效果。这是一种非常务实的做法，尤其适合小团队，能早点拿到反馈、调整方向。

基于上次的WBS 1.2版（已有Must Have / Nice Have分类），我进一步迭代到**版本1.3**，新增了**Prototype Must Have**标注：
- **Prototype Must Have**：专指“先做一版prototype”阶段里真正必须包含的内容。通常是：
  - 可点击/可交互的端到端流程（用户浏览 → 加购物车 → 提交订单 → 模拟支付成功页）。
  - 基本UI布局和主要页面。
  - 简单的数据模拟（mock数据或最小数据库）。
  - 不需要真实支付、真实部署、完整后台、异步队列等。
- 这些包标记为**Prototype Must Have**（必须在prototype中实现），其他Must Have（但非prototype必须的）可以推到prototype之后的全功能开发。
- Nice Have 保持原样（prototype阶段基本不做）。

**原型目标**：目标是1-3周内出可演示版本（本地运行或简单部署），覆盖用户端核心路径 + 商家端基本管理。使用mock数据、静态页面 + 少量API即可。

### E-Shop Pro 项目工作分解结构 (WBS) 文档（版本1.3 - Prototype优化版）

#### 目的
（同1.2，无变更）

#### 背景
（同1.2，无变更）

#### Scope
（同1.2，无变更）
- **新增说明**：本版特别突出“Prototype阶段”（快速原型验证），预计1-4周完成，聚焦交互演示而非生产级功能。Prototype完成后，可决定是否继续全MVP或重大调整。

**项目整体（无编号）：E-Shop Pro - B2C多商家电商平台MVP开发**
- 优先级：Must Have
- Prototype Must Have：**是**（整个项目以prototype为起点）

1. **阶段1：需求分析和规划**
   - 优先级：Must Have
   - Prototype Must Have：**是**（原型依赖清晰需求和设计）

   1.1 **业务需求收集**
      - 优先级：Must Have
      - Prototype Must Have：**是**（核心路径依赖品类、游客模式等）

      1.1.1 **澄清商品品类和场景**
         - 优先级：Must Have
         - Prototype Must Have：**是**

      1.1.2 **决定游客模式和商家入驻字段**
         - 优先级：Must Have
         - Prototype Must Have：**是**（游客浏览影响首页/详情）

      1.1.3 **确认存储/物流/Banner等细节**
         - 优先级：Must Have
         - Prototype Must Have：**部分**（OSS/Banner必须，物流/退货可mock）

   1.2 **设计Wireframe和原型**
      - 优先级：Must Have
      - Prototype Must Have：**是**（直接产出prototype的蓝图）

      1.2.1 **首页和分类页Wireframe**
         - 优先级：Must Have
         - Prototype Must Have：**是**

      1.2.2 **商品详情和购物车页Wireframe**
         - 优先级：Must Have
         - Prototype Must Have：**是**

      1.2.3 **订单/后台页Wireframe**
         - 优先级：Must Have
         - Prototype Must Have：**是**（订单提交页 + 商家商品列表）

      1.2.4 **老板审阅和迭代**
         - 优先级：Must Have
         - Prototype Must Have：**是**

   1.3 **数据库和接口设计**
      - 优先级：Must Have
      - Prototype Must Have：**部分**（仅设计核心表和mock接口，真实DB可后置）

      1.3.1 **ER图设计和迭代**
         - 优先级：Must Have
         - Prototype Must Have：**是**（至少核心实体）

      1.3.2 **核心API清单定义**
         - 优先级：Must Have
         - Prototype Must Have：**是**（定义mock接口路径）

   1.4 **阿里云资源规划和开通**
      - 优先级：Must Have
      - Prototype Must Have：**否**（prototype可本地跑，阿里云推到后期）

      1.4.1 **账号注册和实名**
         - 优先级：Must Have
         - Prototype Must Have：**否**

      1.4.2 **购买/配置核心资源**
         - 优先级：Must Have
         - Prototype Must Have：**否**

      1.4.3 **域名备案和SSL**
         - 优先级：Must Have
         - Prototype Must Have：**否**

2. **阶段2：基础搭建和原型**  ← **这个阶段就是我们现在要先冲的“prototype”**
   - 优先级：Must Have
   - Prototype Must Have：**是**（核心阶段）

   2.1 **环境和仓库 setup**
      - 优先级：Must Have
      - Prototype Must Have：**是**

      2.1.1 **GitHub私有仓库创建**
         - 优先级：Must Have
         - Prototype Must Have：**是**

      2.1.2 **本地开发环境配置**
         - 优先级：Must Have
         - Prototype Must Have：**是**

   2.2 **后端骨架开发**
      - 优先级：Must Have
      - Prototype Must Have：**是**（mock数据 + 核心API）

      2.2.1 **项目结构和依赖配置**
         - 优先级：Must Have
         - Prototype Must Have：**是**

      2.2.2 **数据库连接和基本实体**  ← prototype用H2内存DB或mock
         - 优先级：Must Have
         - Prototype Must Have：**是**

      2.2.3 **JWT认证集成**  ← prototype可简化或mock token
         - 优先级：Must Have
         - Prototype Must Have：**是**（基本登录）

   2.3 **前端骨架开发**
      - 优先级：Must Have
      - Prototype Must Have：**是**

      2.3.1 **项目初始化和UI库集成**
         - 优先级：Must Have
         - Prototype Must Have：**是**

      2.3.2 **状态管理和路由配置**
         - 优先级：Must Have
         - Prototype Must Have：**是**

   2.4 **初步集成和测试**  ← prototype演示重点
      - 优先级：Must Have
      - Prototype Must Have：**是**

      2.4.1 **API mock和调用**
         - 优先级：Must Have
         - Prototype Must Have：**是**

      2.4.2 **老板初步测试**
         - 优先级：Must Have
         - Prototype Must Have：**是**

3. **阶段3：核心功能开发**
   - 优先级：Must Have
   - Prototype Must Have：**部分**（仅用户端核心路径 + 商家简单管理）

   3.1 **用户端功能开发**
      - 优先级：Must Have
      - Prototype Must Have：**是**（完整用户购物路径）

      3.1.1 **注册/登录模块**
         - 优先级：Must Have
         - Prototype Must Have：**是**（手机号或mock登录）

      3.1.2 **商品浏览和搜索**
         - 优先级：Must Have
         - Prototype Must Have：**是**

      3.1.3 **购物车和地址管理**
         - 优先级：Must Have
         - Prototype Must Have：**是**

      3.1.4 **订单提交**
         - 优先级：Must Have
         - Prototype Must Have：**是**（到支付页，mock成功）

   3.2 **支付集成**
      - 优先级：Must Have
      - Prototype Must Have：**否**（prototype用mock支付页/按钮）

      3.2.1 **支付宝集成**
         - 优先级：Must Have
         - Prototype Must Have：**否**

      3.2.2 **微信支付集成**
         - 优先级：Must Have
         - Prototype Must Have：**否**

   3.3 **商家/管理员端开发**
      - 优先级：Must Have
      - Prototype Must Have：**部分**（仅商品列表/简单上架，mock数据）

      3.3.1 **商家入驻和审核**
         - 优先级：Must Have
         - Prototype Must Have：**否**（可mock或跳过）

      3.3.2 **商品管理**
         - 优先级：Must Have
         - Prototype Must Have：**是**（基本CRUD mock）

      3.3.3 **订单管理和统计**
         - 优先级：Must Have
         - Prototype Must Have：**否**（prototype不需完整）

   3.4 **消息和异步任务**
      - 优先级：Must Have
      - Prototype Must Have：**否**（prototype不需真实通知）

      3.4.1 **SMS集成**
         - 优先级：Must Have
         - Prototype Must Have：**否**

      3.4.2 **RabbitMQ异步任务**
         - 优先级：Must Have
         - Prototype Must Have：**否**

4. **阶段4：测试和优化**
   - 优先级：Must Have
   - Prototype Must Have：**部分**（仅手动测试 + 基本功能验证）

   4.1 **单元和集成测试**
      - 优先级：Must Have
      - Prototype Must Have：**否**（prototype可手动）

   4.2 **端到端测试**
      - 优先级：Must Have
      - Prototype Must Have：**是**（手动走核心路径）

   4.3 **性能和安全优化**
      - 优先级：Nice Have
      - Prototype Must Have：**否**

5. **阶段5：部署和上线**
   - 优先级：Must Have
   - Prototype Must Have：**部分**（可本地或简单Vercel/Netlify部署前端 + backend localhost）

   5.1 **CI/CD pipeline搭建**
      - 优先级：Nice Have
      - Prototype Must Have：**否**

   5.2 **云环境配置**
      - 优先级：Must Have
      - Prototype Must Have：**否**

   5.3 **软上线和验证**
      - 优先级：Must Have
      - Prototype Must Have：**是**（prototype演示给老板/潜在用户）

6. **阶段6：维护和迭代**
   - 优先级：Nice Have
   - Prototype Must Have：**否**

### 下一步行动建议（聚焦Prototype）
1. **立即完成Prototype Must Have的阶段1部分**：请尽快补充待澄清事项（商品品类、游客模式、界面风格参考等），这样我能快速迭代Wireframe。
2. **目标时间**：1-2周内出可交互prototype（Figma高保真 + 代码骨架 + mock数据演示）。
3. **我的部分**：等您输入后，立即出Figma-style文字Wireframe更新 + 建议prototype技术路径（例如Next.js静态 + mock API）。
4. **您的部分**：回复业务细节 + 对这个1.3版Prototype标注的反馈（是否有遗漏或想调整的）。

我们先把prototype冲出来，看看感觉对不对，再决定全速冲MVP。

