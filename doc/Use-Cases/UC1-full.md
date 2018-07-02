## UC1(full)：购票

* 范围：BronzeTiki购票系统

* 级别：用户级别

* 主要参与者：购票用户

* 涉众及其关注点：
	
	+ 购票用户：希望以最小代价完成购票活动并得到响应。希望清晰、直观地看到输入的需求详情。希望得到订票成功的确认凭证。

	+ 支付系统：希望接收到正确的授权请求。希望准确计算应付款。
	
* 前置条件：用户成功登录系统。

* 成功保证（或后置条件）：
	
	+ 存储销售信息

	+ 更新场次与座次信息

	+ 生成订单凭证
	
	+ 记录支付授权的批准

* 主成功场景（或基本流程）：

	1. 用户在首页影片选择正在上映的影片。

	2. 系统显示影片详情。

	3. 用户选定放映日期以及时间段。

	4. 系统显示剩余座次信息。

	5. 用户选择座次。

	6. 用户确认座次，系统显示本次订票的基本信息，并显示计算总额。

	7. 用户确认提交订单。

	8. 系统显示订单列表。

	9. 用户支付订单。

	10. 系统记录购票信息，更新用户信息和影片信息。

	11. 系统发送订单凭证给用户。

	12. 用户退出购票系统。

* 扩展（或替代流程）：

	\*a. 客户端与服务端无法正常连接或应答超时。

	1a. 首页“正在上映”影片信息显示失败。

		1. 建议用户尝试刷新页面或检查当前网络状况。	

	1b. 当前地点无正在上映的影片。

		1. 系统建议用户重新选择地点。

	2a. 影片详情信息获取失败。

		1. 系统建议用户尝试刷新页面或检查当前网络状况。

	3a. 影片可预订场次时间获取失败。

		1. 系统建议用户尝试刷新页面或检查当前网络状况。

	4a. 座次信息获取失败。

		1. 建议用户尝试刷新页面或检查当前网络状况。

	4b. 无剩余座次。

		1. 系统建议用户重新选择其他时间段或者日期。

		2. 用户请求座次剩余通知服务。

	5b. 用户选择座次数目超过上限。

		1. 系统限制用户在座位图选择新的座位并提示。

	5c. 当前剩余座次无法满足用户需求

		1. 用户重新选择影片/时间段。

	6a. 预订信息提交失败

		1. 系统建议用户重新尝试提交或检查当前网络状况。
	
	6b. 座次不足，订票信息生成失败。

		1. 系统更新座次信息，用户重新选择座次。

		2. 用户选择其他场次/时间段。

	7a. 订单确认信息提交失败。

		1. 系统建议用户尝试重新提交或检查当前网络状况。

	8a. 订单列表信息获取失败。

		1. 系统建议用户刷新页面或检查当前网络状况。

	9a. 支付验证信息提交失败

		1. 系统返回订单列表，建议用户重新尝试或检查网络状况。

	9b. 用户取消本次订单

		1. 系统更新用户订单记录以及影片座次信息

	9c. 用户在预订时间内未完成支付。

		1. 系统取消该订单，更新用户订单记录以及影片座次信息。

	9d. 用户余额不足，无法支付。

		1. 提示用户及时充值。

		2. 回到订单支付页面。
