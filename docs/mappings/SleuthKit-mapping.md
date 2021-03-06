---
title: SleuthKit CASE UCO mapping
---

# SleuthKit CASE UCO mapping


## Concept mappings

|Sleuthkit|CASE/UCO|
|:---|:---|
|object|Trace|
|parent object|separate Trace with a "contained-within" relationship to it|
|image|Trace with various (Image, File, ContentData, etc) property bundles|
|volume system|Trace with Volume (and possibly other) property bundles|
|partition|Trace with DiskPartition (and possibly other) property bundles|
|file system|Trace with FileSystem (and possibly other) property bundles|
|file|Trace with File (and possibly other (ContentData, ExtInode, MftRecord, ArchiveFile, FilePermissions, etc.) property bundles|
|file layout|Trace for the file as described above; separate Trace with ContentData for each byte run; separate "contained-within" Relationship between fragment and file with DataRange property bundle for each byte run; separate "has-fragment" Relationship between file and fragment with Fragment property bundle for each byte run|
|derived files method|ForensicAction with associated 'instrument' property reference to a Tool object|
|artifact|property bundle on Trace|
|attribute|property|

### Table mappings

|Sleuthkit|CASE/UCO Class|CASE/UCO Property|
|---|---|---|
|object|Trace||
||||
||||
||||
||||
||||
||||
||||
||||
||||
||||
||||
||||
||||
||||

### Artifact mappings

|Sleuthkit|CASE/UCO Class|CASE/UCO Property|
|---|---|---|
|object|Trace||
|[TSK_ACCOUNT](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#a66b7b612ba9d7b304074905a3479ee93)|uco-observable.Account||
|[TSK_BLUETOOTH_PAIRING](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#add0e259a8548babc6a2f525d68fcc4ca)|??? Action?||
|[TSK_CALENDAR_ENTRY](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#aac28ace3211b50e4408e2058888158a9)|uco-observable.CalendarEntry||
|[TSK_CALLLOG](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#a84e358dfcaae582823c3cee135c911b3)|uco-observable.PhoneCall||
|[TSK_CONTACT](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#aea0e0516195152f6f068bf11d4af634b)|uco-observable.Contact||
|[TSK_DEVICE_ATTACHED](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#a9ffe9c7886be6f1f08cf65455f83e2a6)|??? Action?||
|[TSK_EMAIL_MSG](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#a574ebff042ff47260370ed5bf1566626)|uco-observable.EmailMessage||
|[TSK_ENCRYPTION_DETECTED](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#a91446cd75f55eb2204cd260833206d77)|??? Action?||
|[TSK_EXT_MISMATCH_DETECTED](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#af21a3a4ce21ecc4af6fcfb4c42b752ab)|??? Action?||
|[TSK_EXTRACTED_TEXT](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#aa6fdaa63c52fa701856ca6e4e374dd41)|uco-observable.ExtractedStrings||
|[TSK_FACE_DETECTED](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#ac410e94f1fa24831c25f01041215f522)|??? Action?||
|[TSK_GEN_INFO](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#a6a76676c01d69684042d427ff72d2791)|||
|[TSK_GPS_BOOKMARK](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#a4d8b15af919dbaab6c682e763c1077cf)|uco-core.Location; uco-core.GPSCoordinates; uco-observable.GeoLocationEntry||
|[TSK_GPS_LAST_KNOWN_LOCATION](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#a1a4a217e7b412bdb0303635d9a67f07a)|uco-core.Location; uco-core.GPSCoordinates; uco-observable.GeoLocationEntry||
|[TSK_GPS_ROUTE](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#a9d3d6cde583f7657c8534534a16a406d)|uco-observable.GeoLocationTrack||
|[TSK_GPS_SEARCH](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#a7ac3269397e689b23248daa12432029e)|||
|[TSK_GPS_TRACKPOINT](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#a27eb28b36d703bd341491977e76638e7)|uco-core.Location; uco-core.GPSCoordinates; uco-observable.GeoLocationEntry||
|[TSK_HASHSET_HIT](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#afdffc461cb0b99335daf9cf47dda3b91)|||
|[TSK_INSTALLED_PROG](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#ab5f19c827d28e06bac558538636858a9)|??? Action?||
|[TSK_INTERESTING_ARTIFACT_HIT](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#a25776bfaa43b119d2b9f449da66caaa7)|??? Action?||
|[TSK_INTERESTING_FILE_HIT](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#a6cbb8c27f379ee2173342f07b3b5a492)|??? Action?||
|[TSK_KEYWORD_HIT](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#a87ff1c517ea3213acb07f913e7e367a9)|??? Action?||
|[TSK_MESSAGE](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#a728526007ef9164f265a0f07c51e4260)|uco-observable.Message||
|[TSK_METADATA_EXIF](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#af4bdda6f1d364733c419dc273f757d60)|uco-observable.EXIF||
|[TSK_OS_ACCOUNT](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#ac83b8c1f2d20aed50f60523a4c282e59)|uco-observable.Account; uco-observable.DigitalAccount; uco-observable.UserAccount||
|[TSK_OS_INFO](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#a5f4bc64fc9c96fc37ed72ca660236564)|uco-observable.OperatingSystem||
|[TSK_PROG_RUN](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#ae77b765e66c77ada24b7e79ce7960188)|??? Action?||
|[TSK_RECENT_OBJECT](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#abe83c8deff7d1700574d47bfda0d8162)|||
|[TSK_REMOTE_DRIVE](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#a42362a44a47dc2a92846901a82430a96)|||
|[TSK_SERVICE_ACCOUNT](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#a6e15196b34c158ce1ce0311f24072622)|uco-observable.Account; uco-observable.DigitalAccount; uco-observable.UserAccount; uco-observable.ApplicationAccount||
|[TSK_SPEED_DIAL_ENTRY](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#aa3853155596dc52dd4dfa64d7a044ad6)|||
|[TSK_TAG_ARTIFACT](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#af38aad406810bab7b51290d20545282c)|||
|[TSK_TAG_FILE](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#aeb091ebd0323735ca7802b383b174cff)|||
|[TSK_TOOL_OUTPUT](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#aa230eb281346af5f3d22727930874a22)|||
|[TSK_WEB_BOOKMARK](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#a6fd74f94b318f9e1492cb3d03c1c2de3)|uco-observable.BrowserBookmark||
|[TSK_WEB_COOKIE](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#a0cf2e4d60f026959a88d824eb9599356)|uco-observable.BrowserCookie||
|[TSK_WEB_DOWNLOAD](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#aa069d5c924b3ea35aaab61c227830a1d)|||
|[TSK_WEB_HISTORY](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#a53e88535edccf5503cbca43e9a120f39)|||
|[TSK_WEB_SEARCH_QUERY](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_artifact_1_1_a_r_t_i_f_a_c_t___t_y_p_e.html#a83d93e705f4719063645e8f680a273c6)|||
|[]()|||
|[]()|||
|[]()|||
||||


### Attribute mappings

|Sleuthkit|CASE/UCO Class|CASE/UCO Property|
|---|---|---|
|object|Trace||
|[TSK_ACCOUNT_TYPE](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#aa30cd4483ca33be63d706907cca27aee)|uco-observable.Account|uco-observable.Account.accountType|
|[TSK_ASSOCIATED_ARTIFACT](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#ace4e201803d59c740001177e653917fe)|uco-core.Relationship|uco-core.Relationship.target|
|[TSK_BANK_NAME](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#aa8f4548a63da45a15211fa4207e7d32a)|uco-observable.Account; uco-core.Identity|uco-observable.Account.accountIssuer; uco-core.Identity.name|
|[TSK_BRAND_NAME](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#ae65593bdbd9c0135a8c1644d9385d428)|||
|[TSK_CALENDAR_ENTRY_TYPE](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#aa0f7f4240f2206a21a3a972d4956f087)|uco-observable.CalendarEntry|uco-observable.CalendarEntry.eventType ??|
|[TSK_CARD_DISCRETIONARY](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a440f0e51aca2e7b71a919a787f1e04b7)|N/A (Gap)||
|[TSK_CARD_EXPIRATION](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a8de19e364f7ed8feace8ae4b82128a13)|uco-observable.Account|uco-observable.Account.expirationTime|
|[TSK_CARD_LRC](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a0f888c41618dbed0913968a05a8220ac)|N/A (Gap)||
|[TSK_CARD_NUMBER](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a44726ea3f62ffd384ed42e071f0c8732)|uco-observable.Account|uco-observable.Account.accountIdentifier|
|[TSK_CARD_SCHEME](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a59806b158e062bbd13188adc0534ee4f)|N/A (Gap)||
|[TSK_CARD_SERVICE_CODE](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a780404f49e4c574f2f2c37867e44c45f)|N/A (Gap)||
|[TSK_CARD_TYPE](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a6a4200a8fb9e074225c93f7540ac5378)|N/A (Gap)||
|[TSK_CATEGORY](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#aecfcaa5ab662a3dc859d9e4d0d93fded)|||
|[TSK_CITY](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a0ac5b798a2e32d6e050c1847f1290384)|uco-core.SimpleAddress|uco-core.SimpleAddress.locality|
|[TSK_COMMENT](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a04c344dd20c3ae539b6af9f1d692ae55)|uco-core.UcoObject OR uco-core.Annotation|uco-core.UcoObject.description OR uco-core.Annotation.statement|
|[TSK_COUNT](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a216f52251617b4714ce08a0fc08d8815)|||
|[TSK_COUNTRY](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a340c54a00c662fcffc83917d3215dbbf)|uco-core.SimpleAddress|uco-core.SimpleAddress.country|
|[TSK_DATETIME](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#ae4dd8ea71406a07bbdb0997da5cab410)|||
|[TSK_DATETIME_ACCESSED](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a301867cf25db4b56c30f4ac1183e2be9)|uco-observable.File|uco-observable.File.accessedTime|
|[TSK_DATETIME_CREATED](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#af775d5c07c8eeac229ed345aa332e3bb)|uco-observable.File|uco-observable.File.createdTime|
|[TSK_DATETIME_END](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a1563835f74d4f914234eb9a207a65a4b)||endTime|
|[TSK_DATETIME_MODIFIED](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#ac3a78136c91230cb76c26792190f4d17)|uco-observable.File|uco-observable.File.modifiedTime|
|[TSK_DATETIME_RCVD](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a22eb014fa6821d7cd472e60262c4b586)|||
|[TSK_DATETIME_SENT](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a410f42053688ae2c5c3d6fcb1c479dfc)|uco-observable.Message|uco-observable.Message.sentTime|
|[TSK_DATETIME_START](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#ab417cf245ec0a7fea5224e81fc5fa90e)||startTime|
|[TSK_DESCRIPTION](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a66fcb9c1ba67cb5cb8bfb85d476f10f9)|uco-core.UcoObject|uco-core.UcoObject.description|
|[TSK_DEVICE_ID](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a6cc361a87aeb3e803d4f3003e360de4c)|uco-core.UcoObject|uco-core.UcoObject.id|
|[TSK_DEVICE_MAKE](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a7ed88437b0aa37d74aa5bf6ba7bfdccf)|uco-observable.Device|uco-observable.Device.manufacturer|
|[TSK_DEVICE_MODEL](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a4523469ac8562adaf97d3d32de2f3687)|uco-observable.Device|uco-observable.Device.model|
|[TSK_DEVICE_NAME](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a01b226e60a17d4f6da9bbc05424e8a99)|uco-core.UcoObject|uco-core.UcoObject.name|
|[TSK_DIRECTION](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#af77f897ae64c07597add19090758934f)|||
|[TSK_DOMAIN](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a9a776b813050fa9c91abb178af4766f0)|uco-observable.DomainName|uco-observable.DomainName.value|
|[TSK_EMAIL](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#adfeb7a3790f68c41af875e1cb7eb4fd0)|uco-observable.EmailAddress|uco-observable.EmailAddress.value|
|[TSK_EMAIL_BCC](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a7124d4cac1ba0d0017aa288cb120543e)|uco-observable.EmailMessage|uco-observable.EmailMessage.bcc|
|[TSK_EMAIL_CC](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a3887825d482943a61452f630c0549314)|uco-observable.EmailMessage|uco-observable.EmailMessage.cc|
|[TSK_EMAIL_CONTENT_HTML](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a20a9a75b189139edce4d861f5e97ace0)|uco-observable.EmailMessage|uco-observable.EmailMessage.body OR uco-observable.EmailMessage.bodyRaw|
|[TSK_EMAIL_CONTENT_PLAIN](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a9b36cae21a231717bdd604f408df0493)|uco-observable.EmailMessage|uco-observable.EmailMessage.body OR uco-observable.EmailMessage.bodyRaw|
|[TSK_EMAIL_CONTENT_RTF](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a9f72a7772eee50320771255a521a71d7)|uco-observable.EmailMessage|uco-observable.EmailMessage.body OR uco-observable.EmailMessage.bodyRaw|
|[TSK_EMAIL_FROM](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a31e2583ef3a4e7e4ad1d0fc24ce86533)|uco-observable.EmailMessage|uco-observable.EmailMessage.from|
|[TSK_EMAIL_HOME](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#ae7d70246d6b89c42ab51c27b4a979901)|N/A (Gap)||
|[TSK_EMAIL_OFFICE](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#ab02bf742a98de296dbc7a9a18ae5e13a)|N/A (Gap)||
|[TSK_EMAIL_REPLYTO](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#af1f95197cd79d73cefc7120b74e538e8)|uco-observable.EmailMessage|uco-observable.EmailMessage.inReplyTo|
|[TSK_EMAIL_TO](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a722b1a7a0a24a2a7af141464e201a024)|uco-observable.EmailMessage|uco-observable.EmailMessage.to|
|[TSK_ENCRYPTION_DETECTED](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a4a6367b59a85c6fbac92ac54e61333f0)|uco-observable.ContentData|uco-observable.ContentData.isEncrypted|
|[TSK_ENTROPY](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#acfa96834828c94b4b45cdc74385061a0)|uco-observable.ContentData|uco-observable.ContentData.entropy|
|[TSK_FILE_TYPE_EXT](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a33f4282ce2ec35c90fc6aa615d9761d7)|uco-observable.File|uco-observable.File.extension|
|[TSK_FILE_TYPE_SIG](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a1a567844357cc70ec3619220088055bd)|uco-observable.ContentData|uco-observable.ContentData.magicNumber|
|[TSK_FLAG](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#af59a0aadf621169bb49c6a9f9cdb81c8)|||
|[TSK_GEO_ALTITUDE](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a3733a7bebe7f2ae0b1ebcd720a630c76)|uco-core.Location with uco-core.LatLongCoordinates|uco-core.LatLongCoordinates.altitude|
|[TSK_GEO_BEARING](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a5f8ec3f8d7f360e5532e47df92e9c8b7)|N/A (Gap)||
|[TSK_GEO_HPRECISION](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#ae4b7eb4b86925bf73ea0a3cce965d033)|uco-core.Location with uco-core.GPSCoordinates|uco-core.GPSCoordinates.hdop|
|[TSK_GEO_LATITUDE](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a3f1812e475a88d1490fbcb66c99f2e7f)|uco-core.Location with uco-core.LatLongCoordinates|uco-core.LatLongCoordinates.latitude|
|[TSK_GEO_LATITUDE_END](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a7c3895403c75d7d1d55d3ef00416d283)|N/A (Gap)||
|[TSK_GEO_LATITUDE_START](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a90f7836954fbf4f4cb32a758cdaaf249)|N/A (Gap)||
|[TSK_GEO_LONGITUDE](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a0edbb7f599efc1fc3fb5bd8e3710104f)|uco-core.Location with uco-core.LatLongCoordinates|uco-core.LatLongCoordinates.longitude|
|[TSK_GEO_LONGITUDE_END](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a6179ccda3a12263af8c65e7a7c234fec)|N/A (Gap)||
|[TSK_GEO_LONGITUDE_START](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#aa9cf2190c7612513e118315b2a878b87)|N/A (Gap)||
|[TSK_GEO_MAPDATUM](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a05c2c10d1167aada90734366b1448df4)|N/A (Gap)||
|[TSK_GEO_VELOCITY](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#afb6943417c1702404a79d48a66bb7b22)|N/A (Gap)||
|[TSK_GEO_VPRECISION](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a24564d10b8a8031d2acc3c895f9c2643)|uco-core.Location with uco-core.GPSCoordinates|uco-core.GPSCoordinates.vdop|
|[TSK_HASH_MD5](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#ace1b7340ba742057c5ece1f59c8e9da6)|uco-core.Hash|uco-core.Hash.hashMethod="MD5"; uco-core.Hash.hashValue|
|[TSK_HASH_SHA1](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#aaabcb32faea6cac4532ea0518c45818a)|uco-core.Hash|uco-core.Hash.hashMethod="SHA1"; uco-core.Hash.hashValue|
|[TSK_HASH_SHA2_256](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a4b1ca151f57fe884a0bb246cf0030303)|uco-core.Hash|uco-core.Hash.hashMethod="SHA256"; uco-core.Hash.hashValue|
|[TSK_HASH_SHA2_512](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#afef5b8cdf4ec7235f8326ffca2da73a3)|uco-core.Hash|uco-core.Hash.hashMethod="SHA512"; uco-core.Hash.hashValue|
|[TSK_HASHSET_NAME](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#ab5f25bdb24192d6c2ae52ce663fc1794)|||
|[TSK_INTERESTING_FILE](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a44cb6cbdf604844e5231e08c87395276)|||
|[TSK_IP_ADDRESS](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#ac2fbb21a6dd86db5a94b4de7da53419c)|uco-observable.IPv4Address|uco-observable.IPv4Address.value|
|[TSK_ISDELETED](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#af05c6b5817a69a589d7294d9cc222a6d)|||
|[TSK_KEYWORD](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a4e89ad53bbc8309fd889c142debfae57)|||
|[TSK_KEYWORD_PREVIEW](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a56b71163b518817a85928884b251e8aa)|||
|[TSK_KEYWORD_REGEXP](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a2ca6ddd28c0c1327c322f77213156e91)|||
|[TSK_KEYWORD_SEARCH_DOCUMENT_ID](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#af6a30d03473e7e20a51a5d140f26c601)|||
|[TSK_KEYWORD_SEARCH_TYPE](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a4b0e5c99d84953ee3ea1ac74b0ff58b8)|||
|[TSK_KEYWORD_SET](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a6e0174429e85b560b023aedb0a6995a9)|||
|[TSK_LOCAL_PATH](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#ab3540f68cdbc6bed16d1041ff1bfcc2b)|uco-observable.File (for objective location) OR uco-observable.PathRelation (for subjective containment)|uco-observable.File.filePath OR uco-observable.PathRelation.path|
|[TSK_LOCATION](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a43c037b7594dbe821958424645391795)|uco-core.Location with uco-core.LatLongCoordinates OR uco-core.GPSCoordinates OR uco-core.SimpleAddress||
|[TSK_MALWARE_DETECTED](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a1e9f28464480d263292178c3ff49ae56)|||
|[TSK_MESSAGE_TYPE](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#acb348c2679267e82e7f39845fe578591)|uco-observable.Message|uco-observable.Message.messageType|
|[TSK_MIN_COUNT](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#aba6f8dbf8154bfb4f966cfab0e14d290)|||
|[TSK_MSG_ID](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a4de945c0c1bf9bcd245468c669aec5df)|uco-observable.Message|uco-observable.Message.messageID|
|[TSK_MSG_REPLY_ID](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#ab200567ef8735185a79b7372841742ef)|||
|[TSK_NAME](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#ab8bfe8d615b549ac02788d2925248b89)|uco-core.UcoObject OR uco-core.Identity|uco-core.UcoObject.name OR uco-core.Identity.name|
|[TSK_NAME_PERSON](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#ae81ebf25eeac3e766d1309d8cfd41596)|uco-core.Person|uco-core.Person.name|
|[TSK_ORGANIZATION](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#abd7aca68a4d114f2ed29655b6ad667e9)|uco-core.Organization|uco-core.Organization.name|
|[TSK_OWNER](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a765b9a95c21798e2abde85fc5b254ca7)|||
|[TSK_PASSWORD](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a3fd9f1f0b680b85ce030c25abe5070b4)|||
|[TSK_PATH](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a5862e008b4f8c3f6aacda39e246a7c1d)|||
|[TSK_PATH_ID](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#ae93dda506b95e174143d2008b7aa9adf)|||
|[TSK_PATH_SOURCE](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a221f757acb75a703a2b41952893630b8)|||
|[TSK_PERMISSIONS](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#acf5d60772cacccdbd3d9b6239944dfbe)|||
|[TSK_PHONE_NUMBER](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a5365bd518816619b26141b25b4839d4c)|||
|[TSK_PHONE_NUMBER_FROM](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#ae3d9a30b82a73b1fdf217d969f68d990)|||
|[TSK_PHONE_NUMBER_HOME](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a5b52330e319167d8fd896562c6242f43)|N/A (Gap)||
|[TSK_PHONE_NUMBER_MOBILE](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#affac5c3ef868c90cfe8b0417738c806a)|N/A (Gap)||
|[TSK_PHONE_NUMBER_OFFICE](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a08bc2a29f06cbd62c1d5f98742e83dfc)|N/A (Gap)||
|[TSK_PHONE_NUMBER_TO](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a6159d8858dcdbac63a90989fa2fabb34)|||
|[TSK_PROCESSOR_ARCHITECTURE](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a87286e6d6e9d56569439a5232a3ea8d7)|||
|[TSK_PRODUCT_ID](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a89b262fc78af5f4ce94aae7a74cf0e32)|||
|[TSK_PROG_NAME](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a335b66eef9091f5e2e41ae5397370066)|||
|[TSK_READ_STATUS](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a868e9e88c35c2626a5b36839b2edddd8)|||
|[TSK_REFERRER](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#ab57fd079770b615d78615bcb103f13f3)|||
|[TSK_REMOTE_PATH](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#af66d47048b9ed8ee3222a331fd379825)|||
|[TSK_SERVER_NAME](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a555be41e5edc89aec1fc78d9ce323d05)|||
|[TSK_SET_NAME](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a896a65f7f474c7edb99257c5b9359644)|||
|[TSK_SHORTCUT](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a7758aa036cf4384beed607eb8f69be9d)|||
|[TSK_STEG_DETECTED](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#ab9b3b713f8671a7825013b5134799486)|||
|[TSK_SUBJECT](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#aeec65d4b231b7f5e5a9ee09282b2398b)|||
|[TSK_TAG_NAME](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a4809245e57a2769fdd42fe18d35b901b)|||
|[TSK_TAGGED_ARTIFACT](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#ab9b206796efefecaaf26929aaacbabd6)|||
|[TSK_TEMP_DIR](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a943368f6dbf14eea93fd9d6cca8f46f8)|||
|[TSK_TEXT](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a09bfbe263ab99714a32f022704b538a2)|||
|[TSK_TEXT_FILE](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#aa20ee0ce1e3068c5b7d1edf664bc2862)|||
|[TSK_TEXT_LANGUAGE](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a44a03629b1c01c1b70fea2c9cf328140)|||
|[TSK_TITLE](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a3d8177bbf59319c9710557a7e5ea3965)|||
|[TSK_URL](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#ad25804142531c6be839ba426b3e1c273)|||
|[TSK_URL_DECODED](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#ad783b5ad5883513d111f9c3e7d3f5dc4)|||
|[TSK_USER_ID](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#afdf417b5c32f73b041df627c3747eee8)|||
|[TSK_USER_NAME](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a116bd61fe6595867a4a8e9a613e3ad16)|||
|[TSK_VALUE](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#aeab9d3b462c742ef7cd6b0d742bf56d9)|||
|[TSK_VERSION](http://sleuthkit.org/sleuthkit/docs/jni-docs/4.3/enumorg_1_1sleuthkit_1_1datamodel_1_1_blackboard_attribute_1_1_a_t_t_r_i_b_u_t_e___t_y_p_e.html#a1bbcab7dbbb867d796c0bb794ac1ca5b)|||
||||
||||
||||
||||
