# 快速入门

基础数据主要提供服务集成，使用基础数据提供sdk访问，主要提供两个sdk包：  
组织iuap-org-sdk 及 基础数据iuap-basedoc-sdk   
使用时，需要先在开发者中心申请accesskey，配置到使用基础数据的服务目录下（具体请参考开发者中心的使用说明）

具体服务使用，请参考基础数据及组织的sdk说明文档

代码示例如下：

`	// 构造环境变量参数，用户、租户、应用编码
BdRestParam param = new BdRestParam();
	param.setTenantId(InvocationInfoProxy.getTenantId());
	param.setSysId(InvocationInfoProxy.getSysId());
	param.setUserId(InvocationInfoProxy.getUserid());
	// 获取服务接口
	LocationService service = BdRestSingleton.getInst(param).getBdRestService()
.getLocationService();
	// 调用服务方法
	LocationDTO dto = service.getById(id);
`

