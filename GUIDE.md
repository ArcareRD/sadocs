

| 功能| Table Name| Table Name| 
| :-------------: | :-------------: | :-------------: |
| 1.認證與授權| [aspnet_Applications](#aspnet) | 認證與授權-應用程式資料| 
| 2.認證與授權| [aspnet_Users](#aspnet_Users)| 使用者| 
| 3.認證與授權| [#point3 aspnet_Membership]| 成員| 
| 4.認證與授權| [#point4 aspnet_Profile]| 使用者其他屬性| 
| 5.認證與授權| [#point5 aspnet_Roles]| 角色| 
| 6.認證與授權| [#point6 aspnet_SchemaVersions]| Schema Version| 
| 7.認證與授權| [#point7 aspnet_UsersInRoles]| 使用者與角色關係| 
| 8.認證與授權| [#point8 AA_UsersInProject]| 使用者與專案關係| 
| 9.認證與授權| [#point9 AA_RolePrincipal]| 角色權限| 
| 10.認證與授權| [#point10 AA_Function]| 功能清單| 
| 11.認證與授權| [#point11 AA_FunctionURL]| 功能與URL對照| 
| 12.認證與授權| [#point12 AA_UseLog]| 使用記錄| 
| 13.認證與授權| [#point13 AA_Invite]| 專案邀請| 
| 14.認證與授權| [#point14 AA_UserProfile]| 使用者其它資訊| 

<h2 id="aspnet"> aspnet_Applications : 應用程式資料 </h2>

| primary key| index| column name| description| datatype| length| allow null| example| note| 
| :-------------: | :-------------: | :-------------: | :-------------: | :-------------: | :-------------: |:-------------: | :-------------: | :-------------:| 
|  |  | !ApplicationName| 應用程式名稱| nvarchar| 256|  |  |  | 
|  |  | !LoweredApplicationName| 小寫應用程式名稱| nvarchar| 256|  |  |  | 
|  ◎| ◎| !ApplicationId| 應用程式ID| uniqueidentifier|  |  |  |  | 
|  |  | Description| 應用程式說明| nvarchar| 256| ◎|  |  | 



<h2 id="aspnet_Users"> aspnet_Users : 應用程式資料 </h2>

| primary key| index| column name| description| datatype| length|allow null| example| note| 
| :-------------: | :-------------: | :-------------: | :-------------: | :-------------: | :-------------: |:-------------: | :-------------: | :-------------:| 
|  |  | ApplicationId| 應用程式ID| uniqueidentifier|  |  |  |  | 
|  ◎| ◎| UserId| 使用者ID| uniqueidentifier|  |  |  |  | 
|  |  | UserName| 使用者帳號| nvarchar| 256|  |  |  | 
|  |  | LoweredUserName| 小寫的使用者帳號| nvarcha| 256|  |  |  | 
|  |  | MobileAlias| 行動電話| nvarchar| 16| ◎ |  |  | 
|  |  | IsAnonymous| 是否為匿名用戶| bit|  |  |  |  | 
|  |  | LastActivityDate| 最後活動日期| datetime|  |  |  |  | 