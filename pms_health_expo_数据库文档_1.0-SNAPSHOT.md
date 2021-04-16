# fire数据库文档

**数据库名：** pms_health_expo

**文档版本：** 1.0-SNAPSHOT

**文档描述：** 数据库文档生成

#### 目录

| 表名                  | 说明       |
| :-------------------- | :--------- |
| [jpress_content](#jpress_content) |  |
| [jpress_mapping](#jpress_mapping) |  |
| [jpress_taxonomy](#jpress_taxonomy) |  |
| [tb_accusat_info](#tb_accusat_info) | 投诉建议 |
| [tb_bank_access_log](#tb_bank_access_log) | 华夏银行支付接口访问日志 |
| [tb_base_attachment_file](#tb_base_attachment_file) |  |
| [tb_bas_change_log](#tb_bas_change_log) | 药品目录及药品字段变更记录 |
| [tb_bas_org_address](#tb_bas_org_address) | 收货地址表 |
| [tb_bas_org_bank_account](#tb_bas_org_bank_account) | 机构银行账户表 |
| [tb_bas_org_mapping](#tb_bas_org_mapping) | 机构对应表（采购需求发布，供求关系） |
| [tb_bas_org_prod_price](#tb_bas_org_prod_price) | 商品价格维护表 |
| [tb_bas_org_sub_account](#tb_bas_org_sub_account) | 机构银行子账号 |
| [tb_bas_procurer](#tb_bas_procurer) | 区域设置-采购方临时表 |
| [tb_bas_product](#tb_bas_product) | 采购商品表 |
| [tb_bas_product_biz_price](#tb_bas_product_biz_price) | 商品业务价格表 |
| [tb_bas_product_copy](#tb_bas_product_copy) | 采购商品表 |
| [tb_bas_product_directory](#tb_bas_product_directory) | 商品目录表 |
| [tb_bas_product_directory_copy](#tb_bas_product_directory_copy) | 商品目录表 |
| [tb_bas_product_draft](#tb_bas_product_draft) | 采购商品草稿表 |
| [tb_bas_product_group](#tb_bas_product_group) | 采购竞价组 |
| [tb_bas_product_group_bidding_log](#tb_bas_product_group_bidding_log) | 竞价组商品修改历史 |
| [tb_bas_product_group_copy](#tb_bas_product_group_copy) | 采购竞价组 |
| [tb_bas_product_group_mapping](#tb_bas_product_group_mapping) | 竞价组商品对应关系表 |
| [tb_bas_product_group_mapping_copy](#tb_bas_product_group_mapping_copy) | 竞价组商品对应关系表 |
| [tb_bas_product_license](#tb_bas_product_license) | 产品证照表 |
| [tb_bas_product_license_draft](#tb_bas_product_license_draft) | 产品证照表_草稿 |
| [tb_bas_product_medicare_price](#tb_bas_product_medicare_price) | 商品医保支付价格表 |
| [tb_bas_product_org_mapping](#tb_bas_product_org_mapping) | 机构自选商品表 |
| [tb_bas_product_price](#tb_bas_product_price) | 商品最低价和医保支付价格表 |
| [tb_bas_product_supplier_mapping](#tb_bas_product_supplier_mapping) | 商品和生产厂家投标企业对应关系表 |
| [tb_bas_product_supplier_mapping_draft](#tb_bas_product_supplier_mapping_draft) | 商品和生产厂家投标企业对应关系草稿表 |
| [tb_bas_supplier](#tb_bas_supplier) | 区域设置-供应商临时表 |
| [tb_bas_temp_procurer](#tb_bas_temp_procurer) |  |
| [tb_bas_temp_supplier](#tb_bas_temp_supplier) |  |
| [tb_battlefield_report](#tb_battlefield_report) |  |
| [tb_bidd_convert_price](#tb_bidd_convert_price) | 竞价折算价表 |
| [tb_bidd_det](#tb_bidd_det) | 报价文件明细 |
| [tb_bidd_main](#tb_bidd_main) | 报价文件主表 |
| [tb_bnsjfxbg](#tb_bnsjfxbg) | 不良事件分析报告 |
| [tb_comm_file](#tb_comm_file) | 业务对应文件关系表 |
| [tb_deliver_det](#tb_deliver_det) | 发货单明细表 |
| [tb_deliver_main](#tb_deliver_main) | 发货单主表 |
| [tb_dfs_acl_rule](#tb_dfs_acl_rule) | 文件系统的访问权限控制 |
| [tb_dfs_bucket](#tb_dfs_bucket) | 存储空间 |
| [tb_dfs_file](#tb_dfs_file) | 文件信息 |
| [tb_expo_activity](#tb_expo_activity) |  |
| [tb_expo_activity_apply](#tb_expo_activity_apply) | 现场活动登记表 |
| [tb_expo_advert_position](#tb_expo_advert_position) | 广告位表管理表 |
| [tb_expo_area](#tb_expo_area) | 展区表 |
| [tb_expo_area_relation](#tb_expo_area_relation) | 展区分配表 |
| [tb_expo_audience](#tb_expo_audience) | 观众基础信息 |
| [tb_expo_booth](#tb_expo_booth) | 展位表 |
| [tb_expo_booth_copy1](#tb_expo_booth_copy1) | 展位表 |
| [tb_expo_booth_exhibitor](#tb_expo_booth_exhibitor) | 展位分配表 |
| [tb_expo_contact_us](#tb_expo_contact_us) | 展会联系我们信息表 |
| [tb_expo_curator](#tb_expo_curator) | 馆长管理表 |
| [tb_expo_dealer](#tb_expo_dealer) | 经销商基本信息表 |
| [tb_expo_exhibitor](#tb_expo_exhibitor) | 展商基础信息表 |
| [tb_expo_exhibitor_apply](#tb_expo_exhibitor_apply) | 展商信息登记申请表 |
| [tb_expo_exhibitor_copy2](#tb_expo_exhibitor_copy2) | 展商基础信息表 |
| [tb_expo_forum](#tb_expo_forum) | 展会论坛表 |
| [tb_expo_forum_agenda](#tb_expo_forum_agenda) | 论坛议程表 |
| [tb_expo_forum_focus](#tb_expo_forum_focus) | 论坛关注表 |
| [tb_expo_forum_guest](#tb_expo_forum_guest) | 论坛嘉宾 |
| [tb_expo_forum_order](#tb_expo_forum_order) | 报名论坛订单表 |
| [tb_expo_guest](#tb_expo_guest) | 展会嘉宾 |
| [tb_expo_guest_plan](#tb_expo_guest_plan) | 展会嘉宾计划安排表 |
| [tb_expo_guest_trip](#tb_expo_guest_trip) | 嘉宾计划安排子行程表 |
| [tb_expo_hall_hotel](#tb_expo_hall_hotel) |  |
| [tb_expo_hotel](#tb_expo_hotel) |  |
| [tb_expo_hotel_picture](#tb_expo_hotel_picture) |  |
| [tb_expo_hotel_room](#tb_expo_hotel_room) | 酒店房型 |
| [tb_expo_inauguration_staff](#tb_expo_inauguration_staff) | 开幕式人员 |
| [tb_expo_industry](#tb_expo_industry) | 所属行业 |
| [tb_expo_industry_field](#tb_expo_industry_field) | 行业领域 |
| [tb_expo_industry_field_focus](#tb_expo_industry_field_focus) | 关注行业领域表 |
| [tb_expo_info](#tb_expo_info) | 展会届期信息 |
| [tb_expo_invoice_info](#tb_expo_invoice_info) | 展商开票信息表 |
| [tb_expo_lab_switch](#tb_expo_lab_switch) | 开关管理表 |
| [tb_expo_media](#tb_expo_media) | 媒体基础信息表 |
| [tb_expo_message_board](#tb_expo_message_board) | 访客留言 |
| [tb_expo_newproduct](#tb_expo_newproduct) | 新品推介表 |
| [tb_expo_product_introduce](#tb_expo_product_introduce) | 产品推介会报名表 |
| [tb_expo_product_introduce_source](#tb_expo_product_introduce_source) | 产品推介会信息表 |
| [tb_expo_program](#tb_expo_program) | 项目推介表 |
| [tb_expo_question_answer](#tb_expo_question_answer) | 百问百答表 |
| [tb_expo_reg_accompany](#tb_expo_reg_accompany) | 报名随行登记表 |
| [tb_expo_reg_accompany_copy1](#tb_expo_reg_accompany_copy1) | 报名随行登记表 |
| [tb_expo_reg_audience](#tb_expo_reg_audience) | 观众报名信息 |
| [tb_expo_reg_audience_channel](#tb_expo_reg_audience_channel) | 观众报名信息-获知渠道关系表 |
| [tb_expo_reg_dealer](#tb_expo_reg_dealer) | 经销商报名管理表 |
| [tb_expo_reg_employee_card](#tb_expo_reg_employee_card) | 工作证申办表 |
| [tb_expo_reg_exhibitor](#tb_expo_reg_exhibitor) | 参展商登记信息 |
| [tb_expo_reg_exhibitor_channel](#tb_expo_reg_exhibitor_channel) | 展商报名信息-获知渠道关系表 |
| [tb_expo_reg_exhibitor_next](#tb_expo_reg_exhibitor_next) | 参展商下一届登记信息 |
| [tb_expo_reg_exhibitor_prod](#tb_expo_reg_exhibitor_prod) | 参展商登记商品信息表 |
| [tb_expo_reg_exhibitor_purpose](#tb_expo_reg_exhibitor_purpose) | 展商报名信息-参与目的关系表 |
| [tb_expo_reg_media](#tb_expo_reg_media) | 媒体登记信息 |
| [tb_expo_reg_product_introduce](#tb_expo_reg_product_introduce) | 产品推介会信息表 |
| [tb_expo_reg_product_introduce_mapping](#tb_expo_reg_product_introduce_mapping) | 产品推介会报名关系表 |
| [tb_expo_reg_travel](#tb_expo_reg_travel) | 旅游报名登记表 |
| [tb_expo_source](#tb_expo_source) | 资源管理 |
| [tb_expo_tag](#tb_expo_tag) | 标记 |
| [tb_expo_tag_relation](#tb_expo_tag_relation) | 标记关联表 |
| [tb_expo_ticket](#tb_expo_ticket) | 展会入场二维码表 |
| [tb_expo_ticket2_backups](#tb_expo_ticket2_backups) | 展会入场二维码表 |
| [tb_expo_transportation_guide](#tb_expo_transportation_guide) | 交通指南 |
| [tb_finance_account_det](#tb_finance_account_det) | 财务账款明细表 |
| [tb_finance_account_main](#tb_finance_account_main) | 财务账款主表 |
| [tb_invoice_title](#tb_invoice_title) | 增票资质表 |
| [tb_job_qrtz_blob_triggers](#tb_job_qrtz_blob_triggers) |  |
| [tb_job_qrtz_calendars](#tb_job_qrtz_calendars) |  |
| [tb_job_qrtz_cron_triggers](#tb_job_qrtz_cron_triggers) |  |
| [tb_job_qrtz_fired_triggers](#tb_job_qrtz_fired_triggers) |  |
| [tb_job_qrtz_job_details](#tb_job_qrtz_job_details) |  |
| [tb_job_qrtz_locks](#tb_job_qrtz_locks) |  |
| [tb_job_qrtz_paused_trigger_grps](#tb_job_qrtz_paused_trigger_grps) |  |
| [tb_job_qrtz_scheduler_state](#tb_job_qrtz_scheduler_state) |  |
| [tb_job_qrtz_simple_triggers](#tb_job_qrtz_simple_triggers) |  |
| [tb_job_qrtz_simprop_triggers](#tb_job_qrtz_simprop_triggers) |  |
| [tb_job_qrtz_triggers](#tb_job_qrtz_triggers) |  |
| [tb_job_qrtz_trigger_group](#tb_job_qrtz_trigger_group) |  |
| [tb_job_qrtz_trigger_info](#tb_job_qrtz_trigger_info) |  |
| [tb_job_qrtz_trigger_log](#tb_job_qrtz_trigger_log) |  |
| [tb_job_qrtz_trigger_logglue](#tb_job_qrtz_trigger_logglue) |  |
| [tb_job_qrtz_trigger_registry](#tb_job_qrtz_trigger_registry) |  |
| [tb_mq_error_message](#tb_mq_error_message) | MQ死信消息表 |
| [tb_open_relation](#tb_open_relation) | 机构开户关系表 |
| [tb_order_det](#tb_order_det) | 供应商订单明细 |
| [tb_order_draft](#tb_order_draft) | 采购订单草稿明细 |
| [tb_order_main](#tb_order_main) | 供应商订单主表 |
| [tb_order_org_address](#tb_order_org_address) | 订单收货地址表 |
| [tb_order_plan](#tb_order_plan) | 采购订单方案(自动生成) |
| [tb_order_product_his](#tb_order_product_his) | 供应商采购历史表 |
| [tb_org_business_scope](#tb_org_business_scope) | 机构经营范围表 |
| [tb_pay_det](#tb_pay_det) | 支付结果表 |
| [tb_pay_main](#tb_pay_main) | 支付申请表 |
| [tb_procure_area](#tb_procure_area) |  |
| [tb_qfx_data_source](#tb_qfx_data_source) | 查询框架数据源 |
| [tb_qfx_query_info](#tb_qfx_query_info) | 查询信息 |
| [tb_qfx_revision_his](#tb_qfx_revision_his) |  |
| [tb_qfx_template](#tb_qfx_template) | 查询模版（参数） |
| [tb_reconcilia_account](#tb_reconcilia_account) | 交易对账结果表 |
| [tb_refund_dedu_info](#tb_refund_dedu_info) | 退货抵扣表 |
| [tb_refund_det](#tb_refund_det) | 退货申请明细 |
| [tb_refund_main](#tb_refund_main) | 退货申请表 |
| [tb_req_bidd_mapping](#tb_req_bidd_mapping) | 需求竞价映射表 |
| [tb_req_det](#tb_req_det) | 采购需求明细 |
| [tb_req_main](#tb_req_main) | 采购需求主表 |
| [tb_req_supplier](#tb_req_supplier) | 需求指定供应商表 |
| [tb_req_supplier_draft](#tb_req_supplier_draft) | 需求指定供应商草稿表 |
| [tb_req_template](#tb_req_template) | 采购需求模板主表 |
| [tb_req_template_det](#tb_req_template_det) | 采购需求模板明细 |
| [tb_rp_bidding_demand](#tb_rp_bidding_demand) |  |
| [tb_rp_bidding_demand_medical_org](#tb_rp_bidding_demand_medical_org) |  |
| [tb_rp_bidding_summary](#tb_rp_bidding_summary) |  |
| [tb_rp_bidding_summary_supply_org](#tb_rp_bidding_summary_supply_org) |  |
| [tb_rp_drug_area_trans](#tb_rp_drug_area_trans) |  |
| [tb_rp_drug_quality_level](#tb_rp_drug_quality_level) |  |
| [tb_rp_drug_quality_level_detail](#tb_rp_drug_quality_level_detail) |  |
| [tb_rp_drug_summarize](#tb_rp_drug_summarize) |  |
| [tb_rp_drug_summarize_detail](#tb_rp_drug_summarize_detail) |  |
| [tb_rp_drug_summarize_month](#tb_rp_drug_summarize_month) |  |
| [tb_rp_hospital_supervise_city](#tb_rp_hospital_supervise_city) |  |
| [tb_rp_hospital_supervise_transaction_summary](#tb_rp_hospital_supervise_transaction_summary) |  |
| [tb_rp_hospital_supervise_turnover](#tb_rp_hospital_supervise_turnover) |  |
| [tb_rp_hospital_supervise_type](#tb_rp_hospital_supervise_type) |  |
| [tb_rp_medical_area](#tb_rp_medical_area) |  |
| [tb_rp_medical_fund_detail](#tb_rp_medical_fund_detail) |  |
| [tb_rp_money_flow](#tb_rp_money_flow) |  |
| [tb_rp_order_amount](#tb_rp_order_amount) |  |
| [tb_rp_order_amount_org](#tb_rp_order_amount_org) |  |
| [tb_rp_order_cancel](#tb_rp_order_cancel) |  |
| [tb_rp_order_cancel_detail](#tb_rp_order_cancel_detail) |  |
| [tb_rp_order_coverage_rate](#tb_rp_order_coverage_rate) |  |
| [tb_rp_order_coverage_rate_detail](#tb_rp_order_coverage_rate_detail) |  |
| [tb_rp_order_replace](#tb_rp_order_replace) | 订单监管-异常订单替换率 |
| [tb_rp_order_replace_detail](#tb_rp_order_replace_detail) | 订单监管-异常订单替换率-明细 |
| [tb_rp_order_unconfirm](#tb_rp_order_unconfirm) |  |
| [tb_rp_order_unconfirm_detail](#tb_rp_order_unconfirm_detail) |  |
| [tb_rp_order_undelivery](#tb_rp_order_undelivery) |  |
| [tb_rp_order_undelivery_detail](#tb_rp_order_undelivery_detail) |  |
| [tb_rp_procurer_coverage_rate](#tb_rp_procurer_coverage_rate) |  |
| [tb_rp_procurer_coverage_rate_detail](#tb_rp_procurer_coverage_rate_detail) |  |
| [tb_rp_return_goods_medical_detail](#tb_rp_return_goods_medical_detail) |  |
| [tb_rp_return_goods_medical_org](#tb_rp_return_goods_medical_org) |  |
| [tb_rp_return_goods_summary](#tb_rp_return_goods_summary) |  |
| [tb_rp_return_goods_supply_detail](#tb_rp_return_goods_supply_detail) |  |
| [tb_rp_return_goods_supply_org](#tb_rp_return_goods_supply_org) |  |
| [tb_rp_supplier_supervise_monthly_tran_summary](#tb_rp_supplier_supervise_monthly_tran_summary) |  |
| [tb_rp_supplier_supervise_proportion](#tb_rp_supplier_supervise_proportion) |  |
| [tb_rp_supplier_supervise_vote](#tb_rp_supplier_supervise_vote) | 机构评价监管表 |
| [tb_rp_supplier_timely](#tb_rp_supplier_timely) |  |
| [tb_security_code](#tb_security_code) | 安全验证码 |
| [tb_settle_main](#tb_settle_main) | 结算表 |
| [tb_sms_record](#tb_sms_record) | 短信消息记录 |
| [tb_supervise_manage_area](#tb_supervise_manage_area) |  |
| [tb_supplier_delivery_area](#tb_supplier_delivery_area) |  |
| [tb_sys_app](#tb_sys_app) |  |
| [tb_sys_application](#tb_sys_application) |  |
| [tb_sys_bidd_formula_det](#tb_sys_bidd_formula_det) | 竞价公式明细表 |
| [tb_sys_bidd_formula_main](#tb_sys_bidd_formula_main) | 竞价公式主表 |
| [tb_sys_bidd_target](#tb_sys_bidd_target) | 竞价指标表 |
| [tb_sys_dict](#tb_sys_dict) | 字典表 |
| [tb_sys_log](#tb_sys_log) | 日志表 |
| [tb_sys_message](#tb_sys_message) | 短信发送记录表 |
| [tb_sys_org](#tb_sys_org) | 机构表 |
| [tb_sys_org_account](#tb_sys_org_account) | 单位账户表 |
| [tb_sys_org_att](#tb_sys_org_att) | 机构信息附件表 |
| [tb_sys_org_balance_logs](#tb_sys_org_balance_logs) | 机构账户余额变化日志表 |
| [tb_sys_org_balance_recharge](#tb_sys_org_balance_recharge) | 机构账户充值记录 |
| [tb_sys_org_balance_withdraw](#tb_sys_org_balance_withdraw) | 机构账户提现记录 |
| [tb_sys_org_change_request](#tb_sys_org_change_request) | 机构表 |
| [tb_sys_org_enter](#tb_sys_org_enter) |  |
| [tb_sys_org_enter_att](#tb_sys_org_enter_att) |  |
| [tb_sys_org_license_type_mapping](#tb_sys_org_license_type_mapping) | 机构分类和证照类型对应关系表 |
| [tb_sys_org_type_license](#tb_sys_org_type_license) |  |
| [tb_sys_param](#tb_sys_param) |  |
| [tb_sys_params](#tb_sys_params) |  |
| [tb_sys_region](#tb_sys_region) | 区划表 |
| [tb_sys_resource](#tb_sys_resource) | 资源表 |
| [tb_sys_role](#tb_sys_role) | 角色表 |
| [tb_sys_role_org](#tb_sys_role_org) | 角色-机构 |
| [tb_sys_role_resource](#tb_sys_role_resource) | 角色-菜单 |
| [tb_sys_sequence](#tb_sys_sequence) | 序列号生成表 |
| [tb_sys_system](#tb_sys_system) |  |
| [tb_sys_tickets](#tb_sys_tickets) | 雪花算法序列表 |
| [tb_sys_user](#tb_sys_user) | 用户表 |
| [tb_sys_user_member](#tb_sys_user_member) |  |
| [tb_sys_user_org](#tb_sys_user_org) | 用户-管辖机构表 |
| [tb_sys_user_resource](#tb_sys_user_resource) | 用户-功能表 |
| [tb_sys_user_role](#tb_sys_user_role) | 用户-角色 |
| [tb_tmp_calendar](#tb_tmp_calendar) |  |
| [tb_trade](#tb_trade) | 交易记录 |
| [tb_vote_info](#tb_vote_info) | 订单评价信息表 |
| [temp_new_orgid](#temp_new_orgid) |  |
| [temp_new_orgid_enter](#temp_new_orgid_enter) |  |
| [temp_new_userid](#temp_new_userid) |  |
| [tem_ckmsg](#tem_ckmsg) |  |
| [tmp](#tmp) |  |
| [tmp_fix_subaccount](#tmp_fix_subaccount) | 子账号补充记录(手动补充子账号用) |
| [t_tmp_goods](#t_tmp_goods) | 商品(开发用) |
| [参展企业报名表](#参展企业报名表) |  |
| [处理数据字典_补充没有的剂型](#处理数据字典_补充没有的剂型) |  |
| [处理数据字典_补充没有的包装单位](#处理数据字典_补充没有的包装单位) |  |
| [处理数据字典_补充没有的质量类型](#处理数据字典_补充没有的质量类型) |  |
| [处理湖北省数据临时文档_竞价组](#处理湖北省数据临时文档_竞价组) |  |
| [处理生产厂家_准备插入到org表](#处理生产厂家_准备插入到org表) |  |
| [处理目录编码使用的数据表](#处理目录编码使用的数据表) |  |
| [处理目录编码使用的数据表94](#处理目录编码使用的数据表94) |  |
| [处理竞价组基准品的数据表](#处理竞价组基准品的数据表) |  |
| [处理进口代理_准备插入到org表](#处理进口代理_准备插入到org表) |  |
| [媒体登记信息](#媒体登记信息) |  |
| [建湖北用户](#建湖北用户) |  |
| [武汉](#武汉) |  |
| [湖北药品_整理准备导入product](#湖北药品_整理准备导入product) |  |
| [湖北药品_整理准备导入tb_bas_product_group](#湖北药品_整理准备导入tb_bas_product_group) |  |
| [药品基本数据库（3.0版）](#药品基本数据库（3.0版）) |  |
| [药品挂网目录导出1](#药品挂网目录导出1) |  |
| [药品数据源](#药品数据源) |  |
| [观众报名表](#观众报名表) |  |
| [论坛名](#论坛名) |  |
####  <a id="jpress_content">jpress_content</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   bigintunsigned   | 20 |   0    |    N     |  Y   |       | 主键ID  |
|  2   | title |   text   | 65535 |   0    |    Y     |  N   |       | 标题  |
|  3   | text |   longtext   | 2147483647 |   0    |    Y     |  N   |       | 内容  |
|  4   | summary |   text   | 65535 |   0    |    Y     |  N   |       | 摘要  |
|  5   | link_to |   varchar   | 256 |   0    |    Y     |  N   |       | 连接到(常用于谋文章只是一个连接)  |
|  6   | markdown_enable |   tinyint   | 3 |   0    |    Y     |  N   |   0    | 是否启用markdown  |
|  7   | thumbnail |   varchar   | 128 |   0    |    Y     |  N   |       | 缩略图  |
|  8   | module |   varchar   | 32 |   0    |    Y     |  N   |       | 模型  |
|  9   | style |   varchar   | 32 |   0    |    Y     |  N   |       | 样式  |
|  10   | user_id |   bigintunsigned   | 20 |   0    |    Y     |  N   |       | 用户ID  |
|  11   | author |   varchar   | 128 |   0    |    Y     |  N   |       | 匿名稿的用户  |
|  12   | user_email |   varchar   | 128 |   0    |    Y     |  N   |       | 匿名稿的邮箱  |
|  13   | user_ip |   varchar   | 128 |   0    |    Y     |  N   |       | IP地址  |
|  14   | user_agent |   text   | 65535 |   0    |    Y     |  N   |       | 发布浏览agent  |
|  15   | parent_id |   bigintunsigned   | 20 |   0    |    Y     |  N   |       | 父级内容ID  |
|  16   | object_id |   bigintunsigned   | 20 |   0    |    Y     |  N   |       | 关联的对象ID  |
|  17   | order_number |   intunsigned   | 10 |   0    |    Y     |  N   |   0    | 排序编号  |
|  18   | status |   varchar   | 32 |   0    |    Y     |  N   |       | 状态  |
|  19   | vote_up |   intunsigned   | 10 |   0    |    Y     |  N   |   0    | 支持人数  |
|  20   | vote_down |   intunsigned   | 10 |   0    |    Y     |  N   |   0    | 反对人数  |
|  21   | rate |   int   | 10 |   0    |    Y     |  N   |       | 评分分数  |
|  22   | rate_count |   intunsigned   | 10 |   0    |    Y     |  N   |   0    | 评分次数  |
|  23   | price |   decimal   | 10 |   2    |    Y     |  N   |   0.00    | 价格  |
|  24   | comment_status |   varchar   | 32 |   0    |    Y     |  N   |       | 评论状态  |
|  25   | comment_count |   intunsigned   | 10 |   0    |    Y     |  N   |   0    | 评论总数  |
|  26   | comment_time |   datetime   | 19 |   0    |    Y     |  N   |       | 最后评论时间  |
|  27   | view_count |   intunsigned   | 10 |   0    |    Y     |  N   |   0    | 访问量  |
|  28   | created |   datetime   | 19 |   0    |    Y     |  N   |       | 创建日期  |
|  29   | modified |   datetime   | 19 |   0    |    Y     |  N   |       | 最后更新日期  |
|  30   | slug |   varchar   | 128 |   0    |    Y     |  N   |       | slug  |
|  31   | flag |   varchar   | 256 |   0    |    Y     |  N   |       | 标识  |
|  32   | lng |   decimal   | 20 |   16    |    Y     |  N   |       | 经度  |
|  33   | lat |   decimal   | 20 |   16    |    Y     |  N   |       | 纬度  |
|  34   | meta_keywords |   varchar   | 256 |   0    |    Y     |  N   |       | SEO关键字  |
|  35   | meta_description |   varchar   | 256 |   0    |    Y     |  N   |       | SEO描述信息  |
|  36   | remarks |   text   | 65535 |   0    |    Y     |  N   |       | 备注信息  |
####  <a id="jpress_mapping">jpress_mapping</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   bigintunsigned   | 20 |   0    |    N     |  Y   |       | 主键ID  |
|  2   | content_id |   bigintunsigned   | 20 |   0    |    N     |  N   |       | 内容ID  |
|  3   | taxonomy_id |   bigintunsigned   | 20 |   0    |    N     |  N   |       | 分类ID  |
####  <a id="jpress_taxonomy">jpress_taxonomy</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   bigintunsigned   | 20 |   0    |    N     |  Y   |       | 主键ID  |
|  2   | title |   varchar   | 512 |   0    |    Y     |  N   |       | 标题  |
|  3   | text |   text   | 65535 |   0    |    Y     |  N   |       | 内容描述  |
|  4   | slug |   varchar   | 128 |   0    |    Y     |  N   |       | slug  |
|  5   | type |   varchar   | 32 |   0    |    Y     |  N   |       | 类型  |
|  6   | icon |   varchar   | 128 |   0    |    Y     |  N   |       | 图标  |
|  7   | content_module |   varchar   | 32 |   0    |    Y     |  N   |       | 对于的内容模型  |
|  8   | content_count |   intunsigned   | 10 |   0    |    Y     |  N   |   0    | 该分类的内容数量  |
|  9   | order_number |   int   | 10 |   0    |    Y     |  N   |       | 排序编码  |
|  10   | parent_id |   bigintunsigned   | 20 |   0    |    Y     |  N   |       | 父级分类的ID  |
|  11   | object_id |   bigintunsigned   | 20 |   0    |    Y     |  N   |       | 关联的对象ID  |
|  12   | flag |   varchar   | 256 |   0    |    Y     |  N   |       | 标识  |
|  13   | lat |   decimal   | 20 |   16    |    Y     |  N   |       | 经度  |
|  14   | lng |   decimal   | 20 |   16    |    Y     |  N   |       | 纬度  |
|  15   | meta_keywords |   varchar   | 256 |   0    |    Y     |  N   |       | SEO关键字  |
|  16   | meta_description |   varchar   | 256 |   0    |    Y     |  N   |       | SEO描述内容  |
|  17   | created |   datetime   | 19 |   0    |    Y     |  N   |       | 创建日期  |
####  <a id="tb_accusat_info">tb_accusat_info</a>

**说明：** 投诉建议

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | type |   varchar   | 36 |   0    |    Y     |  N   |       | 投诉类型:1-使用问题，2-产品功能改进，3-界面样式问题，4-流程操作问题  |
|  3   | suggest |   varchar   | 1000 |   0    |    Y     |  N   |       | 建议内容  |
|  4   | name |   varchar   | 50 |   0    |    Y     |  N   |       | 姓名  |
|  5   | contactphone |   varchar   | 36 |   0    |    Y     |  N   |       | 联系电话  |
|  6   | contact_email |   varchar   | 36 |   0    |    Y     |  N   |       | 联系邮箱  |
|  7   | acc_file_url |   varchar   | 1000 |   0    |    Y     |  N   |       | 文件url  |
|  8   | acc_file_name |   varchar   | 1000 |   0    |    Y     |  N   |       | 文件名称  |
|  9   | acc_file_size |   varchar   | 1000 |   0    |    Y     |  N   |       | 文件大小  |
|  10   | creator_org_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者所在机构id  |
|  11   | creator_org_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者所在机构名称  |
|  12   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者id  |
|  13   | creator_name |   varchar   | 100 |   0    |    Y     |  N   |       | 创建者姓名  |
|  14   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  15   | del_flag |   int   | 10 |   0    |    Y     |  N   |   0    | 删除标记，0-未删除1-已删除，默认0-未删除  |
|  16   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 备注信息  |
####  <a id="tb_bank_access_log">tb_bank_access_log</a>

**说明：** 华夏银行支付接口访问日志

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 20 |   0    |    N     |  Y   |       |   |
|  2   | trans_code |   char   | 6 |   0    |    N     |  N   |       | 交易编号  |
|  3   | trans_name |   varchar   | 50 |   0    |    Y     |  N   |       | 交易名称  |
|  4   | trans_code_id |   varchar   | 24 |   0    |    N     |  N   |       | 交易流水号  |
|  5   | sub_account |   varchar   | 20 |   0    |    N     |  N   |       | 子账号  |
|  6   | pay_code |   varchar   | 32 |   0    |    Y     |  N   |       | 交易单号  |
|  7   | money |   bigint   | 19 |   0    |    Y     |  N   |       | 交易金额（分）  |
|  8   | sub_account_money |   bigint   | 19 |   0    |    Y     |  N   |       | 子账号总余额  |
|  9   | freeze_money |   bigint   | 19 |   0    |    Y     |  N   |       | 子账号冻结金额  |
|  10   | client_time |   datetime   | 19 |   0    |    N     |  N   |       | 客户端交易时间  |
|  11   | response_code |   char   | 6 |   0    |    Y     |  N   |       | 返回code  |
|  12   | response_msg |   varchar   | 200 |   0    |    Y     |  N   |       | 返回消息  |
|  13   | request_text |   text   | 65535 |   0    |    N     |  N   |       | 请求xml串  |
|  14   | response_text |   text   | 65535 |   0    |    N     |  N   |       | 响应xml串  |
####  <a id="tb_base_attachment_file">tb_base_attachment_file</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | name |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  3   | file_name |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  4   | path |   varchar   | 255 |   0    |    Y     |  N   |       |   |
####  <a id="tb_bas_change_log">tb_bas_change_log</a>

**说明：** 药品目录及药品字段变更记录

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | entry |   varchar   | 50 |   0    |    Y     |  N   |       | 实体名  |
|  3   | entry_pk |   varchar   | 50 |   0    |    Y     |  N   |       | 实体主键  |
|  4   | property |   varchar   | 50 |   0    |    Y     |  N   |       | 属性名  |
|  5   | property_text |   varchar   | 50 |   0    |    Y     |  N   |       | 属性名（显示使用）  |
|  6   | old_data |   varchar   | 50 |   0    |    Y     |  N   |       | 旧值  |
|  7   | old_data_text |   varchar   | 50 |   0    |    Y     |  N   |       | 旧值（显示使用）  |
|  8   | new_data |   varchar   | 50 |   0    |    Y     |  N   |       | 新值  |
|  9   | new_data_text |   varchar   | 50 |   0    |    Y     |  N   |       | 新值（显示使用）  |
|  10   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 修改时间  |
|  11   | op_name |   varchar   | 100 |   0    |    Y     |  N   |       | 修改人姓名  |
|  12   | op_id |   varchar   | 36 |   0    |    Y     |  N   |       | 修改人id  |
####  <a id="tb_bas_org_address">tb_bas_org_address</a>

**说明：** 收货地址表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | org_id |   varchar   | 36 |   0    |    N     |  N   |       | 机构id  |
|  3   | consignee |   varchar   | 255 |   0    |    Y     |  N   |       | 收货人  |
|  4   | phone |   varchar   | 255 |   0    |    Y     |  N   |       | 联系电话  |
|  5   | address |   varchar   | 255 |   0    |    Y     |  N   |       | 收货地址  |
|  6   | region_code |   varchar   | 20 |   0    |    Y     |  N   |       | 区划代码  |
|  7   | region_name |   varchar   | 255 |   0    |    Y     |  N   |       | 区划名称  |
|  8   | default_flag |   int   | 10 |   0    |    Y     |  N   |   0    | 默认标记0未默认，1已默认  |
|  9   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者id  |
|  10   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者姓名  |
|  11   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  12   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者id  |
|  13   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者姓名  |
|  14   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
####  <a id="tb_bas_org_bank_account">tb_bas_org_bank_account</a>

**说明：** 机构银行账户表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | org_id |   varchar   | 36 |   0    |    N     |  N   |       | 机构id  |
|  3   | org_type |   varchar   | 20 |   0    |    Y     |  N   |       | 机构类型(1供应商、2采购商、3监管机构)  |
|  4   | account_no |   varchar   | 100 |   0    |    N     |  N   |       | 银行帐号  |
|  5   | account_bank |   varchar   | 100 |   0    |    Y     |  N   |       | 银行名称，如建设银行  |
|  6   | account_name |   varchar   | 100 |   0    |    N     |  N   |       | 账户名，一般就是公司名  |
|  7   | opening_bank |   varchar   | 200 |   0    |    Y     |  N   |       | 开户行，如建设银行武汉分行光谷支行  |
|  8   | contacts |   varchar   | 255 |   0    |    Y     |  N   |       | 联系人  |
|  9   | phone |   varchar   | 255 |   0    |    Y     |  N   |       | 手机号  |
|  10   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记0未删除，1已删除  |
|  11   | default_flag |   int   | 10 |   0    |    Y     |  N   |   0    | 默认标记0未默认，1已默认  |
|  12   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者id  |
|  13   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者姓名  |
|  14   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  15   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者id  |
|  16   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者姓名  |
|  17   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  18   | bank_no |   varchar   | 40 |   0    |    Y     |  N   |       | 支付系统行号  |
|  19   | account_type |   int   | 10 |   0    |    Y     |  N   |       | 账户类别(0-出入金,1-白名单1,2-白名单2,3-白名单3)  |
|  20   | sign_state |   int   | 10 |   0    |    Y     |  N   |       | 签约状态1-失败2-成功3-未查询  |
####  <a id="tb_bas_org_mapping">tb_bas_org_mapping</a>

**说明：** 机构对应表（采购需求发布，供求关系）

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | procurer_id |   varchar   | 36 |   0    |    N     |  N   |       | 采购方id  |
|  3   | supplier_id |   varchar   | 36 |   0    |    Y     |  N   |       | 供应商id  |
|  4   | create_date |   datetime   | 19 |   0    |    N     |  N   |       | 创建日期  |
|  5   | creator_id |   varchar   | 36 |   0    |    N     |  N   |       | 创建者id  |
|  6   | creator_org_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建机构id  |
|  7   | is_whole_visible |   int   | 10 |   0    |    Y     |  N   |   0    | 0-不可见,1-可见  |
####  <a id="tb_bas_org_prod_price">tb_bas_org_prod_price</a>

**说明：** 商品价格维护表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | prod_id |   varchar   | 36 |   0    |    Y     |  N   |       | 商品id  |
|  3   | org_id |   varchar   | 36 |   0    |    Y     |  N   |       | 机构id  |
|  4   | cost_price |   decimal   | 20 |   4    |    Y     |  N   |       | 综合成本价  |
|  5   | guide_price |   decimal   | 20 |   4    |    Y     |  N   |       | 公司指导价  |
####  <a id="tb_bas_org_sub_account">tb_bas_org_sub_account</a>

**说明：** 机构银行子账号

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | ref_id |   varchar   | 36 |   0    |    Y     |  N   |       | 机构id(可扩展为用户id)/摊位号  |
|  3   | ref_name |   varchar   | 50 |   0    |    Y     |  N   |       | 机构名称  |
|  4   | sub_account |   varchar   | 20 |   0    |    Y     |  N   |       | 子账号  |
|  5   | member_code |   varchar   | 10 |   0    |    Y     |  N   |       | 交易会员代码  |
|  6   | trade_member_grade |   int   | 10 |   0    |    Y     |  N   |       | 交易会员级别  |
|  7   | grade_code |   varchar   | 10 |   0    |    Y     |  N   |       | 上级会员代码  |
|  8   | sub_account_time |   datetime   | 19 |   0    |    Y     |  N   |       | 子账号开户时间  |
|  9   | sub_account_state |   int   | 10 |   0    |    Y     |  N   |       | 子账户当前状态0:正常1:禁用2:销户  |
|  10   | papers_type |   int   | 10 |   0    |    N     |  N   |       | 证件类型  |
|  11   | papers_code |   varchar   | 30 |   0    |    Y     |  N   |       | 证件代码  |
|  12   | is_messager |   int   | 10 |   0    |    N     |  N   |       | 是否需要短信通知  |
|  13   | message_phone |   varchar   | 20 |   0    |    Y     |  N   |       | 短信通知手机号码  |
|  14   | system_source |   int   | 10 |   0    |    N     |  N   |   0    | 数据来源：0-PMS1-商城  |
####  <a id="tb_bas_procurer">tb_bas_procurer</a>

**说明：** 区域设置-采购方临时表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | procurer_id |   varchar   | 36 |   0    |    N     |  N   |       | 采购方id  |
|  3   | create_date |   date   | 10 |   0    |    N     |  N   |       | 创建日期-选中日期  |
|  4   | creator_id |   varchar   | 36 |   0    |    N     |  N   |       | 创建人id  |
####  <a id="tb_bas_product">tb_bas_product</a>

**说明：** 采购商品表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | directory_id |   varchar   | 36 |   0    |    N     |  N   |       | 所属目录id  |
|  3   | directory_code |   varchar   | 20 |   0    |    N     |  N   |       | 所属目录code  |
|  4   | common_name |   varchar   | 100 |   0    |    N     |  N   |       | 通用名（中文）一般来说就是目录名称  |
|  5   | common_memory_code |   varchar   | 255 |   0    |    Y     |  N   |       | 通用名称助记码  |
|  6   | common_english_name |   varchar   | 100 |   0    |    N     |  N   |       | 通用名英文  |
|  7   | common_dosagee_form |   varchar   | 20 |   0    |    Y     |  N   |       | 通用剂型名称（不使用）  |
|  8   | prod_serial_no |   varchar   | 100 |   0    |    Y     |  N   |       | 商品入网编码（医保用，据说集采中只有具有入网编码的才能被采购）  |
|  9   | prod_name |   varchar   | 100 |   0    |    N     |  N   |       | 商品名称  |
|  10   | prod_biz_code |   varchar   | 20 |   0    |    N     |  N   |       | 商品类型编码（新加的字段）  |
|  11   | prod_biz_name |   varchar   | 30 |   0    |    N     |  N   |       | 商品类型名称（新加的字段）  |
|  12   | prod_dosagee_code |   varchar   | 10 |   0    |    Y     |  N   |       | 商品剂型编码(字典)（新加的字段）  |
|  13   | prod_dosagee_form |   varchar   | 100 |   0    |    Y     |  N   |       | 商品剂型(字典)  |
|  14   | prod_spec |   varchar   | 255 |   0    |    N     |  N   |       | 商品规格（每片重0.31克（薄膜衣片））  |
|  15   | prod_package_unit |   varchar   | 50 |   0    |    Y     |  N   |       | 商品包装（铝塑泡罩包装，24片/板*2板/盒）  |
|  16   | prod_package |   varchar   | 100 |   0    |    Y     |  N   |       | 包装（转换系数*制剂单位/包装单位）  |
|  17   | prod_spec_min |   decimal   | 10 |   4    |    Y     |  N   |       | 商品最小规格（0.31）（不使用）  |
|  18   | prod_spec_unit |   varchar   | 100 |   0    |    Y     |  N   |       | 商品最小规格单位（克、ml等等）（不使用）  |
|  19   | exchange_rate |   decimal   | 20 |   4    |    Y     |  N   |   1.0000    | 转换系数（最小规格的数量）  |
|  20   | prod_sum |   decimal   | 20 |   4    |    Y     |  N   |   1.0000    | 总份量=商品最小规格*转换系数（不使用）  |
|  21   | nation_code |   varchar   | 50 |   0    |    Y     |  N   |       | 国家药品编码（不使用）  |
|  22   | spec_bar_code |   varchar   | 100 |   0    |    Y     |  N   |       | 相关条形码（不使用）  |
|  23   | big_package_quantity |   int   | 10 |   0    |    Y     |  N   |       | 通用大包装数量/包装数量(器械)  |
|  24   | mid_package_quantity |   int   | 10 |   0    |    Y     |  N   |       | 通用中包装数量  |
|  25   | manufacture_id |   varchar   | 36 |   0    |    Y     |  N   |       | 生产厂家id  |
|  26   | manufacture_code |   varchar   | 100 |   0    |    Y     |  N   |       | 生产厂家编码（不使用）  |
|  27   | manufacture_name |   varchar   | 100 |   0    |    N     |  N   |       | 生产厂家中文名  |
|  28   | manufacture_memory_code |   varchar   | 255 |   0    |    Y     |  N   |       | 生产厂家助记码  |
|  29   | manufacture_abbreviation |   varchar   | 200 |   0    |    Y     |  N   |       | 生产厂家简称（不使用）  |
|  30   | national_prod_category |   varchar   | 50 |   0    |    Y     |  N   |       | 国家商品类别:终止妊娠药品、非药品...(药品类别)（和prod_biz_code相同，现在不使用这个字段）  |
|  31   | prod_memory_code |   varchar   | 255 |   0    |    Y     |  N   |       | 助记码  |
|  32   | min_dosagee_form_unit |   varchar   | 20 |   0    |    Y     |  N   |       | 最小剂型单位(字典)  |
|  33   | quality_level |   varchar   | 20 |   0    |    Y     |  N   |       | 质量等级(质量层次)(字典)  |
|  34   | min_package |   varchar   | 20 |   0    |    Y     |  N   |       | 最小包装单位(字典)  |
|  35   | drug_standard |   varchar   | 20 |   0    |    Y     |  N   |       | 药品质量标准(字典)  |
|  36   | is_medicare |   int   | 10 |   0    |    Y     |  N   |       | 是否医保0否，1是  |
|  37   | medicare_type |   int   | 10 |   0    |    Y     |  N   |       | 医保类型0乙类、1甲类  |
|  38   | packaging_material |   varchar   | 50 |   0    |    Y     |  N   |       | 包装材质  |
|  39   | storage_classification |   varchar   | 50 |   0    |    Y     |  N   |       | 存储分类  |
|  40   | is_e_supervise |   int   | 10 |   0    |    Y     |  N   |       | 是否电子监管  |
|  41   | expiry |   int   | 10 |   0    |    Y     |  N   |       | 有效期(月)  |
|  42   | is_competitory |   int   | 10 |   0    |    Y     |  N   |       | 是否竞争性0否，1是  |
|  43   | is_essential_12 |   int   | 10 |   0    |    Y     |  N   |       | 理论12基药0否，1是  |
|  44   | is_essential_09 |   int   | 10 |   0    |    Y     |  N   |       | 理论09基药0否，1是  |
|  45   | approval_no |   varchar   | 100 |   0    |    N     |  N   |       | 批准文号  |
|  46   | approval_no_expiry |   varchar   | 100 |   0    |    Y     |  N   |       | 批准文号有效期  |
|  47   | efficacy_category_code |   varchar   | 10 |   0    |    Y     |  N   |       | 药理/功效分类代码（新加的字段）  |
|  48   | efficacy_category |   varchar   | 100 |   0    |    Y     |  N   |       | 药理/功效分类eg青霉素类  |
|  49   | acid_radical_base_code |   varchar   | 10 |   0    |    Y     |  N   |       | 酸根盐基编码（新加的字段）  |
|  50   | acid_radical_base |   varchar   | 50 |   0    |    Y     |  N   |       | 酸根盐基  |
|  51   | drug_attribute |   varchar   | 50 |   0    |    Y     |  N   |       | 药品属性  |
|  52   | apply_org_name |   varchar   | 500 |   0    |    Y     |  N   |       | 申报企业名称  |
|  53   | quality_type |   varchar   | 20 |   0    |    Y     |  N   |       | 质量类型  |
|  54   | actual_quality_type |   varchar   | 100 |   0    |    Y     |  N   |       | 实际质量类型  |
|  55   | basic_drug_property |   varchar   | 20 |   0    |    Y     |  N   |       | 基药属性  |
|  56   | packaging_win_bid_price |   decimal   | 20 |   4    |    Y     |  N   |       | 包装投标价  |
|  57   | is_provincial_standard |   int   | 10 |   0    |    Y     |  N   |       | 是否省标：0否，1是  |
|  58   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
|  59   | useable |   int   | 10 |   0    |    N     |  N   |   0    | 是否启用：0禁用，1启用  |
|  60   | manage_code |   varchar   | 100 |   0    |    Y     |  N   |       | 经营简码  |
|  61   | biz_type |   int   | 10 |   0    |    N     |  N   |       | 业务类型：1药品2医疗器械9其它  |
|  62   | is_import |   int   | 10 |   0    |    Y     |  N   |       | 是否进口:0否，1是  |
|  63   | application_scope |   varchar   | 100 |   0    |    Y     |  N   |       | 适用范围  |
|  64   | product_introduction |   varchar   | 500 |   0    |    Y     |  N   |       | 产品介绍  |
|  65   | brand |   varchar   | 100 |   0    |    Y     |  N   |       | 品牌  |
|  66   | management_class |   varchar   | 20 |   0    |    Y     |  N   |       | 管理类别(字典)  |
|  67   | model |   varchar   | 100 |   0    |    Y     |  N   |       | 型号  |
|  68   | update_date |   datetime   | 19 |   0    |    N     |  N   |   CURRENT_TIMESTAMP    | 更新时间  |
####  <a id="tb_bas_product_biz_price">tb_bas_product_biz_price</a>

**说明：** 商品业务价格表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | org_id |   varchar   | 36 |   0    |    N     |  N   |       | 机构id  |
|  3   | prod_id |   varchar   | 36 |   0    |    N     |  N   |       | 商品id  |
|  4   | lowest_price |   decimal   | 20 |   4    |    Y     |  N   |       | 该机构历史最低成交价  |
|  5   | lowest_price_date |   datetime   | 19 |   0    |    Y     |  N   |       | 该机构历史最低成交价产生时间  |
|  6   | last_price |   decimal   | 20 |   4    |    Y     |  N   |       | 商品上次成交价  |
|  7   | last_price_date |   datetime   | 19 |   0    |    Y     |  N   |       | 商品上次成交价时间  |
####  <a id="tb_bas_product_copy">tb_bas_product_copy</a>

**说明：** 采购商品表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | directory_id |   varchar   | 36 |   0    |    N     |  N   |       | 所属目录id  |
|  3   | directory_code |   varchar   | 20 |   0    |    N     |  N   |       | 所属目录code  |
|  4   | common_name |   varchar   | 100 |   0    |    N     |  N   |       | 通用名（中文）一般来说就是目录名称  |
|  5   | common_english_name |   varchar   | 100 |   0    |    N     |  N   |       | 通用名英文  |
|  6   | common_dosagee_form |   varchar   | 20 |   0    |    Y     |  N   |       | 通用剂型名称（不使用）  |
|  7   | prod_serial_no |   varchar   | 100 |   0    |    Y     |  N   |       | 商品入网编码（医保用，据说集采中只有具有入网编码的才能被采购）  |
|  8   | prod_name |   varchar   | 100 |   0    |    N     |  N   |       | 商品名称  |
|  9   | prod_biz_code |   varchar   | 20 |   0    |    N     |  N   |       | 商品类型编码（新加的字段）  |
|  10   | prod_biz_name |   varchar   | 30 |   0    |    N     |  N   |       | 商品类型名称（新加的字段）  |
|  11   | prod_dosagee_code |   varchar   | 10 |   0    |    N     |  N   |       | 商品剂型编码(字典)（新加的字段）  |
|  12   | prod_dosagee_form |   varchar   | 20 |   0    |    N     |  N   |       | 商品剂型(字典)  |
|  13   | prod_spec |   varchar   | 255 |   0    |    N     |  N   |       | 商品规格（每片重0.31克（薄膜衣片））  |
|  14   | prod_package_unit |   varchar   | 50 |   0    |    Y     |  N   |       | 商品包装（铝塑泡罩包装，24片/板*2板/盒）  |
|  15   | prod_spec_min |   decimal   | 10 |   4    |    Y     |  N   |       | 商品最小规格（0.31）（不使用）  |
|  16   | prod_spec_unit |   varchar   | 100 |   0    |    Y     |  N   |       | 商品最小规格单位（克、ml等等）（不使用）  |
|  17   | exchange_rate |   decimal   | 20 |   4    |    Y     |  N   |   1.0000    | 转换系数（最小规格的数量）  |
|  18   | prod_sum |   decimal   | 20 |   4    |    Y     |  N   |   1.0000    | 总份量=商品最小规格*转换系数（不使用）  |
|  19   | nation_code |   varchar   | 50 |   0    |    Y     |  N   |       | 国家药品编码（不使用）  |
|  20   | spec_bar_code |   varchar   | 100 |   0    |    Y     |  N   |       | 相关条形码（不使用）  |
|  21   | big_package_quantity |   int   | 10 |   0    |    Y     |  N   |       | 通用大包装数量  |
|  22   | mid_package_quantity |   int   | 10 |   0    |    Y     |  N   |       | 通用中包装数量  |
|  23   | manufacture_id |   varchar   | 36 |   0    |    Y     |  N   |       | 生产厂家id  |
|  24   | manufacture_code |   varchar   | 100 |   0    |    Y     |  N   |       | 生产厂家编码（不使用）  |
|  25   | manufacture_name |   varchar   | 100 |   0    |    N     |  N   |       | 生产厂家中文名  |
|  26   | manufacture_abbreviation |   varchar   | 200 |   0    |    Y     |  N   |       | 生产厂家简称（不使用）  |
|  27   | national_prod_category |   varchar   | 50 |   0    |    Y     |  N   |       | 国家商品类别:终止妊娠药品、非药品...(药品类别)（和prod_biz_code相同，现在不使用这个字段）  |
|  28   | prod_memory_code |   varchar   | 100 |   0    |    Y     |  N   |       | 助记码  |
|  29   | min_dosagee_form_unit |   varchar   | 20 |   0    |    Y     |  N   |       | 最小剂型单位(字典)  |
|  30   | quality_level |   varchar   | 20 |   0    |    Y     |  N   |       | 质量等级(质量层次)(字典)  |
|  31   | min_package |   varchar   | 20 |   0    |    Y     |  N   |       | 最小包装单位(字典)  |
|  32   | drug_standard |   varchar   | 20 |   0    |    Y     |  N   |       | 药品质量标准(字典)  |
|  33   | is_medicare |   int   | 10 |   0    |    Y     |  N   |       | 是否医保0否，1是  |
|  34   | medicare_type |   int   | 10 |   0    |    Y     |  N   |       | 医保类型0乙类、1甲类  |
|  35   | packaging_material |   varchar   | 50 |   0    |    Y     |  N   |       | 包装材质  |
|  36   | storage_classification |   varchar   | 50 |   0    |    Y     |  N   |       | 存储分类  |
|  37   | is_e_supervise |   int   | 10 |   0    |    Y     |  N   |       | 是否电子监管  |
|  38   | expiry |   int   | 10 |   0    |    Y     |  N   |       | 有效期(月)  |
|  39   | is_competitory |   int   | 10 |   0    |    Y     |  N   |       | 是否竞争性0否，1是  |
|  40   | is_essential_12 |   int   | 10 |   0    |    Y     |  N   |       | 理论12基药0否，1是  |
|  41   | is_essential_09 |   int   | 10 |   0    |    Y     |  N   |       | 理论09基药0否，1是  |
|  42   | approval_no |   varchar   | 100 |   0    |    N     |  N   |       | 批准文号  |
|  43   | approval_no_expiry |   varchar   | 100 |   0    |    Y     |  N   |       | 批准文号有效期  |
|  44   | efficacy_category_code |   varchar   | 10 |   0    |    Y     |  N   |       | 药理/功效分类代码（新加的字段）  |
|  45   | efficacy_category |   varchar   | 100 |   0    |    Y     |  N   |       | 药理/功效分类eg青霉素类  |
|  46   | acid_radical_base_code |   varchar   | 10 |   0    |    Y     |  N   |       | 酸根盐基编码（新加的字段）  |
|  47   | acid_radical_base |   varchar   | 50 |   0    |    Y     |  N   |       | 酸根盐基  |
|  48   | drug_attribute |   varchar   | 50 |   0    |    Y     |  N   |       | 药品属性  |
|  49   | apply_org_name |   varchar   | 500 |   0    |    Y     |  N   |       | 申报企业名称  |
|  50   | quality_type |   varchar   | 20 |   0    |    Y     |  N   |       | 质量类型  |
|  51   | actual_quality_type |   varchar   | 20 |   0    |    Y     |  N   |       | 实际质量类型  |
|  52   | basic_drug_property |   varchar   | 20 |   0    |    Y     |  N   |       | 基药属性  |
|  53   | packaging_win_bid_price |   decimal   | 20 |   4    |    Y     |  N   |       | 包装投标价  |
|  54   | is_provincial_standard |   int   | 10 |   0    |    Y     |  N   |       | 是否省标：0否，1是  |
|  55   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
####  <a id="tb_bas_product_directory">tb_bas_product_directory</a>

**说明：** 商品目录表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | directory_code |   varchar   | 20 |   0    |    N     |  N   |       | 目录编码（目录号）  |
|  3   | common_name |   varchar   | 100 |   0    |    N     |  N   |       | 目录名称(通用名称)  |
|  4   | common_english_name |   varchar   | 100 |   0    |    N     |  N   |       | 目录名称(通用名称-英文)（新加的字段）  |
|  5   | common_dosagee_form |   varchar   | 20 |   0    |    Y     |  N   |       | 通用剂型(字典)（不使用）  |
|  6   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
|  7   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者id  |
|  8   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者姓名  |
|  9   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  10   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者id  |
|  11   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者姓名  |
|  12   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  13   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 备注信息  |
####  <a id="tb_bas_product_directory_copy">tb_bas_product_directory_copy</a>

**说明：** 商品目录表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | directory_code |   varchar   | 20 |   0    |    N     |  N   |       | 目录编码（目录号）  |
|  3   | common_name |   varchar   | 100 |   0    |    N     |  N   |       | 目录名称(通用名称)  |
|  4   | common_english_name |   varchar   | 100 |   0    |    N     |  N   |       | 目录名称(通用名称-英文)（新加的字段）  |
|  5   | common_dosagee_form |   varchar   | 20 |   0    |    Y     |  N   |       | 通用剂型(字典)（不使用）  |
|  6   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
|  7   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者id  |
|  8   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者姓名  |
|  9   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  10   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者id  |
|  11   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者姓名  |
|  12   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  13   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 备注信息  |
####  <a id="tb_bas_product_draft">tb_bas_product_draft</a>

**说明：** 采购商品草稿表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | directory_id |   varchar   | 36 |   0    |    N     |  N   |       | 所属目录id  |
|  3   | directory_code |   varchar   | 20 |   0    |    N     |  N   |       | 所属目录code  |
|  4   | common_name |   varchar   | 100 |   0    |    N     |  N   |       | 通用名（中文）一般来说就是目录名称  |
|  5   | common_memory_code |   varchar   | 255 |   0    |    Y     |  N   |       | 通用名称助记码  |
|  6   | common_english_name |   varchar   | 100 |   0    |    N     |  N   |       | 通用名英文  |
|  7   | common_dosagee_form |   varchar   | 20 |   0    |    Y     |  N   |       | 通用剂型(字典)  |
|  8   | prod_serial_no |   varchar   | 100 |   0    |    Y     |  N   |       | 商品入网编码（医保用，据说集采中只有具有入网编码的才能被采购）  |
|  9   | prod_name |   varchar   | 100 |   0    |    N     |  N   |       | 商品名称  |
|  10   | prod_biz_code |   varchar   | 20 |   0    |    N     |  N   |       | 商品类型编码（新加的字段）  |
|  11   | prod_biz_name |   varchar   | 30 |   0    |    N     |  N   |       | 商品类型名称（新加的字段）  |
|  12   | prod_dosagee_code |   varchar   | 10 |   0    |    Y     |  N   |       | 商品剂型编码(字典)（新加的字段）  |
|  13   | prod_dosagee_form |   varchar   | 100 |   0    |    Y     |  N   |       | 商品剂型(字典)  |
|  14   | prod_spec |   varchar   | 255 |   0    |    N     |  N   |       | 商品规格（每片重0.31克（薄膜衣片））  |
|  15   | prod_package_unit |   varchar   | 50 |   0    |    Y     |  N   |       | 商品包装（铝塑泡罩包装，24片/板*2板/盒）  |
|  16   | prod_package |   varchar   | 100 |   0    |    Y     |  N   |       | 包装（转换系数*制剂单位/包装单位）  |
|  17   | prod_spec_min |   decimal   | 10 |   4    |    Y     |  N   |       | 商品最小规格（0.31）  |
|  18   | prod_spec_unit |   varchar   | 100 |   0    |    Y     |  N   |       | 商品最小规格单位（克、ml等等）  |
|  19   | exchange_rate |   decimal   | 20 |   4    |    Y     |  N   |   1.0000    | 转换系数（最小规格的数量）  |
|  20   | prod_sum |   decimal   | 20 |   4    |    Y     |  N   |   1.0000    | 总份量=商品最小规格*转换系数  |
|  21   | nation_code |   varchar   | 50 |   0    |    Y     |  N   |       | 国家药品编码  |
|  22   | spec_bar_code |   varchar   | 100 |   0    |    Y     |  N   |       | 相关条形码  |
|  23   | big_package_quantity |   int   | 10 |   0    |    Y     |  N   |       | 通用大包装数量/包装数量(器械)  |
|  24   | mid_package_quantity |   int   | 10 |   0    |    Y     |  N   |       | 通用中包装数量  |
|  25   | manufacture_id |   varchar   | 36 |   0    |    Y     |  N   |       | 生产厂家id  |
|  26   | manufacture_code |   varchar   | 100 |   0    |    Y     |  N   |       | 生产厂家编码  |
|  27   | manufacture_name |   varchar   | 100 |   0    |    N     |  N   |       | 生产厂家中文名  |
|  28   | manufacture_memory_code |   varchar   | 255 |   0    |    Y     |  N   |       | 生产厂家助记码  |
|  29   | manufacture_abbreviation |   varchar   | 200 |   0    |    Y     |  N   |       | 生产厂家简称  |
|  30   | national_prod_category |   varchar   | 50 |   0    |    Y     |  N   |       | 国家商品类别:终止妊娠药品、非药品...(药品类别)  |
|  31   | prod_memory_code |   varchar   | 255 |   0    |    Y     |  N   |       | 助记码  |
|  32   | min_dosagee_form_unit |   varchar   | 20 |   0    |    Y     |  N   |       | 最小剂型单位(字典)  |
|  33   | quality_level |   varchar   | 20 |   0    |    Y     |  N   |       | 质量等级(质量层次)(字典)  |
|  34   | min_package |   varchar   | 20 |   0    |    Y     |  N   |       | 最小包装单位(字典)  |
|  35   | drug_standard |   varchar   | 20 |   0    |    Y     |  N   |       | 药品质量标准(字典)  |
|  36   | is_medicare |   int   | 10 |   0    |    Y     |  N   |       | 是否医保0否，1是  |
|  37   | medicare_type |   int   | 10 |   0    |    Y     |  N   |       | 医保类型0乙类、1甲类  |
|  38   | packaging_material |   varchar   | 50 |   0    |    Y     |  N   |       | 包装材质  |
|  39   | storage_classification |   varchar   | 50 |   0    |    Y     |  N   |       | 存储分类  |
|  40   | is_e_supervise |   int   | 10 |   0    |    Y     |  N   |       | 是否电子监管  |
|  41   | expiry |   int   | 10 |   0    |    Y     |  N   |       | 有效期(月)  |
|  42   | is_competitory |   int   | 10 |   0    |    Y     |  N   |       | 是否竞争性0否，1是  |
|  43   | is_essential_12 |   int   | 10 |   0    |    Y     |  N   |       | 理论12基药0否，1是  |
|  44   | is_essential_09 |   int   | 10 |   0    |    Y     |  N   |       | 理论09基药0否，1是  |
|  45   | approval_no |   varchar   | 100 |   0    |    N     |  N   |       | 批准文号  |
|  46   | approval_no_expiry |   varchar   | 100 |   0    |    Y     |  N   |       | 批准文号有效期  |
|  47   | efficacy_category_code |   varchar   | 10 |   0    |    Y     |  N   |       | 药理/功效分类代码（新加的字段）  |
|  48   | efficacy_category |   varchar   | 100 |   0    |    Y     |  N   |       | 药理/功效分类eg青霉素类  |
|  49   | acid_radical_base_code |   varchar   | 10 |   0    |    Y     |  N   |       | 酸根盐基编码（新加的字段）  |
|  50   | acid_radical_base |   varchar   | 50 |   0    |    Y     |  N   |       | 酸根盐基  |
|  51   | drug_attribute |   varchar   | 50 |   0    |    Y     |  N   |       | 药品属性  |
|  52   | apply_org_name |   varchar   | 500 |   0    |    Y     |  N   |       | 申报企业名称  |
|  53   | quality_type |   varchar   | 20 |   0    |    Y     |  N   |       | 质量类型  |
|  54   | actual_quality_type |   varchar   | 100 |   0    |    Y     |  N   |       | 实际质量类型  |
|  55   | basic_drug_property |   varchar   | 20 |   0    |    Y     |  N   |       | 基药属性  |
|  56   | packaging_win_bid_price |   decimal   | 20 |   4    |    Y     |  N   |       | 包装投标价  |
|  57   | is_provincial_standard |   int   | 10 |   0    |    Y     |  N   |       | 是否省标：0否，1是  |
|  58   | submitter_op_id |   varchar   | 36 |   0    |    Y     |  N   |       | 提交人id  |
|  59   | submitter_time |   datetime   | 19 |   0    |    Y     |  N   |       | 提交时间  |
|  60   | audit_op_id |   varchar   | 36 |   0    |    Y     |  N   |       | 审核人id  |
|  61   | audit_status |   int   | 10 |   0    |    Y     |  N   |       | 审核状态0保存,1待审核,2拒绝,3通过  |
|  62   | audit_time |   datetime   | 19 |   0    |    Y     |  N   |       | 审核时间  |
|  63   | audit_info |   varchar   | 500 |   0    |    Y     |  N   |       | 审核留言  |
|  64   | useable |   int   | 10 |   0    |    N     |  N   |   0    | 是否启用：0禁用，1启用  |
|  65   | manage_code |   varchar   | 100 |   0    |    Y     |  N   |       | 经营简码  |
|  66   | biz_type |   int   | 10 |   0    |    N     |  N   |       | 业务类型：1药品2医疗器械9其它  |
|  67   | is_import |   int   | 10 |   0    |    Y     |  N   |       | 是否进口:0否，1是  |
|  68   | application_scope |   varchar   | 100 |   0    |    Y     |  N   |       | 适用范围  |
|  69   | product_introduction |   varchar   | 500 |   0    |    Y     |  N   |       | 产品介绍  |
|  70   | brand |   varchar   | 100 |   0    |    Y     |  N   |       | 品牌  |
|  71   | management_class |   varchar   | 20 |   0    |    Y     |  N   |       | 管理类别(字典)  |
|  72   | model |   varchar   | 100 |   0    |    Y     |  N   |       | 型号  |
####  <a id="tb_bas_product_group">tb_bas_product_group</a>

**说明：** 采购竞价组

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | group_no |   varchar   | 20 |   0    |    N     |  N   |       | 分组号  |
|  3   | common_name |   varchar   | 100 |   0    |    N     |  N   |       | 通用名称  |
|  4   | common_dosagee_form |   varchar   | 100 |   0    |    N     |  N   |       | 通用剂型(字典)  |
|  5   | prod_spec |   varchar   | 255 |   0    |    N     |  N   |       | 基准规格（取商品表基准品的规格）  |
|  6   | prod_package_unit |   varchar   | 50 |   0    |    N     |  N   |       | 基准包装（取商品表基准品的包装）  |
|  7   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
|  8   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者id  |
|  9   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者姓名  |
|  10   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  11   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者id  |
|  12   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者姓名  |
|  13   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
####  <a id="tb_bas_product_group_bidding_log">tb_bas_product_group_bidding_log</a>

**说明：** 竞价组商品修改历史

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | group_id |   varchar   | 36 |   0    |    N     |  N   |       | 竞价组id  |
|  3   | prod_id |   varchar   | 36 |   0    |    N     |  N   |       | 商品id  |
|  4   | batch_no |   varchar   | 50 |   0    |    N     |  N   |       | 修改批次号  |
|  5   | modify_type |   varchar   | 10 |   0    |    N     |  N   |       | 修改类型new:新增remove:删除  |
|  6   | modify_time |   datetime   | 19 |   0    |    N     |  N   |       | 修改时间  |
|  7   | updater_id |   varchar   | 36 |   0    |    N     |  N   |       | 修改用户id  |
|  8   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 修改用户姓名  |
####  <a id="tb_bas_product_group_copy">tb_bas_product_group_copy</a>

**说明：** 采购竞价组

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | group_no |   varchar   | 20 |   0    |    N     |  N   |       | 分组号  |
|  3   | common_name |   varchar   | 100 |   0    |    N     |  N   |       | 通用名称  |
|  4   | common_dosagee_form |   varchar   | 20 |   0    |    N     |  N   |       | 通用剂型(字典)  |
|  5   | prod_spec |   varchar   | 255 |   0    |    N     |  N   |       | 基准规格（取商品表基准品的规格）  |
|  6   | prod_package_unit |   varchar   | 50 |   0    |    N     |  N   |       | 基准包装（取商品表基准品的包装）  |
|  7   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
|  8   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者id  |
|  9   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者姓名  |
|  10   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  11   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者id  |
|  12   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者姓名  |
|  13   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
####  <a id="tb_bas_product_group_mapping">tb_bas_product_group_mapping</a>

**说明：** 竞价组商品对应关系表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | prod_id |   varchar   | 36 |   0    |    N     |  N   |       | 商品id  |
|  3   | group_id |   varchar   | 36 |   0    |    N     |  N   |       | 竞价组id  |
|  4   | group_no |   varchar   | 20 |   0    |    N     |  N   |       | 竞价组分组号  |
|  5   | is_base_prod |   int   | 10 |   0    |    N     |  N   |   0    | 是否基准品0否，1是  |
|  6   | price_st_ratio |   decimal   | 20 |   4    |    N     |  N   |       | 商品相对竞价组差比率  |
####  <a id="tb_bas_product_group_mapping_copy">tb_bas_product_group_mapping_copy</a>

**说明：** 竞价组商品对应关系表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | prod_id |   varchar   | 36 |   0    |    N     |  N   |       | 商品id  |
|  3   | group_id |   varchar   | 36 |   0    |    N     |  N   |       | 竞价组id  |
|  4   | group_no |   varchar   | 20 |   0    |    N     |  N   |       | 竞价组分组号  |
|  5   | is_base_prod |   int   | 10 |   0    |    N     |  N   |   0    | 是否基准品0否，1是  |
|  6   | price_st_ratio |   decimal   | 20 |   4    |    N     |  N   |       | 商品相对竞价组差比率  |
####  <a id="tb_bas_product_license">tb_bas_product_license</a>

**说明：** 产品证照表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | prod_id |   varchar   | 36 |   0    |    Y     |  N   |       | 商品id  |
|  3   | license_type |   varchar   | 100 |   0    |    Y     |  N   |       | 证照类型  |
|  4   | license_no |   varchar   | 100 |   0    |    Y     |  N   |       | 证照号  |
|  5   | issuing_authority |   varchar   | 100 |   0    |    Y     |  N   |       | 发证机关  |
|  6   | issuing_date |   datetime   | 19 |   0    |    Y     |  N   |       | 发证日期  |
|  7   | expiry_time |   datetime   | 19 |   0    |    Y     |  N   |       | 证照有效日期  |
|  8   | url |   varchar   | 255 |   0    |    Y     |  N   |       | 证照图片文件地址  |
|  9   | del_flag |   int   | 10 |   0    |    Y     |  N   |   0    | 删除标记0未删除，1已删除  |
####  <a id="tb_bas_product_license_draft">tb_bas_product_license_draft</a>

**说明：** 产品证照表_草稿

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | prod_id |   varchar   | 36 |   0    |    Y     |  N   |       | 商品id  |
|  3   | license_type |   varchar   | 100 |   0    |    Y     |  N   |       | 证照类型  |
|  4   | license_no |   varchar   | 100 |   0    |    Y     |  N   |       | 证照号  |
|  5   | issuing_authority |   varchar   | 100 |   0    |    Y     |  N   |       | 发证机关  |
|  6   | issuing_date |   datetime   | 19 |   0    |    Y     |  N   |       | 发证日期  |
|  7   | expiry_time |   datetime   | 19 |   0    |    Y     |  N   |       | 证照有效日期  |
|  8   | url |   varchar   | 255 |   0    |    Y     |  N   |       | 证照图片文件地址  |
|  9   | del_flag |   int   | 10 |   0    |    Y     |  N   |   0    | 删除标记0未删除，1已删除  |
####  <a id="tb_bas_product_medicare_price">tb_bas_product_medicare_price</a>

**说明：** 商品医保支付价格表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | year |   int   | 10 |   0    |    N     |  N   |       | 年度  |
|  3   | prod_serial_no |   varchar   | 100 |   0    |    N     |  N   |       | 流水号  |
|  4   | prod_id |   varchar   | 36 |   0    |    N     |  N   |       | 商品id  |
|  5   | common_name |   varchar   | 100 |   0    |    N     |  N   |       | 通用名称  |
|  6   | prod_name |   varchar   | 100 |   0    |    N     |  N   |       | 商品名称  |
|  7   | prod_dosagee_form |   varchar   | 100 |   0    |    N     |  N   |       | 剂型  |
|  8   | prod_spec |   varchar   | 100 |   0    |    N     |  N   |       | 规格  |
|  9   | prod_package_unit |   varchar   | 100 |   0    |    N     |  N   |       | 包装单位  |
|  10   | manufacture_name |   varchar   | 255 |   0    |    N     |  N   |       | 生产厂家  |
|  11   | medicare_price |   decimal   | 10 |   4    |    N     |  N   |       | 医保价  |
|  12   | start_date |   date   | 10 |   0    |    Y     |  N   |       | 开始日期  |
|  13   | end_date |   date   | 10 |   0    |    Y     |  N   |       | 结束日期  |
|  14   | del_flag |   int   | 10 |   0    |    Y     |  N   |       | 删除标记  |
|  15   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者id  |
|  16   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者姓名  |
|  17   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  18   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者id  |
|  19   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者姓名  |
|  20   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
####  <a id="tb_bas_product_org_mapping">tb_bas_product_org_mapping</a>

**说明：** 机构自选商品表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | prod_id |   varchar   | 36 |   0    |    Y     |  N   |       | 商品id  |
|  3   | org_id |   varchar   | 36 |   0    |    Y     |  N   |       | 机构id  |
|  4   | del_flag |   int   | 10 |   0    |    Y     |  N   |   0    | 删除标记0未删除，1已删除  |
####  <a id="tb_bas_product_price">tb_bas_product_price</a>

**说明：** 商品最低价和医保支付价格表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | prod_id |   varchar   | 36 |   0    |    Y     |  N   |       | 商品id  |
|  3   | lowest_price |   decimal   | 20 |   4    |    Y     |  N   |       | 最低价（因全网最低价弃用，改为按机构历史最低价tb_bas_product_biz_price.lowest_price）  |
|  4   | lowest_price_date |   datetime   | 19 |   0    |    Y     |  N   |       | 最低价对应日期  |
|  5   | medicare_price |   decimal   | 20 |   4    |    Y     |  N   |       | 医保支付价格  |
####  <a id="tb_bas_product_supplier_mapping">tb_bas_product_supplier_mapping</a>

**说明：** 商品和生产厂家投标企业对应关系表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | prod_id |   varchar   | 36 |   0    |    Y     |  N   |       | 商品id  |
|  3   | org_id |   varchar   | 36 |   0    |    Y     |  N   |       | 机构id  |
####  <a id="tb_bas_product_supplier_mapping_draft">tb_bas_product_supplier_mapping_draft</a>

**说明：** 商品和生产厂家投标企业对应关系草稿表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | prod_id |   varchar   | 36 |   0    |    Y     |  N   |       | 商品id  |
|  3   | org_id |   varchar   | 36 |   0    |    Y     |  N   |       | 机构id  |
####  <a id="tb_bas_supplier">tb_bas_supplier</a>

**说明：** 区域设置-供应商临时表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | supplier_id |   varchar   | 36 |   0    |    N     |  N   |       | 供应商id  |
|  3   | create_date |   date   | 10 |   0    |    N     |  N   |       | 创建日期-选中日期  |
|  4   | creator_id |   varchar   | 36 |   0    |    N     |  N   |       | 创建人id  |
####  <a id="tb_bas_temp_procurer">tb_bas_temp_procurer</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | procurer_id |   varchar   | 36 |   0    |    N     |  N   |       | 采购方id  |
|  3   | create_date |   datetime   | 19 |   0    |    N     |  N   |       | 创建日期-选中日期  |
|  4   | creator_id |   varchar   | 36 |   0    |    N     |  N   |       | 创建人id  |
|  5   | creator_org_id |   varchar   | 36 |   0    |    N     |  N   |       | 创建机人构id  |
####  <a id="tb_bas_temp_supplier">tb_bas_temp_supplier</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | supplier_id |   varchar   | 36 |   0    |    N     |  N   |       | 供应商id  |
|  3   | create_date |   datetime   | 19 |   0    |    N     |  N   |       | 创建日期-选中日期  |
|  4   | creator_id |   varchar   | 36 |   0    |    N     |  N   |       | 创建人id  |
|  5   | creator_org_id |   varchar   | 36 |   0    |    N     |  N   |       | 创建机人构id  |
####  <a id="tb_battlefield_report">tb_battlefield_report</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 50 |   0    |    N     |  Y   |       | 注解id  |
|  2   | report_title |   varchar   | 255 |   0    |    N     |  N   |       | 战报标题  |
|  3   | report_url |   varchar   | 255 |   0    |    N     |  N   |       | 战报访问地址  |
|  4   | sort |   int   | 10 |   0    |    N     |  N   |       | 排序号  |
|  5   | token |   varchar   | 255 |   0    |    Y     |  N   |       | 战报token值  |
####  <a id="tb_bidd_convert_price">tb_bidd_convert_price</a>

**说明：** 竞价折算价表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | req_det_id |   varchar   | 36 |   0    |    Y     |  N   |       | 需求明细ID，标记报价明细对应哪条需求明细  |
|  3   | bidd_det_id |   varchar   | 36 |   0    |    Y     |  N   |       | 报价明细记录id  |
|  4   | formula_id |   varchar   | 36 |   0    |    N     |  N   |       | 竞价公式id  |
|  5   | formula_name |   varchar   | 50 |   0    |    N     |  N   |       | 竞价公式名称  |
|  6   | convert_price |   decimal   | 20 |   4    |    N     |  N   |       | 折算价（根据竞价公式计算得出）  |
|  7   | prod_serial_no |   varchar   | 20 |   0    |    Y     |  N   |       | 产品流水号  |
|  8   | entire_quantity |   int   | 10 |   0    |    Y     |  N   |       | 采购数量  |
|  9   | bidd_doc_no |   varchar   | 36 |   0    |    Y     |  N   |       | 竞价单据号  |
|  10   | group_no |   varchar   | 30 |   0    |    Y     |  N   |       | 竞价组分组号  |
|  11   | is_backup |   int   | 10 |   0    |    N     |  N   |       | 是否替代方案1是0否  |
|  12   | price |   decimal   | 20 |   4    |    Y     |  N   |       | 原报价  |
####  <a id="tb_bidd_det">tb_bidd_det</a>

**说明：** 报价文件明细

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | req_det_id |   varchar   | 36 |   0    |    Y     |  N   |       | 需求明细ID，标记报价明细对应哪条需求明细  |
|  3   | bidd_doc_no |   varchar   | 20 |   0    |    N     |  N   |       | 竞价单据编号  |
|  4   | group_no |   varchar   | 20 |   0    |    N     |  N   |       | 所属竞价组分组号。不能提交无法匹配竞价组的商品  |
|  5   | common_name |   varchar   | 100 |   0    |    Y     |  N   |       | 通用名（中文）一般来说就是目录名称  |
|  6   | common_dosagee_form |   varchar   | 20 |   0    |    Y     |  N   |       | 通用剂型(字典)  |
|  7   | prod_id |   varchar   | 36 |   0    |    Y     |  N   |       | 商品ID  |
|  8   | prod_serial_no |   varchar   | 100 |   0    |    Y     |  N   |       | 产品流水号  |
|  9   | prod_name |   varchar   | 100 |   0    |    N     |  N   |       | 商品名称  |
|  10   | prod_dosagee_form |   varchar   | 20 |   0    |    Y     |  N   |       | 商品剂型  |
|  11   | prod_spec |   varchar   | 100 |   0    |    N     |  N   |       | 商品规格  |
|  12   | prod_package_unit |   varchar   | 50 |   0    |    N     |  N   |       | 商品包装  |
|  13   | min_package |   varchar   | 20 |   0    |    Y     |  N   |       | 最小包装单位(字典)  |
|  14   | manufacture_code |   varchar   | 100 |   0    |    Y     |  N   |       | 生产厂家编码  |
|  15   | manufacture_name |   varchar   | 100 |   0    |    N     |  N   |       | 生产厂家中文名  |
|  16   | entire_quantity |   decimal   | 20 |   2    |    N     |  N   |       | 采购数量  |
|  17   | exchange_rate |   decimal   | 20 |   4    |    N     |  N   |   1.0000    | 转换系数  |
|  18   | price |   decimal   | 20 |   4    |    Y     |  N   |       | 最小单位报价  |
|  19   | amount |   decimal   | 20 |   4    |    Y     |  N   |   0.0000    | 单行总价,数量*单价  |
|  20   | gross_profit |   decimal   | 20 |   4    |    Y     |  N   |   0.0000    | 结余率。相当于毛利率计算方式。医保价格-采购价/医保价格  |
|  21   | sort |   int   | 10 |   0    |    Y     |  N   |       | 排序号  |
|  22   | is_backup |   int   | 10 |   0    |    Y     |  N   |   0    | 0:不是替代方案;1:替代方案  |
|  23   | is_got |   int   | 10 |   0    |    Y     |  N   |   0    | 0:未中标;1:已中标  |
|  24   | initial_prod_id |   varchar   | 36 |   0    |    Y     |  N   |       | 初始商品ID  |
|  25   | is_effective |   int   | 10 |   0    |    Y     |  N   |   1    | 是否有效0:否;1:是  |
|  26   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 备注信息  |
|  27   | medicare_price |   decimal   | 20 |   4    |    Y     |  N   |       | 价格参考-医保价  |
|  28   | lowest_price |   decimal   | 20 |   4    |    Y     |  N   |       | 价格参考-历史最低价  |
|  29   | last_bidd_price |   decimal   | 20 |   4    |    Y     |  N   |       | 价格参考-上次中标价  |
|  30   | last_no_bidd_price |   decimal   | 20 |   4    |    Y     |  N   |       | 价格参考-上次未中标价  |
|  31   | cost_price |   decimal   | 20 |   4    |    Y     |  N   |       | 价格参考-综合成本价  |
|  32   | guide_price |   decimal   | 10 |   4    |    Y     |  N   |       | 价格参考-公司指导价  |
|  33   | is_import |   int   | 10 |   0    |    Y     |  N   |       | 是否进口:0否，1是  |
|  34   | application_scope |   varchar   | 100 |   0    |    Y     |  N   |       | 适用范围  |
|  35   | product_introduction |   varchar   | 500 |   0    |    Y     |  N   |       | 产品介绍  |
|  36   | brand |   varchar   | 100 |   0    |    Y     |  N   |       | 品牌  |
|  37   | management_class |   varchar   | 20 |   0    |    Y     |  N   |       | 管理类别(字典)  |
|  38   | model |   varchar   | 100 |   0    |    Y     |  N   |       | 型号  |
|  39   | big_package_quantity |   varchar   | 11 |   0    |    Y     |  N   |       | 通用大包装数量/包装数量(器械)  |
|  40   | biz_type |   int   | 10 |   0    |    Y     |  N   |       | 业务类型：1药品2医疗器械9其它  |
####  <a id="tb_bidd_main">tb_bidd_main</a>

**说明：** 报价文件主表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | bidd_doc_no |   varchar   | 20 |   0    |    N     |  N   |       | 竞价单号  |
|  3   | supplier_id |   varchar   | 36 |   0    |    N     |  N   |       | 供应商ID  |
|  4   | req_doc_no |   varchar   | 20 |   0    |    N     |  N   |       | 需求单号  |
|  5   | bidd_status |   int   | 10 |   0    |    N     |  N   |       | 竞价状态:0-未报价1-未提交2-已报价3-竞价结束4-未中标5-已中标默认0  |
|  6   | submit_time |   datetime   | 19 |   0    |    Y     |  N   |       | 报价提交时间  |
|  7   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者id  |
|  8   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者姓名  |
|  9   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  10   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者id  |
|  11   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者姓名  |
|  12   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  13   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
|  14   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 备注信息  |
|  15   | biz_type |   int   | 10 |   0    |    Y     |  N   |       | 业务类型：1药品2医疗器械9其它  |
####  <a id="tb_bnsjfxbg">tb_bnsjfxbg</a>

**说明：** 不良事件分析报告

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | id  |
|  2   | lsh |   varchar   | 50 |   0    |    Y     |  N   |       | 流水号  |
|  3   | tym |   varchar   | 50 |   0    |    Y     |  N   |       | 通用名  |
|  4   | spmc |   varchar   | 50 |   0    |    Y     |  N   |       | 商品名称  |
|  5   | jx |   varchar   | 50 |   0    |    Y     |  N   |       | 剂型  |
|  6   | gg |   varchar   | 50 |   0    |    Y     |  N   |       | 规格  |
|  7   | bz |   varchar   | 50 |   0    |    Y     |  N   |       | 包装  |
|  8   | sccj |   varchar   | 50 |   0    |    Y     |  N   |       | 生产厂家  |
|  9   | ls |   int   | 10 |   0    |    Y     |  N   |       | 例数  |
|  10   | nan |   int   | 10 |   0    |    Y     |  N   |       | 男  |
|  11   | nv |   int   | 10 |   0    |    Y     |  N   |       | 女  |
|  12   | gnnsfy |   int   | 10 |   0    |    Y     |  N   |       | 国内类似反应  |
####  <a id="tb_comm_file">tb_comm_file</a>

**说明：** 业务对应文件关系表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | biz_id |   varchar   | 36 |   0    |    Y     |  N   |       | 业务id  |
|  3   | type |   int   | 10 |   0    |    Y     |  N   |       | 关联类型  |
|  4   | file_id |   varchar   | 36 |   0    |    Y     |  N   |       | 文件id  |
|  5   | file_name |   varchar   | 255 |   0    |    Y     |  N   |       | 上传时原始的文件名  |
|  6   | file_size |   decimal   | 20 |   0    |    N     |  N   |       | 文件大小，单位：byte(1KB=1024byte)  |
|  7   | file_ext |   varchar   | 20 |   0    |    Y     |  N   |       | 文件扩展名  |
####  <a id="tb_deliver_det">tb_deliver_det</a>

**说明：** 发货单明细表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | deliver_doc_no |   varchar   | 20 |   0    |    N     |  N   |       | 发货单号  |
|  3   | prod_id |   varchar   | 36 |   0    |    Y     |  N   |       | 商品ID  |
|  4   | batch_no |   varchar   | 50 |   0    |    Y     |  N   |       | 批号  |
|  5   | expire_date |   datetime   | 19 |   0    |    Y     |  N   |       | 过期时间  |
|  6   | production_date |   datetime   | 19 |   0    |    Y     |  N   |       | 生产日期  |
|  7   | quantity |   decimal   | 20 |   4    |    N     |  N   |       | 本次发货数量  |
|  8   | order_det_id |   varchar   | 36 |   0    |    N     |  N   |       | 对应订单明细Id  |
|  9   | receive_quantity |   decimal   | 20 |   4    |    Y     |  N   |   0.0000    | 本次收货数量  |
|  10   | receive_amount |   decimal   | 20 |   4    |    Y     |  N   |   0.0000    | 本次收货金额（单价*本次收货数量）  |
|  11   | amount |   decimal   | 20 |   4    |    Y     |  N   |       | 本次发货金额（单价*本次发货数量）  |
|  12   | price |   decimal   | 20 |   4    |    Y     |  N   |       | 单价  |
|  13   | refuse_quantity |   decimal   | 20 |   4    |    Y     |  N   |   0.0000    | 拒收数量  |
|  14   | refuse_amount |   decimal   | 20 |   4    |    Y     |  N   |   0.0000    | 拒收金额  |
|  15   | is_refuse |   int   | 10 |   0    |    Y     |  N   |   0    | 是否拒收（0否1是）  |
|  16   | refuse_reason |   varchar   | 500 |   0    |    Y     |  N   |       | 拒收理由  |
|  17   | refund_quantity |   decimal   | 20 |   4    |    Y     |  N   |   0.0000    | 退货数量  |
|  18   | refund_amount |   decimal   | 20 |   4    |    Y     |  N   |   0.0000    | 退货金额  |
|  19   | refuse_date |   datetime   | 19 |   0    |    Y     |  N   |       | 拒收日期  |
|  20   | sort |   int   | 10 |   0    |    Y     |  N   |       | 排序号  |
|  21   | is_import |   int   | 10 |   0    |    Y     |  N   |       | 是否进口:0否，1是  |
|  22   | application_scope |   varchar   | 100 |   0    |    Y     |  N   |       | 适用范围  |
|  23   | product_introduction |   varchar   | 500 |   0    |    Y     |  N   |       | 产品介绍  |
|  24   | brand |   varchar   | 100 |   0    |    Y     |  N   |       | 品牌  |
|  25   | management_class |   varchar   | 20 |   0    |    Y     |  N   |       | 管理类别(字典)  |
|  26   | model |   varchar   | 100 |   0    |    Y     |  N   |       | 型号  |
|  27   | big_package_quantity |   varchar   | 11 |   0    |    Y     |  N   |       | 通用大包装数量/包装数量(器械)  |
|  28   | biz_type |   int   | 10 |   0    |    Y     |  N   |       | 业务类型：1药品2医疗器械9其它  |
####  <a id="tb_deliver_main">tb_deliver_main</a>

**说明：** 发货单主表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | order_doc_no |   varchar   | 20 |   0    |    N     |  N   |       | 订单编号  |
|  3   | deliver_doc_no |   varchar   | 20 |   0    |    N     |  N   |       | 发货单号  |
|  4   | deliver_id |   varchar   | 36 |   0    |    Y     |  N   |       | 发货人id  |
|  5   | deliver_name |   varchar   | 255 |   0    |    Y     |  N   |       | 发货人姓名  |
|  6   | deliver_date |   datetime   | 19 |   0    |    Y     |  N   |       | 发货时间  |
|  7   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建人id  |
|  8   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建人姓名  |
|  9   | create_date |   datetime   | 19 |   0    |    N     |  N   |       | 创建时间  |
|  10   | confirm_id |   varchar   | 36 |   0    |    Y     |  N   |       | 收货人ID  |
|  11   | confirm_name |   varchar   | 100 |   0    |    Y     |  N   |       | 收货人姓名  |
|  12   | confirm_date |   datetime   | 19 |   0    |    Y     |  N   |       | 收货时间  |
|  13   | auto_accept_date |   datetime   | 19 |   0    |    N     |  N   |       | 自动收货时间  |
|  14   | deliver_status |   int   | 10 |   0    |    N     |  N   |   0    | 1已发货2已收货  |
|  15   | del_flag |   int   | 10 |   0    |    Y     |  N   |   0    | 0未删除1已删除  |
|  16   | procurer_id |   varchar   | 36 |   0    |    Y     |  N   |       | 采购商id  |
|  17   | procurer_name |   varchar   | 200 |   0    |    Y     |  N   |       | 采购商名称  |
|  18   | supplier_id |   varchar   | 36 |   0    |    Y     |  N   |       | 供应商id  |
|  19   | supplier_name |   varchar   | 200 |   0    |    Y     |  N   |       | 供应商名称  |
|  20   | deliver_det_count |   int   | 10 |   0    |    N     |  N   |       | 品规数  |
|  21   | total_price |   decimal   | 20 |   4    |    Y     |  N   |       | 发货金额合计  |
|  22   | receive_total_price |   decimal   | 20 |   4    |    Y     |  N   |       | 已收货金额合计  |
|  23   | is_delay |   int   | 10 |   0    |    Y     |  N   |       | 是否已延长收货（1是0否）  |
|  24   | refuse_date |   datetime   | 19 |   0    |    Y     |  N   |       | 拒收日期  |
|  25   | refuse_total_price |   decimal   | 20 |   4    |    Y     |  N   |   0.0000    | 拒收金额合计  |
|  26   | logistics_company |   varchar   | 50 |   0    |    Y     |  N   |   0.0000    | 物流公司取数据字典  |
|  27   | logistics_number |   varchar   | 50 |   0    |    Y     |  N   |   0.0000    | 物流单号  |
|  28   | refund_total_price |   decimal   | 20 |   4    |    Y     |  N   |   0.0000    | 退货金额合计  |
|  29   | biz_type |   int   | 10 |   0    |    Y     |  N   |       | 业务类型：1药品2医疗器械9其它  |
####  <a id="tb_dfs_acl_rule">tb_dfs_acl_rule</a>

**说明：** 文件系统的访问权限控制

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | bucket_name |   varchar   | 128 |   0    |    N     |  N   |       |   |
|  3   | file_path |   varchar   | 255 |   0    |    N     |  N   |       | 存放路径  |
|  4   | acl_rules |   varchar   | 512 |   0    |    N     |  N   |       | 访问控制的规则  |
|  5   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  6   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者  |
|  7   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  8   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  9   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者  |
|  10   | update_date |   timestamp   | 19 |   0    |    Y     |  N   |   CURRENT_TIMESTAMP    | 更新时间  |
|  11   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记，0-未删除1-已删除，默认0  |
|  12   | remark |   varchar   | 512 |   0    |    Y     |  N   |       | 需求备注  |
####  <a id="tb_dfs_bucket">tb_dfs_bucket</a>

**说明：** 存储空间

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | bucket_name |   varchar   | 128 |   0    |    N     |  N   |       | 存储空间名  |
|  3   | media_types |   varchar   | 512 |   0    |    Y     |  N   |   */*    | 支持的类型，类型之间用逗号分割  |
|  4   | allowed_ext_names |   varchar   | 128 |   0    |    Y     |  N   |       | 允许的扩展名，多个扩展名之间用逗号分割  |
|  5   | denied_ext_names |   varchar   | 128 |   0    |    Y     |  N   |       | 拒绝的扩展名，多个扩展名之间用逗号分割  |
|  6   | remark |   varchar   | 512 |   0    |    Y     |  N   |       | 备注  |
####  <a id="tb_dfs_file">tb_dfs_file</a>

**说明：** 文件信息

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | bucket_name |   varchar   | 128 |   0    |    N     |  N   |       | 存储空间名  |
|  3   | file_path |   varchar   | 255 |   0    |    N     |  N   |       | 上传文件存放路径  |
|  4   | file_key |   varchar   | 255 |   0    |    N     |  N   |       | 在FastDFS中的文件Key(路径)  |
|  5   | content_type |   varchar   | 128 |   0    |    Y     |  N   |       |   |
|  6   | digest |   varchar   | 255 |   0    |    Y     |  N   |       | 文件签名，用于判断是否是同一文件  |
|  7   | digest_type |   char   | 1 |   0    |    Y     |  N   |   1    | 文件签名算法类型（1：MD5；2：SHA-1；）  |
|  8   | file_name |   varchar   | 255 |   0    |    Y     |  N   |       | 上传时原始的文件名  |
|  9   | file_size |   bigint   | 19 |   0    |    N     |  N   |       | 文件大小，单位：byte(1KB=1024byte)  |
|  10   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  11   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者  |
|  12   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  13   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  14   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者  |
|  15   | update_date |   timestamp   | 19 |   0    |    Y     |  N   |   CURRENT_TIMESTAMP    | 更新时间  |
|  16   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记，0-未删除1-已删除，默认0  |
|  17   | remark |   varchar   | 512 |   0    |    Y     |  N   |       | 备注  |
####  <a id="tb_expo_activity">tb_expo_activity</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | expo_id |   varchar   | 36 |   0    |    N     |  N   |       | 所属展会ID  |
|  3   | apply_id |   varchar   | 36 |   0    |    Y     |  N   |       | 现场活动登记ID  |
|  4   | title |   varchar   | 128 |   0    |    Y     |  N   |       | 标题  |
|  5   | time |   varchar   | 100 |   0    |    Y     |  N   |       | 时间  |
|  6   | place |   varchar   | 255 |   0    |    Y     |  N   |       | 地点  |
|  7   | url |   varchar   | 255 |   0    |    Y     |  N   |       | 链接  |
|  8   | content |   longtext   | 2147483647 |   0    |    Y     |  N   |       | 富文本  |
|  9   | status |   int   | 10 |   0    |    Y     |  N   |   0    | 发布状态0-未发布，1-已发布  |
|  10   | sort |   int   | 10 |   0    |    Y     |  N   |       | 排序值  |
|  11   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  12   | del_flag |   int   | 10 |   0    |    Y     |  N   |   0    | 删除标记  |
|  13   | remark |   varchar   | 500 |   0    |    Y     |  N   |       | 备注  |
####  <a id="tb_expo_activity_apply">tb_expo_activity_apply</a>

**说明：** 现场活动登记表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | expo_id |   varchar   | 36 |   0    |    N     |  N   |       | 所属展会ID  |
|  3   | title |   varchar   | 128 |   0    |    Y     |  N   |       | 活动名称  |
|  4   | time |   varchar   | 100 |   0    |    Y     |  N   |       | 时间  |
|  5   | place |   varchar   | 255 |   0    |    Y     |  N   |       | 地点  |
|  6   | content |   longtext   | 2147483647 |   0    |    Y     |  N   |       | 活动内容（富文本）  |
|  7   | expo_parent_id |   varchar   | 36 |   0    |    Y     |  N   |       | 负责展馆ID  |
|  8   | area_id |   varchar   | 36 |   0    |    Y     |  N   |       | 负责展区ID  |
|  9   | status |   int   | 10 |   0    |    Y     |  N   |   0    | 审核状态0-待审核，1-审核通过，2-审核不通过  |
|  10   | audit_desc |   varchar   | 255 |   0    |    Y     |  N   |       | 审核描述  |
|  11   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  12   | creator_name |   varchar   | 50 |   0    |    Y     |  N   |       | 创建者姓名  |
|  13   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  14   | del_flag |   int   | 10 |   0    |    Y     |  N   |   0    | 删除标记  |
####  <a id="tb_expo_advert_position">tb_expo_advert_position</a>

**说明：** 广告位表管理表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | id  |
|  2   | pic_path |   varchar   | 255 |   0    |    Y     |  N   |       | 图片id  |
|  3   | pic_size |   decimal   | 20 |   0    |    N     |  N   |       | 图片文件大小，单位：byte(1KB=1024byte)  |
|  4   | pic_explain |   varchar   | 255 |   0    |    Y     |  N   |       | 图片说明  |
|  5   | platform |   int   | 10 |   0    |    N     |  N   |       | 所属平台：1-移动端2-PC端  |
|  6   | type |   int   | 10 |   0    |    N     |  N   |       | 类别:0-合作媒体1-展商名录2-支持单位3-轮播图  |
|  7   | link |   varchar   | 100 |   0    |    Y     |  N   |       | 着陆页  |
|  8   | sort |   int   | 10 |   0    |    Y     |  N   |       | 排序号  |
|  9   | pub_date |   datetime   | 19 |   0    |    Y     |  N   |       | 发布时间  |
|  10   | status |   int   | 10 |   0    |    N     |  N   |   1    | 状态0-未发布1-已发布  |
|  11   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者id  |
|  12   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者姓名  |
|  13   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  14   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者id  |
|  15   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者姓名  |
|  16   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  17   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 备注信息  |
####  <a id="tb_expo_area">tb_expo_area</a>

**说明：** 展区表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | id  |
|  2   | code |   varchar   | 20 |   0    |    Y     |  N   |       | 编码（树结构的层级编码）  |
|  3   | parent_id |   varchar   | 36 |   0    |    Y     |  N   |       | 父展区ID  |
|  4   | parent_code |   varchar   | 20 |   0    |    Y     |  N   |       | 父编码（树结构的层级编码）  |
|  5   | expo_session_id |   varchar   | 36 |   0    |    Y     |  N   |       | 展会届期ID  |
|  6   | number |   varchar   | 20 |   0    |    Y     |  N   |       | 展区编号  |
|  7   | name |   varchar   | 255 |   0    |    Y     |  N   |       | 展区名称  |
|  8   | name_en |   varchar   | 255 |   0    |    Y     |  N   |       | 展区英文名称  |
|  9   | description |   varchar   | 255 |   0    |    Y     |  N   |       | 展区介绍  |
|  10   | description_en |   varchar   | 255 |   0    |    Y     |  N   |       | 展区英文介绍  |
|  11   | total_area |   decimal   | 10 |   2    |    Y     |  N   |       | 展区总面积(㎡)  |
|  12   | standard_booth_amount |   int   | 10 |   0    |    Y     |  N   |       | 标准展位个数（上限）  |
|  13   | cornerbooth_amount |   int   | 10 |   0    |    Y     |  N   |       | 转角位数量（上限）  |
|  14   | booth_distribution_map |   varchar   | 255 |   0    |    Y     |  N   |       | 展位分布图  |
|  15   | picture |   varchar   | 255 |   0    |    Y     |  N   |       | 图片（缩略图或其他）  |
|  16   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记，0-未删除1-已删除，默认0  |
|  17   | useable |   int   | 10 |   0    |    N     |  N   |   1    | 是否启用  |
|  18   | is_leaf |   tinyint   | 3 |   0    |    Y     |  N   |   0    | 是否叶子节点0：否；1：是  |
|  19   | level |   int   | 10 |   0    |    Y     |  N   |   0    | 树级别,1为顶级节点  |
|  20   | sort |   int   | 10 |   0    |    Y     |  N   |   0    | 排序  |
|  21   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  22   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者姓名  |
|  23   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  24   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  25   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者姓名  |
|  26   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  27   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 备注  |
####  <a id="tb_expo_area_relation">tb_expo_area_relation</a>

**说明：** 展区分配表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | expo_id |   varchar   | 36 |   0    |    N     |  N   |       | 所属展会id  |
|  3   | expo_parent_id |   varchar   | 36 |   0    |    N     |  N   |       | 展馆id  |
|  4   | area_id |   varchar   | 36 |   0    |    N     |  N   |       | 展位ID  |
|  5   | type |   int   | 10 |   0    |    N     |  N   |   1    | 类型1展商报名  |
|  6   | relation_id |   varchar   | 36 |   0    |    N     |  N   |       | 关联ID  |
|  7   | creator_id |   varchar   | 36 |   0    |    N     |  N   |       | 创建者  |
|  8   | creator_name |   varchar   | 255 |   0    |    N     |  N   |       | 创建者姓名  |
|  9   | create_date |   datetime   | 19 |   0    |    N     |  N   |   CURRENT_TIMESTAMP    | 创建时间  |
####  <a id="tb_expo_audience">tb_expo_audience</a>

**说明：** 观众基础信息

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | name |   varchar   | 50 |   0    |    Y     |  N   |       |   |
|  3   | phone |   varchar   | 20 |   0    |    Y     |  N   |       |   |
|  4   | card_type |   varchar   | 20 |   0    |    Y     |  N   |       | 证件类型(1、身份证，2、港澳台通行证，3、护照)  |
|  5   | card |   varchar   | 64 |   0    |    Y     |  N   |       | 身份证  |
|  6   | email |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  7   | org_name |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  8   | org_type |   varchar   | 20 |   0    |    Y     |  N   |       | 字典项  |
|  9   | position |   varchar   | 50 |   0    |    Y     |  N   |       | 职务  |
|  10   | usci_no |   varchar   | 20 |   0    |    Y     |  N   |       | 统一社会信用代码  |
|  11   | source |   int   | 10 |   0    |    Y     |  N   |       | 来源(0：线上收集；1：线下收集导入)  |
|  12   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 备注  |
|  13   | useable |   int   | 10 |   0    |    N     |  N   |   1    | 是否启用  |
|  14   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
|  15   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  16   | creator_name |   varchar   | 50 |   0    |    Y     |  N   |       | 创建者姓名  |
|  17   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  18   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  19   | updater_name |   varchar   | 50 |   0    |    Y     |  N   |       | 更新者姓名  |
|  20   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  21   | open_id |   varchar   | 50 |   0    |    Y     |  N   |       | 微信openid  |
####  <a id="tb_expo_booth">tb_expo_booth</a>

**说明：** 展位表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 展位ID  |
|  2   | expo_session_id |   varchar   | 36 |   0    |    Y     |  N   |       | 展会届期ID  |
|  3   | number |   varchar   | 20 |   0    |    Y     |  N   |       | 展位编号  |
|  4   | name |   varchar   | 255 |   0    |    Y     |  N   |       | 展位名称  |
|  5   | expo_area_id |   varchar   | 36 |   0    |    Y     |  N   |       | 所属展区ID  |
|  6   | expo_area_number |   varchar   | 20 |   0    |    Y     |  N   |       | 所属展区编号  |
|  7   | type |   int   | 10 |   0    |    Y     |  N   |       | 展位类型：1-光地特装，2-标准展位3-线上展位  |
|  8   | specs |   decimal   | 10 |   2    |    Y     |  N   |       | 展位规格（㎡）  |
|  9   | position |   varchar   | 20 |   0    |    Y     |  N   |       | 场馆图位置（坐标：x,y）以逗号分隔  |
|  10   | description |   varchar   | 255 |   0    |    Y     |  N   |       | 展位描述  |
|  11   | state |   int   | 10 |   0    |    Y     |  N   |   0    | 状态（0：未分配；1：已分配）  |
|  12   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
|  13   | useable |   int   | 10 |   0    |    Y     |  N   |   1    | 是否启用  |
|  14   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  15   | creator_name |   varchar   | 50 |   0    |    Y     |  N   |       | 创建者姓名  |
|  16   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  17   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  18   | updater_name |   varchar   | 50 |   0    |    Y     |  N   |       | 更新者姓名  |
|  19   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
####  <a id="tb_expo_booth_copy1">tb_expo_booth_copy1</a>

**说明：** 展位表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 展位ID  |
|  2   | expo_session_id |   varchar   | 36 |   0    |    Y     |  N   |       | 展会届期ID  |
|  3   | number |   varchar   | 20 |   0    |    Y     |  N   |       | 展位编号  |
|  4   | name |   varchar   | 255 |   0    |    Y     |  N   |       | 展位名称  |
|  5   | expo_area_id |   varchar   | 36 |   0    |    Y     |  N   |       | 所属展区ID  |
|  6   | expo_area_number |   varchar   | 20 |   0    |    Y     |  N   |       | 所属展区编号  |
|  7   | type |   int   | 10 |   0    |    Y     |  N   |       | 展位类型：1-光地特装，2-标准展位3-线上展位  |
|  8   | specs |   decimal   | 10 |   2    |    Y     |  N   |       | 展位规格（㎡）  |
|  9   | position |   varchar   | 20 |   0    |    Y     |  N   |       | 场馆图位置（坐标：x,y）以逗号分隔  |
|  10   | description |   varchar   | 255 |   0    |    Y     |  N   |       | 展位描述  |
|  11   | state |   int   | 10 |   0    |    Y     |  N   |   0    | 状态（0：未分配；1：已分配）  |
|  12   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
|  13   | useable |   int   | 10 |   0    |    N     |  N   |   1    | 是否启用  |
|  14   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  15   | creator_name |   varchar   | 50 |   0    |    Y     |  N   |       | 创建者姓名  |
|  16   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  17   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  18   | updater_name |   varchar   | 50 |   0    |    Y     |  N   |       | 更新者姓名  |
|  19   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
####  <a id="tb_expo_booth_exhibitor">tb_expo_booth_exhibitor</a>

**说明：** 展位分配表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | booth_id |   varchar   | 36 |   0    |    Y     |  N   |       | 展位ID  |
|  3   | exhibitor_id |   varchar   | 36 |   0    |    Y     |  N   |       | 展商ID  |
####  <a id="tb_expo_contact_us">tb_expo_contact_us</a>

**说明：** 展会联系我们信息表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | name |   varchar   | 50 |   0    |    N     |  N   |       | 姓名  |
|  3   | mobile |   varchar   | 20 |   0    |    N     |  N   |       | 手机号  |
|  4   | company_name |   varchar   | 256 |   0    |    Y     |  N   |       | 公司名称  |
|  5   | cooperate_intention |   varchar   | 512 |   0    |    Y     |  N   |       | 合作意向  |
|  6   | remark |   varchar   | 256 |   0    |    Y     |  N   |       | 备注  |
|  7   | del_flag |   int   | 10 |   0    |    Y     |  N   |   0    | 删除标记  |
|  8   | create_date |   datetime   | 19 |   0    |    N     |  N   |       | 创建时间  |
|  9   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新人id  |
|  10   | updater_name |   varchar   | 50 |   0    |    Y     |  N   |       | 更新人姓名  |
|  11   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新人日期  |
|  12   | contact_status |   int   | 10 |   0    |    Y     |  N   |   0    | 1-已联系、0-未联系  |
####  <a id="tb_expo_curator">tb_expo_curator</a>

**说明：** 馆长管理表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | expo_id |   varchar   | 36 |   0    |    N     |  N   |       | 所属展会ID  |
|  3   | user_id |   varchar   | 36 |   0    |    N     |  N   |       | 馆长用户id  |
|  4   | company_name |   varchar   | 255 |   0    |    Y     |  N   |       | 所属单位  |
|  5   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 备注信息  |
|  6   | expo_parent_id |   varchar   | 36 |   0    |    Y     |  N   |       | 负责展馆ID  |
|  7   | area_id |   varchar   | 36 |   0    |    Y     |  N   |       | 负责展区ID  |
|  8   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  9   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者姓名  |
|  10   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  11   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  12   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者姓名  |
|  13   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  14   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
####  <a id="tb_expo_dealer">tb_expo_dealer</a>

**说明：** 经销商基本信息表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | name |   varchar   | 255 |   0    |    Y     |  N   |       | 姓名  |
|  3   | mobile |   varchar   | 20 |   0    |    Y     |  N   |       | 手机号  |
|  4   | id_card |   varchar   | 20 |   0    |    Y     |  N   |       | 证件号  |
|  5   | province |   varchar   | 20 |   0    |    Y     |  N   |       | 来源地-省  |
|  6   | city |   varchar   | 20 |   0    |    Y     |  N   |       | 来源地-市  |
|  7   | country |   varchar   | 20 |   0    |    Y     |  N   |       | 来源地-县  |
|  8   | remark |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  9   | source |   int   | 10 |   0    |    Y     |  N   |       | 来源(0：线上收集；1：线下收集导入)  |
|  10   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
|  11   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  12   | creator_name |   varchar   | 50 |   0    |    Y     |  N   |       | 创建者姓名  |
|  13   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  14   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  15   | updater_name |   varchar   | 50 |   0    |    Y     |  N   |       | 更新者姓名  |
|  16   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  17   | type |   int   | 10 |   0    |    Y     |  N   |       | 类型:0:产品代理1:产品推广2:生产厂家  |
|  18   | business_area |   text   | 65535 |   0    |    Y     |  N   |       | 业务所在地  |
|  19   | business_scope |   varchar   | 72 |   0    |    Y     |  N   |       | 业务领域(数据字典471)  |
|  20   | open_id |   varchar   | 50 |   0    |    Y     |  N   |       | 微信openid  |
####  <a id="tb_expo_exhibitor">tb_expo_exhibitor</a>

**说明：** 展商基础信息表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | name |   varchar   | 255 |   0    |    Y     |  N   |       | 企业名称  |
|  3   | name_en |   varchar   | 255 |   0    |    Y     |  N   |       | 企业英文名称  |
|  4   | usci_no |   varchar   | 20 |   0    |    Y     |  N   |       | 统一社会信用代码  |
|  5   | industry |   varchar   | 255 |   0    |    Y     |  N   |       | 所属行业  |
|  6   | province |   varchar   | 20 |   0    |    Y     |  N   |       | 省  |
|  7   | city |   varchar   | 20 |   0    |    Y     |  N   |       | 市  |
|  8   | country |   varchar   | 20 |   0    |    Y     |  N   |       | 县  |
|  9   | legal_person |   varchar   | 50 |   0    |    Y     |  N   |       | 法人  |
|  10   | address |   varchar   | 255 |   0    |    Y     |  N   |       | 公司地址  |
|  11   | zip_code |   varchar   | 20 |   0    |    Y     |  N   |       | 邮编  |
|  12   | tel |   varchar   | 20 |   0    |    Y     |  N   |       | 电话  |
|  13   | card |   varchar   | 20 |   0    |    Y     |  N   |       | 身份证  |
|  14   | fax |   varchar   | 20 |   0    |    Y     |  N   |       | 传真  |
|  15   | parent_company |   varchar   | 255 |   0    |    Y     |  N   |       | 母公司  |
|  16   | website |   varchar   | 255 |   0    |    Y     |  N   |       | 公司官网  |
|  17   | profile |   varchar   | 1000 |   0    |    Y     |  N   |       | 企业简介  |
|  18   | product_introduction |   varchar   | 1000 |   0    |    Y     |  N   |       | 公司产品介绍  |
|  19   | linkman |   varchar   | 50 |   0    |    Y     |  N   |       | 联系人  |
|  20   | dept |   varchar   | 255 |   0    |    Y     |  N   |       | 联系人部门  |
|  21   | position |   varchar   | 50 |   0    |    Y     |  N   |       | 联系人职务  |
|  22   | mobile |   varchar   | 20 |   0    |    Y     |  N   |       | 联系人手机  |
|  23   | qq |   varchar   | 20 |   0    |    Y     |  N   |       | QQ  |
|  24   | wechat |   varchar   | 20 |   0    |    Y     |  N   |       | 微信  |
|  25   | email |   varchar   | 255 |   0    |    Y     |  N   |       | 邮箱  |
|  26   | remark |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  27   | status |   int   | 10 |   0    |    N     |  N   |   0    | 审核状态:0-待审核,1-通过,2-未通过  |
|  28   | source |   int   | 10 |   0    |    Y     |  N   |       | 来源(0：线上收集；1：线下收集导入)  |
|  29   | useable |   int   | 10 |   0    |    N     |  N   |   1    | 是否启用  |
|  30   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
|  31   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  32   | creator_name |   varchar   | 50 |   0    |    Y     |  N   |       | 创建者姓名  |
|  33   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  34   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  35   | updater_name |   varchar   | 50 |   0    |    Y     |  N   |       | 更新者姓名  |
|  36   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  37   | company_introdct |   varchar   | 1000 |   0    |    Y     |  N   |       | 公司介绍-中文（已废弃）  |
|  38   | product_introdct |   varchar   | 1000 |   0    |    Y     |  N   |       | 产品介绍（已废弃）  |
|  39   | corporate_logo_image_url |   varchar   | 512 |   0    |    Y     |  N   |       | 企业logourl  |
|  40   | corporate_style_image_url |   varchar   | 512 |   0    |    Y     |  N   |       | 企业风采url  |
|  41   | company_introdct_en |   varchar   | 1000 |   0    |    Y     |  N   |       | 公司介绍-英文  |
|  42   | open_id |   varchar   | 50 |   0    |    Y     |  N   |       | 微信openid  |
|  43   | user_id |   bigint   | 19 |   0    |    Y     |  N   |       | 用户id  |
|  44   | register_type |   tinyint   | 3 |   0    |    N     |  N   |       | 注册方式：1账号，2：手机号，3：邮箱  |
####  <a id="tb_expo_exhibitor_apply">tb_expo_exhibitor_apply</a>

**说明：** 展商信息登记申请表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | user_id |   bigint   | 19 |   0    |    N     |  N   |       | 用户id  |
|  3   | name |   varchar   | 255 |   0    |    Y     |  N   |       | 企业名称  |
|  4   | name_en |   varchar   | 255 |   0    |    Y     |  N   |       | 企业英文名称  |
|  5   | usci_no |   varchar   | 20 |   0    |    Y     |  N   |       | 统一社会信用代码  |
|  6   | industry |   varchar   | 255 |   0    |    Y     |  N   |       | 所属行业  |
|  7   | province |   varchar   | 20 |   0    |    Y     |  N   |       | 省  |
|  8   | city |   varchar   | 20 |   0    |    Y     |  N   |       | 市  |
|  9   | country |   varchar   | 20 |   0    |    Y     |  N   |       | 县  |
|  10   | address |   varchar   | 255 |   0    |    Y     |  N   |       | 公司地址  |
|  11   | website |   varchar   | 255 |   0    |    Y     |  N   |       | 公司官网  |
|  12   | profile |   varchar   | 255 |   0    |    Y     |  N   |       | 企业简介  |
|  13   | product_introduction |   varchar   | 255 |   0    |    Y     |  N   |       | 公司产品介绍  |
|  14   | corporate_logo_image_url |   varchar   | 255 |   0    |    Y     |  N   |       | 企业logourl  |
|  15   | corporate_style_image_url |   varchar   | 255 |   0    |    Y     |  N   |       | 企业风采url  |
|  16   | linkman |   varchar   | 50 |   0    |    Y     |  N   |       | 联系人  |
|  17   | mobile |   varchar   | 20 |   0    |    Y     |  N   |       | 联系人手机  |
|  18   | tel |   varchar   | 20 |   0    |    Y     |  N   |       | 电话  |
|  19   | wechat |   varchar   | 20 |   0    |    Y     |  N   |       | 微信  |
|  20   | email |   varchar   | 255 |   0    |    Y     |  N   |       | 邮箱  |
|  21   | remark |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  22   | status |   int   | 10 |   0    |    Y     |  N   |   0    | 审核状态:0-待审核,1-通过,2-未通过  |
|  23   | reason |   varchar   | 255 |   0    |    Y     |  N   |       | 未通过原因  |
|  24   | source |   int   | 10 |   0    |    Y     |  N   |       | 来源(0：线上收集；1：线下收集导入)  |
|  25   | useable |   int   | 10 |   0    |    N     |  N   |   1    | 是否启用  |
|  26   | is_current |   int   | 10 |   0    |    N     |  N   |   0    | 是否为当前记录0:是1:否  |
|  27   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
|  28   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  29   | creator_name |   varchar   | 50 |   0    |    Y     |  N   |       | 创建者姓名  |
|  30   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  31   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  32   | updater_name |   varchar   | 50 |   0    |    Y     |  N   |       | 更新者姓名  |
|  33   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
####  <a id="tb_expo_exhibitor_copy2">tb_expo_exhibitor_copy2</a>

**说明：** 展商基础信息表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | name |   varchar   | 255 |   0    |    Y     |  N   |       | 企业名称  |
|  3   | name_en |   varchar   | 255 |   0    |    Y     |  N   |       | 企业英文名称  |
|  4   | usci_no |   varchar   | 20 |   0    |    Y     |  N   |       | 统一社会信用代码  |
|  5   | industry |   varchar   | 255 |   0    |    Y     |  N   |       | 所属行业  |
|  6   | province |   varchar   | 20 |   0    |    Y     |  N   |       | 省  |
|  7   | city |   varchar   | 20 |   0    |    Y     |  N   |       | 市  |
|  8   | country |   varchar   | 20 |   0    |    Y     |  N   |       | 县  |
|  9   | legal_person |   varchar   | 50 |   0    |    Y     |  N   |       | 法人  |
|  10   | address |   varchar   | 255 |   0    |    Y     |  N   |       | 公司地址  |
|  11   | zip_code |   varchar   | 20 |   0    |    Y     |  N   |       | 邮编  |
|  12   | tel |   varchar   | 20 |   0    |    Y     |  N   |       | 电话  |
|  13   | card |   varchar   | 20 |   0    |    Y     |  N   |       | 身份证  |
|  14   | fax |   varchar   | 20 |   0    |    Y     |  N   |       | 传真  |
|  15   | parent_company |   varchar   | 255 |   0    |    Y     |  N   |       | 母公司  |
|  16   | website |   varchar   | 255 |   0    |    Y     |  N   |       | 公司官网  |
|  17   | profile |   varchar   | 1000 |   0    |    Y     |  N   |       | 企业简介  |
|  18   | product_introduction |   varchar   | 1000 |   0    |    Y     |  N   |       | 公司产品介绍  |
|  19   | linkman |   varchar   | 50 |   0    |    Y     |  N   |       | 联系人  |
|  20   | dept |   varchar   | 255 |   0    |    Y     |  N   |       | 联系人部门  |
|  21   | position |   varchar   | 50 |   0    |    Y     |  N   |       | 联系人职务  |
|  22   | mobile |   varchar   | 20 |   0    |    Y     |  N   |       | 联系人手机  |
|  23   | qq |   varchar   | 20 |   0    |    Y     |  N   |       | QQ  |
|  24   | wechat |   varchar   | 20 |   0    |    Y     |  N   |       | 微信  |
|  25   | email |   varchar   | 255 |   0    |    Y     |  N   |       | 邮箱  |
|  26   | remark |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  27   | status |   int   | 10 |   0    |    N     |  N   |   0    | 审核状态:0-待审核,1-通过,2-未通过  |
|  28   | source |   int   | 10 |   0    |    Y     |  N   |       | 来源(0：线上收集；1：线下收集导入)  |
|  29   | useable |   int   | 10 |   0    |    N     |  N   |   1    | 是否启用  |
|  30   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
|  31   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  32   | creator_name |   varchar   | 50 |   0    |    Y     |  N   |       | 创建者姓名  |
|  33   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  34   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  35   | updater_name |   varchar   | 50 |   0    |    Y     |  N   |       | 更新者姓名  |
|  36   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  37   | company_introdct |   varchar   | 1000 |   0    |    Y     |  N   |       | 公司介绍-中文（已废弃）  |
|  38   | product_introdct |   varchar   | 1000 |   0    |    Y     |  N   |       | 产品介绍（已废弃）  |
|  39   | corporate_logo_image_url |   varchar   | 512 |   0    |    Y     |  N   |       | 企业logourl  |
|  40   | corporate_style_image_url |   varchar   | 512 |   0    |    Y     |  N   |       | 企业风采url  |
|  41   | company_introdct_en |   varchar   | 1000 |   0    |    Y     |  N   |       | 公司介绍-英文  |
|  42   | open_id |   varchar   | 50 |   0    |    Y     |  N   |       | 微信openid  |
|  43   | user_id |   bigint   | 19 |   0    |    Y     |  N   |       | 用户id  |
|  44   | register_type |   tinyint   | 3 |   0    |    N     |  N   |       | 注册方式：1账号，2：手机号，3：邮箱  |
####  <a id="tb_expo_forum">tb_expo_forum</a>

**说明：** 展会论坛表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 论坛ID  |
|  2   | expo_session_id |   varchar   | 36 |   0    |    Y     |  N   |       | 展会届期ID  |
|  3   | name |   varchar   | 255 |   0    |    Y     |  N   |       | 论坛名称  |
|  4   | name_en |   varchar   | 255 |   0    |    Y     |  N   |       | 论坛英文名称  |
|  5   | subject |   varchar   | 255 |   0    |    Y     |  N   |       | 论坛主题  |
|  6   | subject_en |   varchar   | 255 |   0    |    Y     |  N   |       | 论坛主题（英文）  |
|  7   | organizer |   varchar   | 255 |   0    |    Y     |  N   |       | 主办单位  |
|  8   | position |   varchar   | 255 |   0    |    Y     |  N   |       | 论坛位置（位置描述）  |
|  9   | start_time |   datetime   | 19 |   0    |    Y     |  N   |       |   |
|  10   | end_time |   datetime   | 19 |   0    |    Y     |  N   |       |   |
|  11   | description |   varchar   | 1024 |   0    |    Y     |  N   |       | 论坛说明  |
|  12   | description_en |   varchar   | 1024 |   0    |    Y     |  N   |       | 论坛说明（英文）  |
|  13   | sort |   int   | 10 |   0    |    Y     |  N   |       | 排序号  |
|  14   | is_charge |   tinyint   | 3 |   0    |    Y     |  N   |       | 是否收费  |
|  15   | reg_fee |   decimal   | 10 |   4    |    Y     |  N   |       | 报名费用  |
|  16   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 备注  |
|  17   | picture |   varchar   | 255 |   0    |    Y     |  N   |       | 图片（缩略图或其他）  |
|  18   | expo_area_id |   varchar   | 36 |   0    |    Y     |  N   |       | 所在展区ID  |
|  19   | expo_area_number |   varchar   | 20 |   0    |    Y     |  N   |       | 所属展区编号  |
|  20   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
|  21   | useable |   int   | 10 |   0    |    N     |  N   |   1    | 是否启用  |
|  22   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  23   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者姓名  |
|  24   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  25   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  26   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者姓名  |
|  27   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  28   | forum_type |   int   | 10 |   0    |    Y     |  N   |       | 0-非专业，1-专业  |
|  29   | quota_number |   int   | 10 |   0    |    Y     |  N   |       | 报名名额  |
|  30   | type |   int   | 10 |   0    |    N     |  N   |   0    | 类型：0:普通论坛1:高峰论坛  |
|  31   | is_main |   tinyint   | 3 |   0    |    N     |  N   |   0    | 是否主论坛:0-否,1-是  |
####  <a id="tb_expo_forum_agenda">tb_expo_forum_agenda</a>

**说明：** 论坛议程表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | content |   varchar   | 255 |   0    |    Y     |  N   |       | 议程内容  |
|  3   | start_time |   datetime   | 19 |   0    |    Y     |  N   |       | 开始时间  |
|  4   | end_time |   datetime   | 19 |   0    |    Y     |  N   |       | 截止时间  |
|  5   | forum_id |   varchar   | 36 |   0    |    Y     |  N   |       | 论坛ID  |
####  <a id="tb_expo_forum_focus">tb_expo_forum_focus</a>

**说明：** 论坛关注表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | type |   int   | 10 |   0    |    Y     |  N   |       | 参与类型1：观众；2：展商；3：媒体，6：经销商  |
|  3   | participant_id |   varchar   | 36 |   0    |    Y     |  N   |       | 参与者ID(报名对应的基本信息ID)  |
|  4   | forum_id |   varchar   | 36 |   0    |    Y     |  N   |       | 论坛ID  |
|  5   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  6   | status |   int   | 10 |   0    |    Y     |  N   |       | 审核状态（0：待审核，1审核通过，2：审核不通过）  |
|  7   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  8   | updater_name |   varchar   | 50 |   0    |    Y     |  N   |       | 更新者  |
|  9   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  10   | reason |   varchar   | 255 |   0    |    Y     |  N   |       | 审核不通过原因  |
|  11   | code |   varchar   | 45 |   0    |    Y     |  N   |       | 验证码  |
|  12   | del_flag |   int   | 10 |   0    |    Y     |  N   |   0    | 是否删除(0:否，1：是)  |
|  13   | expo_id |   varchar   | 36 |   0    |    Y     |  N   |       | 届期id  |
|  14   | reg_id |   varchar   | 36 |   0    |    Y     |  N   |       | 报名id  |
####  <a id="tb_expo_forum_guest">tb_expo_forum_guest</a>

**说明：** 论坛嘉宾

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | forum_id |   varchar   | 36 |   0    |    Y     |  N   |       | 论坛ID  |
|  3   | guest_id |   varchar   | 36 |   0    |    Y     |  N   |       | 嘉宾ID  |
####  <a id="tb_expo_forum_order">tb_expo_forum_order</a>

**说明：** 报名论坛订单表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | order_sn |   varchar   | 30 |   0    |    Y     |  N   |       | 订单编号  |
|  3   | expo_session_id |   varchar   | 36 |   0    |    Y     |  N   |       |   |
|  4   | forum_id |   varchar   | 36 |   0    |    Y     |  N   |       |   |
|  5   | forum_name |   varchar   | 255 |   0    |    Y     |  N   |       | 论坛名称（冗余字段）  |
|  6   | user_id |   varchar   | 36 |   0    |    Y     |  N   |       | 报名人ID  |
|  7   | user_name |   varchar   | 60 |   0    |    Y     |  N   |       | 报名人姓名  |
|  8   | mobile |   varchar   | 20 |   0    |    Y     |  N   |       | 报名人手机  |
|  9   | order_status |   tinyint   | 3 |   0    |    Y     |  N   |       | 0:已确认；1:已取消；2:无效；3:已支付  |
|  10   | order_amount |   decimal   | 10 |   4    |    Y     |  N   |   0.0000    | 订单金额  |
|  11   | payment_code |   varchar   | 20 |   0    |    Y     |  N   |       | 支付方式编码  |
|  12   | payment_name |   varchar   | 255 |   0    |    Y     |  N   |       | 支付方式名称  |
|  13   | create_time |   datetime   | 19 |   0    |    Y     |  N   |       | 订单生成时间  |
|  14   | cancel_time |   datetime   | 19 |   0    |    Y     |  N   |       | 取消订单时间  |
|  15   | pay_time |   datetime   | 19 |   0    |    Y     |  N   |       | 支付时间  |
|  16   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 备注  |
####  <a id="tb_expo_guest">tb_expo_guest</a>

**说明：** 展会嘉宾

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | expo_session_id |   varchar   | 36 |   0    |    Y     |  N   |       | 届期ID  |
|  3   | name |   varchar   | 50 |   0    |    Y     |  N   |       | 嘉宾姓名  |
|  4   | name_en |   varchar   | 50 |   0    |    Y     |  N   |       | 英文名  |
|  5   | mobile |   varchar   | 20 |   0    |    Y     |  N   |       | 手机  |
|  6   | photo |   varchar   | 255 |   0    |    Y     |  N   |       | 照片  |
|  7   | org_name |   varchar   | 255 |   0    |    Y     |  N   |       | 所属机构  |
|  8   | duties |   varchar   | 255 |   0    |    Y     |  N   |       | 职务  |
|  9   | title |   varchar   | 20 |   0    |    Y     |  N   |       | 头衔  |
|  10   | category |   varchar   | 20 |   0    |    Y     |  N   |       | 类别  |
|  11   | profile |   varchar   | 800 |   0    |    Y     |  N   |       | 简介  |
|  12   | remark |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  13   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
|  14   | useable |   int   | 10 |   0    |    N     |  N   |   1    | 是否启用  |
|  15   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  16   | creator_name |   varchar   | 50 |   0    |    Y     |  N   |       | 创建者姓名  |
|  17   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  18   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  19   | updater_name |   varchar   | 50 |   0    |    Y     |  N   |       | 更新者姓名  |
|  20   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  21   | sort |   int   | 10 |   0    |    Y     |  N   |   0    | 排序  |
####  <a id="tb_expo_guest_plan">tb_expo_guest_plan</a>

**说明：** 展会嘉宾计划安排表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | expo_session_id |   varchar   | 36 |   0    |    Y     |  N   |       | 届期ID  |
|  3   | subject |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  4   | guest_id |   varchar   | 36 |   0    |    Y     |  N   |       |   |
|  5   | forum_id |   varchar   | 50 |   0    |    N     |  N   |       | 论坛id  |
|  6   | remark |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  7   | usable |   int   | 10 |   0    |    Y     |  N   |   1    | 启用（0：不启用；1：启用）  |
|  8   | del_flag |   int   | 10 |   0    |    Y     |  N   |       | 删除标记（0：正常；1：已删除）  |
|  9   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  10   | creator_name |   varchar   | 50 |   0    |    Y     |  N   |       | 创建者姓名  |
|  11   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  12   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  13   | updater_name |   varchar   | 50 |   0    |    Y     |  N   |       | 更新者姓名  |
|  14   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
####  <a id="tb_expo_guest_trip">tb_expo_guest_trip</a>

**说明：** 嘉宾计划安排子行程表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | plan_id |   varchar   | 36 |   0    |    Y     |  N   |       | 嘉宾计划安排ID  |
|  3   | guest_id |   varchar   | 36 |   0    |    Y     |  N   |       |   |
|  4   | start_time |   datetime   | 19 |   0    |    Y     |  N   |       | 行程开始时间  |
|  5   | end_time |   datetime   | 19 |   0    |    Y     |  N   |       | 行程结束时间  |
|  6   | content |   varchar   | 255 |   0    |    Y     |  N   |       | 行程内容  |
|  7   | notification_msg |   varchar   | 255 |   0    |    Y     |  N   |       | 通知信息  |
|  8   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 备注  |
|  9   | del_flag |   int   | 10 |   0    |    Y     |  N   |   0    | 删除标记（0：未删除；1：已删除）  |
|  10   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  11   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者姓名  |
|  12   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  13   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  14   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者姓名  |
|  15   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
####  <a id="tb_expo_hall_hotel">tb_expo_hall_hotel</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | expo_session_id |   varchar   | 36 |   0    |    Y     |  N   |       | 届期  |
|  3   | hotel_id |   varchar   | 36 |   0    |    Y     |  N   |       | 酒店id  |
|  4   | expo_hall |   varchar   | 36 |   0    |    Y     |  N   |       | 展馆  |
|  5   | distance |   decimal   | 10 |   2    |    Y     |  N   |       | 距离（公里）  |
|  6   | drive_time |   int   | 10 |   0    |    Y     |  N   |       | 驾车时间（分钟）  |
|  7   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  8   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者姓名  |
|  9   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  10   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  11   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者姓名  |
|  12   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
####  <a id="tb_expo_hotel">tb_expo_hotel</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | name |   varchar   | 255 |   0    |    Y     |  N   |       | 酒店名称  |
|  3   | name_en |   varchar   | 255 |   0    |    Y     |  N   |       | 酒店名称（英文）  |
|  4   | type |   int   | 10 |   0    |    Y     |  N   |   1    | 酒店类型（1展会平台，2高峰论坛）  |
|  5   | sort |   int   | 10 |   0    |    Y     |  N   |       | 排序号  |
|  6   | star_grade |   varchar   | 255 |   0    |    Y     |  N   |       | 酒店星级  |
|  7   | location |   varchar   | 255 |   0    |    Y     |  N   |       | 酒店位置  |
|  8   | map_link_pc |   varchar   | 1000 |   0    |    Y     |  N   |       | 酒店地图位置链接(PC)  |
|  9   | map_link_mobile |   varchar   | 1000 |   0    |    Y     |  N   |       | 酒店地图位置链接(移动端)  |
|  10   | coordinate |   varchar   | 255 |   0    |    Y     |  N   |       | 坐标  |
|  11   | opening_date |   varchar   | 50 |   0    |    Y     |  N   |       | 开业时间  |
|  12   | tel |   varchar   | 20 |   0    |    Y     |  N   |       | 酒店联系电话  |
|  13   | total_rooms |   int   | 10 |   0    |    Y     |  N   |       | 总房间数  |
|  14   | superior_room_area |   decimal   | 10 |   2    |    Y     |  N   |       | 高级房面积  |
|  15   | deluxe_room_area |   decimal   | 10 |   2    |    Y     |  N   |       | 豪华房面积  |
|  16   | introduce |   varchar   | 3000 |   0    |    Y     |  N   |       | 酒店介绍  |
|  17   | introduce_en |   varchar   | 800 |   0    |    Y     |  N   |       | 酒店介绍（英文）  |
|  18   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 备注  |
|  19   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
|  20   | useable |   int   | 10 |   0    |    N     |  N   |   1    | 是否启用  |
|  21   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  22   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者姓名  |
|  23   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  24   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  25   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者姓名  |
|  26   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  27   | thumbnail |   varchar   | 255 |   0    |    Y     |  N   |       | 缩略图  |
####  <a id="tb_expo_hotel_picture">tb_expo_hotel_picture</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | hotel_id |   varchar   | 36 |   0    |    Y     |  N   |       | 酒店id  |
|  3   | path |   varchar   | 255 |   0    |    Y     |  N   |       | 酒店图片地址  |
|  4   | size |   decimal   | 10 |   2    |    Y     |  N   |       | 图片大小  |
|  5   | file_ext |   varchar   | 20 |   0    |    Y     |  N   |       | 图片文件扩展名  |
####  <a id="tb_expo_hotel_room">tb_expo_hotel_room</a>

**说明：** 酒店房型

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | id  |
|  2   | hotel_id |   varchar   | 36 |   0    |    N     |  N   |       | 酒店id  |
|  3   | name |   varchar   | 200 |   0    |    N     |  N   |       | 房型名称  |
|  4   | bed_type |   varchar   | 255 |   0    |    N     |  N   |       | 床型  |
|  5   | area |   varchar   | 255 |   0    |    N     |  N   |   0    | 面积  |
|  6   | floor |   int   | 10 |   0    |    N     |  N   |   1    | 楼层  |
|  7   | price |   decimal   | 20 |   2    |    N     |  N   |   0.00    | 价格  |
|  8   | stock |   decimal   | 20 |   0    |    N     |  N   |   0    | 库存  |
|  9   | remark |   varchar   | 500 |   0    |    N     |  N   |       | 备注  |
|  10   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
|  11   | useable |   int   | 10 |   0    |    N     |  N   |   1    | 是否启用  |
|  12   | creator_id |   varchar   | 36 |   0    |    N     |  N   |       | 创建者  |
|  13   | creator_name |   varchar   | 255 |   0    |    N     |  N   |       | 创建者姓名  |
|  14   | create_date |   datetime   | 19 |   0    |    N     |  N   |   CURRENT_TIMESTAMP    | 创建时间  |
|  15   | updater_id |   varchar   | 36 |   0    |    N     |  N   |       | 更新者  |
|  16   | updater_name |   varchar   | 255 |   0    |    N     |  N   |       | 更新者姓名  |
|  17   | update_date |   datetime   | 19 |   0    |    N     |  N   |   CURRENT_TIMESTAMP    | 更新时间  |
####  <a id="tb_expo_inauguration_staff">tb_expo_inauguration_staff</a>

**说明：** 开幕式人员

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | id  |
|  2   | expo_id |   varchar   | 50 |   0    |    N     |  N   |       | 届期  |
|  3   | name |   varchar   | 200 |   0    |    N     |  N   |       | 姓名  |
|  4   | company |   varchar   | 200 |   0    |    N     |  N   |       | 单位  |
|  5   | post |   varchar   | 50 |   0    |    N     |  N   |       | 职位  |
|  6   | mobile |   varchar   | 50 |   0    |    N     |  N   |       | 联系电话  |
|  7   | id_card |   varchar   | 50 |   0    |    N     |  N   |       | 身份证号  |
|  8   | expo_parent_id |   varchar   | 36 |   0    |    Y     |  N   |       | 展馆编码  |
|  9   | area_id |   varchar   | 36 |   0    |    Y     |  N   |       | 展区编码  |
|  10   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
|  11   | useable |   int   | 10 |   0    |    N     |  N   |   1    | 是否启用  |
|  12   | creator_id |   varchar   | 36 |   0    |    N     |  N   |       | 创建者  |
|  13   | creator_name |   varchar   | 255 |   0    |    N     |  N   |       | 创建者姓名  |
|  14   | create_date |   datetime   | 19 |   0    |    N     |  N   |   CURRENT_TIMESTAMP    | 创建时间  |
|  15   | updater_id |   varchar   | 36 |   0    |    N     |  N   |       | 更新者  |
|  16   | updater_name |   varchar   | 255 |   0    |    N     |  N   |       | 更新者姓名  |
|  17   | update_date |   datetime   | 19 |   0    |    N     |  N   |   CURRENT_TIMESTAMP    | 更新时间  |
####  <a id="tb_expo_industry">tb_expo_industry</a>

**说明：** 所属行业

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | name |   varchar   | 255 |   0    |    Y     |  N   |       | 名称  |
|  3   | name_en |   varchar   | 255 |   0    |    Y     |  N   |       | 名称  |
|  4   | parent_id |   varchar   | 36 |   0    |    N     |  N   |       | 父级id  |
|  5   | parent_name |   varchar   | 255 |   0    |    Y     |  N   |       | 父级名称  |
|  6   | parent_name_en |   varchar   | 255 |   0    |    Y     |  N   |       | 父级名称  |
|  7   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 备注  |
|  8   | status |   int   | 10 |   0    |    Y     |  N   |   0    | 发布状态0-未发布，1-已发布  |
|  9   | sort |   int   | 10 |   0    |    Y     |  N   |   0    | 排序  |
|  10   | useable |   int   | 10 |   0    |    N     |  N   |   1    | 是否启用  |
|  11   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
|  12   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建人id  |
|  13   | create_date |   datetime   | 19 |   0    |    N     |  N   |       | 创建时间  |
|  14   | creator_name |   varchar   | 50 |   0    |    Y     |  N   |       | 创建者姓名  |
|  15   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者id  |
|  16   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  17   | updater_name |   varchar   | 50 |   0    |    Y     |  N   |       | 更新者姓名  |
####  <a id="tb_expo_industry_field">tb_expo_industry_field</a>

**说明：** 行业领域

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | name |   varchar   | 255 |   0    |    Y     |  N   |       | 领域名称  |
|  3   | name_en |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  4   | expo_session_id |   varchar   | 36 |   0    |    Y     |  N   |       | 展会届期ID  |
|  5   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 备注  |
|  6   | status |   int   | 10 |   0    |    Y     |  N   |   0    | 发布状态0-未发布，1-已发布  |
|  7   | sort |   int   | 10 |   0    |    Y     |  N   |   0    | 排序  |
|  8   | useable |   int   | 10 |   0    |    N     |  N   |   1    | 是否启用  |
|  9   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
|  10   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建人id  |
|  11   | create_date |   datetime   | 19 |   0    |    N     |  N   |       | 创建时间  |
|  12   | creator_name |   varchar   | 50 |   0    |    Y     |  N   |       | 创建者姓名  |
|  13   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者id  |
|  14   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  15   | updater_name |   varchar   | 50 |   0    |    Y     |  N   |       | 更新者姓名  |
####  <a id="tb_expo_industry_field_focus">tb_expo_industry_field_focus</a>

**说明：** 关注行业领域表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | type |   int   | 10 |   0    |    Y     |  N   |       | 参与类型0：展商；1：媒体；2：观众  |
|  3   | participant_id |   varchar   | 36 |   0    |    Y     |  N   |       | 参与者ID(报名ID)  |
|  4   | industry_field_id |   varchar   | 36 |   0    |    Y     |  N   |       | 行业领域ID  |
####  <a id="tb_expo_info">tb_expo_info</a>

**说明：** 展会届期信息

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 展会ID  |
|  2   | name |   varchar   | 100 |   0    |    Y     |  N   |       | 展会全称  |
|  3   | name_en |   varchar   | 255 |   0    |    Y     |  N   |       | 展会英文全称  |
|  4   | year |   int   | 10 |   0    |    Y     |  N   |       |   |
|  5   | session |   varchar   | 20 |   0    |    Y     |  N   |       | 展会届期  |
|  6   | reg_deadline |   datetime   | 19 |   0    |    Y     |  N   |       | 报名截止时间  |
|  7   | start_time |   datetime   | 19 |   0    |    Y     |  N   |       | 展会开始时间  |
|  8   | end_time |   datetime   | 19 |   0    |    Y     |  N   |       | 展会结束时间  |
|  9   | status |   int   | 10 |   0    |    Y     |  N   |       | 状态0:预备；1:开启；2:结束  |
|  10   | remark |   varchar   | 512 |   0    |    Y     |  N   |       | 备注  |
|  11   | del_flag |   int   | 10 |   0    |    Y     |  N   |   0    | 0未删除1已删除  |
|  12   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建人id  |
|  13   | create_date |   datetime   | 19 |   0    |    N     |  N   |       | 创建时间  |
|  14   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者id  |
|  15   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
####  <a id="tb_expo_invoice_info">tb_expo_invoice_info</a>

**说明：** 展商开票信息表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | org_id |   varchar   | 255 |   0    |    Y     |  N   |       | 展商ID  |
|  3   | invoice_title |   varchar   | 255 |   0    |    Y     |  N   |       | 发票抬头  |
|  4   | tax_number |   varchar   | 36 |   0    |    Y     |  N   |       | 税号  |
|  5   | org_address |   varchar   | 255 |   0    |    Y     |  N   |       | 单位地址  |
|  6   | org_phone |   varchar   | 20 |   0    |    Y     |  N   |       | 单位电话  |
|  7   | bank |   varchar   | 255 |   0    |    Y     |  N   |       | 开户行  |
|  8   | bank_account |   varchar   | 50 |   0    |    Y     |  N   |       | 银行账号  |
|  9   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  10   | creator_name |   varchar   | 50 |   0    |    Y     |  N   |       | 创建者姓名  |
|  11   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  12   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  13   | updater_name |   varchar   | 50 |   0    |    Y     |  N   |       | 更新者姓名  |
|  14   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
####  <a id="tb_expo_lab_switch">tb_expo_lab_switch</a>

**说明：** 开关管理表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | name |   varchar   | 50 |   0    |    Y     |  N   |       | 开关控制内容  |
|  3   | position |   varchar   | 255 |   0    |    Y     |  N   |       | 开关控制对应位置  |
|  4   | start_time |   datetime   | 19 |   0    |    Y     |  N   |       | 开关开启时间  |
|  5   | end_time |   datetime   | 19 |   0    |    Y     |  N   |       | 开关关闭时间  |
|  6   | status |   int   | 10 |   0    |    Y     |  N   |   0    | 开启状态：0:关闭1:开启  |
|  7   | sort |   int   | 10 |   0    |    Y     |  N   |       | 排序值  |
|  8   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  9   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者姓名  |
|  10   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  11   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  12   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者姓名  |
|  13   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  14   | del_flag |   int   | 10 |   0    |    Y     |  N   |   0    | 删除标记，0-未删除1-已删除，默认0  |
|  15   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 备注  |
|  16   | path |   varchar   | 20 |   0    |    Y     |  N   |       | 开关对应路径  |
|  17   | type |   intunsigned   | 10 |   0    |    Y     |  N   |   0    | 类型：0:用户中心1:报名登记  |
####  <a id="tb_expo_media">tb_expo_media</a>

**说明：** 媒体基础信息表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | name |   varchar   | 255 |   0    |    Y     |  N   |       | 媒体名称  |
|  3   | name_en |   varchar   | 255 |   0    |    Y     |  N   |       | 英文名称  |
|  4   | address |   varchar   | 255 |   0    |    Y     |  N   |       | 联系地址  |
|  5   | zip_code |   varchar   | 20 |   0    |    Y     |  N   |       | 邮编  |
|  6   | tel |   varchar   | 20 |   0    |    Y     |  N   |       | 公司电话  |
|  7   | card |   varchar   | 255 |   0    |    Y     |  N   |       | 身份证  |
|  8   | website |   varchar   | 255 |   0    |    Y     |  N   |       | 官方网站  |
|  9   | linkman |   varchar   | 50 |   0    |    Y     |  N   |       | 联系人  |
|  10   | mobile |   varchar   | 20 |   0    |    Y     |  N   |       | 联系人手机  |
|  11   | email |   varchar   | 255 |   0    |    Y     |  N   |       | 联系人邮箱  |
|  12   | position |   varchar   | 50 |   0    |    Y     |  N   |       | 职务  |
|  13   | source |   int   | 10 |   0    |    Y     |  N   |       | 来源(0：线上收集；1：线下收集导入)  |
|  14   | remark |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  15   | useable |   int   | 10 |   0    |    N     |  N   |   1    | 是否启用  |
|  16   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
|  17   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  18   | creator_name |   varchar   | 50 |   0    |    Y     |  N   |       | 创建者姓名  |
|  19   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  20   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  21   | updater_name |   varchar   | 50 |   0    |    Y     |  N   |       | 更新者姓名  |
|  22   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  23   | retinue_num |   int   | 10 |   0    |    Y     |  N   |       | 随行人数  |
|  24   | open_id |   varchar   | 50 |   0    |    Y     |  N   |       | 微信openid  |
|  25   | id_number |   varchar   | 50 |   0    |    Y     |  N   |       | 身份证号  |
####  <a id="tb_expo_message_board">tb_expo_message_board</a>

**说明：** 访客留言

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | id  |
|  2   | name |   varchar   | 20 |   0    |    Y     |  N   |       | 姓名  |
|  3   | company_name |   varchar   | 256 |   0    |    Y     |  N   |       | 公司名称  |
|  4   | department |   varchar   | 256 |   0    |    Y     |  N   |       | 部门  |
|  5   | duty |   varchar   | 20 |   0    |    Y     |  N   |       | 职务  |
|  6   | mobile |   varchar   | 15 |   0    |    Y     |  N   |       | 手机  |
|  7   | message_content |   varchar   | 500 |   0    |    Y     |  N   |       | 留言内容  |
|  8   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  9   | del_flag |   int   | 10 |   0    |    Y     |  N   |   0    | 0未删除1已删除  |
|  10   | remark |   varchar   | 512 |   0    |    Y     |  N   |       | 备注  |
####  <a id="tb_expo_newproduct">tb_expo_newproduct</a>

**说明：** 新品推介表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | expo_id |   varchar   | 36 |   0    |    N     |  N   |       | 所属展会ID  |
|  3   | title |   varchar   | 128 |   0    |    Y     |  N   |       | 产品名称  |
|  4   | enterprise |   varchar   | 100 |   0    |    Y     |  N   |       | 发布方/企业名称  |
|  5   | url |   varchar   | 255 |   0    |    Y     |  N   |       | 链接  |
|  6   | product_introduction |   longtext   | 2147483647 |   0    |    Y     |  N   |       | 产品简介  |
|  7   | company_introduction |   longtext   | 2147483647 |   0    |    Y     |  N   |       | 企业简介  |
|  8   | status |   int   | 10 |   0    |    Y     |  N   |   0    | 发布状态0-未发布，1-已发布  |
|  9   | sort |   int   | 10 |   0    |    Y     |  N   |       | 排序值  |
|  10   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  11   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者姓名  |
|  12   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  13   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  14   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者姓名  |
|  15   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  16   | del_flag |   int   | 10 |   0    |    Y     |  N   |   0    | 删除标记，0-未删除1-已删除，默认0  |
|  17   | remark |   varchar   | 500 |   0    |    Y     |  N   |       | 备注  |
####  <a id="tb_expo_product_introduce">tb_expo_product_introduce</a>

**说明：** 产品推介会报名表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | name |   varchar   | 255 |   0    |    N     |  N   |       | 企业名称  |
|  3   | contact |   varchar   | 36 |   0    |    N     |  N   |       | 联系人  |
|  4   | mobile |   varchar   | 36 |   0    |    N     |  N   |       | 手机号  |
|  5   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 备注  |
|  6   | useable |   int   | 10 |   0    |    N     |  N   |   1    | 是否启用  |
|  7   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
|  8   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  9   | creator_name |   varchar   | 50 |   0    |    Y     |  N   |       | 创建者姓名  |
|  10   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  11   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  12   | updater_name |   varchar   | 50 |   0    |    Y     |  N   |       | 更新者姓名  |
|  13   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  14   | open_id |   varchar   | 50 |   0    |    Y     |  N   |       | 微信openid  |
####  <a id="tb_expo_product_introduce_source">tb_expo_product_introduce_source</a>

**说明：** 产品推介会信息表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | name |   varchar   | 36 |   0    |    Y     |  N   |       | 推介会名称  |
|  3   | time |   varchar   | 36 |   0    |    Y     |  N   |       | 时间  |
|  4   | place |   varchar   | 36 |   0    |    Y     |  N   |       | 场地  |
|  5   | spread_time |   varchar   | 36 |   0    |    Y     |  N   |       | 推广时间  |
|  6   | sponsor_money |   varchar   | 36 |   0    |    Y     |  N   |       | 赞助费标准  |
|  7   | promotion_enterprise |   varchar   | 255 |   0    |    Y     |  N   |       | 推广企业权益  |
|  8   | sort |   int   | 10 |   0    |    Y     |  N   |       | 排序号  |
|  9   | useable |   int   | 10 |   0    |    N     |  N   |   1    | 是否启用  |
|  10   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
####  <a id="tb_expo_program">tb_expo_program</a>

**说明：** 项目推介表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | expo_id |   varchar   | 36 |   0    |    N     |  N   |       | 所属展会ID  |
|  3   | title |   varchar   | 128 |   0    |    Y     |  N   |       | 项目名称  |
|  4   | enterprise |   varchar   | 100 |   0    |    Y     |  N   |       | 发布方/企业名称  |
|  5   | url |   varchar   | 255 |   0    |    Y     |  N   |       | 链接  |
|  6   | program_introduction |   longtext   | 2147483647 |   0    |    Y     |  N   |       | 项目简介  |
|  7   | company_introduction |   longtext   | 2147483647 |   0    |    Y     |  N   |       | 企业简介  |
|  8   | status |   int   | 10 |   0    |    Y     |  N   |   0    | 发布状态0-未发布，1-已发布  |
|  9   | sort |   int   | 10 |   0    |    Y     |  N   |       | 排序值  |
|  10   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  11   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者姓名  |
|  12   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  13   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  14   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者姓名  |
|  15   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  16   | del_flag |   int   | 10 |   0    |    Y     |  N   |   0    | 删除标记，0-未删除1-已删除，默认0  |
|  17   | remark |   varchar   | 500 |   0    |    Y     |  N   |       | 备注  |
####  <a id="tb_expo_question_answer">tb_expo_question_answer</a>

**说明：** 百问百答表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | expo_id |   varchar   | 36 |   0    |    N     |  N   |       | 所属展会ID  |
|  3   | question |   varchar   | 128 |   0    |    Y     |  N   |       | 问题  |
|  4   | url |   varchar   | 255 |   0    |    Y     |  N   |       | 链接  |
|  5   | answer |   longtext   | 2147483647 |   0    |    Y     |  N   |       | 答复  |
|  6   | keyword |   varchar   | 128 |   0    |    Y     |  N   |       | 关键词  |
|  7   | classification |   varchar   | 50 |   0    |    Y     |  N   |       | 问答分类  |
|  8   | status |   int   | 10 |   0    |    Y     |  N   |   0    | 发布状态0-未发布，1-已发布  |
|  9   | sort |   int   | 10 |   0    |    Y     |  N   |       | 排序值  |
|  10   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  11   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者姓名  |
|  12   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  13   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  14   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者姓名  |
|  15   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  16   | del_flag |   int   | 10 |   0    |    Y     |  N   |   0    | 删除标记，0-未删除1-已删除，默认0  |
|  17   | remark |   varchar   | 500 |   0    |    Y     |  N   |       | 备注  |
####  <a id="tb_expo_reg_accompany">tb_expo_reg_accompany</a>

**说明：** 报名随行登记表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | id  |
|  2   | expo_id |   varchar   | 36 |   0    |    N     |  N   |       | 所属展会ID  |
|  3   | reg_id |   varchar   | 36 |   0    |    N     |  N   |       | 报名ID  |
|  4   | type |   tinyint   | 3 |   0    |    N     |  N   |       | 报名类型（2：展位预定，1观众报名（暂时无用），3：媒体报名,5:旅游报名）  |
|  5   | name |   varchar   | 100 |   0    |    Y     |  N   |       | 姓名  |
|  6   | tel |   varchar   | 20 |   0    |    Y     |  N   |       | 联系人电话  |
|  7   | card_type |   varchar   | 20 |   0    |    Y     |  N   |       | 证件类型(1、身份证，2、港澳台通行证，3、护照)  |
|  8   | card |   varchar   | 64 |   0    |    Y     |  N   |       | 身份证  |
|  9   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建人id  |
|  10   | source_area |   varchar   | 255 |   0    |    Y     |  N   |       | 来源地区(国家名称)  |
|  11   | province |   varchar   | 20 |   0    |    Y     |  N   |       | 省  |
|  12   | city |   varchar   | 20 |   0    |    Y     |  N   |       | 市  |
|  13   | country |   varchar   | 20 |   0    |    Y     |  N   |       | 县  |
|  14   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  15   | del_flag |   int   | 10 |   0    |    Y     |  N   |   0    | 0未删除1已删除  |
|  16   | update_date |   datetime   | 19 |   0    |    Y     |  N   |   CURRENT_TIMESTAMP    | 更新时间  |
|  17   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者id  |
|  18   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 备注  |
|  19   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者姓名  |
|  20   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者姓名  |
####  <a id="tb_expo_reg_accompany_copy1">tb_expo_reg_accompany_copy1</a>

**说明：** 报名随行登记表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | id  |
|  2   | expo_id |   varchar   | 36 |   0    |    N     |  N   |       | 所属展会ID  |
|  3   | reg_id |   varchar   | 36 |   0    |    N     |  N   |       | 报名ID  |
|  4   | type |   tinyint   | 3 |   0    |    N     |  N   |       | 报名类型（2：展位预定，1观众报名（暂时无用），3：媒体报名,5:旅游报名）  |
|  5   | name |   varchar   | 100 |   0    |    Y     |  N   |       | 姓名  |
|  6   | tel |   varchar   | 20 |   0    |    Y     |  N   |       | 联系人电话  |
|  7   | card_type |   varchar   | 20 |   0    |    Y     |  N   |       | 证件类型(1、身份证，2、港澳台通行证，3、护照)  |
|  8   | card |   varchar   | 64 |   0    |    Y     |  N   |       | 身份证  |
|  9   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建人id  |
|  10   | source_area |   varchar   | 255 |   0    |    Y     |  N   |       | 来源地区(国家名称)  |
|  11   | province |   varchar   | 20 |   0    |    Y     |  N   |       | 省  |
|  12   | city |   varchar   | 20 |   0    |    Y     |  N   |       | 市  |
|  13   | country |   varchar   | 20 |   0    |    Y     |  N   |       | 县  |
|  14   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  15   | del_flag |   int   | 10 |   0    |    Y     |  N   |   0    | 0未删除1已删除  |
####  <a id="tb_expo_reg_audience">tb_expo_reg_audience</a>

**说明：** 观众报名信息

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | id  |
|  2   | expo_id |   varchar   | 36 |   0    |    Y     |  N   |       | 所属展会ID  |
|  3   | audience_name |   varchar   | 100 |   0    |    Y     |  N   |       | 观众姓名  |
|  4   | company_type |   varchar   | 50 |   0    |    Y     |  N   |       | 单位类型  |
|  5   | company_name |   varchar   | 100 |   0    |    Y     |  N   |       | 单位名称  |
|  6   | card_type |   varchar   | 20 |   0    |    Y     |  N   |       | 证件类型(1、身份证，2、港澳台通行证，3、护照)  |
|  7   | social_credit_code |   varchar   | 100 |   0    |    Y     |  N   |       | 统一社会信用代码  |
|  8   | title |   varchar   | 50 |   0    |    Y     |  N   |       | 观众职务  |
|  9   | category |   varchar   | 20 |   0    |    Y     |  N   |       | 观众类别  |
|  10   | tel |   varchar   | 20 |   0    |    Y     |  N   |       | 联系人电话  |
|  11   | email |   varchar   | 50 |   0    |    Y     |  N   |       | 邮箱  |
|  12   | focus_areas |   varchar   | 200 |   0    |    Y     |  N   |       | 关注领域  |
|  13   | focus_forums |   varchar   | 500 |   0    |    Y     |  N   |       | 关注论坛  |
|  14   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建人id  |
|  15   | source_area |   varchar   | 255 |   0    |    Y     |  N   |       | 来源地区(国家名称)  |
|  16   | province |   varchar   | 20 |   0    |    Y     |  N   |       | 省  |
|  17   | city |   varchar   | 20 |   0    |    Y     |  N   |       | 市  |
|  18   | country |   varchar   | 20 |   0    |    Y     |  N   |       | 县  |
|  19   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  20   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者id  |
|  21   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  22   | status |   int   | 10 |   0    |    Y     |  N   |   0    | 审核状态:0-待审核,1-通过,2-未通过  |
|  23   | del_flag |   int   | 10 |   0    |    Y     |  N   |   0    | 0未删除1已删除  |
|  24   | remark |   varchar   | 512 |   0    |    Y     |  N   |       | 备注  |
|  25   | leaving_message |   varchar   | 500 |   0    |    Y     |  N   |       | 留言  |
|  26   | other_focus_area |   varchar   | 50 |   0    |    Y     |  N   |       | 关注领域-其他  |
|  27   | audience_id |   varchar   | 36 |   0    |    Y     |  N   |       | 观众基础信息id  |
|  28   | proof_num |   varchar   | 10 |   0    |    Y     |  N   |       | 凭码  |
|  29   | is_continue |   varchar   | 1 |   0    |    Y     |  N   |       | 是否愿意参加下一届(0、否，1、是)  |
|  30   | job |   varchar   | 36 |   0    |    Y     |  N   |       | 职业(0、学生，1、退休人员，2、个人，3在职)  |
|  31   | learn_channel |   varchar   | 255 |   0    |    Y     |  N   |       | 获知渠道（多选）  |
####  <a id="tb_expo_reg_audience_channel">tb_expo_reg_audience_channel</a>

**说明：** 观众报名信息-获知渠道关系表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | id  |
|  2   | expo_id |   varchar   | 36 |   0    |    Y     |  N   |       | 所属展会ID  |
|  3   | reg_id |   varchar   | 36 |   0    |    Y     |  N   |       | 观众报名ID  |
|  4   | learn_channel |   varchar   | 32 |   0    |    Y     |  N   |       | 获知渠道编码（对应数据字典468）  |
####  <a id="tb_expo_reg_dealer">tb_expo_reg_dealer</a>

**说明：** 经销商报名管理表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | expo_session_id |   varchar   | 36 |   0    |    Y     |  N   |       | 届期ID  |
|  3   | name |   varchar   | 255 |   0    |    Y     |  N   |       | 姓名  |
|  4   | mobile |   varchar   | 20 |   0    |    Y     |  N   |       | 手机号  |
|  5   | id_card |   varchar   | 20 |   0    |    Y     |  N   |       | 证件号  |
|  6   | remark |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  7   | status |   int   | 10 |   0    |    N     |  N   |   0    | 审核状态:0-待审核,1-通过,2-未通过  |
|  8   | reason |   varchar   | 255 |   0    |    Y     |  N   |       | 未通过原因  |
|  9   | num_times |   int   | 10 |   0    |    Y     |  N   |   0    | 报名次数（超哥3次不让继续报名）  |
|  10   | send_status |   int   | 10 |   0    |    Y     |  N   |   0    | 短信发送状态（0：未发送，1：已发送）  |
|  11   | code |   varchar   | 45 |   0    |    Y     |  N   |       | 验证码  |
|  12   | source |   int   | 10 |   0    |    Y     |  N   |       | 来源(0：线上收集；1：线下收集导入)  |
|  13   | useable |   int   | 10 |   0    |    N     |  N   |   1    | 是否启用  |
|  14   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
|  15   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  16   | creator_name |   varchar   | 50 |   0    |    Y     |  N   |       | 创建者姓名  |
|  17   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  18   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  19   | updater_name |   varchar   | 50 |   0    |    Y     |  N   |       | 更新者姓名  |
|  20   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  21   | type |   int   | 10 |   0    |    Y     |  N   |       | 类型:0:产品代理1:产品推广2:生产厂家  |
|  22   | dealer_id |   varchar   | 36 |   0    |    Y     |  N   |       | 经销商基本信息id  |
|  23   | send_date |   datetime   | 19 |   0    |    Y     |  N   |       | 短信发送时间  |
####  <a id="tb_expo_reg_employee_card">tb_expo_reg_employee_card</a>

**说明：** 工作证申办表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | id  |
|  2   | expo_id |   varchar   | 36 |   0    |    N     |  N   |       | 所属展会id  |
|  3   | expo_parent_id |   varchar   | 36 |   0    |    Y     |  N   |       | 展馆id  |
|  4   | area_id |   varchar   | 36 |   0    |    Y     |  N   |       | 展区id  |
|  5   | name |   varchar   | 100 |   0    |    Y     |  N   |       | 工作人员姓名  |
|  6   | card |   varchar   | 64 |   0    |    Y     |  N   |       | 证件号码  |
|  7   | card_type |   varchar   | 20 |   0    |    Y     |  N   |       | 证件类型(1、身份证，2、港澳台通行证，3、护照)  |
|  8   | mobile |   varchar   | 20 |   0    |    Y     |  N   |       | 联系人电话  |
|  9   | unit |   varchar   | 255 |   0    |    Y     |  N   |       | 提供单位  |
|  10   | duty |   varchar   | 50 |   0    |    Y     |  N   |       | 职责  |
|  11   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 备注  |
|  12   | del_flag |   int   | 10 |   0    |    Y     |  N   |   0    | 删除标记，0-未删除1-已删除，默认0  |
|  13   | status |   int   | 10 |   0    |    Y     |  N   |   0    | 审核状态:0-待审核,1-通过,2-未通过  |
|  14   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者id  |
|  15   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者姓名  |
|  16   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  17   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者id  |
|  18   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者姓名  |
|  19   | update_date |   datetime   | 19 |   0    |    N     |  N   |   CURRENT_TIMESTAMP    | 更新时间  |
####  <a id="tb_expo_reg_exhibitor">tb_expo_reg_exhibitor</a>

**说明：** 参展商登记信息

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | id  |
|  2   | expo_id |   varchar   | 36 |   0    |    Y     |  N   |       | 所属展会ID  |
|  3   | company_name |   varchar   | 255 |   0    |    Y     |  N   |       | 参展企业名称  |
|  4   | company_en_name |   varchar   | 255 |   0    |    Y     |  N   |       | 参展企业英文名称  |
|  5   | province |   varchar   | 20 |   0    |    Y     |  N   |       | 省  |
|  6   | city |   varchar   | 20 |   0    |    Y     |  N   |       | 市  |
|  7   | country |   varchar   | 20 |   0    |    Y     |  N   |       | 县  |
|  8   | address |   varchar   | 200 |   0    |    Y     |  N   |       | 联系地址  |
|  9   | postcode |   varchar   | 10 |   0    |    Y     |  N   |       | 邮编  |
|  10   | group_name |   varchar   | 100 |   0    |    Y     |  N   |       | 若属于集团子公司，请注明集团母公司名称  |
|  11   | contact_name |   varchar   | 100 |   0    |    Y     |  N   |       | 展会联系人  |
|  12   | contact_dept |   varchar   | 100 |   0    |    Y     |  N   |       | 展会联系人部门  |
|  13   | contact_title |   varchar   | 50 |   0    |    Y     |  N   |       | 展会联系人职务  |
|  14   | contact_tel |   varchar   | 20 |   0    |    Y     |  N   |       | 展会联系人电话  |
|  15   | contact_fax |   varchar   | 20 |   0    |    Y     |  N   |       | 展会联系人传真  |
|  16   | contact_qq |   varchar   | 20 |   0    |    Y     |  N   |       | 展会联系人QQ  |
|  17   | contact_mobile |   varchar   | 20 |   0    |    Y     |  N   |       | 展会联系人手机  |
|  18   | contact_email |   varchar   | 50 |   0    |    Y     |  N   |       | 展会联系人邮箱  |
|  19   | contact_weixin |   varchar   | 50 |   0    |    Y     |  N   |       | 展会联系人微信号  |
|  20   | pos_bare_1 |   int   | 10 |   0    |    Y     |  N   |   0    | 光地特装一类光地650元/平米  |
|  21   | pos_bare_2 |   int   | 10 |   0    |    Y     |  N   |   0    | 光地特装二类光地550元/平米  |
|  22   | pos_std_1 |   varchar   | 100 |   0    |    Y     |  N   |   0    | 标准展位中文楣板  |
|  23   | pos_std_2 |   varchar   | 100 |   0    |    Y     |  N   |   0    | 标准展位英文楣板  |
|  24   | pos_special |   int   | 10 |   0    |    Y     |  N   |   0    | 1-光地特装，2-标准展位3-线上展位  |
|  25   | pos_corner |   int   | 10 |   0    |    Y     |  N   |       | 如有意预订转角位，请勾选此项。标准展位转角位置（两面开展位）加收原价格的20%，0-不选，1-选中  |
|  26   | pos_remark |   varchar   | 500 |   0    |    Y     |  N   |       | 展位申请备注  |
|  27   | invoice_title |   varchar   | 200 |   0    |    Y     |  N   |       | 发票抬头  |
|  28   | tax_number |   varchar   | 50 |   0    |    Y     |  N   |       | 税号  |
|  29   | invoice_address |   varchar   | 200 |   0    |    Y     |  N   |       | 开票地址  |
|  30   | invoice_tel |   varchar   | 20 |   0    |    Y     |  N   |       | 开票电话号码  |
|  31   | bank_name |   varchar   | 50 |   0    |    Y     |  N   |       | 开户行  |
|  32   | bank_account |   varchar   | 200 |   0    |    Y     |  N   |       | 银行账号  |
|  33   | is_continue |   varchar   | 1 |   0    |    Y     |  N   |       | 是否愿意参加下一届(0、否，1、是)  |
|  34   | is_offline_reg |   varchar   | 1 |   0    |    Y     |  N   |       | 是否已线下报名（0、否，1、是）  |
|  35   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建人id  |
|  36   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  37   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者id  |
|  38   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  39   | status |   int   | 10 |   0    |    N     |  N   |   0    | 审核状态:0-待审核,1-通过,2-未通过  |
|  40   | del_flag |   int   | 10 |   0    |    Y     |  N   |   0    | 0未删除1已删除  |
|  41   | remark |   varchar   | 512 |   0    |    Y     |  N   |       | 备注  |
|  42   | legal_represent |   varchar   | 100 |   0    |    Y     |  N   |       | 法人代表  |
|  43   | social_credit_code |   varchar   | 100 |   0    |    Y     |  N   |       | 统一社会信用代码  |
|  44   | industry |   varchar   | 255 |   0    |    Y     |  N   |       | 所属行业  |
|  45   | official_website |   varchar   | 100 |   0    |    Y     |  N   |       | 企业官网  |
|  46   | company_introdct |   varchar   | 5000 |   0    |    Y     |  N   |       | 公司介绍  |
|  47   | product_introdct |   varchar   | 5000 |   0    |    Y     |  N   |       | 产品介绍  |
|  48   | exhibitor_id |   varchar   | 36 |   0    |    Y     |  N   |       | 展商基础信息id  |
|  49   | corporate_logo_image_url |   varchar   | 512 |   0    |    Y     |  N   |       | 企业logourl  |
|  50   | corporate_style_image_url |   varchar   | 512 |   0    |    Y     |  N   |       | 企业风采url  |
|  51   | company_introdct_en |   varchar   | 1000 |   0    |    Y     |  N   |       | 公司介绍-英文  |
|  52   | payment_status |   int   | 10 |   0    |    Y     |  N   |   0    | 缴费状态0-未缴费，1-已缴费  |
|  53   | pwd |   varchar   | 64 |   0    |    Y     |  N   |       | 药众采密码  |
|  54   | user_id |   bigint   | 19 |   0    |    Y     |  N   |       | 用户id  |
|  55   | source_platform |   varchar   | 255 |   0    |    Y     |  N   |       | 来源平台  |
|  56   | is_invite |   int   | 10 |   0    |    Y     |  N   |   0    | 是否邀请（0：否，1是）  |
|  57   | is_hotel_reservation |   int   | 10 |   0    |    N     |  N   |   0    | 是否需要主办方代订酒店0-否1-是  |
|  58   | hotel_start_time |   varchar   | 45 |   0    |    Y     |  N   |       | 入住时间  |
|  59   | hotel_end_time |   varchar   | 45 |   0    |    Y     |  N   |       | 离店时间  |
|  60   | room_num |   int   | 10 |   0    |    N     |  N   |   0    | 房间数  |
|  61   | is_referrals |   int   | 10 |   0    |    Y     |  N   |   0    | 是否有产品推介需求  |
|  62   | referrals_codes |   varchar   | 32 |   0    |    Y     |  N   |       | 推介会场(数据字典470)  |
####  <a id="tb_expo_reg_exhibitor_channel">tb_expo_reg_exhibitor_channel</a>

**说明：** 展商报名信息-获知渠道关系表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 32 |   0    |    N     |  Y   |       | id  |
|  2   | expo_id |   varchar   | 32 |   0    |    Y     |  N   |       | 所属展会ID  |
|  3   | reg_id |   varchar   | 32 |   0    |    Y     |  N   |       | 观众报名ID  |
|  4   | learn_channel |   varchar   | 32 |   0    |    Y     |  N   |       | 获知渠道编码（对应数据字典468）  |
|  5   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
####  <a id="tb_expo_reg_exhibitor_next">tb_expo_reg_exhibitor_next</a>

**说明：** 参展商下一届登记信息

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | id  |
|  2   | company_name |   varchar   | 255 |   0    |    Y     |  N   |       | 参展企业名称  |
|  3   | contact_name |   varchar   | 100 |   0    |    Y     |  N   |       | 展会联系人  |
|  4   | contact_mobile |   varchar   | 20 |   0    |    Y     |  N   |       | 展会联系人手机  |
|  5   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建人id  |
|  6   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  7   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者id  |
|  8   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  9   | status |   int   | 10 |   0    |    N     |  N   |   0    | 审核状态:0-待审核,1-通过,2-未通过  |
|  10   | del_flag |   int   | 10 |   0    |    Y     |  N   |   0    | 0未删除1已删除  |
|  11   | remark |   varchar   | 512 |   0    |    Y     |  N   |       | 备注  |
####  <a id="tb_expo_reg_exhibitor_prod">tb_expo_reg_exhibitor_prod</a>

**说明：** 参展商登记商品信息表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | expo_exhibitor_id |   varchar   | 36 |   0    |    N     |  N   |       | 参展商信息ID  |
|  3   | prod_no |   varchar   | 36 |   0    |    N     |  N   |       | 展品编号(唯一)  |
|  4   | prod_name |   varchar   | 100 |   0    |    N     |  N   |       | 商品名称  |
|  5   | prod_desc |   varchar   | 1024 |   0    |    Y     |  N   |       | 商品描述  |
|  6   | prod_image_url |   varchar   | 512 |   0    |    Y     |  N   |       |   |
|  7   | status |   int   | 10 |   0    |    Y     |  N   |   0    | 审核状态:0-待审核,1-通过,2-未通过  |
|  8   | publish_status |   int   | 10 |   0    |    Y     |  N   |   0    | 发布状态:0-未发布,1-已发布  |
|  9   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  10   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者姓名  |
|  11   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  12   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  13   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者姓名  |
|  14   | update_date |   datetime   | 19 |   0    |    Y     |  N   |   CURRENT_TIMESTAMP    | 更新时间  |
|  15   | del_flag |   int   | 10 |   0    |    Y     |  N   |       |   |
|  16   | manufacture |   varchar   | 50 |   0    |    Y     |  N   |       | 厂商  |
|  17   | sort |   int   | 10 |   0    |    Y     |  N   |       | 顺序  |
|  18   | reason |   varchar   | 255 |   0    |    Y     |  N   |       | 原因  |
####  <a id="tb_expo_reg_exhibitor_purpose">tb_expo_reg_exhibitor_purpose</a>

**说明：** 展商报名信息-参与目的关系表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | id  |
|  2   | expo_id |   varchar   | 36 |   0    |    Y     |  N   |       | 所属展会ID  |
|  3   | reg_id |   varchar   | 36 |   0    |    Y     |  N   |       | 展会报名ID  |
|  4   | purpose |   varchar   | 32 |   0    |    Y     |  N   |       | 参会目的（对应数据字典469）  |
|  5   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
####  <a id="tb_expo_reg_media">tb_expo_reg_media</a>

**说明：** 媒体登记信息

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | id  |
|  2   | expo_id |   varchar   | 36 |   0    |    Y     |  N   |       | 所属展会ID  |
|  3   | media_name |   varchar   | 100 |   0    |    Y     |  N   |       | 媒体名称  |
|  4   | address |   varchar   | 200 |   0    |    Y     |  N   |       | 联系地址  |
|  5   | postcode |   varchar   | 10 |   0    |    Y     |  N   |       | 邮编  |
|  6   | contact_name |   varchar   | 100 |   0    |    Y     |  N   |       | 联系人  |
|  7   | contact_title |   varchar   | 50 |   0    |    Y     |  N   |       | 联系人职务  |
|  8   | contact_tel |   varchar   | 20 |   0    |    Y     |  N   |       | 公司电话  |
|  9   | contact_mobile |   varchar   | 20 |   0    |    Y     |  N   |       | 联系人手机  |
|  10   | contact_email |   varchar   | 50 |   0    |    Y     |  N   |       | 联系人邮箱  |
|  11   | contact_website |   varchar   | 100 |   0    |    Y     |  N   |       | 联系人网站  |
|  12   | participant_name |   varchar   | 100 |   0    |    Y     |  N   |       | 参会代表姓名  |
|  13   | participant_title |   varchar   | 50 |   0    |    Y     |  N   |       | 参会代表职务  |
|  14   | participant_tel |   varchar   | 20 |   0    |    Y     |  N   |       | 参会代表电话  |
|  15   | focus_areas |   varchar   | 200 |   0    |    Y     |  N   |       | 关注领域  |
|  16   | focus_forums |   varchar   | 500 |   0    |    Y     |  N   |       | 关注论坛  |
|  17   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建人id  |
|  18   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  19   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者id  |
|  20   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  21   | status |   int   | 10 |   0    |    N     |  N   |   0    | 审核状态:0-待审核,1-通过,2-未通过  |
|  22   | del_flag |   int   | 10 |   0    |    Y     |  N   |   0    | 0未删除1已删除  |
|  23   | remark |   varchar   | 512 |   0    |    Y     |  N   |       | 备注  |
|  24   | interview_requirements |   varchar   | 500 |   0    |    Y     |  N   |       | 采访需求  |
|  25   | id_number |   varchar   | 30 |   0    |    Y     |  N   |       | 身份证号  |
|  26   | electronic_photos_file_name |   varchar   | 100 |   0    |    Y     |  N   |       | 电子照片文件名称  |
|  27   | electronic_photos_file_id |   varchar   | 200 |   0    |    Y     |  N   |       | 电子照片文件id  |
|  28   | electronic_photos_file_size |   varchar   | 50 |   0    |    Y     |  N   |       | 电子照片文件大小  |
|  29   | retinue_num |   int   | 10 |   0    |    Y     |  N   |   0    | 随行人数  |
|  30   | other_focus_area |   varchar   | 50 |   0    |    Y     |  N   |       | 关注领域-其他  |
|  31   | media_id |   varchar   | 36 |   0    |    Y     |  N   |       | 媒体基础信息id  |
|  32   | is_continue |   varchar   | 1 |   0    |    Y     |  N   |       | 是否愿意参加下一届(0、否，1、是)  |
####  <a id="tb_expo_reg_product_introduce">tb_expo_reg_product_introduce</a>

**说明：** 产品推介会信息表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | expo_id |   varchar   | 36 |   0    |    Y     |  N   |       | 所属展会ID  |
|  3   | name |   varchar   | 255 |   0    |    N     |  N   |       | 企业名称  |
|  4   | contact |   varchar   | 36 |   0    |    N     |  N   |       | 联系人  |
|  5   | mobile |   varchar   | 36 |   0    |    N     |  N   |       | 手机号  |
|  6   | status |   int   | 10 |   0    |    N     |  N   |   0    | 审核状态:0-未审核、1-审核通过、2-审核不通过，默认0  |
|  7   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者ID  |
|  8   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者  |
|  9   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  10   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者ID  |
|  11   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者  |
|  12   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  13   | product_introduce_id |   varchar   | 36 |   0    |    Y     |  N   |       | 产品推介会基础信息id  |
|  14   | audit_date |   datetime   | 19 |   0    |    Y     |  N   |       | 审核时间  |
####  <a id="tb_expo_reg_product_introduce_mapping">tb_expo_reg_product_introduce_mapping</a>

**说明：** 产品推介会报名关系表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | reg_id |   varchar   | 36 |   0    |    N     |  N   |       | 产品推介会报名表主键ID  |
|  3   | prod_introduce_id |   varchar   | 36 |   0    |    N     |  N   |       | 产品推介会信息表主键ID  |
|  4   | expo_id |   varchar   | 36 |   0    |    Y     |  N   |       | 所属展会ID  |
####  <a id="tb_expo_reg_travel">tb_expo_reg_travel</a>

**说明：** 旅游报名登记表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | id  |
|  2   | expo_id |   varchar   | 36 |   0    |    N     |  N   |       | 所属展会ID  |
|  3   | reg_id |   varchar   | 36 |   0    |    N     |  N   |       | 报名ID  |
|  4   | name |   varchar   | 50 |   0    |    Y     |  N   |       | 姓名  |
|  5   | certificate_img_uri |   varchar   | 512 |   0    |    Y     |  N   |       | 资格证图片  |
|  6   | tel |   varchar   | 20 |   0    |    Y     |  N   |       | 联系电话  |
|  7   | card |   varchar   | 64 |   0    |    Y     |  N   |       | 身份证  |
|  8   | hspt_name |   varchar   | 255 |   0    |    Y     |  N   |       | 所属医院  |
|  9   | dept_name |   varchar   | 20 |   0    |    Y     |  N   |       | 科室  |
|  10   | travle_time |   datetime   | 19 |   0    |    Y     |  N   |       | 旅游时间  |
|  11   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  12   | del_flag |   int   | 10 |   0    |    Y     |  N   |   0    | 0未删除1已删除  |
|  13   | remark |   varchar   | 100 |   0    |    Y     |  N   |       | 备注  |
####  <a id="tb_expo_source">tb_expo_source</a>

**说明：** 资源管理

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 32 |   0    |    N     |  Y   |       | 主键id  |
|  2   | name |   varchar   | 255 |   0    |    Y     |  N   |       | 资源名称  |
|  3   | size |   varchar   | 15 |   0    |    Y     |  N   |       | 文件大小  |
|  4   | url |   varchar   | 255 |   0    |    Y     |  N   |       | 引用地址  |
|  5   | type |   int   | 10 |   0    |    Y     |  N   |       | 类型，0:下载中心1:其他  |
|  6   | sort |   int   | 10 |   0    |    Y     |  N   |       | 排序  |
|  7   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  8   | creator_name |   varchar   | 64 |   0    |    Y     |  N   |       | 创建者姓名  |
|  9   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  10   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  11   | updater_name |   varchar   | 64 |   0    |    Y     |  N   |       | 更新者姓名  |
|  12   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  13   | del_flag |   int   | 10 |   0    |    Y     |  N   |   0    | 删除标记，0-未删除1-已删除，默认0  |
|  14   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 备注  |
####  <a id="tb_expo_tag">tb_expo_tag</a>

**说明：** 标记

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | id  |
|  2   | name |   varchar   | 200 |   0    |    N     |  N   |       | 标记名称  |
|  3   | tag_type |   int   | 10 |   0    |    N     |  N   |   1    | 标记类型:1-展商标记  |
|  4   | css_class |   varchar   | 255 |   0    |    N     |  N   |       | 样式属性  |
|  5   | tag_sort |   int   | 10 |   0    |    N     |  N   |   1    | 排序  |
|  6   | remark |   varchar   | 500 |   0    |    N     |  N   |       | 备注  |
|  7   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
|  8   | useable |   int   | 10 |   0    |    N     |  N   |   1    | 是否启用  |
|  9   | creator_id |   varchar   | 36 |   0    |    N     |  N   |       | 创建者  |
|  10   | creator_name |   varchar   | 255 |   0    |    N     |  N   |       | 创建者姓名  |
|  11   | create_date |   datetime   | 19 |   0    |    N     |  N   |   CURRENT_TIMESTAMP    | 创建时间  |
|  12   | updater_id |   varchar   | 36 |   0    |    N     |  N   |       | 更新者  |
|  13   | updater_name |   varchar   | 255 |   0    |    N     |  N   |       | 更新者姓名  |
|  14   | update_date |   datetime   | 19 |   0    |    N     |  N   |   CURRENT_TIMESTAMP    | 更新时间  |
####  <a id="tb_expo_tag_relation">tb_expo_tag_relation</a>

**说明：** 标记关联表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | id  |
|  2   | relation_type |   int   | 10 |   0    |    N     |  N   |   1    | 关联类型:1-展商  |
|  3   | relation_id |   varchar   | 50 |   0    |    N     |  N   |       | 关联id  |
|  4   | tag_id |   varchar   | 50 |   0    |    N     |  N   |       | 标记id  |
|  5   | creator_id |   varchar   | 36 |   0    |    N     |  N   |       | 创建者  |
|  6   | creator_name |   varchar   | 255 |   0    |    N     |  N   |       | 创建者姓名  |
|  7   | create_date |   datetime   | 19 |   0    |    N     |  N   |   CURRENT_TIMESTAMP    | 创建时间  |
####  <a id="tb_expo_ticket">tb_expo_ticket</a>

**说明：** 展会入场二维码表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | join_id |   varchar   | 36 |   0    |    N     |  N   |       | 参会人id  |
|  3   | ticket_id |   varchar   | 36 |   0    |    N     |  N   |       | 入场二维码id  |
|  4   | is_sync |   int   | 10 |   0    |    Y     |  N   |       | 是否同步0否，1是  |
|  5   | is_used |   int   | 10 |   0    |    Y     |  N   |       | 是否已使用0否，1是  |
|  6   | sort |   int   | 10 |   0    |    N     |  N   |       | 序号  |
|  7   | create_date |   datetime   | 19 |   0    |    N     |  N   |       | 创建时间  |
####  <a id="tb_expo_ticket2_backups">tb_expo_ticket2_backups</a>

**说明：** 展会入场二维码表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | join_id |   varchar   | 36 |   0    |    N     |  N   |       | 参会人id  |
|  3   | ticket_id |   varchar   | 36 |   0    |    N     |  N   |       | 入场二维码id  |
|  4   | is_sync |   int   | 10 |   0    |    Y     |  N   |       | 是否同步0否，1是  |
|  5   | is_used |   int   | 10 |   0    |    Y     |  N   |       | 是否已使用0否，1是  |
|  6   | sort |   int   | 10 |   0    |    N     |  N   |       | 序号  |
|  7   | create_date |   datetime   | 19 |   0    |    N     |  N   |       | 创建时间  |
####  <a id="tb_expo_transportation_guide">tb_expo_transportation_guide</a>

**说明：** 交通指南

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | landmark_name |   varchar   | 100 |   0    |    N     |  N   |       | 地标名称  |
|  3   | sort |   int   | 10 |   0    |    Y     |  N   |   0    | 排序值  |
|  4   | app_map_path |   varchar   | 512 |   0    |    N     |  N   |       | 小程序地图链接  |
|  5   | pc_map_path |   varchar   | 512 |   0    |    N     |  N   |       | pc地图链接  |
|  6   | app_lon_lat |   varchar   | 512 |   0    |    N     |  N   |       | 小程序经纬度  |
|  7   | travel_info |   text   | 65535 |   0    |    Y     |  N   |       | 出行信息  |
|  8   | remark |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  9   | status |   int   | 10 |   0    |    N     |  N   |   0    | 发布状态:0-未发布,1-已发布  |
|  10   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
|  11   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  12   | creator_name |   varchar   | 50 |   0    |    Y     |  N   |       | 创建者姓名  |
|  13   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  14   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  15   | updater_name |   varchar   | 50 |   0    |    Y     |  N   |       | 更新者姓名  |
|  16   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
####  <a id="tb_finance_account_det">tb_finance_account_det</a>

**说明：** 财务账款明细表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | pay_org_id |   varchar   | 36 |   0    |    N     |  N   |       | 付款方机构id  |
|  3   | pay_org_name |   varchar   | 100 |   0    |    N     |  N   |       | 付款方机构名称  |
|  4   | income_org_id |   varchar   | 36 |   0    |    N     |  N   |       | 收款方机构id  |
|  5   | income_org_name |   varchar   | 100 |   0    |    N     |  N   |       | 收款方机构名称  |
|  6   | biz_doc_no |   varchar   | 36 |   0    |    Y     |  N   |       | 业务单据编号  |
|  7   | amount |   decimal   | 20 |   4    |    Y     |  N   |   0.0000    | 金额  |
|  8   | biz_doc_type |   int   | 10 |   0    |    N     |  N   |       | 单据类型(1采购订单、2退货单、3退款单、4拒收单、5缺货单、6线上支付单、7线下结算登记单)  |
|  9   | pay_mode |   int   | 10 |   0    |    N     |  N   |       | 支付方式0:线上支付1:线下支付  |
|  10   | create_date |   datetime   | 19 |   0    |    N     |  N   |       | 创建时间  |
####  <a id="tb_finance_account_main">tb_finance_account_main</a>

**说明：** 财务账款主表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | pay_org_id |   varchar   | 36 |   0    |    N     |  N   |       | 付款方机构id  |
|  3   | pay_org_name |   varchar   | 100 |   0    |    N     |  N   |       | 付款方机构名称  |
|  4   | income_org_id |   varchar   | 36 |   0    |    N     |  N   |       | 收款方机构id  |
|  5   | income_org_name |   varchar   | 100 |   0    |    N     |  N   |       | 收款方机构名称  |
|  6   | online_amount |   decimal   | 20 |   4    |    Y     |  N   |   0.0000    | 线上总金额  |
|  7   | offline_amount |   decimal   | 20 |   4    |    Y     |  N   |   0.0000    | 线下总金额  |
####  <a id="tb_invoice_title">tb_invoice_title</a>

**说明：** 增票资质表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | org_id |   varchar   | 20 |   0    |    N     |  N   |       | 机构id  |
|  3   | account_name |   varchar   | 255 |   0    |    N     |  N   |       | 公司名称  |
|  4   | taxpayer_identification_number |   varchar   | 100 |   0    |    N     |  N   |       | 纳税人识别号  |
|  5   | register_address |   varchar   | 255 |   0    |    N     |  N   |       | 注册地址  |
|  6   | phone |   varchar   | 36 |   0    |    N     |  N   |       | 联系电话  |
|  7   | account_bank |   varchar   | 100 |   0    |    N     |  N   |       | 开户行名称  |
|  8   | account_no |   varchar   | 100 |   0    |    N     |  N   |       | 基本开户账号  |
|  9   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者id  |
|  10   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者  |
|  11   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  12   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者id  |
|  13   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者  |
|  14   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  15   | del_flag |   int   | 10 |   0    |    Y     |  N   |   0    | 删除标记(0-未删除,1-已删除,默认0)  |
|  16   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 备注信息  |
|  17   | invoice_status |   int   | 10 |   0    |    Y     |  N   |   0    | 是否默认发票(0-否,1-是)  |
####  <a id="tb_job_qrtz_blob_triggers">tb_job_qrtz_blob_triggers</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | SCHED_NAME |   varchar   | 120 |   0    |    N     |  Y   |       |   |
|  2   | TRIGGER_NAME |   varchar   | 200 |   0    |    N     |  Y   |       |   |
|  3   | TRIGGER_GROUP |   varchar   | 200 |   0    |    N     |  Y   |       |   |
|  4   | BLOB_DATA |   blob   | 65535 |   0    |    Y     |  N   |       |   |
####  <a id="tb_job_qrtz_calendars">tb_job_qrtz_calendars</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | SCHED_NAME |   varchar   | 120 |   0    |    N     |  Y   |       |   |
|  2   | CALENDAR_NAME |   varchar   | 200 |   0    |    N     |  Y   |       |   |
|  3   | CALENDAR |   blob   | 65535 |   0    |    N     |  N   |       |   |
####  <a id="tb_job_qrtz_cron_triggers">tb_job_qrtz_cron_triggers</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | SCHED_NAME |   varchar   | 120 |   0    |    N     |  Y   |       |   |
|  2   | TRIGGER_NAME |   varchar   | 200 |   0    |    N     |  Y   |       |   |
|  3   | TRIGGER_GROUP |   varchar   | 200 |   0    |    N     |  Y   |       |   |
|  4   | CRON_EXPRESSION |   varchar   | 200 |   0    |    N     |  N   |       |   |
|  5   | TIME_ZONE_ID |   varchar   | 80 |   0    |    Y     |  N   |       |   |
####  <a id="tb_job_qrtz_fired_triggers">tb_job_qrtz_fired_triggers</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | SCHED_NAME |   varchar   | 120 |   0    |    N     |  Y   |       |   |
|  2   | ENTRY_ID |   varchar   | 95 |   0    |    N     |  Y   |       |   |
|  3   | TRIGGER_NAME |   varchar   | 200 |   0    |    N     |  N   |       |   |
|  4   | TRIGGER_GROUP |   varchar   | 200 |   0    |    N     |  N   |       |   |
|  5   | INSTANCE_NAME |   varchar   | 200 |   0    |    N     |  N   |       |   |
|  6   | FIRED_TIME |   bigint   | 19 |   0    |    N     |  N   |       |   |
|  7   | SCHED_TIME |   bigint   | 19 |   0    |    N     |  N   |       |   |
|  8   | PRIORITY |   int   | 10 |   0    |    N     |  N   |       |   |
|  9   | STATE |   varchar   | 16 |   0    |    N     |  N   |       |   |
|  10   | JOB_NAME |   varchar   | 200 |   0    |    Y     |  N   |       |   |
|  11   | JOB_GROUP |   varchar   | 200 |   0    |    Y     |  N   |       |   |
|  12   | IS_NONCONCURRENT |   varchar   | 1 |   0    |    Y     |  N   |       |   |
|  13   | REQUESTS_RECOVERY |   varchar   | 1 |   0    |    Y     |  N   |       |   |
####  <a id="tb_job_qrtz_job_details">tb_job_qrtz_job_details</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | SCHED_NAME |   varchar   | 120 |   0    |    N     |  Y   |       |   |
|  2   | JOB_NAME |   varchar   | 200 |   0    |    N     |  Y   |       |   |
|  3   | JOB_GROUP |   varchar   | 200 |   0    |    N     |  Y   |       |   |
|  4   | DESCRIPTION |   varchar   | 250 |   0    |    Y     |  N   |       |   |
|  5   | JOB_CLASS_NAME |   varchar   | 250 |   0    |    N     |  N   |       |   |
|  6   | IS_DURABLE |   varchar   | 1 |   0    |    N     |  N   |       |   |
|  7   | IS_NONCONCURRENT |   varchar   | 1 |   0    |    N     |  N   |       |   |
|  8   | IS_UPDATE_DATA |   varchar   | 1 |   0    |    N     |  N   |       |   |
|  9   | REQUESTS_RECOVERY |   varchar   | 1 |   0    |    N     |  N   |       |   |
|  10   | JOB_DATA |   blob   | 65535 |   0    |    Y     |  N   |       |   |
####  <a id="tb_job_qrtz_locks">tb_job_qrtz_locks</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | SCHED_NAME |   varchar   | 120 |   0    |    N     |  Y   |       |   |
|  2   | LOCK_NAME |   varchar   | 40 |   0    |    N     |  Y   |       |   |
####  <a id="tb_job_qrtz_paused_trigger_grps">tb_job_qrtz_paused_trigger_grps</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | SCHED_NAME |   varchar   | 120 |   0    |    N     |  Y   |       |   |
|  2   | TRIGGER_GROUP |   varchar   | 200 |   0    |    N     |  Y   |       |   |
####  <a id="tb_job_qrtz_scheduler_state">tb_job_qrtz_scheduler_state</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | SCHED_NAME |   varchar   | 120 |   0    |    N     |  Y   |       |   |
|  2   | INSTANCE_NAME |   varchar   | 200 |   0    |    N     |  Y   |       |   |
|  3   | LAST_CHECKIN_TIME |   bigint   | 19 |   0    |    N     |  N   |       |   |
|  4   | CHECKIN_INTERVAL |   bigint   | 19 |   0    |    N     |  N   |       |   |
####  <a id="tb_job_qrtz_simple_triggers">tb_job_qrtz_simple_triggers</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | SCHED_NAME |   varchar   | 120 |   0    |    N     |  Y   |       |   |
|  2   | TRIGGER_NAME |   varchar   | 200 |   0    |    N     |  Y   |       |   |
|  3   | TRIGGER_GROUP |   varchar   | 200 |   0    |    N     |  Y   |       |   |
|  4   | REPEAT_COUNT |   bigint   | 19 |   0    |    N     |  N   |       |   |
|  5   | REPEAT_INTERVAL |   bigint   | 19 |   0    |    N     |  N   |       |   |
|  6   | TIMES_TRIGGERED |   bigint   | 19 |   0    |    N     |  N   |       |   |
####  <a id="tb_job_qrtz_simprop_triggers">tb_job_qrtz_simprop_triggers</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | SCHED_NAME |   varchar   | 120 |   0    |    N     |  Y   |       |   |
|  2   | TRIGGER_NAME |   varchar   | 200 |   0    |    N     |  Y   |       |   |
|  3   | TRIGGER_GROUP |   varchar   | 200 |   0    |    N     |  Y   |       |   |
|  4   | STR_PROP_1 |   varchar   | 512 |   0    |    Y     |  N   |       |   |
|  5   | STR_PROP_2 |   varchar   | 512 |   0    |    Y     |  N   |       |   |
|  6   | STR_PROP_3 |   varchar   | 512 |   0    |    Y     |  N   |       |   |
|  7   | INT_PROP_1 |   int   | 10 |   0    |    Y     |  N   |       |   |
|  8   | INT_PROP_2 |   int   | 10 |   0    |    Y     |  N   |       |   |
|  9   | LONG_PROP_1 |   bigint   | 19 |   0    |    Y     |  N   |       |   |
|  10   | LONG_PROP_2 |   bigint   | 19 |   0    |    Y     |  N   |       |   |
|  11   | DEC_PROP_1 |   decimal   | 13 |   4    |    Y     |  N   |       |   |
|  12   | DEC_PROP_2 |   decimal   | 13 |   4    |    Y     |  N   |       |   |
|  13   | BOOL_PROP_1 |   varchar   | 1 |   0    |    Y     |  N   |       |   |
|  14   | BOOL_PROP_2 |   varchar   | 1 |   0    |    Y     |  N   |       |   |
####  <a id="tb_job_qrtz_triggers">tb_job_qrtz_triggers</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | SCHED_NAME |   varchar   | 120 |   0    |    N     |  Y   |       |   |
|  2   | TRIGGER_NAME |   varchar   | 200 |   0    |    N     |  Y   |       |   |
|  3   | TRIGGER_GROUP |   varchar   | 200 |   0    |    N     |  Y   |       |   |
|  4   | JOB_NAME |   varchar   | 200 |   0    |    N     |  N   |       |   |
|  5   | JOB_GROUP |   varchar   | 200 |   0    |    N     |  N   |       |   |
|  6   | DESCRIPTION |   varchar   | 250 |   0    |    Y     |  N   |       |   |
|  7   | NEXT_FIRE_TIME |   bigint   | 19 |   0    |    Y     |  N   |       |   |
|  8   | PREV_FIRE_TIME |   bigint   | 19 |   0    |    Y     |  N   |       |   |
|  9   | PRIORITY |   int   | 10 |   0    |    Y     |  N   |       |   |
|  10   | TRIGGER_STATE |   varchar   | 16 |   0    |    N     |  N   |       |   |
|  11   | TRIGGER_TYPE |   varchar   | 8 |   0    |    N     |  N   |       |   |
|  12   | START_TIME |   bigint   | 19 |   0    |    N     |  N   |       |   |
|  13   | END_TIME |   bigint   | 19 |   0    |    Y     |  N   |       |   |
|  14   | CALENDAR_NAME |   varchar   | 200 |   0    |    Y     |  N   |       |   |
|  15   | MISFIRE_INSTR |   smallint   | 5 |   0    |    Y     |  N   |       |   |
|  16   | JOB_DATA |   blob   | 65535 |   0    |    Y     |  N   |       |   |
####  <a id="tb_job_qrtz_trigger_group">tb_job_qrtz_trigger_group</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | app_name |   varchar   | 64 |   0    |    N     |  N   |       | 执行器AppName  |
|  3   | title |   varchar   | 12 |   0    |    N     |  N   |       | 执行器名称  |
|  4   | order |   tinyint   | 3 |   0    |    N     |  N   |   0    | 排序  |
|  5   | address_type |   tinyint   | 3 |   0    |    N     |  N   |   0    | 执行器地址类型：0=自动注册、1=手动录入  |
|  6   | address_list |   varchar   | 512 |   0    |    Y     |  N   |       | 执行器地址列表，多地址逗号分隔  |
####  <a id="tb_job_qrtz_trigger_info">tb_job_qrtz_trigger_info</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | job_group |   int   | 10 |   0    |    N     |  N   |       | 执行器主键ID  |
|  3   | job_cron |   varchar   | 128 |   0    |    N     |  N   |       | 任务执行CRON  |
|  4   | job_desc |   varchar   | 255 |   0    |    N     |  N   |       |   |
|  5   | add_time |   datetime   | 19 |   0    |    Y     |  N   |       |   |
|  6   | update_time |   datetime   | 19 |   0    |    Y     |  N   |       |   |
|  7   | author |   varchar   | 64 |   0    |    Y     |  N   |       | 作者  |
|  8   | alarm_email |   varchar   | 255 |   0    |    Y     |  N   |       | 报警邮件  |
|  9   | executor_route_strategy |   varchar   | 50 |   0    |    Y     |  N   |       | 执行器路由策略  |
|  10   | executor_handler |   varchar   | 255 |   0    |    Y     |  N   |       | 执行器任务handler  |
|  11   | executor_param |   varchar   | 512 |   0    |    Y     |  N   |       | 执行器任务参数  |
|  12   | executor_block_strategy |   varchar   | 50 |   0    |    Y     |  N   |       | 阻塞处理策略  |
|  13   | executor_fail_strategy |   varchar   | 50 |   0    |    Y     |  N   |       | 失败处理策略  |
|  14   | glue_type |   varchar   | 50 |   0    |    N     |  N   |       | GLUE类型  |
|  15   | glue_source |   text   | 65535 |   0    |    Y     |  N   |       | GLUE源代码  |
|  16   | glue_remark |   varchar   | 128 |   0    |    Y     |  N   |       | GLUE备注  |
|  17   | glue_updatetime |   datetime   | 19 |   0    |    Y     |  N   |       | GLUE更新时间  |
|  18   | child_jobid |   varchar   | 255 |   0    |    Y     |  N   |       | 子任务ID，多个逗号分隔  |
|  19   | biz_id |   varchar   | 36 |   0    |    Y     |  N   |       |   |
####  <a id="tb_job_qrtz_trigger_log">tb_job_qrtz_trigger_log</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | job_group |   int   | 10 |   0    |    N     |  N   |       | 执行器主键ID  |
|  3   | job_id |   int   | 10 |   0    |    N     |  N   |       | 任务，主键ID  |
|  4   | glue_type |   varchar   | 50 |   0    |    Y     |  N   |       | GLUE类型  |
|  5   | executor_address |   varchar   | 255 |   0    |    Y     |  N   |       | 执行器地址，本次执行的地址  |
|  6   | executor_handler |   varchar   | 255 |   0    |    Y     |  N   |       | 执行器任务handler  |
|  7   | executor_param |   varchar   | 512 |   0    |    Y     |  N   |       | 执行器任务参数  |
|  8   | trigger_time |   datetime   | 19 |   0    |    Y     |  N   |       | 调度-时间  |
|  9   | trigger_code |   varchar   | 255 |   0    |    N     |  N   |   0    | 调度-结果  |
|  10   | trigger_msg |   varchar   | 2048 |   0    |    Y     |  N   |       | 调度-日志  |
|  11   | handle_time |   datetime   | 19 |   0    |    Y     |  N   |       | 执行-时间  |
|  12   | handle_code |   varchar   | 255 |   0    |    N     |  N   |   0    | 执行-状态  |
|  13   | handle_msg |   varchar   | 2048 |   0    |    Y     |  N   |       | 执行-日志  |
####  <a id="tb_job_qrtz_trigger_logglue">tb_job_qrtz_trigger_logglue</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | job_id |   int   | 10 |   0    |    N     |  N   |       | 任务，主键ID  |
|  3   | glue_type |   varchar   | 50 |   0    |    Y     |  N   |       | GLUE类型  |
|  4   | glue_source |   text   | 65535 |   0    |    Y     |  N   |       | GLUE源代码  |
|  5   | glue_remark |   varchar   | 128 |   0    |    N     |  N   |       | GLUE备注  |
|  6   | add_time |   timestamp   | 19 |   0    |    Y     |  N   |       |   |
|  7   | update_time |   timestamp   | 19 |   0    |    Y     |  N   |       |   |
####  <a id="tb_job_qrtz_trigger_registry">tb_job_qrtz_trigger_registry</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | registry_group |   varchar   | 255 |   0    |    N     |  N   |       |   |
|  3   | registry_key |   varchar   | 255 |   0    |    N     |  N   |       |   |
|  4   | registry_value |   varchar   | 255 |   0    |    N     |  N   |       |   |
|  5   | update_time |   timestamp   | 19 |   0    |    N     |  N   |   CURRENT_TIMESTAMP    |   |
####  <a id="tb_mq_error_message">tb_mq_error_message</a>

**说明：** MQ死信消息表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | msg_id |   varchar   | 32 |   0    |    N     |  Y   |       | 消息id  |
|  2   | topic |   varchar   | 60 |   0    |    N     |  N   |       | 消息主题  |
|  3   | tag |   varchar   | 100 |   0    |    N     |  N   |       | 消息分类  |
|  4   | msg_key |   varchar   | 40 |   0    |    Y     |  N   |       | 消息key  |
|  5   | msg_body |   text   | 65535 |   0    |    Y     |  N   |       | 消息体  |
|  6   | properties |   text   | 65535 |   0    |    Y     |  N   |       | 消息属性json串  |
|  7   | consume_flag |   int   | 10 |   0    |    Y     |  N   |   0    | 消费成功标识1成功0失败  |
|  8   | create_time |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  9   | consume_time |   datetime   | 19 |   0    |    Y     |  N   |       | 消费成功时间  |
####  <a id="tb_open_relation">tb_open_relation</a>

**说明：** 机构开户关系表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  N   |       | 主键id  |
|  2   | procurer_id |   varchar   | 36 |   0    |    N     |  N   |       | 采购方id  |
|  3   | supplier_id |   varchar   | 36 |   0    |    N     |  N   |       | 供应商id  |
####  <a id="tb_order_det">tb_order_det</a>

**说明：** 供应商订单明细

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | req_doc_no |   varchar   | 20 |   0    |    N     |  N   |       | 需求单号  |
|  3   | order_doc_no |   varchar   | 20 |   0    |    N     |  N   |       | 订单编号  |
|  4   | group_no |   varchar   | 20 |   0    |    N     |  N   |       | 所属竞价组分组号。不能提交无法匹配竞价组的商品  |
|  5   | common_name |   varchar   | 100 |   0    |    Y     |  N   |       | 通用名（中文）一般来说就是目录名称  |
|  6   | common_dosagee_form |   varchar   | 20 |   0    |    Y     |  N   |       | 通用剂型  |
|  7   | prod_id |   varchar   | 36 |   0    |    Y     |  N   |       | 商品ID  |
|  8   | prod_serial_no |   varchar   | 100 |   0    |    N     |  N   |       | 产品入网序列号  |
|  9   | prod_name |   varchar   | 100 |   0    |    N     |  N   |       | 商品名称  |
|  10   | prod_dosagee_form |   varchar   | 20 |   0    |    Y     |  N   |       | 商品剂型(字典)  |
|  11   | prod_spec |   varchar   | 100 |   0    |    N     |  N   |       | 商品规格  |
|  12   | prod_package_unit |   varchar   | 50 |   0    |    N     |  N   |       | 商品包装  |
|  13   | min_package |   varchar   | 20 |   0    |    Y     |  N   |       | 最小包装单位(字典)  |
|  14   | manufacture_code |   varchar   | 100 |   0    |    Y     |  N   |       | 生产厂家编码  |
|  15   | manufacture_name |   varchar   | 100 |   0    |    N     |  N   |       | 生产厂家中文名  |
|  16   | entire_quantity |   decimal   | 20 |   4    |    N     |  N   |       | 采购数量  |
|  17   | exchange_rate |   decimal   | 20 |   4    |    Y     |  N   |   1.0000    | 转换系数  |
|  18   | price |   decimal   | 20 |   4    |    Y     |  N   |       | 最小单位报价  |
|  19   | amount |   decimal   | 20 |   4    |    Y     |  N   |       | 单行总价  |
|  20   | gross_profit |   decimal   | 20 |   4    |    Y     |  N   |       | 结余率。相当于毛利率计算方式。医保价格-采购价/医保价格  |
|  21   | complete_quantity |   decimal   | 20 |   4    |    N     |  N   |       | 收货数量/入库数量  |
|  22   | supplier_id |   varchar   | 36 |   0    |    N     |  N   |       | 供应商ID  |
|  23   | send_quantity |   decimal   | 20 |   4    |    Y     |  N   |       | 发货数量  |
|  24   | complete_amount |   decimal   | 20 |   4    |    Y     |  N   |       | 入库金额（入库数量*单价）  |
|  25   | lack_quantity |   decimal   | 20 |   4    |    Y     |  N   |   0.0000    | 缺货数量  |
|  26   | lack_amount |   decimal   | 20 |   4    |    Y     |  N   |   0.0000    | 缺货金额  |
|  27   | lack_reason |   varchar   | 500 |   0    |    Y     |  N   |       | 缺货原因  |
|  28   | refuse_quantity |   decimal   | 20 |   4    |    Y     |  N   |   0.0000    | 拒收数量合计  |
|  29   | refuse_amount |   decimal   | 20 |   4    |    Y     |  N   |   0.0000    | 拒收金额合计  |
|  30   | apply_pay_quantity |   decimal   | 20 |   4    |    Y     |  N   |   0.0000    | 申请支付数量  |
|  31   | apply_pay_amount |   decimal   | 20 |   4    |    Y     |  N   |   0.0000    | 申请支付金额  |
|  32   | complete_pay_quantity |   decimal   | 20 |   4    |    Y     |  N   |   0.0000    | 同意支付数量  |
|  33   | complete_pay_amount |   decimal   | 20 |   4    |    Y     |  N   |   0.0000    | 同意支付金额  |
|  34   | refuse_pay_quantity |   decimal   | 20 |   4    |    Y     |  N   |   0.0000    | 拒绝支付数量  |
|  35   | refuse_pay_amount |   decimal   | 20 |   4    |    Y     |  N   |   0.0000    | 拒绝支付金额  |
|  36   | refund_quantity |   decimal   | 20 |   4    |    Y     |  N   |   0.0000    | 退货数量  |
|  37   | refund_amount |   decimal   | 20 |   4    |    Y     |  N   |   0.0000    | 退货金额  |
|  38   | last_got_price |   decimal   | 20 |   4    |    Y     |  N   |       | 上次中标价  |
|  39   | sort |   int   | 10 |   0    |    Y     |  N   |       | 排序  |
|  40   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 报价备注  |
|  41   | medicare_price |   decimal   | 20 |   4    |    Y     |  N   |       | 当前医保价  |
|  42   | lowest_price |   decimal   | 20 |   4    |    Y     |  N   |       | 当前历史最低价  |
|  43   | is_import |   int   | 10 |   0    |    Y     |  N   |       | 是否进口:0否，1是  |
|  44   | application_scope |   varchar   | 100 |   0    |    Y     |  N   |       | 适用范围  |
|  45   | product_introduction |   varchar   | 500 |   0    |    Y     |  N   |       | 产品介绍  |
|  46   | brand |   varchar   | 100 |   0    |    Y     |  N   |       | 品牌  |
|  47   | management_class |   varchar   | 20 |   0    |    Y     |  N   |       | 管理类别(字典)  |
|  48   | model |   varchar   | 100 |   0    |    Y     |  N   |       | 型号  |
|  49   | big_package_quantity |   varchar   | 11 |   0    |    Y     |  N   |       | 通用大包装数量/包装数量(器械)  |
|  50   | biz_type |   int   | 10 |   0    |    Y     |  N   |       | 业务类型：1药品2医疗器械9其它  |
####  <a id="tb_order_draft">tb_order_draft</a>

**说明：** 采购订单草稿明细

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | req_doc_no |   varchar   | 20 |   0    |    N     |  N   |       | 需求单号  |
|  3   | req_det_id |   varchar   | 35 |   0    |    Y     |  N   |       | 需求明细ID，标记报价明细对应哪条需求明细  |
|  4   | group_no |   varchar   | 20 |   0    |    N     |  N   |       | 所属竞价组分组号。不能提交无法匹配竞价组的商品  |
|  5   | common_name |   varchar   | 100 |   0    |    Y     |  N   |       | 通用名（中文）一般来说就是目录名称  |
|  6   | common_dosagee_form |   varchar   | 20 |   0    |    Y     |  N   |       | 通用剂型  |
|  7   | prod_id |   varchar   | 36 |   0    |    Y     |  N   |       | 商品ID  |
|  8   | prod_serial_no |   varchar   | 100 |   0    |    N     |  N   |       | 产品入网序列号  |
|  9   | prod_name |   varchar   | 100 |   0    |    N     |  N   |       | 商品名称  |
|  10   | prod_dosagee_form |   varchar   | 20 |   0    |    Y     |  N   |       | 商品剂型(字典)  |
|  11   | prod_spec |   varchar   | 100 |   0    |    N     |  N   |       | 商品规格  |
|  12   | prod_package_unit |   varchar   | 50 |   0    |    N     |  N   |       | 商品包装  |
|  13   | min_package |   varchar   | 20 |   0    |    Y     |  N   |       | 最小包装单位(字典)  |
|  14   | manufacture_code |   varchar   | 100 |   0    |    Y     |  N   |       | 生产厂家编码  |
|  15   | manufacture_name |   varchar   | 100 |   0    |    N     |  N   |       | 生产厂家中文名  |
|  16   | entire_quantity |   decimal   | 20 |   4    |    N     |  N   |       | 采购数量  |
|  17   | exchange_rate |   decimal   | 20 |   4    |    N     |  N   |   1.0000    | 转换系数  |
|  18   | price |   decimal   | 20 |   4    |    Y     |  N   |       | 最小单位报价  |
|  19   | amount |   decimal   | 20 |   4    |    Y     |  N   |       | 单行总价  |
|  20   | gross_profit |   decimal   | 20 |   4    |    Y     |  N   |       | 结余率。相当于毛利率计算方式。医保价格-采购价/医保价格  |
|  21   | supplier_id |   varchar   | 36 |   0    |    N     |  N   |       | 供应商ID  |
|  22   | prod_serial_not_in_plan |   varchar   | 50 |   0    |    N     |  N   |       | 被替换的预生成的明细商品序列号  |
|  23   | is_backup |   int   | 10 |   0    |    Y     |  N   |       | '0:不是替代方案;1:替代方案  |
|  24   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者id  |
|  25   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者姓名  |
|  26   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  27   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  28   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者  |
|  29   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  30   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 备注信息  |
|  31   | bidd_det_id |   varchar   | 36 |   0    |    N     |  N   |       | 竞价单明细id  |
|  32   | flavor |   varchar   | 36 |   0    |    N     |  N   |       | 订单生成规则1单项最低2总价最低  |
|  33   | same_factory |   int   | 10 |   0    |    Y     |  N   |   1    | 厂家一致（1是0否）  |
|  34   | is_import |   int   | 10 |   0    |    Y     |  N   |       | 是否进口:0否，1是  |
|  35   | application_scope |   varchar   | 100 |   0    |    Y     |  N   |       | 适用范围  |
|  36   | product_introduction |   varchar   | 500 |   0    |    Y     |  N   |       | 产品介绍  |
|  37   | brand |   varchar   | 100 |   0    |    Y     |  N   |       | 品牌  |
|  38   | management_class |   varchar   | 20 |   0    |    Y     |  N   |       | 管理类别(字典)  |
|  39   | model |   varchar   | 100 |   0    |    Y     |  N   |       | 型号  |
|  40   | biz_type |   int   | 10 |   0    |    Y     |  N   |       | 业务类型：1药品2医疗器械9其它  |
####  <a id="tb_order_main">tb_order_main</a>

**说明：** 供应商订单主表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | req_doc_no |   varchar   | 20 |   0    |    N     |  N   |       | 需求单号  |
|  3   | order_doc_no |   varchar   | 20 |   0    |    N     |  N   |       | 订单编号  |
|  4   | supplier_id |   varchar   | 36 |   0    |    N     |  N   |       | 供应商ID  |
|  5   | total_price |   decimal   | 20 |   4    |    N     |  N   |       | 总价格  |
|  6   | is_evaluate |   int   | 10 |   0    |    N     |  N   |   0    | 0未评价1已评价  |
|  7   | order_status |   int   | 10 |   0    |    N     |  N   |       | 1-订单已生成2-待发货3-待收货4-已收货5-待评价7-已评价8-申请取消订单9-订单取消0-交易关闭  |
|  8   | payment_method_code |   varchar   | 10 |   0    |    Y     |  N   |       | 支付方式代码  |
|  9   | payment_method_name |   varchar   | 20 |   0    |    Y     |  N   |       | 支付方式名称  |
|  10   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  11   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者  |
|  12   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  13   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  14   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者  |
|  15   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  16   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记，0-未删除1-已删除，默认0  |
|  17   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 需求备注  |
|  18   | procurer_id |   varchar   | 36 |   0    |    Y     |  N   |       | 采购方id  |
|  19   | procurer_name |   varchar   | 200 |   0    |    Y     |  N   |       | 采购方名称  |
|  20   | supplier_name |   varchar   | 200 |   0    |    Y     |  N   |       | 供应商名称  |
|  21   | order_det_count |   int   | 10 |   0    |    N     |  N   |       | 品规数  |
|  22   | pay_total_price |   decimal   | 20 |   4    |    Y     |  N   |       | 应支付总金额（实际收货数量*单价）  |
|  23   | lack_date |   datetime   | 19 |   0    |    Y     |  N   |       | 缺货日期  |
|  24   | lack_total_price |   decimal   | 20 |   4    |    Y     |  N   |   0.0000    | 缺货总金额  |
|  25   | refuse_total_price |   decimal   | 20 |   4    |    Y     |  N   |   0.0000    | 拒收总金额  |
|  26   | reason |   varchar   | 500 |   0    |    Y     |  N   |       | 撤销/拒签合同原因  |
|  27   | file_id |   varchar   | 500 |   0    |    Y     |  N   |       | 合同附件id  |
|  28   | file_name |   varchar   | 500 |   0    |    Y     |  N   |       | 合同附件名称  |
|  29   | file_size |   varchar   | 500 |   0    |    Y     |  N   |       | 合同附件大小  |
|  30   | payment_status |   int   | 10 |   0    |    Y     |  N   |       | 支付状态0-待付款2-已付款3-待退款4-已退款9-线下结算10-无  |
|  31   | biz_type |   int   | 10 |   0    |    Y     |  N   |       | 业务类型：1药品2医疗器械9其它  |
|  32   | refund_total_price |   decimal   | 20 |   4    |    Y     |  N   |   0.0000    | 退货总金额  |
|  33   | transaction_method |   int   | 10 |   0    |    Y     |  N   |   0    | 交易方式:0-非账期支付1-账期支付  |
|  34   | settlement_date |   varchar   | 10 |   0    |    Y     |  N   |       | 结算日期/天数  |
|  35   | receive_confirm_date |   datetime   | 19 |   0    |    Y     |  N   |       | 收货确认时间  |
|  36   | paid_price |   decimal   | 20 |   4    |    Y     |  N   |       | 已支付金额  |
|  37   | payment_date |   datetime   | 19 |   0    |    Y     |  N   |       | 线下结算时间  |
####  <a id="tb_order_org_address">tb_order_org_address</a>

**说明：** 订单收货地址表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | order_doc_no |   varchar   | 20 |   0    |    N     |  N   |       | 订单编号  |
|  3   | org_id |   varchar   | 36 |   0    |    N     |  N   |       | 采购机构id  |
|  4   | consignee |   varchar   | 255 |   0    |    Y     |  N   |       | 收货人  |
|  5   | phone |   varchar   | 255 |   0    |    Y     |  N   |       | 联系电话  |
|  6   | address |   varchar   | 255 |   0    |    Y     |  N   |       | 收货地址  |
|  7   | region_code |   varchar   | 20 |   0    |    Y     |  N   |       | 区划代码  |
|  8   | region_name |   varchar   | 255 |   0    |    Y     |  N   |       | 区划名称  |
|  9   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者id  |
|  10   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者姓名  |
|  11   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  12   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者id  |
|  13   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者姓名  |
|  14   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
####  <a id="tb_order_plan">tb_order_plan</a>

**说明：** 采购订单方案(自动生成)

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | supplier_id |   varchar   | 36 |   0    |    N     |  N   |       | 供应商ID  |
|  3   | req_doc_no |   varchar   | 20 |   0    |    N     |  N   |       | 需求单号  |
|  4   | req_det_id |   varchar   | 36 |   0    |    Y     |  N   |       | 需求明细ID，标记报价明细对应哪条需求明细  |
|  5   | bidd_doc_no |   varchar   | 20 |   0    |    N     |  N   |       | 竞价单据编号  |
|  6   | group_no |   varchar   | 20 |   0    |    N     |  N   |       | 所属竞价组分组号。不能提交无法匹配竞价组的商品  |
|  7   | common_name |   varchar   | 100 |   0    |    Y     |  N   |       | 通用名（中文）一般来说就是目录名称  |
|  8   | common_dosagee_form |   varchar   | 20 |   0    |    Y     |  N   |       | 通用剂型(字典)  |
|  9   | prod_id |   varchar   | 36 |   0    |    Y     |  N   |       | 商品ID  |
|  10   | prod_serial_no |   varchar   | 100 |   0    |    N     |  N   |       | 产品入网序列号  |
|  11   | prod_name |   varchar   | 100 |   0    |    N     |  N   |       | 商品名称  |
|  12   | prod_dosagee_form |   varchar   | 20 |   0    |    Y     |  N   |       | 商品剂型(字典)  |
|  13   | prod_spec |   varchar   | 100 |   0    |    N     |  N   |       | 商品规格  |
|  14   | prod_package_unit |   varchar   | 50 |   0    |    N     |  N   |       | 商品包装  |
|  15   | min_package |   varchar   | 20 |   0    |    Y     |  N   |       | 最小包装单位(字典)  |
|  16   | manufacture_code |   varchar   | 100 |   0    |    Y     |  N   |       | 生产厂家编码  |
|  17   | manufacture_name |   varchar   | 100 |   0    |    N     |  N   |       | 生产厂家中文名  |
|  18   | entire_quantity |   decimal   | 20 |   4    |    N     |  N   |       | 采购数量  |
|  19   | exchange_rate |   decimal   | 20 |   4    |    N     |  N   |   1.0000    | 转换系数  |
|  20   | price |   decimal   | 20 |   4    |    Y     |  N   |       | 最小单位报价  |
|  21   | amount |   decimal   | 20 |   4    |    Y     |  N   |   0.0000    | 单行总价  |
|  22   | gross_profit |   decimal   | 20 |   4    |    Y     |  N   |   0.0000    | 结余率。相当于毛利率计算方式。医保价格-采购价/医保价格  |
|  23   | flavor |   varchar   | 36 |   0    |    N     |  N   |       | 公式主表id，一个公式代表一种偏好策略  |
|  24   | is_backup |   int   | 10 |   0    |    Y     |  N   |       | '0:不是替代方案;1:替代方案  |
|  25   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者id  |
|  26   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者姓名  |
|  27   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  28   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 备注信息  |
|  29   | bidd_det_id |   varchar   | 36 |   0    |    N     |  N   |       | 竞价单明细id  |
|  30   | same_factory |   int   | 10 |   0    |    Y     |  N   |   1    | 厂家一致（1是0否）  |
|  31   | is_import |   int   | 10 |   0    |    Y     |  N   |       | 是否进口:0否，1是  |
|  32   | application_scope |   varchar   | 100 |   0    |    Y     |  N   |       | 适用范围  |
|  33   | product_introduction |   varchar   | 500 |   0    |    Y     |  N   |       | 产品介绍  |
|  34   | brand |   varchar   | 100 |   0    |    Y     |  N   |       | 品牌  |
|  35   | management_class |   varchar   | 20 |   0    |    Y     |  N   |       | 管理类别(字典)  |
|  36   | model |   varchar   | 100 |   0    |    Y     |  N   |       | 型号  |
|  37   | biz_type |   int   | 10 |   0    |    Y     |  N   |       | 业务类型：1药品2医疗器械9其它  |
####  <a id="tb_order_product_his">tb_order_product_his</a>

**说明：** 供应商采购历史表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | prod_id |   varchar   | 36 |   0    |    N     |  N   |       | 商品id  |
|  3   | procurer_id |   varchar   | 36 |   0    |    N     |  N   |       | 采购方id  |
####  <a id="tb_org_business_scope">tb_org_business_scope</a>

**说明：** 机构经营范围表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | org_id |   varchar   | 36 |   0    |    N     |  N   |       | 机构ID  |
|  3   | biz_type |   int   | 10 |   0    |    N     |  N   |       | 业务类型：1药品2医疗器械9其它  |
####  <a id="tb_pay_det">tb_pay_det</a>

**说明：** 支付结果表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | pay_doc_no |   varchar   | 20 |   0    |    N     |  N   |       | 支付单号  |
|  3   | order_doc_no |   varchar   | 20 |   0    |    N     |  N   |       | 订单编号  |
|  4   | pay_amount |   decimal   | 20 |   4    |    N     |  N   |       | 支付金额  |
|  5   | order_amount |   decimal   | 20 |   4    |    N     |  N   |       | 订单金额  |
|  6   | order_det_count |   int   | 10 |   0    |    N     |  N   |       | 订单品规数  |
|  7   | order_date |   datetime   | 19 |   0    |    Y     |  N   |       | 订单单据日期  |
####  <a id="tb_pay_main">tb_pay_main</a>

**说明：** 支付申请表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | pay_doc_no |   varchar   | 20 |   0    |    N     |  N   |       | 支付单号  |
|  3   | order_doc_no |   varchar   | 20 |   0    |    N     |  N   |       | 订单号  |
|  4   | supplier_id |   varchar   | 36 |   0    |    N     |  N   |       | 供应商id  |
|  5   | supplier_name |   varchar   | 100 |   0    |    Y     |  N   |       | 供应商名称  |
|  6   | recv_acct_id |   varchar   | 36 |   0    |    N     |  N   |       | 供应商选定的收钱的银行帐号  |
|  7   | sup_contact_oper_id |   varchar   | 36 |   0    |    N     |  N   |       | 供应商联系人ID  |
|  8   | sup_contact_oper_name |   varchar   | 50 |   0    |    N     |  N   |       | 供应商联系人名称  |
|  9   | sup_contact_number |   varchar   | 20 |   0    |    N     |  N   |       | 供应商联系人电话号码  |
|  10   | procurer_id |   varchar   | 36 |   0    |    N     |  N   |       | 采购方id  |
|  11   | procurer_name |   varchar   | 100 |   0    |    Y     |  N   |       | 采购方名称  |
|  12   | pay_acct_id |   varchar   | 36 |   0    |    Y     |  N   |       | 采购方选定的支付银行帐号Id  |
|  13   | procu_contact_oper_id |   varchar   | 20 |   0    |    Y     |  N   |       | 采购方选定的联系人ID  |
|  14   | procu_contact_oper_name |   varchar   | 36 |   0    |    Y     |  N   |       | 采购方选定的联系人名称  |
|  15   | procu_contact_number |   varchar   | 20 |   0    |    Y     |  N   |       | 采购方联系人电话号码  |
|  16   | pay_apply_date |   datetime   | 19 |   0    |    Y     |  N   |       | 支付申请时间  |
|  17   | pay_exp_date |   datetime   | 19 |   0    |    Y     |  N   |       | 支付确认有效截止时间  |
|  18   | paid_date |   datetime   | 19 |   0    |    Y     |  N   |       | 采购方支付时间  |
|  19   | cancel_date |   datetime   | 19 |   0    |    Y     |  N   |       | 采购方支付取消时间  |
|  20   | status |   int   | 10 |   0    |    N     |  N   |   0    | 0-待支付,1-支付完成,2-支付取消(采购方)，默认0  |
|  21   | remark |   varchar   | 520 |   0    |    Y     |  N   |       | 备注  |
|  22   | cancel_reason |   varchar   | 50 |   0    |    Y     |  N   |       | 支付取消原因，支付状态为2时候必填  |
|  23   | pay_total_amount |   decimal   | 12 |   4    |    N     |  N   |   0.0000    | 支付总金额  |
|  24   | creator_org_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者所在机构id  |
|  25   | creator_org_name |   varchar   | 260 |   0    |    Y     |  N   |       | 创建者所在机构名称  |
|  26   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者id  |
|  27   | creator_name |   varchar   | 100 |   0    |    Y     |  N   |       | 创建者姓名  |
|  28   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  29   | updater_org_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者所在机构id  |
|  30   | updater_org_name |   varchar   | 260 |   0    |    Y     |  N   |       | 更新者所在机构名称  |
|  31   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者id  |
|  32   | updater_name |   varchar   | 100 |   0    |    Y     |  N   |       | 创建者姓名  |
|  33   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  34   | del_flag |   int   | 10 |   0    |    Y     |  N   |       | 删除标记，0-未删除1-已删除，默认0-未删除  |
####  <a id="tb_procure_area">tb_procure_area</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | procureArea |   varchar   | 300 |   0    |    Y     |  N   |       |   |
|  2   | tsrdCode |   varchar   | 10 |   0    |    N     |  N   |       | 区划编码  |
####  <a id="tb_qfx_data_source">tb_qfx_data_source</a>

**说明：** 查询框架数据源

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | name |   varchar   | 100 |   0    |    Y     |  N   |       | 数据源名称  |
|  3   | data_source_type |   int   | 10 |   0    |    Y     |  N   |       | 数据源类型(0:MySQL;10:ElasticSearch;20:MongoDB;)  |
|  4   | conn_properties |   varchar   | 5000 |   0    |    Y     |  N   |       | 数据源连接属性  |
|  5   | salt |   varchar   | 36 |   0    |    Y     |  N   |       | 数据源连接属性加密用盐  |
|  6   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  7   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  8   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  9   | update_date |   timestamp   | 19 |   0    |    Y     |  N   |   CURRENT_TIMESTAMP    | 更新时间  |
|  10   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记，0-未删除1-已删除，默认0  |
|  11   | remark |   varchar   | 512 |   0    |    Y     |  N   |       | 备注  |
####  <a id="tb_qfx_query_info">tb_qfx_query_info</a>

**说明：** 查询信息

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | key |   varchar   | 36 |   0    |    N     |  N   |       | 查询信息KEY  |
|  3   | name |   varchar   | 100 |   0    |    Y     |  N   |       | 查询信息名称  |
|  4   | category |   varchar   | 100 |   0    |    Y     |  N   |       | 查询分类  |
|  5   | content |   longtext   | 2147483647 |   0    |    Y     |  N   |       | 查询的参数(扩展参数)和代码  |
|  6   | data_source_id |   varchar   | 36 |   0    |    Y     |  N   |       | 查询框架数据源ID  |
|  7   | settings |   varchar   | 1000 |   0    |    Y     |  N   |       | 查询设置信息  |
|  8   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  9   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  10   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  11   | update_date |   timestamp   | 19 |   0    |    Y     |  N   |   CURRENT_TIMESTAMP    | 更新时间  |
|  12   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记，0-未删除1-已删除，默认0  |
|  13   | remark |   varchar   | 512 |   0    |    Y     |  N   |       | 备注  |
####  <a id="tb_qfx_revision_his">tb_qfx_revision_his</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | query_id |   varchar   | 36 |   0    |    Y     |  N   |       | 查询的查询参数(扩展参数)和代码  |
|  3   | content_old |   longtext   | 2147483647 |   0    |    Y     |  N   |       | 查询的查询参数和代码的备份  |
|  4   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  5   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  6   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记，0-未删除1-已删除，默认0  |
|  7   | remark |   varchar   | 512 |   0    |    Y     |  N   |       | 备注  |
####  <a id="tb_qfx_template">tb_qfx_template</a>

**说明：** 查询模版（参数）

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | name |   varchar   | 100 |   0    |    Y     |  N   |       | 模版名称  |
|  3   | content |   text   | 65535 |   0    |    Y     |  N   |       | 查询的参数模版  |
|  4   | template_type |   int   | 10 |   0    |    Y     |  N   |       | 模版类型（0.参数;1.MySQL常用脚本）  |
|  5   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者(就是修改查询者)  |
|  6   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  7   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记，0-未删除1-已删除，默认0  |
|  8   | remark |   varchar   | 512 |   0    |    Y     |  N   |       | 备注  |
####  <a id="tb_reconcilia_account">tb_reconcilia_account</a>

**说明：** 交易对账结果表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 32 |   0    |    N     |  Y   |       |   |
|  2   | sub_account |   varchar   | 20 |   0    |    N     |  N   |       | 子账号  |
|  3   | trans_code |   varchar   | 10 |   0    |    N     |  N   |       | 交易编号  |
|  4   | trans_name |   varchar   | 20 |   0    |    N     |  N   |       | 交易名称  |
|  5   | trans_code_id |   varchar   | 24 |   0    |    Y     |  N   |       | 交易流水号  |
|  6   | pay_code |   varchar   | 32 |   0    |    Y     |  N   |       | 支付单号  |
|  7   | trade_account |   bigint   | 19 |   0    |    Y     |  N   |       | 交易金额（分）  |
|  8   | sub_account_money |   bigint   | 19 |   0    |    Y     |  N   |       | 子账号余额（分）  |
|  9   | freeze_money |   bigint   | 19 |   0    |    Y     |  N   |       | 子账户冻结余额（分）  |
|  10   | trade_time |   datetime   | 19 |   0    |    Y     |  N   |       | 交易时间  |
|  11   | status |   int   | 10 |   0    |    Y     |  N   |       | 对账结果0-未对账1：账平2：未对上3-短款（银行少账）4-长款（银行多账）9-其它  |
####  <a id="tb_refund_dedu_info">tb_refund_dedu_info</a>

**说明：** 退货抵扣表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | refund_det_id |   varchar   | 36 |   0    |    Y     |  N   |       | 抵扣对应的退货申请明细ID  |
|  3   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  4   | dedu_amount |   decimal   | 20 |   4    |    Y     |  N   |       | 抵扣金额  |
|  5   | pay_doc_no |   varchar   | 20 |   0    |    Y     |  N   |       | 支付单号  |
|  6   | procurer_id |   varchar   | 36 |   0    |    Y     |  N   |       | 采购方id  |
|  7   | supplier_id |   varchar   | 36 |   0    |    Y     |  N   |       | 供应商id  |
####  <a id="tb_refund_det">tb_refund_det</a>

**说明：** 退货申请明细

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | refund_doc_no |   varchar   | 20 |   0    |    N     |  N   |       | 退货单号  |
|  3   | deliver_doc_no |   varchar   | 20 |   0    |    N     |  N   |       | 发货单号  |
|  4   | prod_id |   varchar   | 36 |   0    |    N     |  N   |       | 商品id  |
|  5   | batch_no |   varchar   | 50 |   0    |    N     |  N   |       | 批次号  |
|  6   | price |   decimal   | 20 |   4    |    N     |  N   |   0.0000    | 价格  |
|  7   | refund_num |   decimal   | 12 |   2    |    N     |  N   |   0.00    | 退货数量  |
|  8   | refund_amount |   decimal   | 20 |   4    |    N     |  N   |   0.0000    | 退货金额  |
|  9   | refund_reason |   varchar   | 100 |   0    |    Y     |  N   |       | 退货原因  |
|  10   | remark |   varchar   | 512 |   0    |    Y     |  N   |       | 备注  |
|  11   | is_import |   int   | 10 |   0    |    Y     |  N   |       | 是否进口:0否，1是  |
|  12   | application_scope |   varchar   | 100 |   0    |    Y     |  N   |       | 适用范围  |
|  13   | product_introduction |   varchar   | 500 |   0    |    Y     |  N   |       | 产品介绍  |
|  14   | brand |   varchar   | 100 |   0    |    Y     |  N   |       | 品牌  |
|  15   | management_class |   varchar   | 20 |   0    |    Y     |  N   |       | 管理类别(字典)  |
|  16   | model |   varchar   | 100 |   0    |    Y     |  N   |       | 型号  |
|  17   | big_package_quantity |   varchar   | 11 |   0    |    Y     |  N   |       | 通用大包装数量/包装数量(器械)  |
|  18   | biz_type |   int   | 10 |   0    |    Y     |  N   |       | 业务类型：1药品2医疗器械9其它  |
####  <a id="tb_refund_main">tb_refund_main</a>

**说明：** 退货申请表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | refund_doc_no |   varchar   | 20 |   0    |    N     |  N   |       | 退货单号  |
|  3   | supplier_id |   varchar   | 36 |   0    |    N     |  N   |       | 供应商id  |
|  4   | supplier_name |   varchar   | 100 |   0    |    Y     |  N   |       | 供应商名称  |
|  5   | procurer_id |   varchar   | 36 |   0    |    Y     |  N   |       | 采购方id  |
|  6   | procurer_name |   varchar   | 100 |   0    |    Y     |  N   |       | 采购方名称  |
|  7   | apply_date |   datetime   | 19 |   0    |    Y     |  N   |       | 退货申请时间  |
|  8   | approved_date |   datetime   | 19 |   0    |    Y     |  N   |       | 退货确认时间  |
|  9   | refund_total_amount |   decimal   | 12 |   4    |    Y     |  N   |   0.0000    | 退货总金额  |
|  10   | refund_pgs |   int   | 10 |   0    |    Y     |  N   |   0    | 退货品规数  |
|  11   | status |   int   | 10 |   0    |    Y     |  N   |   0    | '退货状态：,0-退货申请,1-退货完成,7-退货取消(采),9-拒绝退货，默认0',  |
|  12   | reject_reason |   varchar   | 200 |   0    |    Y     |  N   |       | 拒绝退货原因，退货状态为9时必填  |
|  13   | reject_date |   datetime   | 19 |   0    |    Y     |  N   |       | 退货拒绝时间  |
|  14   | cancel_reason |   varchar   | 200 |   0    |    Y     |  N   |       | 取消退货原因  |
|  15   | cancel_date |   datetime   | 19 |   0    |    Y     |  N   |       | 取消退货时间  |
|  16   | consigneer |   varchar   | 100 |   0    |    Y     |  N   |       | 收货人  |
|  17   | consigneer_phone |   varchar   | 20 |   0    |    Y     |  N   |       | 收货人手机号  |
|  18   | address |   varchar   | 200 |   0    |    Y     |  N   |       | 收货地址  |
|  19   | address_id |   varchar   | 36 |   0    |    Y     |  N   |       | 收货地址id  |
|  20   | org_name |   varchar   | 200 |   0    |    Y     |  N   |       | 收货机构名称  |
|  21   | org_id |   varchar   | 36 |   0    |    Y     |  N   |       | 收货机构id  |
|  22   | creator_org_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者所在机构id  |
|  23   | creator_org_name |   varchar   | 260 |   0    |    Y     |  N   |       | 创建者所在机构名称  |
|  24   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者id  |
|  25   | creator_name |   varchar   | 100 |   0    |    Y     |  N   |       | 创建者姓名  |
|  26   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  27   | updater_org_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者所在机构id  |
|  28   | updater_org_name |   varchar   | 260 |   0    |    Y     |  N   |       | 更新者所在机构名称  |
|  29   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者id  |
|  30   | updater_name |   varchar   | 100 |   0    |    Y     |  N   |       | 创建者姓名  |
|  31   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  32   | del_flag |   int   | 10 |   0    |    Y     |  N   |       | 删除标记，0-未删除1-已删除，默认0-未删除  |
|  33   | remark |   varchar   | 520 |   0    |    Y     |  N   |       | 备注  |
|  34   | refund_money_status |   int   | 10 |   0    |    Y     |  N   |       | 1-未退款,2-已退款,3-线下结算  |
|  35   | order_doc_no |   varchar   | 36 |   0    |    Y     |  N   |       | 订单号  |
|  36   | biz_type |   int   | 10 |   0    |    Y     |  N   |       | 业务类型：1药品2医疗器械9其它  |
####  <a id="tb_req_bidd_mapping">tb_req_bidd_mapping</a>

**说明：** 需求竞价映射表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | req_doc_no |   varchar   | 20 |   0    |    N     |  N   |       | 需求单号  |
|  3   | procurer_id |   varchar   | 36 |   0    |    N     |  N   |       | 采购方id  |
|  4   | supplier_id |   varchar   | 36 |   0    |    N     |  N   |       | 供应商id  |
|  5   | is_end_bidding |   int   | 10 |   0    |    N     |  N   |       | 是否完成报价0-未开始报价，1-已保存报价，2-已提交报价，默认0  |
####  <a id="tb_req_det">tb_req_det</a>

**说明：** 采购需求明细

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | req_doc_no |   varchar   | 20 |   0    |    N     |  N   |       | 需求单号  |
|  3   | group_no |   varchar   | 20 |   0    |    N     |  N   |       | 竞价组分组号，不能提交无法匹配竞价组的商品  |
|  4   | common_name |   varchar   | 100 |   0    |    Y     |  N   |       | 通用名（中文）一般来说就是目录名称  |
|  5   | common_dosagee_form |   varchar   | 20 |   0    |    Y     |  N   |       | 通用剂型(字典)  |
|  6   | prod_id |   varchar   | 36 |   0    |    Y     |  N   |       | 商品id  |
|  7   | prod_serial_no |   varchar   | 100 |   0    |    Y     |  N   |       | 产品流水号  |
|  8   | prod_name |   varchar   | 100 |   0    |    N     |  N   |       | 商品名称  |
|  9   | prod_biz_code |   varchar   | 20 |   0    |    N     |  N   |       | 商品类型名称（新加的字段）  |
|  10   | prod_biz_name |   varchar   | 30 |   0    |    N     |  N   |       | 商品类型名称（新加的字段）  |
|  11   | prod_dosagee_code |   varchar   | 10 |   0    |    Y     |  N   |       | 商品剂型编码(字典)  |
|  12   | prod_dosagee_form |   varchar   | 20 |   0    |    Y     |  N   |       | 商品剂型(字典)  |
|  13   | prod_spec |   varchar   | 100 |   0    |    N     |  N   |       | 商品规格  |
|  14   | prod_package_unit |   varchar   | 50 |   0    |    N     |  N   |       | 商品包装  |
|  15   | prod_package |   varchar   | 100 |   0    |    Y     |  N   |       | 包装（转换系数*制剂单位/包装单位）  |
|  16   | min_package |   varchar   | 20 |   0    |    Y     |  N   |       | 最小包装单位(字典)  |
|  17   | manufacture_code |   varchar   | 100 |   0    |    Y     |  N   |       | 生产厂家编码  |
|  18   | manufacture_name |   varchar   | 100 |   0    |    N     |  N   |       | 生产厂家中文名  |
|  19   | exchange_rate |   decimal   | 20 |   4    |    Y     |  N   |   1.0000    | 转换系数（最小规格的数量）  |
|  20   | entire_quantity |   decimal   | 20 |   2    |    N     |  N   |       | 采购数量  |
|  21   | big_package_quantity |   decimal   | 20 |   0    |    Y     |  N   |       | 大包装数量  |
|  22   | whole_number |   decimal   | 20 |   2    |    Y     |  N   |       | 整装数  |
|  23   | sort |   int   | 10 |   0    |    Y     |  N   |       | 排序号  |
|  24   | is_two_vote_system |   int   | 10 |   0    |    N     |  N   |   0    | 是否两票制,0-否,1-是默认为0  |
|  25   | is_replace |   int   | 10 |   0    |    N     |  N   |   0    | 是否可替代,0-否,1-是默认为0  |
|  26   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  27   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记，0-未删除1-已删除，默认0  |
|  28   | is_import |   int   | 10 |   0    |    Y     |  N   |       | 是否进口:0否，1是  |
|  29   | application_scope |   varchar   | 100 |   0    |    Y     |  N   |       | 适用范围  |
|  30   | product_introduction |   varchar   | 500 |   0    |    Y     |  N   |       | 产品介绍  |
|  31   | brand |   varchar   | 100 |   0    |    Y     |  N   |       | 品牌  |
|  32   | management_class |   varchar   | 20 |   0    |    Y     |  N   |       | 管理类别(字典)  |
|  33   | model |   varchar   | 100 |   0    |    Y     |  N   |       | 型号  |
|  34   | biz_type |   int   | 10 |   0    |    Y     |  N   |       | 业务类型：1药品2医疗器械9其它  |
####  <a id="tb_req_main">tb_req_main</a>

**说明：** 采购需求主表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | req_doc_no |   varchar   | 20 |   0    |    N     |  N   |       | 需求单号，业务主键，唯一编号  |
|  3   | procurer_id |   varchar   | 36 |   0    |    N     |  N   |       | 采购方ID  |
|  4   | procurer_name |   varchar   | 100 |   0    |    Y     |  N   |       | 采购名称  |
|  5   | req_status |   int   | 10 |   0    |    N     |  N   |   1    | 需求状态:0-未提交、1-竞价中、2-竞价结束、3-竞价结束(预案生成完成)、4-订单生成、9-需求取消，默认0  |
|  6   | parity_method |   int   | 10 |   0    |    Y     |  N   |   1    | 报价方式:0-公开竞价、1-匿名报价  |
|  7   | open_method |   int   | 10 |   0    |    N     |  N   |   0    | 选择开放方式：0-所有供应商可见1-关联供应商可见2-指定供应商可见  |
|  8   | severity |   int   | 10 |   0    |    N     |  N   |   1    | 需求级别:0-普通、1-紧急,默认0  |
|  9   | bidd_start_time |   datetime   | 19 |   0    |    Y     |  N   |       | 竞价开始时间  |
|  10   | bidd_end_time |   datetime   | 19 |   0    |    Y     |  N   |       | 竞价结束时间  |
|  11   | bidding_title |   varchar   | 512 |   0    |    Y     |  N   |       | 本次提交竞价的标题内容  |
|  12   | buy_type |   varchar   | 36 |   0    |    Y     |  N   |       | 采购类型(数据字典，默认是药品)  |
|  13   | transaction_method |   int   | 10 |   0    |    N     |  N   |   0    | 交易方式:0-非账期支付1-账期支付  |
|  14   | expect_receive_start_date |   datetime   | 19 |   0    |    Y     |  N   |       | 期望收货开始日期  |
|  15   | expect_receive_end_date |   datetime   | 19 |   0    |    Y     |  N   |       | 期望收货结束日期  |
|  16   | settlement_date_method |   int   | 10 |   0    |    Y     |  N   |       | 账期结算方式0-指定1-不指定  |
|  17   | appoint_settlement_date |   datetime   | 19 |   0    |    Y     |  N   |       | 指定结算日期  |
|  18   | unspecified_settlement_date |   varchar   | 20 |   0    |    Y     |  N   |       | 不指定结算日期  |
|  19   | unspecified_settlement_date_write |   varchar   | 20 |   0    |    Y     |  N   |       | 不指定结算日期(手动填写)  |
|  20   | contactor_oper_id |   varchar   | 36 |   0    |    Y     |  N   |       | 报价联系人operId(不使用)  |
|  21   | contactor_oper_name |   varchar   | 50 |   0    |    Y     |  N   |       | 联系人名称(输入)  |
|  22   | contactor_oper_phone |   varchar   | 20 |   0    |    Y     |  N   |       | 联系人电话(输入)  |
|  23   | contactor_oper_email |   varchar   | 255 |   0    |    Y     |  N   |       | 报价联系人邮箱(不使用)  |
|  24   | requested_count |   int   | 10 |   0    |    Y     |  N   |       | 要求的供应商数量  |
|  25   | responded_count |   int   | 10 |   0    |    Y     |  N   |   0    | 已响应供应商数量  |
|  26   | req_det_count |   int   | 10 |   0    |    Y     |  N   |   0    | 需求品规数  |
|  27   | res_det_count |   int   | 10 |   0    |    Y     |  N   |   0    | 响应中已经被覆盖的产品总数  |
|  28   | bidd_org_count |   int   | 10 |   0    |    Y     |  N   |   0    | 参与竞价机构数  |
|  29   | pre_order_count |   int   | 10 |   0    |    Y     |  N   |   0    | 预生成订单数量  |
|  30   | actual_order_count |   int   | 10 |   0    |    Y     |  N   |   0    | 实际订单数量  |
|  31   | submit_pact_count |   int   | 10 |   0    |    Y     |  N   |   0    | 提交合同的数量  |
|  32   | first_cancel_pact |   int   | 10 |   0    |    Y     |  N   |   0    | 甲方取消的数量  |
|  33   | sign_pact_count |   int   | 10 |   0    |    Y     |  N   |   0    | 签订合同的数量  |
|  34   | second_cancel_pact |   int   | 10 |   0    |    Y     |  N   |   0    | 乙方取消合同的数量  |
|  35   | biz_type |   int   | 10 |   0    |    Y     |  N   |       | 业务类型：1药品2医疗器械9其它  |
|  36   | is_replace |   int   | 10 |   0    |    Y     |  N   |   0    | 明细是否存在可替代,0-否,1-是默认为0  |
|  37   | is_watched |   int   | 10 |   0    |    N     |  N   |   0    | 是否有供应商查看过：0-否、1-是  |
|  38   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  39   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者  |
|  40   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  41   | req_submit_date |   datetime   | 19 |   0    |    Y     |  N   |       | 需求提交时间  |
|  42   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  43   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者  |
|  44   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  45   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记，0-未删除1-已删除，默认0  |
|  46   | remark |   varchar   | 512 |   0    |    Y     |  N   |       | 需求备注  |
####  <a id="tb_req_supplier">tb_req_supplier</a>

**说明：** 需求指定供应商表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | req_doc_no |   varchar   | 36 |   0    |    N     |  N   |       | 需求单号  |
|  3   | supplier_id |   varchar   | 36 |   0    |    Y     |  N   |       | 供应商id  |
|  4   | supplier_name |   varchar   | 64 |   0    |    Y     |  N   |       | 供应商名称  |
|  5   | is_vite |   int   | 10 |   0    |    Y     |  N   |       | 是否邀请0、否，1、是  |
|  6   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
####  <a id="tb_req_supplier_draft">tb_req_supplier_draft</a>

**说明：** 需求指定供应商草稿表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | req_doc_no |   varchar   | 36 |   0    |    N     |  N   |       | 需求单号  |
|  3   | supplier_id |   varchar   | 36 |   0    |    Y     |  N   |       | 供应商id  |
|  4   | supplier_name |   varchar   | 64 |   0    |    Y     |  N   |       | 供应商名称  |
|  5   | is_vite |   int   | 10 |   0    |    Y     |  N   |       | 是否邀请0、否，1、是  |
|  6   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
####  <a id="tb_req_template">tb_req_template</a>

**说明：** 采购需求模板主表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | req_doc_no |   varchar   | 36 |   0    |    Y     |  N   |       | 需求单号：模板  |
|  3   | template_name |   varchar   | 128 |   0    |    Y     |  N   |       | 模板标题(名称),当做为草稿的时候这里是null  |
|  4   | procurer_id |   varchar   | 36 |   0    |    N     |  N   |       | 采购方id  |
|  5   | procurer_name |   varchar   | 100 |   0    |    N     |  N   |       | 采购方名称  |
|  6   | severity |   int   | 10 |   0    |    Y     |  N   |   1    | 需求级别:0-普通、1-紧急,默认0  |
|  7   | is_template |   int   | 10 |   0    |    N     |  N   |   0    | 是否模板0-草稿1-模板，默认0-草稿  |
|  8   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者id  |
|  9   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者姓名  |
|  10   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  11   | remark |   varchar   | 512 |   0    |    Y     |  N   |       | 备注  |
|  12   | biz_type |   int   | 10 |   0    |    N     |  N   |       | 业务类型：1药品2医疗器械9其它  |
####  <a id="tb_req_template_det">tb_req_template_det</a>

**说明：** 采购需求模板明细

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | req_doc_no |   varchar   | 36 |   0    |    N     |  N   |       | 需求单号：模板  |
|  3   | group_no |   varchar   | 20 |   0    |    N     |  N   |       | 所属竞价组分组号。不能提交无法匹配竞价组的商品  |
|  4   | common_name |   varchar   | 100 |   0    |    Y     |  N   |       | 通用名（中文）一般来说就是目录名称  |
|  5   | common_dosagee_form |   varchar   | 20 |   0    |    Y     |  N   |       | 通用剂型(字典)  |
|  6   | prod_id |   varchar   | 36 |   0    |    Y     |  N   |       | 商品ID  |
|  7   | prod_serial_no |   varchar   | 100 |   0    |    Y     |  N   |       | 产品流水号  |
|  8   | prod_name |   varchar   | 100 |   0    |    N     |  N   |       | 商品名称  |
|  9   | prod_biz_code |   varchar   | 20 |   0    |    N     |  N   |       | 商品类型名称（新加的字段）  |
|  10   | prod_biz_name |   varchar   | 30 |   0    |    N     |  N   |       | 商品类型名称（新加的字段）  |
|  11   | prod_dosagee_code |   varchar   | 10 |   0    |    Y     |  N   |       | 商品剂型编码(字典)  |
|  12   | prod_dosagee_form |   varchar   | 20 |   0    |    Y     |  N   |       | 商品剂型(字典)  |
|  13   | prod_spec |   varchar   | 100 |   0    |    N     |  N   |       | 商品规格  |
|  14   | prod_package_unit |   varchar   | 50 |   0    |    N     |  N   |       | 商品包装  |
|  15   | prod_package |   varchar   | 100 |   0    |    Y     |  N   |       | 包装（转换系数*制剂单位/包装单位）  |
|  16   | min_package |   varchar   | 20 |   0    |    Y     |  N   |       | 最小包装单位(字典)  |
|  17   | manufacture_code |   varchar   | 100 |   0    |    Y     |  N   |       | 生产厂家编码  |
|  18   | manufacture_name |   varchar   | 100 |   0    |    N     |  N   |       | 生产厂家中文名  |
|  19   | exchange_rate |   decimal   | 20 |   4    |    Y     |  N   |   1.0000    | 转换系数（最小规格的数量）  |
|  20   | entire_quantity |   decimal   | 20 |   2    |    N     |  N   |       | 采购数量  |
|  21   | big_package_quantity |   decimal   | 20 |   0    |    Y     |  N   |       | 大包装数量  |
|  22   | whole_number |   decimal   | 20 |   2    |    Y     |  N   |       | 整装数  |
|  23   | sort |   int   | 10 |   0    |    Y     |  N   |       | 排序号  |
|  24   | is_two_vote_system |   int   | 10 |   0    |    N     |  N   |   0    | 是否两票制,0-否,1-是默认为0  |
|  25   | is_replace |   int   | 10 |   0    |    N     |  N   |   0    | 是否可替代,0-否,1-是默认为0  |
|  26   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  27   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记，0-未删除1-已删除，默认0  |
|  28   | is_import |   int   | 10 |   0    |    Y     |  N   |       | 是否进口:0否，1是  |
|  29   | application_scope |   varchar   | 100 |   0    |    Y     |  N   |       | 适用范围  |
|  30   | product_introduction |   varchar   | 500 |   0    |    Y     |  N   |       | 产品介绍  |
|  31   | brand |   varchar   | 100 |   0    |    Y     |  N   |       | 品牌  |
|  32   | management_class |   varchar   | 20 |   0    |    Y     |  N   |       | 管理类别(字典)  |
|  33   | model |   varchar   | 100 |   0    |    Y     |  N   |       | 型号  |
|  34   | biz_type |   int   | 10 |   0    |    N     |  N   |       | 业务类型：1药品2医疗器械9其它  |
####  <a id="tb_rp_bidding_demand">tb_rp_bidding_demand</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 32 |   0    |    N     |  Y   |       | id  |
|  2   | statistics_type |   varchar   | 1 |   0    |    Y     |  N   |       | 统计类型:1-采购需求统计，2-订购需求统计，3-完成需求统计，4-取消需求统计  |
|  3   | year_and_month |   varchar   | 8 |   0    |    Y     |  N   |       | 统计年月  |
|  4   | statistics_number |   int   | 10 |   0    |    Y     |  N   |       | 统计数量  |
|  5   | operation_time |   datetime   | 19 |   0    |    Y     |  N   |       | 数据插入时间  |
####  <a id="tb_rp_bidding_demand_medical_org">tb_rp_bidding_demand_medical_org</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 32 |   0    |    N     |  Y   |       | 主键  |
|  2   | hospital_id |   varchar   | 32 |   0    |    Y     |  N   |       | 医疗机构id  |
|  3   | hospital_name |   varchar   | 50 |   0    |    Y     |  N   |       | 医疗机构名称  |
|  4   | year_and_month |   varchar   | 8 |   0    |    Y     |  N   |       | 年月  |
|  5   | opration_time |   date   | 10 |   0    |    Y     |  N   |       | 数据更新时间  |
|  6   | purchase_requirement_statistics |   int   | 10 |   0    |    Y     |  N   |       | 统计类型:1-采购需求统计  |
|  7   | order_requirement_statistics |   int   | 10 |   0    |    Y     |  N   |       | 统计类型:2-订购需求统计  |
|  8   | complete_requirements_statistics |   int   | 10 |   0    |    Y     |  N   |       | 统计类型:3-完成需求统计  |
|  9   | cancel_demand_statistics |   int   | 10 |   0    |    Y     |  N   |       | 统计类型:4-取消需求统计  |
####  <a id="tb_rp_bidding_summary">tb_rp_bidding_summary</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 32 |   0    |    N     |  Y   |       | id  |
|  2   | statistics_type |   varchar   | 1 |   0    |    Y     |  N   |       | 统计类型:1-采购需求，2-已报价需求，3-已中标报价  |
|  3   | year_And_month |   varchar   | 8 |   0    |    Y     |  N   |       | 统计年月  |
|  4   | statistics_number |   int   | 10 |   0    |    Y     |  N   |       | 统计数量  |
|  5   | operation_time |   datetime   | 19 |   0    |    Y     |  N   |       | 数据插入时间  |
####  <a id="tb_rp_bidding_summary_supply_org">tb_rp_bidding_summary_supply_org</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 32 |   0    |    N     |  Y   |       | 主键  |
|  2   | supply_id |   varchar   | 32 |   0    |    Y     |  N   |       | 供应商id  |
|  3   | supply_name |   varchar   | 50 |   0    |    Y     |  N   |       | 供应商名称  |
|  4   | year_and_month |   varchar   | 8 |   0    |    Y     |  N   |       | 年月  |
|  5   | opration_time |   date   | 10 |   0    |    Y     |  N   |       | 数据更新时间  |
|  6   | purchase_requirement_statistics |   int   | 10 |   0    |    Y     |  N   |       | 统计类型:1-采购需求  |
|  7   | quoted_requirement_statistics |   int   | 10 |   0    |    Y     |  N   |       | 统计类型:2-已报价需求  |
|  8   | offer_requirements_statistics |   int   | 10 |   0    |    Y     |  N   |       | 统计类型:3-已中标报价  |
####  <a id="tb_rp_drug_area_trans">tb_rp_drug_area_trans</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | area_id |   int   | 10 |   0    |    Y     |  N   |       |   |
|  3   | area_name |   varchar   | 200 |   0    |    Y     |  N   |       |   |
|  4   | total_deal_amount |   double   | 22 |   0    |    Y     |  N   |       | 合计成交金额  |
|  5   | in_store_amount |   double   | 22 |   0    |    Y     |  N   |       | 入库金额  |
|  6   | total_surplus_amount |   double   | 22 |   0    |    Y     |  N   |       | 合计结余金额  |
|  7   | date_year |   varchar   | 10 |   0    |    Y     |  N   |       |   |
####  <a id="tb_rp_drug_quality_level">tb_rp_drug_quality_level</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | quality_level |   varchar   | 100 |   0    |    Y     |  N   |       | 质量层次  |
|  3   | buy_amount |   double   | 22 |   0    |    Y     |  N   |       | 采购金额  |
|  4   | buy_total_quantity |   int   | 10 |   0    |    Y     |  N   |       | 采购总数量  |
|  5   | buy_spec_quantity |   int   | 10 |   0    |    Y     |  N   |       | 采购品规数  |
|  6   | buy_times |   int   | 10 |   0    |    Y     |  N   |       | 采购次数  |
|  7   | in_store_amout |   double   | 22 |   0    |    Y     |  N   |       | 入库金额  |
|  8   | in_store_quantity |   int   | 10 |   0    |    Y     |  N   |       | 入库数量  |
|  9   | total_surplus_amount |   double   | 22 |   0    |    Y     |  N   |       | 合计结余金额  |
####  <a id="tb_rp_drug_quality_level_detail">tb_rp_drug_quality_level_detail</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | procurer_name |   varchar   | 200 |   0    |    Y     |  N   |       | 医院名称  |
|  3   | quality_level |   varchar   | 100 |   0    |    Y     |  N   |       | 质量层次  |
|  4   | buy_amount |   double   | 22 |   0    |    Y     |  N   |       | 采购金额  |
|  5   | buy_total_quantity |   int   | 10 |   0    |    Y     |  N   |       | 采购总数量  |
|  6   | buy_times |   int   | 10 |   0    |    Y     |  N   |       | 采购次数  |
|  7   | in_store_amout |   double   | 22 |   0    |    Y     |  N   |       | 入库金额  |
|  8   | in_store_quantity |   int   | 10 |   0    |    Y     |  N   |       | 入库数量  |
####  <a id="tb_rp_drug_summarize">tb_rp_drug_summarize</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | prod_id |   varchar   | 36 |   0    |    Y     |  N   |       | 产品id  |
|  3   | prod_seria_no |   varchar   | 50 |   0    |    Y     |  N   |       | 流水号  |
|  4   | prod_name |   varchar   | 200 |   0    |    Y     |  N   |       | 产品名称  |
|  5   | dosagee_form |   varchar   | 100 |   0    |    Y     |  N   |       | 剂型  |
|  6   | prod_spec |   varchar   | 100 |   0    |    Y     |  N   |       | 规格  |
|  7   | package_unit |   varchar   | 50 |   0    |    Y     |  N   |       | 包装  |
|  8   | manufacture |   varchar   | 200 |   0    |    Y     |  N   |       | 生产厂家  |
|  9   | buy_amount |   double   | 22 |   0    |    Y     |  N   |       | 采购金额  |
|  10   | buy_total_quantity |   double   | 22 |   0    |    Y     |  N   |       | 采购总数量  |
|  11   | buy_times |   int   | 10 |   0    |    Y     |  N   |       | 采购次数  |
|  12   | in_store_amout |   double   | 22 |   0    |    Y     |  N   |       | 入库金额  |
|  13   | in_store_quantity |   int   | 10 |   0    |    Y     |  N   |       | 入库数量  |
|  14   | total_surplus_amount |   double   | 22 |   0    |    Y     |  N   |       | 合计结余金额  |
|  15   | date_year |   varchar   | 10 |   0    |    Y     |  N   |       | 统计年份  |
####  <a id="tb_rp_drug_summarize_detail">tb_rp_drug_summarize_detail</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | procurer_id |   varchar   | 36 |   0    |    Y     |  N   |       | 医疗机构id  |
|  3   | procurer_name |   varchar   | 200 |   0    |    Y     |  N   |       | 医疗机构名称  |
|  4   | prod_id |   varchar   | 36 |   0    |    Y     |  N   |       | 产品id  |
|  5   | prod_seria_no |   varchar   | 50 |   0    |    Y     |  N   |       | 流水号  |
|  6   | prod_name |   varchar   | 200 |   0    |    Y     |  N   |       | 产品名称  |
|  7   | dosagee_form |   varchar   | 100 |   0    |    Y     |  N   |       | 剂型  |
|  8   | buy_amount |   double   | 22 |   0    |    Y     |  N   |       | 采购金额  |
|  9   | buy_total_quantity |   int   | 10 |   0    |    Y     |  N   |       | 采购总数量  |
|  10   | buy_times |   int   | 10 |   0    |    Y     |  N   |       | 采购次数  |
|  11   | in_store_amout |   double   | 22 |   0    |    Y     |  N   |       | 入库金额  |
|  12   | in_store_quantity |   int   | 10 |   0    |    Y     |  N   |       | 入库数量  |
|  13   | date_year |   varchar   | 10 |   0    |    Y     |  N   |       | 统计年份  |
####  <a id="tb_rp_drug_summarize_month">tb_rp_drug_summarize_month</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | prod_id |   varchar   | 36 |   0    |    Y     |  N   |       | 产品id  |
|  3   | prod_name |   varchar   | 200 |   0    |    Y     |  N   |       | 产品名称  |
|  4   | dosagee_form |   varchar   | 100 |   0    |    Y     |  N   |       | 剂型  |
|  5   | prod_spec |   varchar   | 100 |   0    |    Y     |  N   |       | 规格  |
|  6   | monthly_trans_quantity |   int   | 10 |   0    |    Y     |  N   |       | 月交易数量  |
|  7   | monthly_trans_amount |   double   | 22 |   0    |    Y     |  N   |       | 月交易金额  |
|  8   | monthly_avg_quantity |   int   | 10 |   0    |    Y     |  N   |       | 月平均交易数量  |
|  9   | monthly_avg_amount |   double   | 22 |   0    |    Y     |  N   |       | 月平均交易金额  |
|  10   | date_year |   varchar   | 10 |   0    |    Y     |  N   |       | 统计年份  |
|  11   | date_month |   varchar   | 10 |   0    |    Y     |  N   |       | 统计月份  |
####  <a id="tb_rp_hospital_supervise_city">tb_rp_hospital_supervise_city</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 32 |   0    |    N     |  Y   |       | 主键  |
|  2   | num |   int   | 10 |   0    |    Y     |  N   |       | 数量  |
|  3   | type |   varchar   | 50 |   0    |    Y     |  N   |       | 地市  |
|  4   | opration_time |   date   | 10 |   0    |    Y     |  N   |       | 数据操作时间  |
####  <a id="tb_rp_hospital_supervise_transaction_summary">tb_rp_hospital_supervise_transaction_summary</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 32 |   0    |    N     |  Y   |       | id  |
|  2   | region |   varchar   | 50 |   0    |    Y     |  N   |       | 地区  |
|  3   | hospital_name |   varchar   | 50 |   0    |    Y     |  N   |       | 医院名称  |
|  4   | hospital_lever |   varchar   | 10 |   0    |    Y     |  N   |       | 医院等级  |
|  5   | hospital_type |   varchar   | 10 |   0    |    Y     |  N   |       | 医院类型  |
|  6   | demand_specificat |   int   | 10 |   0    |    Y     |  N   |       | 需求品规数  |
|  7   | order_number_of_goods_regulations |   int   | 10 |   0    |    Y     |  N   |       | 订单品规数  |
|  8   | total_tran_amoun |   double   | 22 |   0    |    Y     |  N   |       | 合计成交金额  |
|  9   | distri_amoun |   double   | 22 |   0    |    Y     |  N   |       | 配送金额  |
|  10   | warehouse_amoun |   double   | 22 |   0    |    Y     |  N   |       | 入库金额  |
|  11   | total_surplus_amoun |   double   | 22 |   0    |    Y     |  N   |       | 合计结余金额  |
|  12   | year_and_month |   varchar   | 7 |   0    |    Y     |  N   |       | 业务发生的年月  |
|  13   | opration_time |   date   | 10 |   0    |    Y     |  N   |       | 数据插入时间  |
####  <a id="tb_rp_hospital_supervise_turnover">tb_rp_hospital_supervise_turnover</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 32 |   0    |    N     |  Y   |       | id  |
|  2   | turnover |   double   | 22 |   0    |    Y     |  N   |       | 成交金额  |
|  3   | amount_of_storage |   double   | 22 |   0    |    Y     |  N   |       | 入库金额  |
|  4   | lever |   varchar   | 10 |   0    |    Y     |  N   |       | 医院等级  |
|  5   | opration_time |   date   | 10 |   0    |    Y     |  N   |       | 数据插入时间  |
####  <a id="tb_rp_hospital_supervise_type">tb_rp_hospital_supervise_type</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 32 |   0    |    N     |  Y   |       | id  |
|  2   | num |   int   | 10 |   0    |    Y     |  N   |       | 数量  |
|  3   | lever |   varchar   | 10 |   0    |    Y     |  N   |       | 医院等级  |
|  4   | opration_time |   date   | 10 |   0    |    Y     |  N   |       | 数据插入时间  |
####  <a id="tb_rp_medical_area">tb_rp_medical_area</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | area_id |   int   | 10 |   0    |    N     |  N   |       | 地区id  |
|  3   | area_name |   varchar   | 100 |   0    |    Y     |  N   |       | 地区名称  |
|  4   | medical_amount |   double   | 22 |   0    |    Y     |  N   |       | 医保支付金额  |
|  5   | total_amount |   double   | 22 |   0    |    Y     |  N   |       | 采购金额  |
|  6   | pay_date |   varchar   | 10 |   0    |    Y     |  N   |       | 日期  |
|  7   | is_medical |   int   | 10 |   0    |    Y     |  N   |       | 是否医保资金  |
####  <a id="tb_rp_medical_fund_detail">tb_rp_medical_fund_detail</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | procurer_id |   varchar   | 36 |   0    |    Y     |  N   |       | 医疗机构id  |
|  3   | procurer_name |   varchar   | 200 |   0    |    Y     |  N   |       | 医疗机构名称  |
|  4   | buy_total |   double   | 22 |   0    |    Y     |  N   |       | 采购总金额  |
|  5   | medical_total |   double   | 22 |   0    |    Y     |  N   |       | 医保总额度  |
|  6   | medical_pay |   double   | 22 |   0    |    Y     |  N   |       | 医保支出金额  |
|  7   | date_year |   varchar   | 4 |   0    |    Y     |  N   |       | 统计年度  |
|  8   | is_medical |   int   | 10 |   0    |    Y     |  N   |       | 是否医保0否1是  |
|  9   | surplus_amount |   double   | 22 |   0    |    Y     |  N   |       | 医保结余金额  |
####  <a id="tb_rp_money_flow">tb_rp_money_flow</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | flow_in_total |   double   | 22 |   0    |    Y     |  N   |       | 流入资金总额  |
|  3   | flow_in_org |   varchar   | 200 |   0    |    Y     |  N   |       | 流入单位名称  |
|  4   | flow_out_org |   varchar   | 200 |   0    |    Y     |  N   |       | 流出机构名称  |
|  5   | flow_out |   double   | 22 |   0    |    Y     |  N   |       | 流出金额  |
|  6   | difference |   double   | 22 |   0    |    Y     |  N   |       | 资金差  |
|  7   | flow_date |   char   | 4 |   0    |    Y     |  N   |       | 日期年份  |
####  <a id="tb_rp_order_amount">tb_rp_order_amount</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | rp_month |   varchar   | 10 |   0    |    Y     |  N   |       | 统计月份  |
|  3   | order_total |   int   | 10 |   0    |    Y     |  N   |   0    | 订单总数  |
|  4   | order_total_amount |   double   | 22 |   0    |    Y     |  N   |   0    | 订单总金额  |
|  5   | order_finish |   int   | 10 |   0    |    Y     |  N   |   0    | 已完成订单数  |
|  6   | order_finish_amount |   double   | 22 |   0    |    Y     |  N   |   0    | 已完成订单总额  |
|  7   | order_paid |   int   | 10 |   0    |    Y     |  N   |   0    | 已支付订单数  |
|  8   | order_paid_amount |   double   | 22 |   0    |    Y     |  N   |   0    | 已支付订单总额  |
|  9   | order_unconfirmed |   int   | 10 |   0    |    Y     |  N   |   0    | 未及时确认订单数  |
|  10   | order_unconfirmed_amount |   double   | 22 |   0    |    Y     |  N   |   0    | 未及时确认订单金额  |
|  11   | order_undelivery |   int   | 10 |   0    |    Y     |  N   |   0    | 未及时发货订单数  |
|  12   | order_undelivery_amount |   double   | 22 |   0    |    Y     |  N   |   0    | 未及时发货订单金额  |
|  13   | order_cancel |   int   | 10 |   0    |    Y     |  N   |   0    | 已取消订单数  |
|  14   | order_cancel_amount |   double   | 22 |   0    |    Y     |  N   |   0    | 已取消订单金额  |
|  15   | order_cancel_rows |   int   | 10 |   0    |    Y     |  N   |       | 取消品规数  |
####  <a id="tb_rp_order_amount_org">tb_rp_order_amount_org</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | rp_month |   varchar   | 10 |   0    |    Y     |  N   |       | 统计月份  |
|  3   | org_id |   varchar   | 36 |   0    |    Y     |  N   |       | 机构id  |
|  4   | org_name |   varchar   | 100 |   0    |    Y     |  N   |       | 机构名称  |
|  5   | org_type |   varchar   | 2 |   0    |    Y     |  N   |       | 机构类型1-医疗机构2-供应商  |
|  6   | order_total |   int   | 10 |   0    |    Y     |  N   |       | 总订单数  |
|  7   | order_total_amount |   double   | 11 |   0    |    Y     |  N   |       | 订单总金额  |
|  8   | order_total_rows |   int   | 10 |   0    |    Y     |  N   |       | 订单总品规数  |
####  <a id="tb_rp_order_cancel">tb_rp_order_cancel</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | rp_date |   varchar   | 10 |   0    |    Y     |  N   |       | 统计年月  |
|  3   | org_id |   varchar   | 36 |   0    |    Y     |  N   |       | 机构ID  |
|  4   | org_name |   varchar   | 50 |   0    |    Y     |  N   |       | 机构名称  |
|  5   | org_type |   varchar   | 2 |   0    |    Y     |  N   |       | 机构类型1-医疗机构2-供应商  |
|  6   | order_total |   int   | 10 |   0    |    Y     |  N   |       | 取消订单数  |
|  7   | order_amount |   double   | 22 |   0    |    Y     |  N   |       | 取消订单金额  |
|  8   | order_rows |   int   | 10 |   0    |    Y     |  N   |       | 取消品规数  |
####  <a id="tb_rp_order_cancel_detail">tb_rp_order_cancel_detail</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | cancel_org_id |   varchar   | 36 |   0    |    Y     |  N   |       |   |
|  3   | org_id |   varchar   | 36 |   0    |    Y     |  N   |       | 机构ID  |
|  4   | org_name |   varchar   | 50 |   0    |    Y     |  N   |       | 机构名称  |
|  5   | org_type |   varchar   | 2 |   0    |    Y     |  N   |       | 机构类型1-医疗机构2-供应商  |
|  6   | order_total |   int   | 10 |   0    |    Y     |  N   |       | 取消订单数  |
|  7   | order_amount |   double   | 22 |   0    |    Y     |  N   |       | 取消订单金额  |
|  8   | order_rows |   int   | 10 |   0    |    Y     |  N   |       | 取消品规数  |
####  <a id="tb_rp_order_coverage_rate">tb_rp_order_coverage_rate</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 32 |   0    |    N     |  Y   |       |   |
|  2   | rp_date |   varchar   | 10 |   0    |    Y     |  N   |       | 统计日期  |
|  3   | supplier_id |   varchar   | 36 |   0    |    Y     |  N   |       | 供应商ID  |
|  4   | supplier_name |   varchar   | 50 |   0    |    Y     |  N   |       | 供应商名称  |
|  5   | delivery_rank |   int   | 10 |   0    |    Y     |  N   |       | 配送订单排名  |
|  6   | delivery_num |   int   | 10 |   0    |    Y     |  N   |       | 配送订单数量  |
|  7   | delivery_rows |   int   | 10 |   0    |    Y     |  N   |       | 配送品规数  |
|  8   | delivery_rate |   varchar   | 10 |   0    |    Y     |  N   |       | 覆盖率  |
####  <a id="tb_rp_order_coverage_rate_detail">tb_rp_order_coverage_rate_detail</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 32 |   0    |    N     |  Y   |       |   |
|  2   | rp_date |   varchar   | 10 |   0    |    Y     |  N   |       | 统计日期  |
|  3   | supplier_id |   varchar   | 36 |   0    |    Y     |  N   |       | 供应商ID  |
|  4   | supplier_name |   varchar   | 50 |   0    |    Y     |  N   |       | 供应商名称  |
|  5   | sub_order_no |   varchar   | 32 |   0    |    Y     |  N   |       | 订单编号  |
|  6   | order_amount |   double   | 11 |   4    |    Y     |  N   |       | 订单金额  |
|  7   | delivery_rows |   int   | 10 |   0    |    Y     |  N   |       | 配送品规数  |
|  8   | procurer_id |   varchar   | 36 |   0    |    Y     |  N   |       | 医院id  |
|  9   | procurer_name |   varchar   | 50 |   0    |    Y     |  N   |       | 医院名称  |
####  <a id="tb_rp_order_replace">tb_rp_order_replace</a>

**说明：** 订单监管-异常订单替换率

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | supplier_id |   varchar   | 36 |   0    |    Y     |  N   |       | 供应商ID  |
|  3   | supplier_name |   varchar   | 50 |   0    |    Y     |  N   |       | 供应商名称  |
|  4   | procurer_id |   varchar   | 36 |   0    |    Y     |  N   |       | 医疗机构ID  |
|  5   | procurer_name |   varchar   | 50 |   0    |    Y     |  N   |       | 医疗机构名称  |
|  6   | replace_rate |   double   | 22 |   0    |    Y     |  N   |       | 替换率  |
|  7   | order_date |   varchar   | 20 |   0    |    Y     |  N   |       |   |
|  8   | all_order |   int   | 10 |   0    |    Y     |  N   |       | 总订单数  |
|  9   | replace_order |   int   | 10 |   0    |    Y     |  N   |       | 替换订单数  |
####  <a id="tb_rp_order_replace_detail">tb_rp_order_replace_detail</a>

**说明：** 订单监管-异常订单替换率-明细

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | order_doc_no |   varchar   | 30 |   0    |    Y     |  N   |       | 订单编号  |
|  3   | order_date |   datetime   | 19 |   0    |    Y     |  N   |       | 订单日期  |
|  4   | prod_serial_no |   varchar   | 100 |   0    |    Y     |  N   |       | 流水号  |
|  5   | prod_name |   varchar   | 100 |   0    |    Y     |  N   |       | 产品名称  |
|  6   | prod_dosagee_form |   varchar   | 50 |   0    |    Y     |  N   |       | 剂型  |
|  7   | prod_spec |   varchar   | 100 |   0    |    Y     |  N   |       | 规格  |
|  8   | entire_quantity |   int   | 10 |   0    |    Y     |  N   |       | 数量  |
|  9   | procurer_id |   varchar   | 36 |   0    |    Y     |  N   |       |   |
|  10   | supplier_id |   varchar   | 36 |   0    |    Y     |  N   |       |   |
|  11   | date_year |   varchar   | 10 |   0    |    Y     |  N   |       | 统计日期  |
####  <a id="tb_rp_order_unconfirm">tb_rp_order_unconfirm</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | sub_Order_No |   varchar   | 32 |   0    |    Y     |  N   |       | 订单编号  |
|  3   | supplier_Id |   varchar   | 36 |   0    |    Y     |  N   |       | 供应商ID  |
|  4   | supplier_Name |   varchar   | 50 |   0    |    Y     |  N   |       |   |
|  5   | procurer_Id |   varchar   | 36 |   0    |    Y     |  N   |       |   |
|  6   | procurer_Name |   varchar   | 50 |   0    |    Y     |  N   |       |   |
|  7   | order_Date |   datetime   | 19 |   0    |    Y     |  N   |       |   |
|  8   | status |   varchar   | 2 |   0    |    Y     |  N   |   0    | 紧急程度0-紧急  |
|  9   | total_amount |   double   | 22 |   0    |    Y     |  N   |       |   |
|  10   | row_count |   int   | 10 |   0    |    Y     |  N   |       |   |
####  <a id="tb_rp_order_unconfirm_detail">tb_rp_order_unconfirm_detail</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | sub_Order_No |   varchar   | 32 |   0    |    Y     |  N   |       | 订单编号  |
|  3   | prod_Seria_No |   varchar   | 100 |   0    |    Y     |  N   |       | 供应商ID  |
|  4   | prod_Name |   varchar   | 100 |   0    |    Y     |  N   |       |   |
|  5   | dosagee_Form |   varchar   | 50 |   0    |    Y     |  N   |       |   |
|  6   | prod_Spec |   varchar   | 100 |   0    |    Y     |  N   |       |   |
|  7   | total_amount |   double   | 22 |   0    |    Y     |  N   |       |   |
|  8   | row_count |   int   | 10 |   0    |    Y     |  N   |       |   |
####  <a id="tb_rp_order_undelivery">tb_rp_order_undelivery</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | sub_Order_No |   varchar   | 32 |   0    |    Y     |  N   |       | 订单编号  |
|  3   | supplier_Id |   int   | 10 |   0    |    Y     |  N   |       | 供应商ID  |
|  4   | supplier_Name |   varchar   | 50 |   0    |    Y     |  N   |       |   |
|  5   | procurer_Id |   int   | 10 |   0    |    Y     |  N   |       |   |
|  6   | procurer_Name |   varchar   | 50 |   0    |    Y     |  N   |       |   |
|  7   | order_Date |   datetime   | 19 |   0    |    Y     |  N   |       |   |
|  8   | status |   varchar   | 2 |   0    |    Y     |  N   |   0    | 紧急程度0-紧急  |
|  9   | total_amount |   double   | 22 |   0    |    Y     |  N   |       |   |
|  10   | row_count |   int   | 10 |   0    |    Y     |  N   |       |   |
####  <a id="tb_rp_order_undelivery_detail">tb_rp_order_undelivery_detail</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | sub_Order_No |   varchar   | 32 |   0    |    Y     |  N   |       | 订单编号  |
|  3   | prod_Seria_No |   varchar   | 100 |   0    |    Y     |  N   |       | 供应商ID  |
|  4   | prod_Name |   varchar   | 100 |   0    |    Y     |  N   |       |   |
|  5   | dosagee_Form |   varchar   | 50 |   0    |    Y     |  N   |       |   |
|  6   | prod_Spec |   varchar   | 100 |   0    |    Y     |  N   |       |   |
|  7   | total_amount |   double   | 22 |   0    |    Y     |  N   |       |   |
|  8   | row_count |   int   | 10 |   0    |    Y     |  N   |       |   |
####  <a id="tb_rp_procurer_coverage_rate">tb_rp_procurer_coverage_rate</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 32 |   0    |    N     |  Y   |       |   |
|  2   | rp_date |   varchar   | 10 |   0    |    Y     |  N   |       | 统计日期  |
|  3   | supplier_id |   varchar   | 36 |   0    |    Y     |  N   |       | 供应商ID  |
|  4   | supplier_name |   varchar   | 50 |   0    |    Y     |  N   |       | 供应商名称  |
|  5   | procurer_rank |   int   | 10 |   0    |    Y     |  N   |       | 配送医院排名  |
|  6   | procurer_num |   int   | 10 |   0    |    Y     |  N   |       | 配送医院数量  |
|  7   | coverage_rate |   varchar   | 10 |   0    |    Y     |  N   |       | 覆盖率  |
####  <a id="tb_rp_procurer_coverage_rate_detail">tb_rp_procurer_coverage_rate_detail</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 32 |   0    |    N     |  Y   |       |   |
|  2   | rp_date |   varchar   | 10 |   0    |    Y     |  N   |       | 统计日期  |
|  3   | supplier_id |   varchar   | 36 |   0    |    Y     |  N   |       | 供应商ID  |
|  4   | supplier_name |   varchar   | 50 |   0    |    Y     |  N   |       | 供应商名称  |
|  5   | procurer_rank |   int   | 10 |   0    |    Y     |  N   |       | 配送医院排名  |
|  6   | procurer_num |   int   | 10 |   0    |    Y     |  N   |       | 配送医院次数  |
|  7   | procurer_id |   varchar   | 36 |   0    |    Y     |  N   |       | 医疗机构ID  |
|  8   | procurer_name |   varchar   | 50 |   0    |    Y     |  N   |       | 医疗机构名称  |
####  <a id="tb_rp_return_goods_medical_detail">tb_rp_return_goods_medical_detail</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 32 |   0    |    N     |  Y   |       | id  |
|  2   | prodSeria_no |   varchar   | 32 |   0    |    Y     |  N   |       | 流水号  |
|  3   | prod_name |   varchar   | 100 |   0    |    Y     |  N   |       | 产品名称  |
|  4   | package_unit |   varchar   | 20 |   0    |    Y     |  N   |       | 单位  |
|  5   | prod_spec |   varchar   | 20 |   0    |    Y     |  N   |       | 规格  |
|  6   | return_amount |   double   | 22 |   0    |    Y     |  N   |       | 退货金额  |
|  7   | opration_time |   timestamp   | 19 |   0    |    Y     |  N   |       | 操作时间  |
|  8   | hospital_id |   varchar   | 32 |   0    |    Y     |  N   |       | 医疗机构id  |
|  9   | hospital_name |   varchar   | 50 |   0    |    Y     |  N   |       | 医疗机构名称  |
####  <a id="tb_rp_return_goods_medical_org">tb_rp_return_goods_medical_org</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 32 |   0    |    N     |  Y   |       | 主键  |
|  2   | hospital_id |   varchar   | 32 |   0    |    Y     |  N   |       | 医疗机构id  |
|  3   | hospital_name |   varchar   | 50 |   0    |    Y     |  N   |       | 医疗机构名称  |
|  4   | year_and_month |   varchar   | 8 |   0    |    Y     |  N   |       | 年月  |
|  5   | opration_time |   date   | 10 |   0    |    Y     |  N   |       | 数据更新时间  |
|  6   | number_returned_goods |   int   | 10 |   0    |    Y     |  N   |       | 退货品规数  |
|  7   | return_amount |   double   | 22 |   0    |    Y     |  N   |       | 退货金额  |
|  8   | amount_not_deducted |   double   | 22 |   0    |    Y     |  N   |       | 未抵扣金额  |
####  <a id="tb_rp_return_goods_summary">tb_rp_return_goods_summary</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 32 |   0    |    N     |  Y   |       | id  |
|  2   | number_returned_goods |   int   | 10 |   0    |    Y     |  N   |       | 退货品规数  |
|  3   | return_amount |   double   | 22 |   0    |    Y     |  N   |       | 退货金额  |
|  4   | amount_not_deducted |   double   | 22 |   0    |    Y     |  N   |       | 未抵扣金额  |
|  5   | year_And_month |   varchar   | 8 |   0    |    Y     |  N   |       | 统计年月  |
|  6   | operation_time |   datetime   | 19 |   0    |    Y     |  N   |       | 数据插入时间  |
####  <a id="tb_rp_return_goods_supply_detail">tb_rp_return_goods_supply_detail</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 32 |   0    |    N     |  Y   |       | id  |
|  2   | prodSeria_no |   varchar   | 32 |   0    |    Y     |  N   |       | 流水号  |
|  3   | prod_name |   varchar   | 100 |   0    |    Y     |  N   |       | 产品名称  |
|  4   | package_unit |   varchar   | 20 |   0    |    Y     |  N   |       | 单位  |
|  5   | prod_spec |   varchar   | 20 |   0    |    Y     |  N   |       | 规格  |
|  6   | return_amount |   double   | 22 |   0    |    Y     |  N   |       | 退货金额  |
|  7   | opration_time |   timestamp   | 19 |   0    |    Y     |  N   |       | 操作时间  |
|  8   | supply_id |   varchar   | 32 |   0    |    Y     |  N   |       | 供应商id  |
|  9   | supply_name |   varchar   | 50 |   0    |    Y     |  N   |       | 供应商名称  |
####  <a id="tb_rp_return_goods_supply_org">tb_rp_return_goods_supply_org</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 32 |   0    |    N     |  Y   |       | 主键  |
|  2   | supply_id |   varchar   | 32 |   0    |    Y     |  N   |       | 供应商id  |
|  3   | supply_name |   varchar   | 50 |   0    |    Y     |  N   |       | 供应商名称  |
|  4   | year_and_month |   varchar   | 8 |   0    |    Y     |  N   |       | 年月  |
|  5   | opration_time |   date   | 10 |   0    |    Y     |  N   |       | 数据更新时间  |
|  6   | number_returned_goods |   int   | 10 |   0    |    Y     |  N   |       | 退货品规数  |
|  7   | return_amount |   double   | 22 |   0    |    Y     |  N   |       | 退货金额  |
|  8   | amount_not_deducted |   double   | 22 |   0    |    Y     |  N   |       | 未抵扣金额  |
####  <a id="tb_rp_supplier_supervise_monthly_tran_summary">tb_rp_supplier_supervise_monthly_tran_summary</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 32 |   0    |    N     |  Y   |       |   |
|  2   | supplier_name |   varchar   | 100 |   0    |    Y     |  N   |       | 供应商名称  |
|  3   | city |   varchar   | 50 |   0    |    Y     |  N   |       | 地区  |
|  4   | type |   varchar   | 10 |   0    |    Y     |  N   |       | 类型  |
|  5   | number_of_win_bi |   int   | 10 |   0    |    Y     |  N   |       | 中标品规数  |
|  6   | bid_amoun |   double   | 22 |   0    |    Y     |  N   |       | 中标金额  |
|  7   | bid_rat |   double   | 22 |   0    |    Y     |  N   |       | 中标率  |
|  8   | amount_of_goods_shippe |   double   | 22 |   0    |    Y     |  N   |       | 发货金额  |
|  9   | warehousing_amoun |   double   | 22 |   0    |    Y     |  N   |       | 入库金额  |
|  10   | return_amoun |   double   | 22 |   0    |    Y     |  N   |       | 退货金额  |
|  11   | year_and_month |   varchar   | 8 |   0    |    Y     |  N   |       | 业务发生时间  |
|  12   | opration_time |   date   | 10 |   0    |    Y     |  N   |       | 数据插入时间  |
####  <a id="tb_rp_supplier_supervise_proportion">tb_rp_supplier_supervise_proportion</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 32 |   0    |    N     |  Y   |       | id  |
|  2   | circulation_enterp |   int   | 10 |   0    |    Y     |  N   |       | 流通企业  |
|  3   | manufacturing_enterp |   int   | 10 |   0    |    Y     |  N   |       | 生产企业  |
|  4   | first_agen |   int   | 10 |   0    |    Y     |  N   |       | 一级代理商  |
|  5   | opration_time |   date   | 10 |   0    |    Y     |  N   |       | 数据操作时间  |
|  6   | totol |   int   | 10 |   0    |    Y     |  N   |       | 供应商总数  |
|  7   | statics_type |   varchar   | 2 |   0    |    Y     |  N   |       | 1:供应商类型数统计,2:供应商中标数统计  |
####  <a id="tb_rp_supplier_supervise_vote">tb_rp_supplier_supervise_vote</a>

**说明：** 机构评价监管表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | supplier_id |   varchar   | 36 |   0    |    Y     |  N   |       | 供应商id  |
|  3   | supplier_name |   varchar   | 100 |   0    |    Y     |  N   |       | 供应商名称  |
|  4   | procurer_id |   varchar   | 36 |   0    |    Y     |  N   |       | 采购方id  |
|  5   | procurer_name |   varchar   | 100 |   0    |    Y     |  N   |       | 采购方名称  |
|  6   | eval_type_1 |   int   | 10 |   0    |    Y     |  N   |       | 总体满意度  |
|  7   | eval_type_2 |   int   | 10 |   0    |    Y     |  N   |       | 订单响应速度  |
|  8   | eval_type_3 |   int   | 10 |   0    |    Y     |  N   |       | 发货速度  |
|  9   | eval_type_4 |   int   | 10 |   0    |    Y     |  N   |       | 物流服务  |
|  10   | eval_type_5 |   int   | 10 |   0    |    Y     |  N   |       | 配送质量  |
|  11   | eval_type_6 |   int   | 10 |   0    |    Y     |  N   |       | 问题处置有效性  |
|  12   | eval_avg |   decimal   | 10 |   2    |    Y     |  N   |       | 历史分值(平均分)  |
|  13   | eval_time |   datetime   | 19 |   0    |    Y     |  N   |       | 评价时间  |
|  14   | opration_time |   date   | 10 |   0    |    Y     |  N   |       | 数据操作时间  |
####  <a id="tb_rp_supplier_timely">tb_rp_supplier_timely</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 32 |   0    |    N     |  Y   |       |   |
|  2   | rp_date |   varchar   | 10 |   0    |    Y     |  N   |       | 统计年月  |
|  3   | supplier_id |   varchar   | 36 |   0    |    Y     |  N   |       | 供应商id  |
|  4   | supplier_name |   varchar   | 50 |   0    |    Y     |  N   |       | 供应商名称  |
|  5   | order_amount |   double   | 22 |   0    |    Y     |  N   |       | 订单金额  |
|  6   | order_amount_hour |   double   | 22 |   0    |    Y     |  N   |       | 72小时到货金额  |
|  7   | order_hour_rate |   varchar   | 10 |   0    |    Y     |  N   |       | 72小时到货率  |
####  <a id="tb_security_code">tb_security_code</a>

**说明：** 安全验证码

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | code |   varchar   | 45 |   0    |    Y     |  N   |       | 验证码  |
|  3   | expires |   datetime   | 19 |   0    |    Y     |  N   |       | 过期时间  |
|  4   | biz_type |   int   | 10 |   0    |    Y     |  N   |       | 验证码类型  |
|  5   | ref_user |   varchar   | 45 |   0    |    Y     |  N   |       | 验证码所属用户电话或邮箱  |
####  <a id="tb_settle_main">tb_settle_main</a>

**说明：** 结算表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | settle_doc_no |   varchar   | 20 |   0    |    N     |  N   |       | 结算单号  |
|  3   | settle_date |   datetime   | 19 |   0    |    N     |  N   |       | 结算单日期  |
|  4   | supplier_id |   varchar   | 36 |   0    |    N     |  N   |       | 供应商id  |
|  5   | supplier_name |   varchar   | 50 |   0    |    N     |  N   |       | 供应商名称  |
|  6   | payable_amount_total |   decimal   | 15 |   4    |    N     |  N   |   0.0000    | 应付总金额  |
|  7   | apply_amount_total |   decimal   | 15 |   4    |    N     |  N   |   0.0000    | 申请支付金额  |
|  8   | settle_status |   int   | 10 |   0    |    N     |  N   |       | 结算状态-1:待确认，2-已确认，3-已拒绝  |
|  9   | settle_type |   int   | 10 |   0    |    N     |  N   |       | 结算类型-1:线下，2-线上  |
|  10   | rejectreason |   varchar   | 50 |   0    |    Y     |  N   |       | 拒绝原因  |
|  11   | creator_org_id |   varchar   | 36 |   0    |    N     |  N   |       | 创建者所在机构id  |
|  12   | creator_org_name |   varchar   | 260 |   0    |    N     |  N   |       | 创建者所在机构名称  |
|  13   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者id  |
|  14   | creator_name |   varchar   | 100 |   0    |    Y     |  N   |       | 创建者姓名  |
|  15   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  16   | updater_org_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者所在机构id  |
|  17   | updater_org_name |   varchar   | 260 |   0    |    Y     |  N   |       | 更新者所在机构名称  |
|  18   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者id  |
|  19   | updater_name |   varchar   | 100 |   0    |    Y     |  N   |       | 创建者姓名  |
|  20   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  21   | del_flag |   int   | 10 |   0    |    N     |  N   |       | 删除标记，0-未删除1-已删除，默认0-未删除  |
####  <a id="tb_sms_record">tb_sms_record</a>

**说明：** 短信消息记录

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | mobile |   varchar   | 11 |   0    |    Y     |  N   |       | 手机号  |
|  3   | content |   varchar   | 150 |   0    |    Y     |  N   |       | 短信内容  |
|  4   | send_date |   datetime   | 19 |   0    |    Y     |  N   |       | 发送时间  |
|  5   | result |   varchar   | 500 |   0    |    Y     |  N   |       | 发送结果  |
####  <a id="tb_supervise_manage_area">tb_supervise_manage_area</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | org_id |   varchar   | 36 |   0    |    Y     |  N   |       |   |
|  3   | region_code |   varchar   | 20 |   0    |    Y     |  N   |       |   |
####  <a id="tb_supplier_delivery_area">tb_supplier_delivery_area</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | org_id |   varchar   | 36 |   0    |    N     |  N   |       | 供应商单位ID  |
|  3   | region_code |   varchar   | 20 |   0    |    Y     |  N   |       | 配送区域编码  |
|  4   | region_name |   varchar   | 50 |   0    |    Y     |  N   |       | 配送区域名称(市)  |
|  5   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  6   | creator_org_id |   varchar   | 36 |   0    |    Y     |  N   |       |   |
|  7   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者  |
|  8   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  9   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  10   | updater_org_id |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  11   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者  |
|  12   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
####  <a id="tb_sys_app">tb_sys_app</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 255 |   0    |    N     |  Y   |       |   |
|  2   | app_code |   varchar   | 20 |   0    |    Y     |  N   |       |   |
|  3   | app_name |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  4   | useable |   int   | 10 |   0    |    N     |  N   |   1    | 是否启用  |
|  5   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
|  6   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 备注信息  |
|  7   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  8   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者姓名  |
|  9   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  10   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  11   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者姓名  |
|  12   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
####  <a id="tb_sys_application">tb_sys_application</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | app_code |   varchar   | 40 |   0    |    Y     |  N   |       | APP编码  |
|  3   | app_name |   varchar   | 255 |   0    |    Y     |  N   |       | APP名称  |
|  4   | secret_key |   varchar   | 255 |   0    |    Y     |  N   |       | APP秘钥  |
|  5   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 备注  |
|  6   | useable |   int   | 10 |   0    |    N     |  N   |   1    | 是否启用  |
|  7   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
|  8   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  9   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者姓名  |
|  10   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  11   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  12   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者姓名  |
|  13   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
####  <a id="tb_sys_bidd_formula_det">tb_sys_bidd_formula_det</a>

**说明：** 竞价公式明细表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | formula_id |   varchar   | 36 |   0    |    N     |  N   |       | 公式id  |
|  3   | target_doc_no |   varchar   | 36 |   0    |    N     |  N   |       | 指标编号  |
|  4   | target_coefficient |   double   | 22 |   0    |    N     |  N   |       | 指标系数  |
####  <a id="tb_sys_bidd_formula_main">tb_sys_bidd_formula_main</a>

**说明：** 竞价公式主表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | formula_name |   varchar   | 30 |   0    |    N     |  N   |       | 公式名称  |
|  3   | remark |   varchar   | 200 |   0    |    Y     |  N   |       | 备注  |
|  4   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  5   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  6   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  7   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  8   | rank |   int   | 10 |   0    |    Y     |  N   |       | 排序  |
####  <a id="tb_sys_bidd_target">tb_sys_bidd_target</a>

**说明：** 竞价指标表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | target_doc_no |   varchar   | 20 |   0    |    N     |  N   |       | 指标编号  |
|  3   | target_name |   varchar   | 30 |   0    |    N     |  N   |       | 指标名称  |
|  4   | remark |   varchar   | 200 |   0    |    Y     |  N   |       | 备注  |
|  5   | is_use |   int   | 10 |   0    |    Y     |  N   |   0    | 是否启用0否1是  |
|  6   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  7   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  8   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  9   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
####  <a id="tb_sys_dict">tb_sys_dict</a>

**说明：** 字典表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | parent_id |   varchar   | 36 |   0    |    Y     |  N   |   0    | 父级编号  |
|  3   | dict_group_code |   varchar   | 20 |   0    |    Y     |  N   |       | 字典分组编码  |
|  4   | dict_group_name |   varchar   | 100 |   0    |    Y     |  N   |       | 字典分组名称  |
|  5   | dict_code |   varchar   | 20 |   0    |    N     |  N   |       | 字典编码  |
|  6   | dict_name |   varchar   | 100 |   0    |    N     |  N   |       | 字典名称  |
|  7   | dict_name_en |   varchar   | 100 |   0    |    Y     |  N   |       | 字典名称英文  |
|  8   | type |   int   | 10 |   0    |    N     |  N   |       | 类型0：字典分组；1：字典项  |
|  9   | sort |   int   | 10 |   0    |    N     |  N   |       | 排序（升序）  |
|  10   | useable |   int   | 10 |   0    |    N     |  N   |   1    | 是否启用  |
|  11   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
|  12   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 备注信息  |
|  13   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  14   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者姓名  |
|  15   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  16   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  17   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者姓名  |
|  18   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
####  <a id="tb_sys_log">tb_sys_log</a>

**说明：** 日志表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | type |   int   | 10 |   0    |    Y     |  N   |   1    | 日志类型  |
|  3   | ip |   varchar   | 50 |   0    |    Y     |  N   |       | 操作IP地址  |
|  4   | description |   varchar   | 100 |   0    |    Y     |  N   |       | 操作描述  |
|  5   | user_id |   varchar   | 36 |   0    |    Y     |  N   |       |   |
|  6   | user_name |   varchar   | 20 |   0    |    Y     |  N   |       |   |
|  7   | username |   varchar   | 20 |   0    |    Y     |  N   |       | 操作用户  |
|  8   | log_date |   date   | 10 |   0    |    Y     |  N   |       |   |
|  9   | start_time_date |   datetime   | 19 |   0    |    Y     |  N   |       | 操作时间  |
|  10   | start_time_long |   bigint   | 19 |   0    |    Y     |  N   |       |   |
|  11   | spend_time |   bigint   | 19 |   0    |    Y     |  N   |       | 消耗时间  |
|  12   | referer |   varchar   | 255 |   0    |    Y     |  N   |       | 请求源  |
|  13   | referer_page |   varchar   | 255 |   0    |    Y     |  N   |       | 源页面  |
|  14   | base_path |   varchar   | 500 |   0    |    Y     |  N   |       | 根路径  |
|  15   | base_uri |   varchar   | 100 |   0    |    Y     |  N   |       |   |
|  16   | uri |   varchar   | 500 |   0    |    Y     |  N   |       | URI  |
|  17   | url |   varchar   | 500 |   0    |    Y     |  N   |       | URL  |
|  18   | method |   varchar   | 10 |   0    |    Y     |  N   |       | 请求类型  |
|  19   | parameter |   mediumtext   | 16777215 |   0    |    Y     |  N   |       | 参数  |
|  20   | user_agent |   varchar   | 500 |   0    |    Y     |  N   |       | 用户标识  |
|  21   | result |   mediumtext   | 16777215 |   0    |    Y     |  N   |       | 请求结果  |
|  22   | permissions |   varchar   | 100 |   0    |    Y     |  N   |       | 权限标识  |
|  23   | exception |   mediumtext   | 16777215 |   0    |    Y     |  N   |       |   |
####  <a id="tb_sys_message">tb_sys_message</a>

**说明：** 短信发送记录表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | user_id |   varchar   | 100 |   0    |    N     |  N   |       | 用户id(发送人userid)  |
|  3   | sender_mobile_phone |   varchar   | 11 |   0    |    N     |  N   |       | 发送人号码  |
|  4   | receiver_mobile_phone |   varchar   | 11 |   0    |    N     |  N   |       | 接收人号码  |
|  5   | creator_id |   varchar   | 36 |   0    |    N     |  N   |       | 创建者  |
|  6   | creator_name |   varchar   | 255 |   0    |    N     |  N   |       | 创建者姓名  |
|  7   | create_date |   datetime   | 19 |   0    |    N     |  N   |       | 创建时间  |
|  8   | random_code |   varchar   | 6 |   0    |    N     |  N   |       | 随机码  |
|  9   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 备注信息  |
####  <a id="tb_sys_org">tb_sys_org</a>

**说明：** 机构表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | parent_id |   varchar   | 36 |   0    |    Y     |  N   |       | 父级编号  |
|  3   | name |   varchar   | 100 |   0    |    N     |  N   |       | 名称  |
|  4   | pinyin_code |   varchar   | 500 |   0    |    Y     |  N   |       | 机构名称拼音首字母  |
|  5   | org_code |   varchar   | 50 |   0    |    Y     |  N   |       | 机构代码  |
|  6   | licence |   varchar   | 50 |   0    |    Y     |  N   |       | 营业执照号  |
|  7   | legal_person_cert_type |   varchar   | 50 |   0    |    Y     |  N   |       | 法人证件类型  |
|  8   | legal_person_name |   varchar   | 50 |   0    |    Y     |  N   |       | 法定代表人  |
|  9   | legal_person_no |   varchar   | 50 |   0    |    Y     |  N   |       | 法人证件号  |
|  10   | sort |   int   | 10 |   0    |    Y     |  N   |       | 排序  |
|  11   | region_code |   varchar   | 20 |   0    |    Y     |  N   |       | 区域编码  |
|  12   | region_name |   varchar   | 255 |   0    |    Y     |  N   |       | 区划名称  |
|  13   | org_type |   int   | 10 |   0    |    N     |  N   |       | 机构类型(1供应商、2医疗机构、3监管机构)  |
|  14   | grade |   varchar   | 20 |   0    |    Y     |  N   |       | 机构等级  |
|  15   | classification |   varchar   | 50 |   0    |    Y     |  N   |       | 机构分类  |
|  16   | is_group |   int   | 10 |   0    |    Y     |  N   |       | 是否集团：0-否，1-是  |
|  17   | group_name |   varchar   | 200 |   0    |    Y     |  N   |       | 集团名称  |
|  18   | registered_fund |   decimal   | 20 |   4    |    Y     |  N   |       | 注册资金  |
|  19   | address |   varchar   | 255 |   0    |    Y     |  N   |       | 详细地址  |
|  20   | zip_code |   varchar   | 6 |   0    |    Y     |  N   |       | 邮政编码  |
|  21   | master |   varchar   | 100 |   0    |    Y     |  N   |       | 负责人(联系人)  |
|  22   | phone |   varchar   | 200 |   0    |    Y     |  N   |       | 电话(联系人电话)  |
|  23   | fax |   varchar   | 200 |   0    |    Y     |  N   |       | 传真  |
|  24   | email |   varchar   | 200 |   0    |    Y     |  N   |       | 邮箱  |
|  25   | latitude |   decimal   | 10 |   4    |    Y     |  N   |       | 纬度  |
|  26   | longitude |   decimal   | 10 |   4    |    Y     |  N   |       | 经度  |
|  27   | useable |   int   | 10 |   0    |    N     |  N   |   1    | 是否启用  |
|  28   | primary_person_name |   varchar   | 64 |   0    |    Y     |  N   |       | 主负责人姓名  |
|  29   | deputy_person_name |   varchar   | 64 |   0    |    Y     |  N   |       | 副负责人姓名  |
|  30   | org_phone |   varchar   | 20 |   0    |    Y     |  N   |       | 公司电话  |
|  31   | reg_address |   varchar   | 255 |   0    |    Y     |  N   |       | 注册地址  |
|  32   | submit_status |   int   | 10 |   0    |    Y     |  N   |       | 申请提交状态0：未提交；1：已提交  |
|  33   | submit_time |   datetime   | 19 |   0    |    Y     |  N   |       | 提交申请时间  |
|  34   | audit_status |   int   | 10 |   0    |    Y     |  N   |   0    | 审核状态（0：未审核；1：审核通过；2：驳回）  |
|  35   | audit_time |   datetime   | 19 |   0    |    Y     |  N   |       | 审核时间  |
|  36   | audit_desc |   varchar   | 255 |   0    |    Y     |  N   |       | 审核描述  |
|  37   | auditor_id |   varchar   | 36 |   0    |    Y     |  N   |       | 审核人ID  |
|  38   | auditor_name |   varchar   | 100 |   0    |    Y     |  N   |       | 审核人姓名  |
|  39   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
|  40   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 备注信息  |
|  41   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者id  |
|  42   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者姓名  |
|  43   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  44   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者id  |
|  45   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者姓名  |
|  46   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
####  <a id="tb_sys_org_account">tb_sys_org_account</a>

**说明：** 单位账户表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | org_id |   varchar   | 36 |   0    |    N     |  N   |       | 机构ID  |
|  3   | bank_account |   varchar   | 50 |   0    |    Y     |  N   |       | 银行账号（对应华夏银行子账号）  |
|  4   | balance |   decimal   | 20 |   2    |    Y     |  N   |       | 余额  |
|  5   | freeze_amount |   decimal   | 20 |   2    |    Y     |  N   |       | 冻结金额  |
|  6   | salt |   varchar   | 36 |   0    |    Y     |  N   |       | 盐  |
|  7   | payment_password |   varchar   | 36 |   0    |    Y     |  N   |       | 支付密码  |
|  8   | status |   int   | 10 |   0    |    Y     |  N   |   0    | 状态（预留字段）  |
|  9   | create_time |   datetime   | 19 |   0    |    Y     |  N   |   CURRENT_TIMESTAMP    | 创建时间  |
####  <a id="tb_sys_org_att">tb_sys_org_att</a>

**说明：** 机构信息附件表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | org_id |   varchar   | 36 |   0    |    N     |  N   |       | 机构ID  |
|  3   | name |   varchar   | 255 |   0    |    Y     |  N   |       | 附件名称  |
|  4   | file_name |   varchar   | 255 |   0    |    Y     |  N   |       | 文件名称  |
|  5   | type |   varchar   | 20 |   0    |    Y     |  N   |       | 附件类型（证照字典）  |
|  6   | path |   varchar   | 255 |   0    |    Y     |  N   |       | 附件地址  |
|  7   | size |   decimal   | 10 |   2    |    Y     |  N   |       | 附件大小  |
|  8   | file_ext |   varchar   | 20 |   0    |    Y     |  N   |       | 文件扩展名  |
|  9   | sort |   int   | 10 |   0    |    Y     |  N   |       | 排序号  |
|  10   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  11   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  12   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  13   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  14   | credentials_number |   varchar   | 50 |   0    |    Y     |  N   |       | 证件号码  |
|  15   | expire_date_begin |   datetime   | 19 |   0    |    Y     |  N   |       | 有效期起始时间  |
|  16   | expire_date_end |   datetime   | 19 |   0    |    Y     |  N   |       | 有效期结束时间  |
####  <a id="tb_sys_org_balance_logs">tb_sys_org_balance_logs</a>

**说明：** 机构账户余额变化日志表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | org_id |   varchar   | 36 |   0    |    N     |  N   |       | 机构ID  |
|  3   | org_name |   varchar   | 50 |   0    |    N     |  N   |       | 机构名称  |
|  4   | money_before |   decimal   | 20 |   2    |    N     |  N   |       | 变化之前的余额  |
|  5   | money_after |   decimal   | 20 |   2    |    N     |  N   |       | 变化之后的余额  |
|  6   | money |   decimal   | 20 |   2    |    N     |  N   |       | 变化金额  |
|  7   | state |   int   | 10 |   0    |    N     |  N   |       | 1、充值；2、退款；3、支出；4、收入；5、提款  |
|  8   | pay_code |   varchar   | 32 |   0    |    N     |  N   |       | 支付单号(根据业务不同，分别取自充值，提现，交易表)  |
|  9   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建人id  |
|  10   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建人姓名  |
|  11   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  12   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 操作备注  |
|  13   | system_source |   int   | 10 |   0    |    N     |  N   |   0    | 系统来源0-PMS1-商城  |
####  <a id="tb_sys_org_balance_recharge">tb_sys_org_balance_recharge</a>

**说明：** 机构账户充值记录

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | payment_code |   varchar   | 20 |   0    |    N     |  N   |   BANK    | 支付方式code：BANK；PCALIPAY；H5ALIPAY；PCWXPAY；H5WXPAY  |
|  3   | payment_name |   varchar   | 100 |   0    |    N     |  N   |   银行账号直充    | 支付方式名称：银行账号直充；PC支付宝；H5支付宝；PC微信；H5微信  |
|  4   | pay_money |   decimal   | 20 |   2    |    N     |  N   |       | 支付金额  |
|  5   | pay_state |   int   | 10 |   0    |    N     |  N   |       | 支付状态0-初始1-成功2-失败  |
|  6   | error_message |   varchar   | 200 |   0    |    Y     |  N   |       | 错误信息  |
|  7   | pay_code |   varchar   | 32 |   0    |    Y     |  N   |       | 支付单号  |
|  8   | trade_no |   varchar   | 100 |   0    |    Y     |  N   |       | 支付交易流水号  |
|  9   | current_balance |   decimal   | 20 |   2    |    N     |  N   |       | 当前余额  |
|  10   | account_no |   varchar   | 100 |   0    |    N     |  N   |       | 银行帐号  |
|  11   | account_bank |   varchar   | 100 |   0    |    Y     |  N   |       | 银行名称，如建设银行  |
|  12   | account_name |   varchar   | 100 |   0    |    Y     |  N   |       | 账户名，一般就是公司名  |
|  13   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建人id  |
|  14   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建人姓名  |
|  15   | org_id |   varchar   | 36 |   0    |    N     |  N   |       | 机构id  |
|  16   | sub_account |   varchar   | 20 |   0    |    N     |  N   |       | 子账号  |
|  17   | org_name |   varchar   | 100 |   0    |    N     |  N   |       | 机构名称  |
|  18   | create_date |   datetime   | 19 |   0    |    N     |  N   |       | 创建时间  |
|  19   | handle_time |   datetime   | 19 |   0    |    Y     |  N   |       | 处理时间  |
|  20   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 备注  |
|  21   | system_source |   int   | 10 |   0    |    Y     |  N   |   0    | 系统来源0-PMS1-商城  |
####  <a id="tb_sys_org_balance_withdraw">tb_sys_org_balance_withdraw</a>

**说明：** 机构账户提现记录

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | pay_code |   varchar   | 32 |   0    |    Y     |  N   |       | 支付单号  |
|  3   | pay_state |   int   | 10 |   0    |    N     |  N   |       | 支付状态1-成功2-失败  |
|  4   | sub_account |   varchar   | 20 |   0    |    N     |  N   |       | 子账号  |
|  5   | trade_mem_code |   varchar   | 32 |   0    |    Y     |  N   |       | 交易会员代码  |
|  6   | out_come_money |   decimal   | 20 |   2    |    Y     |  N   |       | 提现金额  |
|  7   | channel_no |   varchar   | 4 |   0    |    Y     |  N   |       | 渠道号  |
|  8   | sum_sub_money |   decimal   | 20 |   2    |    Y     |  N   |       | 总扣款金额  |
|  9   | other_bank_cost |   decimal   | 20 |   2    |    Y     |  N   |       | 手续费/跨行手续费  |
|  10   | cus_pay_money |   decimal   | 20 |   2    |    Y     |  N   |       | 客户自付手续费  |
|  11   | mer_other_pay_money |   decimal   | 20 |   2    |    Y     |  N   |       | 商户代付手续费  |
|  12   | sub_account_money |   decimal   | 20 |   2    |    Y     |  N   |       | 子账号余额  |
|  13   | out_account |   varchar   | 20 |   0    |    N     |  N   |       | 出金帐号  |
|  14   | out_account_name |   varchar   | 120 |   0    |    N     |  N   |       | 出金帐号户名  |
|  15   | out_account_bank |   varchar   | 100 |   0    |    Y     |  N   |       | 出金帐号银行名称，如建设银行  |
|  16   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建人id  |
|  17   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建人姓名  |
|  18   | org_id |   varchar   | 36 |   0    |    N     |  N   |       | 机构id  |
|  19   | org_name |   varchar   | 100 |   0    |    N     |  N   |       | 机构名称  |
|  20   | create_date |   datetime   | 19 |   0    |    N     |  N   |       | 创建时间  |
|  21   | handle_time |   datetime   | 19 |   0    |    Y     |  N   |       | 处理时间  |
|  22   | remark |   varchar   | 200 |   0    |    Y     |  N   |       | 备注  |
|  23   | system_source |   int   | 10 |   0    |    N     |  N   |   0    | 系统来源0-PMS1-商城  |
####  <a id="tb_sys_org_change_request">tb_sys_org_change_request</a>

**说明：** 机构表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | org_id |   varchar   | 36 |   0    |    N     |  N   |       |   |
|  3   | org_name |   varchar   | 255 |   0    |    Y     |  N   |       | 单位名称（申请变更时的原名称）  |
|  4   | submit_status |   int   | 10 |   0    |    Y     |  N   |       | 申请提交状态0：未提交；1：已提交  |
|  5   | submit_time |   datetime   | 19 |   0    |    Y     |  N   |       | 提交申请时间  |
|  6   | submit_reason |   varchar   | 255 |   0    |    Y     |  N   |       | 变更原因  |
|  7   | submitter |   varchar   | 36 |   0    |    Y     |  N   |       | 提交变更人ID  |
|  8   | submitter_name |   varchar   | 30 |   0    |    Y     |  N   |       | 提交变更人姓名  |
|  9   | audit_status |   int   | 10 |   0    |    Y     |  N   |   0    | 审核状态（0：未审核；1：审核通过；2：审核不通过）  |
|  10   | audit_time |   datetime   | 19 |   0    |    Y     |  N   |       | 审核时间  |
|  11   | audit_desc |   varchar   | 255 |   0    |    Y     |  N   |       | 审核描述  |
|  12   | auditor |   varchar   | 36 |   0    |    Y     |  N   |       | 审核人ID  |
|  13   | auditor_name |   varchar   | 100 |   0    |    Y     |  N   |       | 审核人姓名  |
|  14   | original_data |   mediumtext   | 16777215 |   0    |    Y     |  N   |       | 原信息  |
|  15   | change_data |   mediumtext   | 16777215 |   0    |    Y     |  N   |       | 改变的信息  |
####  <a id="tb_sys_org_enter">tb_sys_org_enter</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | parent_id |   varchar   | 36 |   0    |    Y     |  N   |       | 父级编号  |
|  3   | name |   varchar   | 100 |   0    |    N     |  N   |       | 名称  |
|  4   | pinyin_code |   varchar   | 500 |   0    |    Y     |  N   |       | 机构名称拼音首字母  |
|  5   | org_code |   varchar   | 50 |   0    |    Y     |  N   |       | 机构代码  |
|  6   | licence |   varchar   | 50 |   0    |    Y     |  N   |       | 营业执照号  |
|  7   | legal_person_cert_type |   varchar   | 50 |   0    |    Y     |  N   |       | 法人证件类型  |
|  8   | legal_person_name |   varchar   | 50 |   0    |    Y     |  N   |       | 法人姓名  |
|  9   | legal_person_no |   varchar   | 50 |   0    |    Y     |  N   |       | 法人证件号  |
|  10   | sort |   int   | 10 |   0    |    Y     |  N   |       | 排序  |
|  11   | region_code |   varchar   | 20 |   0    |    Y     |  N   |       | 区域编码  |
|  12   | region_name |   varchar   | 255 |   0    |    Y     |  N   |       | 区划名称  |
|  13   | org_type |   int   | 10 |   0    |    N     |  N   |       | 机构类型(1供应商、2采购商、3监管机构)  |
|  14   | grade |   varchar   | 20 |   0    |    Y     |  N   |       | 机构等级  |
|  15   | classification |   varchar   | 50 |   0    |    Y     |  N   |       | 机构分类  |
|  16   | is_group |   int   | 10 |   0    |    Y     |  N   |       | 是否集团：0-否，1-是  |
|  17   | group_name |   varchar   | 200 |   0    |    Y     |  N   |       | 集团名称  |
|  18   | registered_fund |   decimal   | 20 |   4    |    Y     |  N   |       | 注册资金  |
|  19   | address |   varchar   | 255 |   0    |    Y     |  N   |       | 联系地址  |
|  20   | zip_code |   varchar   | 6 |   0    |    Y     |  N   |       | 邮政编码  |
|  21   | master |   varchar   | 100 |   0    |    Y     |  N   |       | 负责人  |
|  22   | phone |   varchar   | 200 |   0    |    Y     |  N   |       | 电话  |
|  23   | fax |   varchar   | 200 |   0    |    Y     |  N   |       | 传真  |
|  24   | email |   varchar   | 200 |   0    |    Y     |  N   |       | 邮箱  |
|  25   | latitude |   decimal   | 10 |   4    |    Y     |  N   |       | 纬度  |
|  26   | longitude |   decimal   | 10 |   4    |    Y     |  N   |       | 经度  |
|  27   | useable |   int   | 10 |   0    |    N     |  N   |   1    | 是否启用  |
|  28   | primary_person_name |   varchar   | 64 |   0    |    Y     |  N   |       | 主负责人姓名  |
|  29   | deputy_person_name |   varchar   | 64 |   0    |    Y     |  N   |       | 副负责人姓名  |
|  30   | org_phone |   varchar   | 20 |   0    |    Y     |  N   |       | 公司电话  |
|  31   | reg_address |   varchar   | 255 |   0    |    Y     |  N   |       | 注册地址  |
|  32   | submit_status |   int   | 10 |   0    |    Y     |  N   |   0    | 申请提交状态0：未提交；1：已提交；2：驳回  |
|  33   | submit_time |   datetime   | 19 |   0    |    Y     |  N   |       | 提交申请时间  |
|  34   | audit_status |   int   | 10 |   0    |    N     |  N   |   0    | 审核状态（0：未审核；1：审核通过；2：驳回；）  |
|  35   | audit_time |   datetime   | 19 |   0    |    Y     |  N   |       | 审核时间  |
|  36   | audit_desc |   varchar   | 255 |   0    |    Y     |  N   |       | 审核描述  |
|  37   | auditor_id |   varchar   | 36 |   0    |    Y     |  N   |       | 审核人ID  |
|  38   | auditor_name |   varchar   | 100 |   0    |    Y     |  N   |       | 审核人姓名  |
|  39   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
|  40   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 备注信息  |
|  41   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者id  |
|  42   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  43   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者id  |
|  44   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  45   | medical_industry |   int   | 10 |   0    |    Y     |  N   |       | 是否医药行业  |
####  <a id="tb_sys_org_enter_att">tb_sys_org_enter_att</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | org_id |   varchar   | 36 |   0    |    N     |  N   |       | 机构ID  |
|  3   | name |   varchar   | 255 |   0    |    Y     |  N   |       | 附件名称  |
|  4   | file_name |   varchar   | 255 |   0    |    Y     |  N   |       | 文件名称  |
|  5   | type |   varchar   | 20 |   0    |    Y     |  N   |       | 附件类型（证照字典）  |
|  6   | path |   varchar   | 255 |   0    |    Y     |  N   |       | 附件地址  |
|  7   | size |   decimal   | 10 |   2    |    Y     |  N   |       | 附件大小  |
|  8   | file_ext |   varchar   | 20 |   0    |    Y     |  N   |       | 文件扩展名  |
|  9   | sort |   int   | 10 |   0    |    Y     |  N   |       | 排序号  |
|  10   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  11   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  12   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  13   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  14   | credentials_number |   varchar   | 50 |   0    |    Y     |  N   |       | 证件号码  |
|  15   | expire_date_begin |   datetime   | 19 |   0    |    Y     |  N   |       | 有效期起始时间  |
|  16   | expire_date_end |   datetime   | 19 |   0    |    Y     |  N   |       | 有效期结束时间  |
####  <a id="tb_sys_org_license_type_mapping">tb_sys_org_license_type_mapping</a>

**说明：** 机构分类和证照类型对应关系表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | org_classification |   varchar   | 36 |   0    |    N     |  N   |       | 机构分类(字典)  |
|  3   | license_type |   varchar   | 36 |   0    |    N     |  N   |       | 证照类型(字典)  |
####  <a id="tb_sys_org_type_license">tb_sys_org_type_license</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | org_type |   int   | 10 |   0    |    N     |  N   |       | 机构类型(1:供应商；2:采购商)  |
|  3   | org_classification |   varchar   | 20 |   0    |    N     |  N   |       | 机构分类(取自数据字典)  |
|  4   | code |   varchar   | 20 |   0    |    Y     |  N   |       | 证照编码  |
|  5   | name |   varchar   | 255 |   0    |    N     |  N   |       | 证照名称  |
|  6   | required |   int   | 10 |   0    |    N     |  N   |   1    | 是否必填  |
|  7   | sort |   int   | 10 |   0    |    Y     |  N   |   0    | 排序序号  |
|  8   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 证照描述  |
####  <a id="tb_sys_param">tb_sys_param</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | code |   varchar   | 20 |   0    |    Y     |  N   |       | 参数编码  |
|  3   | name |   varchar   | 100 |   0    |    Y     |  N   |       | 参数名称  |
|  4   | type |   int   | 10 |   0    |    N     |  N   |   1    | 参数类型1：文本值；2：开关值；3：日期值  |
|  5   | description |   varchar   | 255 |   0    |    Y     |  N   |       | 参数描述  |
|  6   | value |   varchar   | 255 |   0    |    Y     |  N   |       | 参数值  |
|  7   | useable |   int   | 10 |   0    |    N     |  N   |   1    | 是否启用  |
|  8   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  9   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者姓名  |
|  10   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  11   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  12   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者姓名  |
|  13   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
####  <a id="tb_sys_params">tb_sys_params</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | code |   varchar   | 20 |   0    |    Y     |  N   |       | 参数编码  |
|  3   | name |   varchar   | 100 |   0    |    Y     |  N   |       | 参数名称  |
|  4   | type |   int   | 10 |   0    |    N     |  N   |   1    | 参数类型1：文本值；2：开关值；3：日期值  |
|  5   | desc |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  6   | value |   varchar   | 255 |   0    |    Y     |  N   |       | 参数值  |
|  7   | useable |   int   | 10 |   0    |    N     |  N   |   1    | 是否启用  |
|  8   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  9   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者姓名  |
|  10   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  11   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  12   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者姓名  |
|  13   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
####  <a id="tb_sys_region">tb_sys_region</a>

**说明：** 区划表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | code |   varchar   | 10 |   0    |    N     |  N   |       | 区划编码  |
|  3   | name |   varchar   | 100 |   0    |    N     |  N   |       | 区划名称  |
|  4   | parent_id |   varchar   | 36 |   0    |    Y     |  N   |       | 父级ID  |
|  5   | parent_code |   varchar   | 10 |   0    |    N     |  N   |       | 父级编号  |
|  6   | sort |   int   | 10 |   0    |    N     |  N   |   0    | 排序  |
|  7   | region_type |   int   | 10 |   0    |    Y     |  N   |       | 区划类型  |
|  8   | is_leaf |   int   | 10 |   0    |    N     |  N   |   0    | 是否叶子节点0：否；1：是  |
|  9   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 备注信息  |
|  10   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
|  11   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  12   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  13   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  14   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
####  <a id="tb_sys_resource">tb_sys_resource</a>

**说明：** 资源表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | app_id |   varchar   | 36 |   0    |    Y     |  N   |       |   |
|  3   | parent_id |   varchar   | 36 |   0    |    N     |  N   |       | 父级编号  |
|  4   | code |   varchar   | 50 |   0    |    Y     |  N   |       | 资源编码  |
|  5   | name |   varchar   | 100 |   0    |    N     |  N   |       | 资源名称  |
|  6   | permission |   varchar   | 512 |   0    |    Y     |  N   |       | 权限标识  |
|  7   | sort |   bigint   | 19 |   0    |    N     |  N   |       | 排序  |
|  8   | url |   varchar   | 512 |   0    |    Y     |  N   |       | 资源URI  |
|  9   | static_url |   varchar   | 512 |   0    |    Y     |  N   |       |   |
|  10   | target |   varchar   | 20 |   0    |    Y     |  N   |       | 目标  |
|  11   | icon |   varchar   | 100 |   0    |    Y     |  N   |       | 图标  |
|  12   | useable |   int   | 10 |   0    |    N     |  N   |   1    | 是否启用  |
|  13   | is_show |   int   | 10 |   0    |    N     |  N   |   1    | 是否在菜单中显示  |
|  14   | resource_type |   int   | 10 |   0    |    Y     |  N   |   1    | 资源类型1：目录；2：菜单；3：按钮  |
|  15   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  16   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者姓名  |
|  17   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  18   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  19   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者姓名  |
|  20   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  21   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
|  22   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 备注信息  |
####  <a id="tb_sys_role">tb_sys_role</a>

**说明：** 角色表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | org_id |   varchar   | 36 |   0    |    Y     |  N   |       | 归属机构  |
|  3   | name |   varchar   | 100 |   0    |    N     |  N   |       | 角色名称  |
|  4   | role_type |   varchar   | 255 |   0    |    Y     |  N   |       | 角色类型1:供应商；2：医疗机构；3：监管机构；4：平台运营  |
|  5   | data_scope |   int   | 10 |   0    |    Y     |  N   |       | 数据范围  |
|  6   | is_sys |   int   | 10 |   0    |    N     |  N   |   0    | 是否系统数据  |
|  7   | useable |   int   | 10 |   0    |    N     |  N   |   1    | 是否启用  |
|  8   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  9   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者姓名  |
|  10   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  11   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  12   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者姓名  |
|  13   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  14   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
|  15   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 备注信息  |
####  <a id="tb_sys_role_org">tb_sys_role_org</a>

**说明：** 角色-机构

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | role_id |   varchar   | 36 |   0    |    N     |  N   |       | 角色编号  |
|  3   | org_id |   varchar   | 36 |   0    |    N     |  N   |       | 机构编号  |
####  <a id="tb_sys_role_resource">tb_sys_role_resource</a>

**说明：** 角色-菜单

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | role_id |   varchar   | 36 |   0    |    N     |  N   |       | 角色编号  |
|  3   | resource_id |   varchar   | 36 |   0    |    N     |  N   |       | 菜单编号  |
####  <a id="tb_sys_sequence">tb_sys_sequence</a>

**说明：** 序列号生成表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | sequence_type |   varchar   | 100 |   0    |    N     |  N   |       | 序列号类型  |
|  3   | sequence_no |   int   | 10 |   0    |    Y     |  N   |       | 序列号值  |
####  <a id="tb_sys_system">tb_sys_system</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | code |   varchar   | 40 |   0    |    Y     |  N   |       | APP编码  |
|  3   | name |   varchar   | 255 |   0    |    Y     |  N   |       | APP名称  |
|  4   | secret_key |   varchar   | 255 |   0    |    Y     |  N   |       | APP秘钥  |
|  5   | desc |   varchar   | 255 |   0    |    Y     |  N   |       | APP描述  |
|  6   | enable |   varchar   | 255 |   0    |    Y     |  N   |       |   |
####  <a id="tb_sys_tickets">tb_sys_tickets</a>

**说明：** 雪花算法序列表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   bigint   | 19 |   0    |    N     |  Y   |       |   |
|  2   | stub |   char   | 1 |   0    |    N     |  N   |       |   |
####  <a id="tb_sys_user">tb_sys_user</a>

**说明：** 用户表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | user_code |   varchar   | 100 |   0    |    N     |  N   |       | 用户编码  |
|  3   | user_name |   varchar   | 100 |   0    |    N     |  N   |       | 姓名  |
|  4   | password |   varchar   | 100 |   0    |    N     |  N   |       | 密码  |
|  5   | salt |   varchar   | 100 |   0    |    Y     |  N   |       | 盐  |
|  6   | user_no |   varchar   | 100 |   0    |    Y     |  N   |       | 工号  |
|  7   | org_id |   varchar   | 36 |   0    |    N     |  N   |       | 归属机构部门  |
|  8   | email |   varchar   | 200 |   0    |    Y     |  N   |       | 邮箱  |
|  9   | phone |   varchar   | 200 |   0    |    Y     |  N   |       | 电话  |
|  10   | mobile |   varchar   | 20 |   0    |    Y     |  N   |       | 手机  |
|  11   | user_type |   int   | 10 |   0    |    Y     |  N   |       | 用户类型(1供应商用户、2采购单位用户、3监管机构用户)  |
|  12   | photo |   varchar   | 1000 |   0    |    Y     |  N   |       | 用户头像  |
|  13   | login_ip |   varchar   | 100 |   0    |    Y     |  N   |       | 最后登陆IP  |
|  14   | login_date |   datetime   | 19 |   0    |    Y     |  N   |       | 最后登陆时间  |
|  15   | login_flag |   int   | 10 |   0    |    Y     |  N   |       | 是否可登录  |
|  16   | status |   int   | 10 |   0    |    N     |  N   |   0    | 状态（0：申请入驻；1：已审核）  |
|  17   | useable |   int   | 10 |   0    |    N     |  N   |   1    | 是否启用  |
|  18   | is_exist_manage_org |   int   | 10 |   0    |    Y     |  N   |   0    | 是否存在管辖机构(供应商用户有效)0:否；1:是  |
|  19   | is_admin |   int   | 10 |   0    |    Y     |  N   |   0    | 是否机构管理员(机构用户有效)0:否；1:是  |
|  20   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建者  |
|  21   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建者姓名  |
|  22   | create_date |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  23   | updater_id |   varchar   | 36 |   0    |    Y     |  N   |       | 更新者  |
|  24   | updater_name |   varchar   | 255 |   0    |    Y     |  N   |       | 更新者姓名  |
|  25   | update_date |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
|  26   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
|  27   | remark |   varchar   | 255 |   0    |    Y     |  N   |       | 备注信息  |
####  <a id="tb_sys_user_member">tb_sys_user_member</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | user_id |   varchar   | 36 |   0    |    Y     |  N   |       |   |
|  3   | user_name |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  4   | account_balance |   decimal   | 12 |   4    |    Y     |  N   |   0.0000    | 账户余额  |
|  5   | payment_pwd |   varchar   | 30 |   0    |    Y     |  N   |       | 支付密码  |
|  6   | grade |   int   | 10 |   0    |    N     |  N   |   1    | 会员等级  |
|  7   | grade_value |   int   | 10 |   0    |    N     |  N   |   0    | 会员经验值  |
|  8   | integral |   int   | 10 |   0    |    N     |  N   |   0    | 会员积分  |
####  <a id="tb_sys_user_org">tb_sys_user_org</a>

**说明：** 用户-管辖机构表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | user_id |   varchar   | 36 |   0    |    N     |  N   |       | 用户id  |
|  3   | org_id |   varchar   | 36 |   0    |    N     |  N   |       | 机构id  |
####  <a id="tb_sys_user_resource">tb_sys_user_resource</a>

**说明：** 用户-功能表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | user_id |   varchar   | 36 |   0    |    N     |  N   |       | 用户ID  |
|  3   | resource_id |   varchar   | 36 |   0    |    Y     |  N   |       | 资源ID  |
|  4   | type |   int   | 10 |   0    |    Y     |  N   |       | 权限类型：-1：减权限，1：增权限  |
####  <a id="tb_sys_user_role">tb_sys_user_role</a>

**说明：** 用户-角色

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | user_id |   varchar   | 36 |   0    |    N     |  N   |       | 用户id  |
|  3   | role_id |   varchar   | 36 |   0    |    N     |  N   |       | 角色id  |
####  <a id="tb_tmp_calendar">tb_tmp_calendar</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | date |   date   | 10 |   0    |    N     |  N   |       |   |
####  <a id="tb_trade">tb_trade</a>

**说明：** 交易记录

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       |   |
|  2   | pay_code |   varchar   | 32 |   0    |    Y     |  N   |       | 支付单号  |
|  3   | sub_account |   varchar   | 20 |   0    |    N     |  N   |       | 子账号  |
|  4   | trade_mem_code |   varchar   | 32 |   0    |    Y     |  N   |       | 交易会员代码  |
|  5   | org_id |   varchar   | 36 |   0    |    N     |  N   |       | 机构id  |
|  6   | org_name |   varchar   | 100 |   0    |    N     |  N   |       | 机构名称  |
|  7   | other_org_id |   varchar   | 36 |   0    |    N     |  N   |       | 对方机构id  |
|  8   | other_sub_account |   varchar   | 20 |   0    |    Y     |  N   |       | 对方子账号  |
|  9   | other_org_name |   varchar   | 100 |   0    |    N     |  N   |       | 对方机构名称  |
|  10   | biz_code |   varchar   | 20 |   0    |    N     |  N   |       | 单据类型代码ORDER,REFUND  |
|  11   | biz_name |   varchar   | 30 |   0    |    N     |  N   |       | 单据类型名称采购订单,退货单  |
|  12   | trade_account |   decimal   | 20 |   2    |    Y     |  N   |       | 交易金额  |
|  13   | sub_account_money |   decimal   | 20 |   2    |    Y     |  N   |       | 账户余额  |
|  14   | trade_currency |   varchar   | 6 |   0    |    Y     |  N   |   CNY    | 交易币种  |
|  15   | trade_abstract |   varchar   | 100 |   0    |    Y     |  N   |       | 交易摘要  |
|  16   | pay_payee_sign |   varchar   | 2 |   0    |    N     |  N   |       | 收付款标志0-付款1-收款  |
|  17   | creator_id |   varchar   | 36 |   0    |    Y     |  N   |       | 创建人id  |
|  18   | creator_name |   varchar   | 255 |   0    |    Y     |  N   |       | 创建人姓名  |
|  19   | create_date |   datetime   | 19 |   0    |    N     |  N   |       | 创建时间  |
|  20   | remark |   varchar   | 200 |   0    |    Y     |  N   |       | 备注  |
|  21   | biz_doc_no |   varchar   | 36 |   0    |    Y     |  N   |       | 业务单据号  |
|  22   | unfreeze_pay_code |   varchar   | 32 |   0    |    Y     |  N   |       | 解冻交易单号  |
|  23   | unfreeze_money |   decimal   | 20 |   2    |    Y     |  N   |       | 解冻金额  |
|  24   | system_source |   int   | 10 |   0    |    N     |  N   |   0    | 数据来源：0-PMS1-商城  |
####  <a id="tb_vote_info">tb_vote_info</a>

**说明：** 订单评价信息表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | supplier_id |   varchar   | 36 |   0    |    Y     |  N   |       | 供应商id  |
|  3   | supplier_name |   varchar   | 100 |   0    |    Y     |  N   |       | 供应商名称  |
|  4   | procurer_id |   varchar   | 36 |   0    |    Y     |  N   |       | 采购方id  |
|  5   | procurer_name |   varchar   | 100 |   0    |    Y     |  N   |       | 采购方名称  |
|  6   | order_doc_no |   varchar   | 20 |   0    |    Y     |  N   |       | 订单编号  |
|  7   | eval_type_1 |   int   | 10 |   0    |    Y     |  N   |       | 总体满意度  |
|  8   | eval_type_2 |   int   | 10 |   0    |    Y     |  N   |       | 订单响应速度  |
|  9   | eval_type_3 |   int   | 10 |   0    |    Y     |  N   |       | 发货速度  |
|  10   | eval_type_4 |   int   | 10 |   0    |    Y     |  N   |       | 物流服务  |
|  11   | eval_type_5 |   int   | 10 |   0    |    Y     |  N   |       | 配送质量  |
|  12   | eval_type_6 |   int   | 10 |   0    |    Y     |  N   |       | 问题处置有效性  |
|  13   | eval_avg |   decimal   | 10 |   2    |    Y     |  N   |       | 历史分值(平均分)  |
|  14   | eval_text |   varchar   | 600 |   0    |    Y     |  N   |       | 评价信息  |
|  15   | eval_text_other |   varchar   | 600 |   0    |    Y     |  N   |       | 追加评价信息  |
|  16   | img_url |   varchar   | 600 |   0    |    Y     |  N   |       | 评价图片名称(图片文件路径)  |
|  17   | eval_time |   datetime   | 19 |   0    |    Y     |  N   |       | 评价时间  |
|  18   | status |   int   | 10 |   0    |    Y     |  N   |   0    | 是否已追加评价0-未追加1-已追加默认0  |
|  19   | total_price |   decimal   | 10 |   2    |    Y     |  N   |       | 订单金额  |
####  <a id="temp_new_orgid">temp_new_orgid</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | name |   varchar   | 100 |   0    |    N     |  N   |       | 名称  |
|  3   | new_id |   bigint   | 19 |   0    |    Y     |  N   |       |   |
####  <a id="temp_new_orgid_enter">temp_new_orgid_enter</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | name |   varchar   | 100 |   0    |    N     |  N   |       | 名称  |
|  3   | new_id |   bigint   | 19 |   0    |    Y     |  N   |       |   |
####  <a id="temp_new_userid">temp_new_userid</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | 主键id  |
|  2   | user_code |   varchar   | 100 |   0    |    N     |  N   |       | 用户编码  |
|  3   | user_name |   varchar   | 100 |   0    |    N     |  N   |       | 姓名  |
|  4   | new_id |   bigint   | 19 |   0    |    Y     |  N   |       |   |
####  <a id="tem_ckmsg">tem_ckmsg</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | msg |   text   | 65535 |   0    |    Y     |  N   |       |   |
####  <a id="tmp">tmp</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    Y     |  N   |       |   |
|  2   | sort |   varchar   | 20 |   0    |    Y     |  N   |       |   |
####  <a id="tmp_fix_subaccount">tmp_fix_subaccount</a>

**说明：** 子账号补充记录(手动补充子账号用)

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | login_name |   varchar   | 100 |   0    |    N     |  Y   |       |   |
|  2   | org_id |   varchar   | 40 |   0    |    Y     |  N   |       |   |
|  3   | org_name |   varchar   | 100 |   0    |    Y     |  N   |       |   |
|  4   | fixed |   int   | 10 |   0    |    Y     |  N   |   0    | 0否1是  |
####  <a id="t_tmp_goods">t_tmp_goods</a>

**说明：** 商品(开发用)

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   bigint   | 19 |   0    |    N     |  Y   |       |   |
|  2   | descript |   varchar   | 255 |   0    |    Y     |  N   |       | 产品简介  |
|  3   | detail |   text   | 65535 |   0    |    Y     |  N   |       | 产品详情  |
|  4   | gallery |   varchar   | 512 |   0    |    Y     |  N   |       | 大图相册列表,以逗号分隔  |
|  5   | id_category |   bigint   | 19 |   0    |    Y     |  N   |       | 类别id  |
|  6   | is_delete |   tinyint   | 3 |   0    |    Y     |  N   |       | 是否删除  |
|  7   | is_hot |   tinyint   | 3 |   0    |    Y     |  N   |       | 是否人气商品  |
|  8   | is_new |   tinyint   | 3 |   0    |    Y     |  N   |       | 是否新品推荐  |
|  9   | is_on_sale |   tinyint   | 3 |   0    |    Y     |  N   |       | 是否上架  |
|  10   | like_num |   int   | 10 |   0    |    Y     |  N   |       | 收藏数  |
|  11   | name |   varchar   | 32 |   0    |    Y     |  N   |       | 名称  |
|  12   | pic |   varchar   | 64 |   0    |    Y     |  N   |       | 小图  |
|  13   | price |   varchar   | 16 |   0    |    Y     |  N   |       | 价格  |
|  14   | stock |   int   | 10 |   0    |    Y     |  N   |       | 库存数量  |
|  15   | del_flag |   int   | 10 |   0    |    N     |  N   |   0    | 删除标记  |
|  16   | useable |   int   | 10 |   0    |    N     |  N   |   1    | 是否启用  |
|  17   | creator_id |   varchar   | 36 |   0    |    N     |  N   |       | 创建者  |
|  18   | creator_name |   varchar   | 255 |   0    |    N     |  N   |       | 创建者姓名  |
|  19   | create_date |   datetime   | 19 |   0    |    N     |  N   |   CURRENT_TIMESTAMP    | 创建时间  |
|  20   | updater_id |   varchar   | 36 |   0    |    N     |  N   |       | 更新者  |
|  21   | updater_name |   varchar   | 255 |   0    |    N     |  N   |       | 更新者姓名  |
|  22   | update_date |   datetime   | 19 |   0    |    N     |  N   |   CURRENT_TIMESTAMP    | 更新时间  |
####  <a id="参展企业报名表">参展企业报名表</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | 参展企业名称 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  2   | 参展企业英文名称 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  3   | 省 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  4   | 市 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  5   | 联系地址 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  6   | 邮编 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  7   | 若属于集团子公司，请注明集团母公司名称 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  8   | 展会联系人 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  9   | 展会联系人部门 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  10   | 展会联系人职务 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  11   | 展会联系人电话 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  12   | 展会联系人传真 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  13   | 展会联系人QQ |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  14   | 展会联系人手机 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  15   | 展会联系人邮箱 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  16   | 展会联系人微信号 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  17   | 光地特装一类光地650元/平米 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  18   | 光地特装二类光地550元/平米 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  19   | 标准展位一类6800元/个 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  20   | 标准展位二类5800元/个 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  21   | 如需要进行“标改特”，请勾选 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  22   | 如有意预订转角位，请勾选此项。标准展位转角位置（两面开展位）加收原价格的20%，0-不选，1-选中 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  23   | 展位申请备注 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  24   | 发票抬头 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  25   | 税号 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  26   | 开票地址 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  27   | 开票电话号码 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  28   | 开户行 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  29   | 银行账号 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
####  <a id="处理数据字典_补充没有的剂型">处理数据字典_补充没有的剂型</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  2   | *剂型 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  3   | dict_code |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  4   | sort |   varchar   | 255 |   0    |    Y     |  N   |       |   |
####  <a id="处理数据字典_补充没有的包装单位">处理数据字典_补充没有的包装单位</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  2   | *包装单位 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  3   | dict_code |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  4   | sort |   varchar   | 255 |   0    |    Y     |  N   |       |   |
####  <a id="处理数据字典_补充没有的质量类型">处理数据字典_补充没有的质量类型</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  2   | 质量类型 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  3   | dict_code |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  4   | sort |   varchar   | 255 |   0    |    Y     |  N   |       |   |
####  <a id="处理湖北省数据临时文档_竞价组">处理湖北省数据临时文档_竞价组</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | UUID |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  2   | *剂型 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  3   | 竞价组编码 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  4   | *包装单位 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  5   | *通用名称（中文） |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  6   | *规格 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
####  <a id="处理生产厂家_准备插入到org表">处理生产厂家_准备插入到org表</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 36 |   0    |    Y     |  N   |       |   |
|  2   | manufacture_name |   varchar   | 100 |   0    |    N     |  N   |       | 生产厂家中文名  |
####  <a id="处理目录编码使用的数据表">处理目录编码使用的数据表</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  2   | 目录编码 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  3   | 目录名称 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  4   | 备注 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
####  <a id="处理目录编码使用的数据表94">处理目录编码使用的数据表94</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  2   | 目录编码 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  3   | 目录名称 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  4   | 备注 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
####  <a id="处理竞价组基准品的数据表">处理竞价组基准品的数据表</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | prod_id |   varchar   | 255 |   0    |    Y     |  N   |       |   |
####  <a id="处理进口代理_准备插入到org表">处理进口代理_准备插入到org表</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | prod_id |   varchar   | 36 |   0    |    N     |  N   |       | 主键id  |
|  2   | id |   varchar   | 36 |   0    |    Y     |  N   |       |   |
|  3   | manufacture_name |   varchar   | 100 |   0    |    N     |  N   |       | 生产厂家中文名  |
|  4   | apply_org_name |   varchar   | 500 |   0    |    Y     |  N   |       | 申报企业名称  |
####  <a id="媒体登记信息">媒体登记信息</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | 媒体名称 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  2   | 联系人网站 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  3   | 联系地址 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  4   | 邮编 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  5   | 联系人 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  6   | 联系人职务 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  7   | 联系人电话 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  8   | 联系人手机 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  9   | 联系人邮箱 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  10   | 参会代表姓名 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  11   | 参会代表职务 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  12   | 参会代表电话 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  13   | 关注领域 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  14   | 关注论坛 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
####  <a id="建湖北用户">建湖北用户</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | user_id |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  2   | user_code |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  3   | user_name |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  4   | org_id |   varchar   | 255 |   0    |    Y     |  N   |       |   |
####  <a id="武汉">武汉</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | *角色 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  2   | *机构类型 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  3   | *机构名称 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  4   | 机构用户登录账号 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  5   | 机构id |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  6   | 机构等级 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  7   | *法定代表人 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  8   | *联系人 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  9   | *手机号 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  10   | 所属行政区划 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  11   | *所属地区-省 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  12   | *所属地区-市 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  13   | *所属地区-县 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  14   | *详细地址 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  15   | F15 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  16   | F16 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  17   | F17 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
####  <a id="湖北药品_整理准备导入product">湖北药品_整理准备导入product</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | prod_id |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  2   | 产品流水号 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  3   | group_id |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  4   | 竞价组号 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  5   | *通用名称（中文） |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  6   | 通用名称（英文） |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  7   | *商品名称 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  8   | *剂型 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  9   | *规格 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  10   | *包装单位 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  11   | *生产厂家 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  12   | *批准文号 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  13   | prod_biz_code |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  14   | *药品类别 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  15   | directory_id |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  16   | directory_code |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  17   | 转换系数 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  18   | 药理/功效 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  19   | *是否医保 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  20   | 大包装数量 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  21   | 中包装数量 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  22   | 最小制剂单位 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  23   | 酸根盐基 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  24   | 质量类型 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  25   | 实际质量类型 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  26   | 基药属性 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  27   | 投标企业 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  28   | 包装中标价 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  29   | 是否省标 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
####  <a id="湖北药品_整理准备导入tb_bas_product_group">湖北药品_整理准备导入tb_bas_product_group</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | prod_id |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  2   | 产品流水号 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  3   | group_id |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  4   | 竞价组号 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  5   | *通用名称（中文） |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  6   | 通用名称（英文） |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  7   | *商品名称 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  8   | *剂型 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  9   | *规格 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  10   | *包装单位 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  11   | *生产厂家 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  12   | *批准文号 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  13   | prod_biz_code |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  14   | *药品类别 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  15   | directory_id |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  16   | directory_code |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  17   | 转换系数 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  18   | 药理/功效 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  19   | *是否医保 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  20   | 大包装数量 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  21   | 中包装数量 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  22   | 最小制剂单位 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  23   | 酸根盐基 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  24   | 质量类型 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  25   | 实际质量类型 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  26   | 基药属性 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  27   | 投标企业 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  28   | 包装中标价 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  29   | 是否省标 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
####  <a id="药品基本数据库（3.0版）">药品基本数据库（3.0版）</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | 数据标志 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  2   | ypid |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  3   | 产品名称 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  4   | 药品类别 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  5   | 药品类别代码 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  6   | 药理/功效分类 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  7   | 药理/功效分类码 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  8   | 通用名（中文） |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  9   | 通用名（英文） |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  10   | 通用名代码 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  11   | 酸根盐基 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  12   | 酸根盐基分类码 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  13   | 剂型分类名称 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  14   | 剂型分类码 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  15   | 规格 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  16   | 制剂规格分类码 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  17   | 企业名称 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  18   | 企业编码 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  19   | 批准文号 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  20   | 转换系数 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  21   | 转换系数编码 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  22   | 顺序码 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  23   | 顺序码备注 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  24   | 材质 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  25   | 最小包装单位 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  26   | 最小制剂单位 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  27   | 进口专利药 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  28   | 原研药 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  29   | 低价药 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  30   | 定点生产药品 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  31   | 妇产科用药 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  32   | 儿科用药 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  33   | 急抢救用药 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  34   | 血液制品 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  35   | 医保中成药 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  36   | 理论09基药 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  37   | 基药序号09 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  38   | 理论12基药 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  39   | 基药序号12 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  40   | 12基药分类名 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  41   | 同种药品（通用名+酸根盐基）企业数 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  42   | 同通用名同剂型的企业数 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  43   | 企业名称变更记录 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  44   | 企业编码变更记录 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  45   | 属性修改备注 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  46   | 原YPID（2.0版） |   varchar   | 255 |   0    |    Y     |  N   |       |   |
####  <a id="药品挂网目录导出1">药品挂网目录导出1</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | 流水号 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  2   | 通用名 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  3   | 剂型 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  4   | 规格 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  5   | 包装 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  6   | 质量类型 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  7   | 新版基药属性 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  8   | 新版基药编码 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  9   | 生产企业注册号 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  10   | 生产企业名称 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  11   | 申报企业注册号 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  12   | 申报企业名称 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  13   | 挂网价中标价 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  14   | 挂网类型 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  15   | 状态 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  16   | 范围 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
####  <a id="药品数据源">药品数据源</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | prod_id |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  2   | 产品流水号 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  3   | group_id |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  4   | 竞价组号 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  5   | *通用名称（中文） |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  6   | 通用名称（英文） |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  7   | *商品名称 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  8   | *剂型 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  9   | *规格 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  10   | *包装单位 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  11   | *生产厂家 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  12   | *批准文号 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  13   | prod_biz_code |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  14   | *药品类别 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  15   | directory_id |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  16   | directory_code |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  17   | 转换系数 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  18   | 药理/功效 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  19   | *是否医保 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  20   | 大包装数量 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  21   | 中包装数量 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  22   | 最小制剂单位 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  23   | 酸根盐基 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  24   | 质量类型 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  25   | 实际质量类型 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  26   | 基药属性 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  27   | 投标企业 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  28   | 包装中标价 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  29   | 是否省标 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
####  <a id="观众报名表">观众报名表</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | 观众姓名 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  2   | 单位名称 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  3   | 观众职务 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  4   | 观众类别 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  5   | 联系人电话 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  6   | 邮箱 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  7   | 关注领域 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
|  8   | 关注论坛 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
####  <a id="论坛名">论坛名</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | 论坛名称 |   varchar   | 255 |   0    |    Y     |  N   |       |   |
