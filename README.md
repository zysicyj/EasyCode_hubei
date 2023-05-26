## 干什么的
配合优化的项目架构，能够自动生成基础CURUD，实现10秒钟开发新业务接口

## 网址
https://brucege.com/doc/#/generateByTemplate

## 自动生成以下类，还有一个xml没截取到
![image](https://github.com/zysicyj/EasyCode_hubei/assets/64080867/b730d785-bbf2-4ef6-9a3f-b5aaccb981a6)

## 生成的controller
```java
package com.nari.supervision.daily.outbound.controller;

import com.nari.core.basic.BasicController;
import com.nari.supervision.daily.outbound.model.IdLibraryChecklist;
import com.nari.supervision.daily.outbound.param.IdLibraryChecklistParam;
import com.nari.supervision.daily.outbound.view.IdLibraryChecklistView;
import com.nari.supervision.daily.outbound.transform.IdLibraryChecklistTransform;
import com.nari.supervision.daily.outbound.dto.IdLibraryChecklistDto;
import com.nari.supervision.daily.outbound.service.IdLibraryChecklistService;
import org.springframework.web.bind.annotation.*;
import org.springframework.stereotype.Controller;
import lombok.extern.slf4j.Slf4j;

import javax.annotation.Resource;
import javax.validation.Valid;

/**
 * 证照清单-路由管理
 *
 * @author <a href="mailto:17602556550@189.cn"> 朱永胜 </a>
 * @version 1.0.0
 * @since 2023-05-26 17:08:30
 */
@Controller
@Valid
@Slf4j
@RequestMapping("idLibraryChecklist")
public class IdLibraryChecklistController extends BasicController<IdLibraryChecklist, IdLibraryChecklistParam, IdLibraryChecklistView, IdLibraryChecklistDto, IdLibraryChecklistTransform> {

}
```

## 生成的mapper
```java
package com.nari.supervision.daily.outbound.mapper;

import java.io.Serializable;
import java.util.List;

import lombok.Data;
import io.swagger.annotations.ApiModel;

import com.nari.supervision.daily.outbound.model.IdLibraryChecklist;
import com.nari.supervision.daily.outbound.param.IdLibraryChecklistParam;
import com.nari.supervision.daily.outbound.dto.IdLibraryChecklistDto;
import com.nari.core.basic.BasicDao;
import com.nari.core.web.PageParam;
import org.apache.ibatis.annotations.Mapper;
import org.apache.ibatis.annotations.Param;

/**
 * 证照清单-SQL处理
 *
 * @author <a href="mailto:17602556550@189.cn"> 朱永胜 </a>
 * @version 1.0.0
 * @since 2023-05-26 17:08:31
 */
@Mapper
public interface IdLibraryChecklistMapper extends BasicDao<IdLibraryChecklist, IdLibraryChecklistDto, IdLibraryChecklistParam> {
    List<IdLibraryChecklistDto> selectPageRel(@Param("page") PageParam<IdLibraryChecklistDto, IdLibraryChecklistParam> page, @Param("param") IdLibraryChecklistParam param);
}

```
## 如何使用
### 一、将项目拷贝到该位置
![image](https://github.com/zysicyj/EasyCode_hubei/assets/64080867/4ea2b22d-414e-4bf6-9236-0a6468cacf6e)

我们需要使用的是第三个模板

![image](https://github.com/zysicyj/EasyCode_hubei/assets/64080867/2c89ad74-2e9c-4f53-aa57-0f9e70f09d96)

### 二、安装插件

![image](https://github.com/zysicyj/EasyCode_hubei/assets/64080867/2fc5d35f-b20b-45c8-b4ed-87508b866e26)

### 三、右键表，按照图示点击

>  如果你的idea没有配置db，请自行百度配置下


![image](https://github.com/zysicyj/EasyCode_hubei/assets/64080867/14f8dab8-8520-4965-903d-a57e9c2b8dcb)

### 四、按照图示勾选即可

![image](https://github.com/zysicyj/EasyCode_hubei/assets/64080867/020af128-fded-441f-a5fa-e58b683cdced)

