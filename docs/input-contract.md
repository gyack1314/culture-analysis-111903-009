# 合成分析资料契约

所有机构、企业、受访者、交易和事件均为本地合成，不来自新闻所涉真实主体，不声称新闻发生过这些分析问题。

seed.json与同名Parquet是相同原始值的两种载体；actions.json列尚未应用的后续输入动作。inventory.json只记录原件物理摘要和行数，不提供分析结论。时间均含时区或明确日期，金钱字段minor以CNY分计，空值保留未知含义。已有代码只做物理完整性检查，没有估计、预测、方案求解或产品发布功能。

choice_sets按design/task列出alt及price_minor/style/licensed，outside=true为都不选且价格为0，不是普通免费商品。submissions以person/design/task为正式选择键，revision明确替代同键旧提交，draft不参与。chosen_alt必须来自该题集合；未作答保留缺失。respondents定义group、split和bridge，split以person为单位；validation_tasks可检验未见集合，不可用于调模型后自称独立。D-confounded是合法但识别受限的设计：licensed与price同步变化，不是可直接删除的坏数据。scenarios给完整可用备选集合及价格，不提供需求真值；价格单位CNY分，报告支付意愿时须转换并说明是否可识别。
