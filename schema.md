# Schema Types

<details>
  <summary><strong>Table of Contents</strong></summary>

  * [Query](#query)
  * [Mutation](#mutation)
  * [Objects](#objects)
    * [Account](#account)
    * [AccountGroup](#accountgroup)
    * [AccountGroupPermission](#accountgrouppermission)
    * [AccountInvoice](#accountinvoice)
    * [AccountInvoiceLineItem](#accountinvoicelineitem)
    * [AccountIp](#accountip)
    * [AccountPaymentMethod](#accountpaymentmethod)
    * [AccountPlan](#accountplan)
    * [AccountPlanDiscount](#accountplandiscount)
    * [AccountPlanFeature](#accountplanfeature)
    * [AccountReceipt](#accountreceipt)
    * [AccountSetting](#accountsetting)
    * [Article](#article)
    * [ArticleContent](#articlecontent)
    * [BillingAddress](#billingaddress)
    * [CalculatedItem](#calculateditem)
    * [CalculatedPlanCost](#calculatedplancost)
    * [CampaignView](#campaignview)
    * [Category](#category)
    * [ChangePlanResult](#changeplanresult)
    * [Column](#column)
    * [Condition](#condition)
    * [ConditionGroup](#conditiongroup)
    * [DataField](#datafield)
    * [DataFieldLanguageLabel](#datafieldlanguagelabel)
    * [DataFieldValue](#datafieldvalue)
    * [Email](#email)
    * [Export](#export)
    * [File](#file)
    * [FileInfo](#fileinfo)
    * [FileView](#fileview)
    * [Folder](#folder)
    * [Form](#form)
    * [FormAnswer](#formanswer)
    * [FormDialog](#formdialog)
    * [FormEvent](#formevent)
    * [FormPage](#formpage)
    * [FormQuestion](#formquestion)
    * [FormQuestionAnswer](#formquestionanswer)
    * [FormResponse](#formresponse)
    * [Group](#group)
    * [Import](#import)
    * [Invite](#invite)
    * [List](#list)
    * [Notification](#notification)
    * [NotificationContent](#notificationcontent)
    * [Permission](#permission)
    * [ProfileField](#profilefield)
    * [ReactivationCosts](#reactivationcosts)
    * [SenderDomain](#senderdomain)
    * [ServicePlan](#serviceplan)
    * [ServicePlanCredit](#serviceplancredit)
    * [ServicePlanFeature](#serviceplanfeature)
    * [ServicePlanScale](#serviceplanscale)
    * [Subscriber](#subscriber)
    * [SubscriberConversation](#subscriberconversation)
    * [SubscriberEvent](#subscriberevent)
    * [SubscriberList](#subscriberlist)
    * [SubscriberListForm](#subscriberlistform)
    * [SubscriberListTag](#subscriberlisttag)
    * [SubscriberListView](#subscriberlistview)
    * [SubscriberNote](#subscribernote)
    * [Tag](#tag)
    * [Template](#template)
    * [TemplateCampaign](#templatecampaign)
    * [TemplateContent](#templatecontent)
    * [TemplateInformationViewModel](#templateinformationviewmodel)
    * [TemplateUsage](#templateusage)
    * [TemplateVersion](#templateversion)
    * [TemplateVersions](#templateversions)
    * [TemplateView](#templateview)
    * [TransactionResponse](#transactionresponse)
    * [User](#user)
    * [UserSetting](#usersetting)
    * [VerifyDomainResult](#verifydomainresult)
    * [Version](#version)
  * [Inputs](#inputs)
    * [AddBillingAddressInput](#addbillingaddressinput)
    * [AddCreditCardInfoInput](#addcreditcardinfoinput)
    * [AutoSaveArticleContentInput](#autosavearticlecontentinput)
    * [AutoSaveArticleInput](#autosavearticleinput)
    * [AutoSaveTemplateContentInput](#autosavetemplatecontentinput)
    * [AutoSaveTemplateInput](#autosavetemplateinput)
    * [CalculateAccountPlanCostInput](#calculateaccountplancostinput)
    * [ChangeAccountPlanInput](#changeaccountplaninput)
    * [ChangeSubscriberStatusInput](#changesubscriberstatusinput)
    * [ComparableDateTimeOperationFilterInput](#comparabledatetimeoperationfilterinput)
    * [ComparableDoubleOperationFilterInput](#comparabledoubleoperationfilterinput)
    * [ComparableInt32OperationFilterInput](#comparableint32operationfilterinput)
    * [ComparableInt64OperationFilterInput](#comparableint64operationfilterinput)
    * [ConditionGroupInput](#conditiongroupinput)
    * [ConditionInput](#conditioninput)
    * [CreateAccountGroupInput](#createaccountgroupinput)
    * [CreateAccountInput](#createaccountinput)
    * [CreateArticleContentInput](#createarticlecontentinput)
    * [CreateArticleInput](#createarticleinput)
    * [CreateCampaignViewInput](#createcampaignviewinput)
    * [CreateCategoryInput](#createcategoryinput)
    * [CreateDataFieldInput](#createdatafieldinput)
    * [CreateDataFieldLanguageLabelInput](#createdatafieldlanguagelabelinput)
    * [CreateDataFieldValueInput](#createdatafieldvalueinput)
    * [CreateExportInput](#createexportinput)
    * [CreateFileViewInput](#createfileviewinput)
    * [CreateFolderInput](#createfolderinput)
    * [CreateFormInput](#createforminput)
    * [CreateGroupInput](#creategroupinput)
    * [CreateGroupSubscriberInput](#creategroupsubscriberinput)
    * [CreateImportInput](#createimportinput)
    * [CreatePaymentMethodInput](#createpaymentmethodinput)
    * [CreateProfileFieldInput](#createprofilefieldinput)
    * [CreateQuestionCategoryInput](#createquestioncategoryinput)
    * [CreateQuestionInput](#createquestioninput)
    * [CreateSenderDomainInput](#createsenderdomaininput)
    * [CreateSubscriberConversationInput](#createsubscriberconversationinput)
    * [CreateSubscriberInput](#createsubscriberinput)
    * [CreateSubscriberListInput](#createsubscriberlistinput)
    * [CreateSubscriberListSecurityGroupInput](#createsubscriberlistsecuritygroupinput)
    * [CreateSubscriberListViewInput](#createsubscriberlistviewinput)
    * [CreateSubscriberNoteInput](#createsubscribernoteinput)
    * [CreateTagInput](#createtaginput)
    * [CreateTemplateInput](#createtemplateinput)
    * [CreateTemplateViewInput](#createtemplateviewinput)
    * [CreateTransactionInput](#createtransactioninput)
    * [CreateUrlFileInput](#createurlfileinput)
    * [CreateUserAccountGroupInput](#createuseraccountgroupinput)
    * [CreateUserInviteInput](#createuserinviteinput)
    * [DataColumnInput](#datacolumninput)
    * [DeleteCategoryInput](#deletecategoryinput)
    * [DeleteDataFieldInput](#deletedatafieldinput)
    * [DeleteFormInput](#deleteforminput)
    * [DeleteGroupInput](#deletegroupinput)
    * [DeleteSubscriberListSecurityGroupInput](#deletesubscriberlistsecuritygroupinput)
    * [DeleteSubscriberNoteInput](#deletesubscribernoteinput)
    * [DeleteTagInput](#deletetaginput)
    * [DeleteUserAccountGroupInput](#deleteuseraccountgroupinput)
    * [EmailFilterInput](#emailfilterinput)
    * [ExportFormInput](#exportforminput)
    * [GetAllFilesInput](#getallfilesinput)
    * [GetAllSubscriberListsInput](#getallsubscriberlistsinput)
    * [GetAllTemplatesInfoInput](#getalltemplatesinfoinput)
    * [GetAllTemplatesInput](#getalltemplatesinput)
    * [GetArticleContentInput](#getarticlecontentinput)
    * [GetExportInput](#getexportinput)
    * [GetQuestionInput](#getquestioninput)
    * [GetTemplateContentInput](#gettemplatecontentinput)
    * [GroupInput](#groupinput)
    * [GroupSubscriberInput](#groupsubscriberinput)
    * [InviteFilterInput](#invitefilterinput)
    * [InviteStatusOperationFilterInput](#invitestatusoperationfilterinput)
    * [ListFilterInputTypeOfServicePlanCreditItemFilterInput](#listfilterinputtypeofserviceplancredititemfilterinput)
    * [ListFilterInputTypeOfServicePlanFeatureViewModelFilterInput](#listfilterinputtypeofserviceplanfeatureviewmodelfilterinput)
    * [ListFilterInputTypeOfServicePlanScaleFilterInput](#listfilterinputtypeofserviceplanscalefilterinput)
    * [NameValueInput](#namevalueinput)
    * [PublishFormInput](#publishforminput)
    * [SendDomainInfoInput](#senddomaininfoinput)
    * [ServicePlanCreditFilterInput](#serviceplancreditfilterinput)
    * [ServicePlanFeatureFilterInput](#serviceplanfeaturefilterinput)
    * [ServicePlanFilterInput](#serviceplanfilterinput)
    * [ServicePlanScaleFilterInput](#serviceplanscalefilterinput)
    * [ServiceTypeOperationFilterInput](#servicetypeoperationfilterinput)
    * [StringOperationFilterInput](#stringoperationfilterinput)
    * [SubmitAccountPaymentInput](#submitaccountpaymentinput)
    * [TransactionAnalyticsInput](#transactionanalyticsinput)
    * [TransactionContentBodyInput](#transactioncontentbodyinput)
    * [TransactionContentInput](#transactioncontentinput)
    * [TransactionContentSettingsInput](#transactioncontentsettingsinput)
    * [TransactionDomainAnalyticsInput](#transactiondomainanalyticsinput)
    * [TransactionFromInput](#transactionfrominput)
    * [TransactionHeaderInput](#transactionheaderinput)
    * [TransactionRecipientInput](#transactionrecipientinput)
    * [TransactionReplyToInput](#transactionreplytoinput)
    * [TransactionSandboxInput](#transactionsandboxinput)
    * [TransactionSettingsInput](#transactionsettingsinput)
    * [TransactionTrackingInput](#transactiontrackinginput)
    * [UpdateAccountGroupInput](#updateaccountgroupinput)
    * [UpdateAccountInput](#updateaccountinput)
    * [UpdateAccountStatusInput](#updateaccountstatusinput)
    * [UpdateArticleContentInput](#updatearticlecontentinput)
    * [UpdateArticleInput](#updatearticleinput)
    * [UpdateBillingAddressInput](#updatebillingaddressinput)
    * [UpdateCampaignViewInput](#updatecampaignviewinput)
    * [UpdateCreditCardInfoInput](#updatecreditcardinfoinput)
    * [UpdateDataFieldInput](#updatedatafieldinput)
    * [UpdateDataFieldValueInput](#updatedatafieldvalueinput)
    * [UpdateDoubleOptInContentInput](#updatedoubleoptincontentinput)
    * [UpdateDoubleOptInEmailInput](#updatedoubleoptinemailinput)
    * [UpdateFileInput](#updatefileinput)
    * [UpdateFileViewInput](#updatefileviewinput)
    * [UpdateFolderInput](#updatefolderinput)
    * [UpdateGroupInput](#updategroupinput)
    * [UpdateGroupSubscriberInput](#updategroupsubscriberinput)
    * [UpdatePaymentMethodInput](#updatepaymentmethodinput)
    * [UpdateProfileFieldInput](#updateprofilefieldinput)
    * [UpdateQuestionCategoryInput](#updatequestioncategoryinput)
    * [UpdateQuestionInput](#updatequestioninput)
    * [UpdateSubscriberInput](#updatesubscriberinput)
    * [UpdateSubscriberListFormDialogInput](#updatesubscriberlistformdialoginput)
    * [UpdateSubscriberListFormInput](#updatesubscriberlistforminput)
    * [UpdateSubscriberListFormPageInput](#updatesubscriberlistformpageinput)
    * [UpdateSubscriberListInput](#updatesubscriberlistinput)
    * [UpdateSubscriberListViewInput](#updatesubscriberlistviewinput)
    * [UpdateTemplateContentInput](#updatetemplatecontentinput)
    * [UpdateTemplateInput](#updatetemplateinput)
    * [UpdateTemplateViewInput](#updatetemplateviewinput)
    * [UpdateUserInput](#updateuserinput)
    * [VerifySenderDomainInput](#verifysenderdomaininput)
  * [Enums](#enums)
    * [AccountStatus](#accountstatus)
    * [AppTheme](#apptheme)
    * [ApplyPolicy](#applypolicy)
    * [ArticleDefaultLayout](#articledefaultlayout)
    * [CampaignFields](#campaignfields)
    * [CampaignSendStatus](#campaignsendstatus)
    * [CardDeclineReason](#carddeclinereason)
    * [Charset](#charset)
    * [ConditionGroupOperator](#conditiongroupoperator)
    * [CreditCardNetwork](#creditcardnetwork)
    * [DataType](#datatype)
    * [EmailEventType](#emaileventtype)
    * [EventSourceType](#eventsourcetype)
    * [ExportStatus](#exportstatus)
    * [FieldValueType](#fieldvaluetype)
    * [FileDelimiter](#filedelimiter)
    * [FileFields](#filefields)
    * [FileType](#filetype)
    * [FormAction](#formaction)
    * [FormAttachmentFormat](#formattachmentformat)
    * [FormDialogIcon](#formdialogicon)
    * [FormDialogType](#formdialogtype)
    * [FormDuplicateEmailAction](#formduplicateemailaction)
    * [FormEventType](#formeventtype)
    * [FormExportStyle](#formexportstyle)
    * [FormPageType](#formpagetype)
    * [FormType](#formtype)
    * [ImportDeleteArea](#importdeletearea)
    * [ImportStatus](#importstatus)
    * [InviteStatus](#invitestatus)
    * [InvoiceStatus](#invoicestatus)
    * [MimeType](#mimetype)
    * [Operator](#operator)
    * [OptInSource](#optinsource)
    * [OptOutSource](#optoutsource)
    * [PaymentStatus](#paymentstatus)
    * [QuestionType](#questiontype)
    * [RawDataType](#rawdatatype)
    * [RecipientType](#recipienttype)
    * [ResourceType](#resourcetype)
    * [SandboxErrorType](#sandboxerrortype)
    * [SendFormat](#sendformat)
    * [ServiceType](#servicetype)
    * [Status](#status)
    * [SubscriberListMessageType](#subscriberlistmessagetype)
    * [SubscriberStatus](#subscriberstatus)
    * [TemplateCategory](#templatecategory)
    * [TemplateFields](#templatefields)
    * [TemplateSubCategory](#templatesubcategory)
    * [TemplateType](#templatetype)
    * [UserStatus](#userstatus)
  * [Scalars](#scalars)
    * [Boolean](#boolean)
    * [Byte](#byte)
    * [DateTime](#datetime)
    * [Decimal](#decimal)
    * [Float](#float)
    * [Int](#int)
    * [Long](#long)
    * [String](#string)

</details>

## Query
<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>myUser</strong></td>
<td valign="top"><a href="#user">User</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>account</strong></td>
<td valign="top"><a href="#account">Account</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>users</strong></td>
<td valign="top">[<a href="#user">User</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>user</strong></td>
<td valign="top"><a href="#user">User</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>accountGroups</strong></td>
<td valign="top">[<a href="#accountgroup">AccountGroup</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>accountGroup</strong></td>
<td valign="top"><a href="#accountgroup">AccountGroup</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>accountPlans</strong></td>
<td valign="top">[<a href="#accountplan">AccountPlan</a>]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>accountPaymentMethod</strong></td>
<td valign="top"><a href="#accountpaymentmethod">AccountPaymentMethod</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>accountPaymentMethods</strong></td>
<td valign="top">[<a href="#accountpaymentmethod">AccountPaymentMethod</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>accountInvoice</strong></td>
<td valign="top"><a href="#accountinvoice">AccountInvoice</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>accountInvoices</strong></td>
<td valign="top">[<a href="#accountinvoice">AccountInvoice</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>accountDedicatedIps</strong></td>
<td valign="top">[<a href="#accountip">AccountIp</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>accountReactivationCosts</strong></td>
<td valign="top"><a href="#reactivationcosts">ReactivationCosts</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>permissions</strong></td>
<td valign="top">[<a href="#permission">Permission</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>userInvites</strong></td>
<td valign="top">[<a href="#invite">Invite</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#invitefilterinput">InviteFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>servicePlan</strong></td>
<td valign="top"><a href="#serviceplan">ServicePlan</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>servicePlans</strong></td>
<td valign="top">[<a href="#serviceplan">ServicePlan</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">where</td>
<td valign="top"><a href="#serviceplanfilterinput">ServicePlanFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>senderDomain</strong></td>
<td valign="top"><a href="#senderdomain">SenderDomain</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>senderDomains</strong></td>
<td valign="top">[<a href="#senderdomain">SenderDomain</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>currentSelector</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>templatesInformation</strong></td>
<td valign="top">[<a href="#templateinformationviewmodel">TemplateInformationViewModel</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#getalltemplatesinfoinput">GetAllTemplatesInfoInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>templates</strong></td>
<td valign="top">[<a href="#templateinformationviewmodel">TemplateInformationViewModel</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#getalltemplatesinput">GetAllTemplatesInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>template</strong></td>
<td valign="top"><a href="#template">Template</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>templateContent</strong></td>
<td valign="top"><a href="#template">Template</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#gettemplatecontentinput">GetTemplateContentInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>templateVersions</strong></td>
<td valign="top"><a href="#templateversions">TemplateVersions</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>templateViews</strong></td>
<td valign="top">[<a href="#templateview">TemplateView</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>templateView</strong></td>
<td valign="top"><a href="#templateview">TemplateView</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#tag">Tag</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">resourceType</td>
<td valign="top"><a href="#resourcetype">ResourceType</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberList</strong></td>
<td valign="top"><a href="#subscriberlist">SubscriberList</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberLists</strong></td>
<td valign="top">[<a href="#subscriberlist">SubscriberList</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#getallsubscriberlistsinput">GetAllSubscriberListsInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberListView</strong></td>
<td valign="top"><a href="#subscriberlistview">SubscriberListView</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberListViews</strong></td>
<td valign="top">[<a href="#subscriberlistview">SubscriberListView</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberListDateField</strong></td>
<td valign="top"><a href="#datafield">DataField</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberListDataFields</strong></td>
<td valign="top">[<a href="#datafield">DataField</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberListExport</strong></td>
<td valign="top"><a href="#export">Export</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#getexportinput">GetExportInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberListExports</strong></td>
<td valign="top">[<a href="#export">Export</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">subscriberListId</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberListGroup</strong></td>
<td valign="top"><a href="#group">Group</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberListGroups</strong></td>
<td valign="top">[<a href="#group">Group</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberConversations</strong></td>
<td valign="top">[<a href="#subscriberconversation">SubscriberConversation</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">subscriberId</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberNotes</strong></td>
<td valign="top">[<a href="#subscribernote">SubscriberNote</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">subscriberId</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriber</strong></td>
<td valign="top"><a href="#subscriber">Subscriber</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscribers</strong></td>
<td valign="top">[<a href="#subscriber">Subscriber</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">subscriberListId</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberListForm</strong></td>
<td valign="top"><a href="#subscriberlistform">SubscriberListForm</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberListForms</strong></td>
<td valign="top">[<a href="#subscriberlistform">SubscriberListForm</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">subscriberListId</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>formQuestion</strong></td>
<td valign="top"><a href="#formquestion">FormQuestion</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#getquestioninput">GetQuestionInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>formQuestions</strong></td>
<td valign="top">[<a href="#formquestion">FormQuestion</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">formId</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>folders</strong></td>
<td valign="top">[<a href="#folder">Folder</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>file</strong></td>
<td valign="top"><a href="#file">File</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>files</strong></td>
<td valign="top">[<a href="#fileinfo">FileInfo</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#getallfilesinput">GetAllFilesInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>article</strong></td>
<td valign="top"><a href="#article">Article</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">articleId</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>articleContent</strong></td>
<td valign="top"><a href="#article">Article</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#getarticlecontentinput">GetArticleContentInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>categories</strong></td>
<td valign="top">[<a href="#category">Category</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>fileView</strong></td>
<td valign="top"><a href="#fileview">FileView</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>fileViews</strong></td>
<td valign="top">[<a href="#fileview">FileView</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>campaignView</strong></td>
<td valign="top"><a href="#campaignview">CampaignView</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>campaignViews</strong></td>
<td valign="top">[<a href="#campaignview">CampaignView</a>!]</td>
<td></td>
</tr>
</tbody>
</table>

## Mutation
<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>subscriberListImport</strong></td>
<td valign="top"><a href="#import">Import</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberListImports</strong></td>
<td valign="top">[<a href="#import">Import</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createAccount</strong></td>
<td valign="top"><a href="#account">Account</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createaccountinput">CreateAccountInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateAccount</strong></td>
<td valign="top"><a href="#account">Account</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#updateaccountinput">UpdateAccountInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateAccountStatus</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#updateaccountstatusinput">UpdateAccountStatusInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createAccountGroup</strong></td>
<td valign="top"><a href="#accountgroup">AccountGroup</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createaccountgroupinput">CreateAccountGroupInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateAccountGroup</strong></td>
<td valign="top"><a href="#accountgroup">AccountGroup</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#updateaccountgroupinput">UpdateAccountGroupInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteAccountGroup</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createUserAccountGroup</strong></td>
<td valign="top"><a href="#accountgroup">AccountGroup</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createuseraccountgroupinput">CreateUserAccountGroupInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteUserAccountGroup</strong></td>
<td valign="top"><a href="#accountgroup">AccountGroup</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#deleteuseraccountgroupinput">DeleteUserAccountGroupInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>changeAccountPlan</strong></td>
<td valign="top"><a href="#changeplanresult">ChangePlanResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#changeaccountplaninput">ChangeAccountPlanInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createAccountPaymentMethod</strong></td>
<td valign="top"><a href="#accountpaymentmethod">AccountPaymentMethod</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createpaymentmethodinput">CreatePaymentMethodInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateAccountPaymentMethod</strong></td>
<td valign="top"><a href="#accountpaymentmethod">AccountPaymentMethod</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#updatepaymentmethodinput">UpdatePaymentMethodInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteAccountPaymentMethod</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>calculateAccountPlanCost</strong></td>
<td valign="top"><a href="#calculatedplancost">CalculatedPlanCost</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#calculateaccountplancostinput">CalculateAccountPlanCostInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>submitAccountPayment</strong></td>
<td valign="top"><a href="#accountreceipt">AccountReceipt</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#submitaccountpaymentinput">SubmitAccountPaymentInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>cancelAccountPlanDowngrade</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">planId</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateUser</strong></td>
<td valign="top"><a href="#user">User</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#updateuserinput">UpdateUserInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createUserInvite</strong></td>
<td valign="top"><a href="#invite">Invite</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createuserinviteinput">CreateUserInviteInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>resendUserInvite</strong></td>
<td valign="top"><a href="#invite">Invite</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>processUserInvite</strong></td>
<td valign="top"><a href="#invite">Invite</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>revokeUserInvite</strong></td>
<td valign="top"><a href="#invite">Invite</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createTag</strong></td>
<td valign="top"><a href="#tag">Tag</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createtaginput">CreateTagInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteTag</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#deletetaginput">DeleteTagInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createSenderDomain</strong></td>
<td valign="top"><a href="#senderdomain">SenderDomain</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createsenderdomaininput">CreateSenderDomainInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateSenderDomain</strong></td>
<td valign="top"><a href="#senderdomain">SenderDomain</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sendDomainInfoEmail</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#senddomaininfoinput">SendDomainInfoInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>verifySenderDomain</strong></td>
<td valign="top"><a href="#verifydomainresult">VerifyDomainResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#verifysenderdomaininput">VerifySenderDomainInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteSenderDomain</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createTransaction</strong></td>
<td valign="top">[<a href="#transactionresponse">TransactionResponse</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createtransactioninput">CreateTransactionInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createTemplate</strong></td>
<td valign="top"><a href="#template">Template</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createtemplateinput">CreateTemplateInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>autoSaveTemplate</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#autosavetemplateinput">AutoSaveTemplateInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateTemplate</strong></td>
<td valign="top"><a href="#template">Template</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#updatetemplateinput">UpdateTemplateInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteTemplate</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createTemplateView</strong></td>
<td valign="top"><a href="#templateview">TemplateView</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createtemplateviewinput">CreateTemplateViewInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateTemplateView</strong></td>
<td valign="top"><a href="#templateview">TemplateView</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#updatetemplateviewinput">UpdateTemplateViewInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteTemplateView</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createSubscriberList</strong></td>
<td valign="top"><a href="#subscriberlist">SubscriberList</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createsubscriberlistinput">CreateSubscriberListInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateDoubleOptInContent</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#updatedoubleoptincontentinput">UpdateDoubleOptInContentInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateSubscriberList</strong></td>
<td valign="top"><a href="#subscriberlist">SubscriberList</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#updatesubscriberlistinput">UpdateSubscriberListInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createSubscriberListSecurityGroup</strong></td>
<td valign="top"><a href="#subscriberlist">SubscriberList</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createsubscriberlistsecuritygroupinput">CreateSubscriberListSecurityGroupInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteSubscriberList</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteSubscriberListSecurityGroup</strong></td>
<td valign="top"><a href="#subscriberlist">SubscriberList</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#deletesubscriberlistsecuritygroupinput">DeleteSubscriberListSecurityGroupInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createSubscriberListView</strong></td>
<td valign="top"><a href="#subscriberlistview">SubscriberListView</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createsubscriberlistviewinput">CreateSubscriberListViewInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateSubscriberListView</strong></td>
<td valign="top"><a href="#subscriberlistview">SubscriberListView</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#updatesubscriberlistviewinput">UpdateSubscriberListViewInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteSubscriberListView</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createSubscriberListDataField</strong></td>
<td valign="top"><a href="#datafield">DataField</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createdatafieldinput">CreateDataFieldInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateSubscriberListDataField</strong></td>
<td valign="top"><a href="#datafield">DataField</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#updatedatafieldinput">UpdateDataFieldInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteSubscriberListDataField</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#deletedatafieldinput">DeleteDataFieldInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createExport</strong></td>
<td valign="top"><a href="#export">Export</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createexportinput">CreateExportInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createSubscriberListGroup</strong></td>
<td valign="top"><a href="#group">Group</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#creategroupinput">CreateGroupInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateSubscriberListGroup</strong></td>
<td valign="top"><a href="#group">Group</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#updategroupinput">UpdateGroupInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteSubscriberListGroup</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#deletegroupinput">DeleteGroupInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createSubscriberListImport</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createimportinput">CreateImportInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createSubscriberConversation</strong></td>
<td valign="top"><a href="#subscriber">Subscriber</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createsubscriberconversationinput">CreateSubscriberConversationInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createSubscriberNote</strong></td>
<td valign="top"><a href="#subscriber">Subscriber</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createsubscribernoteinput">CreateSubscriberNoteInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteSubscriberNote</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#deletesubscribernoteinput">DeleteSubscriberNoteInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createSubscriber</strong></td>
<td valign="top"><a href="#subscriber">Subscriber</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createsubscriberinput">CreateSubscriberInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateSubscriber</strong></td>
<td valign="top"><a href="#subscriber">Subscriber</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#updatesubscriberinput">UpdateSubscriberInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateSubscriberStatus</strong></td>
<td valign="top"><a href="#subscriber">Subscriber</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#changesubscriberstatusinput">ChangeSubscriberStatusInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createGroupSubscriber</strong></td>
<td valign="top"><a href="#subscriber">Subscriber</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteGroupSubscriber</strong></td>
<td valign="top"><a href="#subscriber">Subscriber</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteSubscriber</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createForm</strong></td>
<td valign="top"><a href="#subscriberlistform">SubscriberListForm</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createforminput">CreateFormInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>publishForm</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#publishforminput">PublishFormInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>unpublishForm</strong></td>
<td valign="top"><a href="#subscriberlistform">SubscriberListForm</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateForm</strong></td>
<td valign="top"><a href="#subscriberlistform">SubscriberListForm</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#updatesubscriberlistforminput">UpdateSubscriberListFormInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateFormDialog</strong></td>
<td valign="top"><a href="#subscriberlistform">SubscriberListForm</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#updatesubscriberlistformdialoginput">UpdateSubscriberListFormDialogInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateFormPage</strong></td>
<td valign="top"><a href="#subscriberlistform">SubscriberListForm</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#updatesubscriberlistformpageinput">UpdateSubscriberListFormPageInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>exportForm</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#exportforminput">ExportFormInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteForm</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#deleteforminput">DeleteFormInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createFormQuestion</strong></td>
<td valign="top"><a href="#formquestion">FormQuestion</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createquestioninput">CreateQuestionInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateFormQuestion</strong></td>
<td valign="top"><a href="#formquestion">FormQuestion</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#updatequestioninput">UpdateQuestionInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteFormQuestion</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createFolder</strong></td>
<td valign="top"><a href="#folder">Folder</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createfolderinput">CreateFolderInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateFolder</strong></td>
<td valign="top"><a href="#folder">Folder</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#updatefolderinput">UpdateFolderInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteFolder</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createUrlFile</strong></td>
<td valign="top"><a href="#file">File</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createurlfileinput">CreateUrlFileInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateFile</strong></td>
<td valign="top"><a href="#file">File</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#updatefileinput">UpdateFileInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteFile</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createCategory</strong></td>
<td valign="top"><a href="#category">Category</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createcategoryinput">CreateCategoryInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteCategory</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#deletecategoryinput">DeleteCategoryInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createFileView</strong></td>
<td valign="top"><a href="#fileview">FileView</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createfileviewinput">CreateFileViewInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateFileView</strong></td>
<td valign="top"><a href="#fileview">FileView</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#updatefileviewinput">UpdateFileViewInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteFileView</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createArticle</strong></td>
<td valign="top"><a href="#article">Article</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createarticleinput">CreateArticleInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>autoSaveArticle</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#autosavearticleinput">AutoSaveArticleInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateArticle</strong></td>
<td valign="top"><a href="#article">Article</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#updatearticleinput">UpdateArticleInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteArticle</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createCampaignView</strong></td>
<td valign="top"><a href="#campaignview">CampaignView</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createcampaignviewinput">CreateCampaignViewInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateCampaignView</strong></td>
<td valign="top"><a href="#campaignview">CampaignView</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#updatecampaignviewinput">UpdateCampaignViewInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteCampaignView</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

## Objects

### Account

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>settings</strong></td>
<td valign="top">[<a href="#accountsetting">AccountSetting</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>users</strong></td>
<td valign="top">[<a href="#user">User</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>owner</strong></td>
<td valign="top"><a href="#user">User</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>status</strong></td>
<td valign="top"><a href="#accountstatus">AccountStatus</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isStatusChangeable</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>lastStatusChangedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>paymentStatus</strong></td>
<td valign="top"><a href="#paymentstatus">PaymentStatus</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>streetAddressLine1</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

Gets or sets the address.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>streetAddressLine2</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Gets or sets the address2.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>city</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

Gets or sets the city.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>state_Province</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

Gets or sets the region.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>zip_PostalCode</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Gets or sets the postal code.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>country_Region</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

Gets or sets the country.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>website</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Gets or sets the website url.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>phone</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdBy</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedBy</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>groups</strong></td>
<td valign="top">[<a href="#accountgroup">AccountGroup</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>senderDomains</strong></td>
<td valign="top">[<a href="#senderdomain">SenderDomain</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>invites</strong></td>
<td valign="top">[<a href="#invite">Invite</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dedicatedIps</strong></td>
<td valign="top">[<a href="#accountip">AccountIp</a>!]!</td>
<td></td>
</tr>
</tbody>
</table>

### AccountGroup

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>users</strong></td>
<td valign="top">[<a href="#user">User</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>permissions</strong></td>
<td valign="top">[<a href="#permission">Permission</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>userCount</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isActive</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isAdmin</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>lists</strong></td>
<td valign="top">[<a href="#list">List</a>]</td>
<td></td>
</tr>
</tbody>
</table>

### AccountGroupPermission

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>accountId</strong></td>
<td valign="top"><a href="#long">Long</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>permissionKey</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>permissionId</strong></td>
<td valign="top"><a href="#long">Long</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>groupId</strong></td>
<td valign="top"><a href="#long">Long</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>group</strong></td>
<td valign="top"><a href="#accountgroup">AccountGroup</a></td>
<td></td>
</tr>
</tbody>
</table>

### AccountInvoice

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>status</strong></td>
<td valign="top"><a href="#invoicestatus">InvoiceStatus</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>pdfUrl</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>orderNbr</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>amount</strong></td>
<td valign="top"><a href="#float">Float</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>totalAmount</strong></td>
<td valign="top"><a href="#float">Float</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>servicePeriodStartUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>servicePeriodEndUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dueUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>lineItems</strong></td>
<td valign="top">[<a href="#accountinvoicelineitem">AccountInvoiceLineItem</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>receipts</strong></td>
<td valign="top">[<a href="#accountreceipt">AccountReceipt</a>]</td>
<td></td>
</tr>
</tbody>
</table>

### AccountInvoiceLineItem

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>serviceType</strong></td>
<td valign="top"><a href="#servicetype">ServiceType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rate</strong></td>
<td valign="top"><a href="#float">Float</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>qty</strong></td>
<td valign="top"><a href="#float">Float</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>amount</strong></td>
<td valign="top"><a href="#float">Float</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isDiscount</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### AccountIp

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### AccountPaymentMethod

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>billingAddress</strong></td>
<td valign="top"><a href="#billingaddress">BillingAddress</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>nickname</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>expMonth</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>expYear</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isDefault</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>last4Digits</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>cardNetwork</strong></td>
<td valign="top"><a href="#creditcardnetwork">CreditCardNetwork</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### AccountPlan

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>subscriberCount</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>emailSent</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>creditBalance</strong></td>
<td valign="top"><a href="#float">Float</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>averageMonthlyCreditsUsed</strong></td>
<td valign="top"><a href="#float">Float</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>discounts</strong></td>
<td valign="top">[<a href="#accountplandiscount">AccountPlanDiscount</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>nextPlan</strong></td>
<td valign="top"><a href="#serviceplan">ServicePlan</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>servicePlanId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>serviceType</strong></td>
<td valign="top"><a href="#servicetype">ServiceType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>fee</strong></td>
<td valign="top"><a href="#float">Float</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>minSubscribers</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>maxSubscribers</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>qty</strong></td>
<td valign="top"><a href="#float">Float</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>currBillPeriodStartUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>nextBillUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isMonthly</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isTrial</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>trialEndUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>autoRefillCredits</strong></td>
<td valign="top"><a href="#float">Float</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>minimumCredits</strong></td>
<td valign="top"><a href="#float">Float</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>features</strong></td>
<td valign="top">[<a href="#accountplanfeature">AccountPlanFeature</a>!]!</td>
<td></td>
</tr>
</tbody>
</table>

### AccountPlanDiscount

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>discountAmt</strong></td>
<td valign="top"><a href="#float">Float</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>discountPct</strong></td>
<td valign="top"><a href="#float">Float</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isRecurring</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>startUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>nextUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>endUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### AccountPlanFeature

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>limit</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>limitDescription</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### AccountReceipt

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>invoiceId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>transactionId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>amount</strong></td>
<td valign="top"><a href="#float">Float</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>reason</strong></td>
<td valign="top"><a href="#carddeclinereason">CardDeclineReason</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>status</strong></td>
<td valign="top"><a href="#paymentstatus">PaymentStatus</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>paymentNickname</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>paymentExpMonth</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>paymentExpYear</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>paymentLast4Digits</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>paymentCardNetwork</strong></td>
<td valign="top"><a href="#creditcardnetwork">CreditCardNetwork</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### AccountSetting

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>value</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### Article

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>folderId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>title</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>language</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>recoveryFile</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>defaultLayout</strong></td>
<td valign="top"><a href="#articledefaultlayout">ArticleDefaultLayout</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>category</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>publishedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#string">String</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>versions</strong></td>
<td valign="top">[<a href="#version">Version</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>contentBodies</strong></td>
<td valign="top">[<a href="#articlecontent">ArticleContent</a>!]</td>
<td></td>
</tr>
</tbody>
</table>

### ArticleContent

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>mimeType</strong></td>
<td valign="top"><a href="#mimetype">MimeType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>content</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### BillingAddress

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>firstName</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>lastName</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>emailAddr</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>streetAddressLine1</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>streetAddressLine2</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>city</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>state_Province</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>zip_PostalCode</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>country_Region</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>phone</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CalculatedItem

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>serviceType</strong></td>
<td valign="top"><a href="#servicetype">ServiceType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isCurrentPlan</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>proratedFee</strong></td>
<td valign="top"><a href="#float">Float</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>totalFee</strong></td>
<td valign="top"><a href="#float">Float</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>discountAmt</strong></td>
<td valign="top"><a href="#float">Float</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>discountPct</strong></td>
<td valign="top"><a href="#float">Float</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CalculatedPlanCost

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>items</strong></td>
<td valign="top">[<a href="#calculateditem">CalculatedItem</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>effectiveUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>nextBillingUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CampaignView

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sendStartUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sendEndUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedStartUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedEndUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdStartUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdEndUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>groupBy</strong></td>
<td valign="top"><a href="#campaignfields">CampaignFields</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sortBy</strong></td>
<td valign="top"><a href="#campaignfields">CampaignFields</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPrivate</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#string">String</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>statuses</strong></td>
<td valign="top">[<a href="#campaignsendstatus">CampaignSendStatus</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### Category

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>categoryName</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### ChangePlanResult

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>successful</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>failedPaymentReason</strong></td>
<td valign="top"><a href="#carddeclinereason">CardDeclineReason</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>receipt</strong></td>
<td valign="top"><a href="#accountreceipt">AccountReceipt</a></td>
<td></td>
</tr>
</tbody>
</table>

### Column

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>subscribers</strong></td>
<td valign="top"><a href="#datafield">DataField</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>skip</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### Condition

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dataField</strong></td>
<td valign="top"><a href="#datafield">DataField</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>conditionGroup</strong></td>
<td valign="top"><a href="#conditiongroup">ConditionGroup</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>fieldName</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>operator</strong></td>
<td valign="top"><a href="#operator">Operator</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>value</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### ConditionGroup

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>parentConditionGroup</strong></td>
<td valign="top"><a href="#conditiongroup">ConditionGroup</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>operator</strong></td>
<td valign="top"><a href="#conditiongroupoperator">ConditionGroupOperator</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>conditions</strong></td>
<td valign="top">[<a href="#condition">Condition</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>childConditionGroups</strong></td>
<td valign="top">[<a href="#conditiongroup">ConditionGroup</a>]</td>
<td></td>
</tr>
</tbody>
</table>

### DataField

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dataType</strong></td>
<td valign="top"><a href="#datatype">DataType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>labelText</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dscr</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>required</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPublic</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>mergeTag</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>defaultValue</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>possibleValues</strong></td>
<td valign="top">[<a href="#datafieldvalue">DataFieldValue</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>valueType</strong></td>
<td valign="top"><a href="#fieldvaluetype">FieldValueType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>minNbr</strong></td>
<td valign="top"><a href="#decimal">Decimal</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>maxNbr</strong></td>
<td valign="top"><a href="#decimal">Decimal</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>minUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>maxUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>allowOther</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>monthDayFormat</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>conditions</strong></td>
<td valign="top">[<a href="#condition">Condition</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### DataFieldLanguageLabel

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#long">Long</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>language</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>label</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### DataFieldValue

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>label</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>value</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>displayOrder</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>languageLabels</strong></td>
<td valign="top">[<a href="#datafieldlanguagelabel">DataFieldLanguageLabel</a>]</td>
<td></td>
</tr>
</tbody>
</table>

### Email

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>domain</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

255 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>localPart</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

65 character limit

</td>
</tr>
</tbody>
</table>

### Export

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>notificationEmail</strong></td>
<td valign="top"><a href="#email">Email</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberStatus</strong></td>
<td valign="top"><a href="#subscriberstatus">SubscriberStatus</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>groupIds</strong></td>
<td valign="top">[<a href="#string">String</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>behaviors</strong></td>
<td valign="top">[<a href="#string">String</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>fields</strong></td>
<td valign="top">[<a href="#string">String</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>delimiter</strong></td>
<td valign="top"><a href="#filedelimiter">FileDelimiter</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>status</strong></td>
<td valign="top"><a href="#exportstatus">ExportStatus</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dataLocationUrl</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberListId</strong></td>
<td valign="top"><a href="#long">Long</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### File

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>publicUrl</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>thumbnailUrl</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>size</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>uploadedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#string">String</a>!]!</td>
<td></td>
</tr>
</tbody>
</table>

### FileInfo

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>thumbnailUrl</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>publicUrl</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#filetype">FileType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>size</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#string">String</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### FileView

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedStartUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedEndUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdStartUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdEndUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>groupBy</strong></td>
<td valign="top"><a href="#filefields">FileFields</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sortBy</strong></td>
<td valign="top"><a href="#filefields">FileFields</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPrivate</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#string">String</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>types</strong></td>
<td valign="top">[<a href="#filetype">FileType</a>!]</td>
<td></td>
</tr>
</tbody>
</table>

### Folder

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>parentId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>hasChildren</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### Form

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#long">Long</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#formtype">FormType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPublished</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>publishedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>answeredCount</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>visitedCount</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>skipped</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>submissionAction</strong></td>
<td valign="top"><a href="#formaction">FormAction</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sendThankYouEmail</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sendNotificationEmail</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>notificationAttachmentFormat</strong></td>
<td valign="top"><a href="#formattachmentformat">FormAttachmentFormat</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>duplicateEmailAction</strong></td>
<td valign="top"><a href="#formduplicateemailaction">FormDuplicateEmailAction</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>duplicationEmailMessageAction</strong></td>
<td valign="top"><a href="#formaction">FormAction</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>accountId</strong></td>
<td valign="top"><a href="#long">Long</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberListId</strong></td>
<td valign="top"><a href="#long">Long</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberList</strong></td>
<td valign="top"><a href="#subscriberlist">SubscriberList</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>notifications</strong></td>
<td valign="top">[<a href="#notification">Notification</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>questions</strong></td>
<td valign="top">[<a href="#formquestion">FormQuestion</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>events</strong></td>
<td valign="top">[<a href="#formevent">FormEvent</a>]</td>
<td></td>
</tr>
</tbody>
</table>

### FormAnswer

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>question</strong></td>
<td valign="top"><a href="#formquestion">FormQuestion</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>answerText</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>comment</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sourceId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sourceType</strong></td>
<td valign="top"><a href="#eventsourcetype">EventSourceType</a></td>
<td></td>
</tr>
</tbody>
</table>

### FormDialog

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#formdialogtype">FormDialogType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>message</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>thankYouIcon</strong></td>
<td valign="top"><a href="#formdialogicon">FormDialogIcon</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>iconColor</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>displayRedirectButton</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>redirectButtonText</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>redirectButtonUrl</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>redirectButtonColor</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>showRedirectButton</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>buttonText</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>redirectUrl</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>displayCloseButton</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>displayResults</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>displayAnswers</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### FormEvent

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#long">Long</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>respondentId</strong></td>
<td valign="top"><a href="#long">Long</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>eventUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>eventType</strong></td>
<td valign="top"><a href="#formeventtype">FormEventType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>readSeconds</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ipAddress</strong></td>
<td valign="top">[<a href="#byte">Byte</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>software</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>os</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>device</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>userAgent</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>campaignId</strong></td>
<td valign="top"><a href="#long">Long</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>accountId</strong></td>
<td valign="top"><a href="#long">Long</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberId</strong></td>
<td valign="top"><a href="#long">Long</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriber</strong></td>
<td valign="top"><a href="#subscriber">Subscriber</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>formId</strong></td>
<td valign="top"><a href="#long">Long</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>form</strong></td>
<td valign="top"><a href="#form">Form</a></td>
<td></td>
</tr>
</tbody>
</table>

### FormPage

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#formpagetype">FormPageType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>content</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### FormQuestion

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#long">Long</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>text</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#questiontype">QuestionType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>required</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>answeredCount</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>skippedCount</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>display</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isActive</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>characterLimit</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>displayOrder</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>accountId</strong></td>
<td valign="top"><a href="#long">Long</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>parentQuestionId</strong></td>
<td valign="top"><a href="#long">Long</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>formId</strong></td>
<td valign="top"><a href="#long">Long</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>form</strong></td>
<td valign="top"><a href="#form">Form</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>answers</strong></td>
<td valign="top">[<a href="#formquestionanswer">FormQuestionAnswer</a>]</td>
<td></td>
</tr>
</tbody>
</table>

### FormQuestionAnswer

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#long">Long</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>text</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>displayOrder</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>accountId</strong></td>
<td valign="top"><a href="#long">Long</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>questionId</strong></td>
<td valign="top"><a href="#long">Long</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>question</strong></td>
<td valign="top"><a href="#formquestion">FormQuestion</a></td>
<td></td>
</tr>
</tbody>
</table>

### FormResponse

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>collector</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>submissionUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>timeSpentMinutes</strong></td>
<td valign="top"><a href="#float">Float</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>answers</strong></td>
<td valign="top">[<a href="#formanswer">FormAnswer</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### Group

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscribers</strong></td>
<td valign="top">[<a href="#subscriber">Subscriber</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPublic</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isDynamic</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>totalSubscribers</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>totalActiveSubscribers</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>totalUnconfirmedSubscribers</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>totalUndeliverableSubscribers</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>totalUnsubscribedSubscribers</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>totalComplaintSubscribers</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### Import

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>groups</strong></td>
<td valign="top">[<a href="#group">Group</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>columns</strong></td>
<td valign="top">[<a href="#column">Column</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteArea</strong></td>
<td valign="top"><a href="#importdeletearea">ImportDeleteArea</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>update</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>unsubscribe</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>skipFirstRow</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>confirmEmail</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>delimiter</strong></td>
<td valign="top"><a href="#filedelimiter">FileDelimiter</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>status</strong></td>
<td valign="top"><a href="#importstatus">ImportStatus</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>FileRecords</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>recordsAdded</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>recordsUpdated</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>badRecords</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>duplicateRecords</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>jobStartedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>jobEndedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ErrorCode</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### Invite

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>firstName</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>lastName</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>status</strong></td>
<td valign="top"><a href="#invitestatus">InviteStatus</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>emailAddr</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>groups</strong></td>
<td valign="top">[<a href="#accountgroup">AccountGroup</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>user</strong></td>
<td valign="top"><a href="#user">User</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>account</strong></td>
<td valign="top"><a href="#account">Account</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### List

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>listId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### Notification

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#long">Long</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberListMessageType</strong></td>
<td valign="top"><a href="#subscriberlistmessagetype">SubscriberListMessageType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>enabled</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>fromText</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>fromEmail</strong></td>
<td valign="top"><a href="#email">Email</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subject</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>notificationContents</strong></td>
<td valign="top">[<a href="#notificationcontent">NotificationContent</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>formId</strong></td>
<td valign="top"><a href="#long">Long</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>accountId</strong></td>
<td valign="top"><a href="#long">Long</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### NotificationContent

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#long">Long</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>mimeType</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dataBlobId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>workingDataBlobId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>recoveryDataBlobId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>thumbnailUrl</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>validContent</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>autoSaveUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>notificationId</strong></td>
<td valign="top"><a href="#long">Long</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>notification</strong></td>
<td valign="top"><a href="#notification">Notification</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>accountId</strong></td>
<td valign="top"><a href="#long">Long</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### Permission

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>key</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### ProfileField

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>datafield</strong></td>
<td valign="top"><a href="#datafield">DataField</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>value</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>valueType</strong></td>
<td valign="top"><a href="#rawdatatype">RawDataType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### ReactivationCosts

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>previousCost</strong></td>
<td valign="top"><a href="#float">Float</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>newCost</strong></td>
<td valign="top"><a href="#float">Float</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dueNow</strong></td>
<td valign="top"><a href="#float">Float</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>currentCost</strong></td>
<td valign="top"><a href="#float">Float</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### SenderDomain

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>domain</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dkimSelector</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dkimValid</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dkimReason</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dmarcValid</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dmarcReason</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>lastVerifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>lastVerifiedResults</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### ServicePlan

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>serviceType</strong></td>
<td valign="top"><a href="#servicetype">ServiceType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>creditValue</strong></td>
<td valign="top"><a href="#float">Float</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>_do</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td>

Internal use only

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>scales</strong></td>
<td valign="top">[<a href="#serviceplanscale">ServicePlanScale</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>credits</strong></td>
<td valign="top">[<a href="#serviceplancredit">ServicePlanCredit</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>features</strong></td>
<td valign="top">[<a href="#serviceplanfeature">ServicePlanFeature</a>!]!</td>
<td></td>
</tr>
</tbody>
</table>

### ServicePlanCredit

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>qty</strong></td>
<td valign="top"><a href="#float">Float</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>fee</strong></td>
<td valign="top"><a href="#float">Float</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### ServicePlanFeature

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>limit</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>limitDescription</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>_do</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td>

Internal use only

</td>
</tr>
</tbody>
</table>

### ServicePlanScale

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>minLimit</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>maxLimit</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>fee</strong></td>
<td valign="top"><a href="#float">Float</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### Subscriber

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>optInIp</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>confirmedIp</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>optOutIp</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>groups</strong></td>
<td valign="top">[<a href="#group">Group</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#tag">Tag</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>rating</strong></td>
<td valign="top"><a href="#decimal">Decimal</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>longitude</strong></td>
<td valign="top"><a href="#decimal">Decimal</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>latitude</strong></td>
<td valign="top"><a href="#decimal">Decimal</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>city</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>state</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>postalCode</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>country</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>timeZone</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>cultureCode</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sendFormat</strong></td>
<td valign="top"><a href="#sendformat">SendFormat</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>status</strong></td>
<td valign="top"><a href="#subscriberstatus">SubscriberStatus</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>email</strong></td>
<td valign="top"><a href="#email">Email</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>optInUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>optInSource</strong></td>
<td valign="top"><a href="#optinsource">OptInSource</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>confirmedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>optOutUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>optOutSource</strong></td>
<td valign="top"><a href="#optoutsource">OptOutSource</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>optOutReason</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>conversations</strong></td>
<td valign="top">[<a href="#subscriberconversation">SubscriberConversation</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>notes</strong></td>
<td valign="top">[<a href="#subscribernote">SubscriberNote</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>profileFields</strong></td>
<td valign="top">[<a href="#profilefield">ProfileField</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>events</strong></td>
<td valign="top">[<a href="#subscriberevent">SubscriberEvent</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### SubscriberConversation

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>fromSubscriber</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>message</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>status</strong></td>
<td valign="top"><a href="#status">Status</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### SubscriberEvent

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sourceId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sourceLinkId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ipAddress</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>eventUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>eventType</strong></td>
<td valign="top"><a href="#emaileventtype">EmailEventType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>readSeconds</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sourceType</strong></td>
<td valign="top"><a href="#eventsourcetype">EventSourceType</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### SubscriberList

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>CompanyName</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>address1</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>address2</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>city</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>state</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>zipCode</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>country</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>phone</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>website</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>defaultFromEmail</strong></td>
<td valign="top"><a href="#email">Email</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>defaultFromText</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>requireDoubleOptIn</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>totalSubscribers</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>totalActiveSubscribers</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>totalUnconfirmedSubscribers</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>totalUndeliverableSubscribers</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>totalUnsubscribedSubscribers</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>totalComplaintSubscribers</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>totalScrubbedSubscribers</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dataFields</strong></td>
<td valign="top">[<a href="#datafield">DataField</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>groups</strong></td>
<td valign="top">[<a href="#group">Group</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscribers</strong></td>
<td valign="top">[<a href="#subscriber">Subscriber</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>imports</strong></td>
<td valign="top">[<a href="#import">Import</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>exports</strong></td>
<td valign="top">[<a href="#export">Export</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#subscriberlisttag">SubscriberListTag</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>forms</strong></td>
<td valign="top">[<a href="#form">Form</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### SubscriberListForm

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sharableUrl</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>answeredCount</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>visitedCount</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>skippedCount</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>published</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>publishedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>pageName</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>pageTitle</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>metaDescription</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>metaKeywords</strong></td>
<td valign="top">[<a href="#string">String</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>socialStoryImageUrl</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>defaultLanguage</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>translationLanguages</strong></td>
<td valign="top">[<a href="#string">String</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>requiredTextTranslation</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>formErrorTextTranslation</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>redirectUrl</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>submitAction</strong></td>
<td valign="top"><a href="#formaction">FormAction</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sendThankYou</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>groups</strong></td>
<td valign="top">[<a href="#group">Group</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#string">String</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sendNotificationEmail</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>attachmentFormat</strong></td>
<td valign="top"><a href="#formattachmentformat">FormAttachmentFormat</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>duplicateEmailAction</strong></td>
<td valign="top"><a href="#formduplicateemailaction">FormDuplicateEmailAction</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>duplicateEmailErrorAction</strong></td>
<td valign="top"><a href="#formaction">FormAction</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>duplicateEmailErrorRedirectUrl</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberListId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dialogs</strong></td>
<td valign="top">[<a href="#formdialog">FormDialog</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>pages</strong></td>
<td valign="top">[<a href="#formpage">FormPage</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>questions</strong></td>
<td valign="top">[<a href="#formquestion">FormQuestion</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>responses</strong></td>
<td valign="top">[<a href="#formresponse">FormResponse</a>!]!</td>
<td></td>
</tr>
</tbody>
</table>

### SubscriberListTag

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>tagHash</strong></td>
<td valign="top">[<a href="#byte">Byte</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tag</strong></td>
<td valign="top"><a href="#tag">Tag</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberListId</strong></td>
<td valign="top"><a href="#long">Long</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberList</strong></td>
<td valign="top"><a href="#subscriberlist">SubscriberList</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>accountId</strong></td>
<td valign="top"><a href="#long">Long</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### SubscriberListView

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>minOpenRate</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>maxOpenRate</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>minClickRate</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>maxClickRate</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>groupBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sortBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPrivate</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>userId</strong></td>
<td valign="top"><a href="#long">Long</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#string">String</a>]</td>
<td></td>
</tr>
</tbody>
</table>

### SubscriberNote

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>message</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>status</strong></td>
<td valign="top"><a href="#status">Status</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### Tag

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>tagName</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### Template

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>usage</strong></td>
<td valign="top"><a href="#templateusage">TemplateUsage</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>versionInfo</strong></td>
<td valign="top"><a href="#templateversions">TemplateVersions</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#string">String</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#templatetype">TemplateType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>category</strong></td>
<td valign="top"><a href="#templatecategory">TemplateCategory</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>contentBodies</strong></td>
<td valign="top">[<a href="#templatecontent">TemplateContent</a>!]!</td>
<td></td>
</tr>
</tbody>
</table>

### TemplateCampaign

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>status</strong></td>
<td valign="top"><a href="#campaignsendstatus">CampaignSendStatus</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sentUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
</tbody>
</table>

### TemplateContent

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#mimetype">MimeType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>content</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### TemplateInformationViewModel

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>thumbnailUrl</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>lastModifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#string">String</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#templatetype">TemplateType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>category</strong></td>
<td valign="top"><a href="#templatecategory">TemplateCategory</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subcategory</strong></td>
<td valign="top"><a href="#templatesubcategory">TemplateSubCategory</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### TemplateUsage

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>sentCampaigns</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>draftCampaigns</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>campaigns</strong></td>
<td valign="top">[<a href="#templatecampaign">TemplateCampaign</a>!]!</td>
<td></td>
</tr>
</tbody>
</table>

### TemplateVersion

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>lastModifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### TemplateVersions

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>versions</strong></td>
<td valign="top">[<a href="#templateversion">TemplateVersion</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>recoveryFile</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### TemplateView

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedStartUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedEndUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdStartUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdEndUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>groupBy</strong></td>
<td valign="top"><a href="#templatefields">TemplateFields</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sortBy</strong></td>
<td valign="top"><a href="#templatefields">TemplateFields</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPrivate</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>userId</strong></td>
<td valign="top"><a href="#long">Long</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#string">String</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>types</strong></td>
<td valign="top">[<a href="#templatetype">TemplateType</a>!]</td>
<td></td>
</tr>
</tbody>
</table>

### TransactionResponse

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>transactionId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>requestId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>emailAddress</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>errorCode</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>errorMsg</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### User

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>accounts</strong></td>
<td valign="top">[<a href="#account">Account</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>groups</strong></td>
<td valign="top">[<a href="#accountgroup">AccountGroup</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>settings</strong></td>
<td valign="top">[<a href="#usersetting">UserSetting</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>permissions</strong></td>
<td valign="top">[<a href="#permission">Permission</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>status</strong></td>
<td valign="top"><a href="#userstatus">UserStatus</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>firstName</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>lastName</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>company</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>businessPhone</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>mobilePhone</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>otherPhone</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>emailAddr</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>mfaEnabled</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdBy</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedBy</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### UserSetting

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>value</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### VerifyDomainResult

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>lastVerifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dkimValid</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dkimReason</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dmarcValid</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dmarcReason</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### Version

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#float">Float</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>lastModifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
</tbody>
</table>

## Inputs

### AddBillingAddressInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>firstName</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>lastName</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>emailAddr</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

320 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>streetAddressLine1</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>streetAddressLine2</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

50 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>city</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>state_Province</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>zip_PostalCode</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

15 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>country_Region</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>phone</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

25 character limit

</td>
</tr>
</tbody>
</table>

### AddCreditCardInfoInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>cardNumber</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

Needs to be a 13-16 digit value

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>expirationMonth</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td>

1-12

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>expirationYear</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td>

yyyy format (ex: 2021)

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>cvv</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td>

3 or 4 digit number

</td>
</tr>
</tbody>
</table>

### AutoSaveArticleContentInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>mimeType</strong></td>
<td valign="top"><a href="#mimetype">MimeType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>content</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### AutoSaveArticleInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>contentBodies</strong></td>
<td valign="top">[<a href="#autosavearticlecontentinput">AutoSaveArticleContentInput</a>!]!</td>
<td></td>
</tr>
</tbody>
</table>

### AutoSaveTemplateContentInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>mimeType</strong></td>
<td valign="top"><a href="#mimetype">MimeType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>content</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### AutoSaveTemplateInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>contentBodies</strong></td>
<td valign="top">[<a href="#autosavetemplatecontentinput">AutoSaveTemplateContentInput</a>!]!</td>
<td></td>
</tr>
</tbody>
</table>

### CalculateAccountPlanCostInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>currentPlanId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>newPlanId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>newCreditItemId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

Should be set to '0' if the new plan a monthly plan.

</td>
</tr>
</tbody>
</table>

### ChangeAccountPlanInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>newPlanId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>newCreditItemId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Should be set to 0 or null if new plan is monthly.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>paymentMethodId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>autoRefillCreditItemId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>minimumCredits</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
</tbody>
</table>

### ChangeSubscriberStatusInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>status</strong></td>
<td valign="top"><a href="#subscriberstatus">SubscriberStatus</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### ComparableDateTimeOperationFilterInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>eq</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>neq</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>in</strong></td>
<td valign="top">[<a href="#datetime">DateTime</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>nin</strong></td>
<td valign="top">[<a href="#datetime">DateTime</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>gt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ngt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>gte</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ngte</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>lt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>nlt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>lte</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>nlte</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
</tbody>
</table>

### ComparableDoubleOperationFilterInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>eq</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>neq</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>in</strong></td>
<td valign="top">[<a href="#float">Float</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>nin</strong></td>
<td valign="top">[<a href="#float">Float</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>gt</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ngt</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>gte</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ngte</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>lt</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>nlt</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>lte</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>nlte</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
</tbody>
</table>

### ComparableInt32OperationFilterInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>eq</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>neq</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>in</strong></td>
<td valign="top">[<a href="#int">Int</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>nin</strong></td>
<td valign="top">[<a href="#int">Int</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>gt</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ngt</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>gte</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ngte</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>lt</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>nlt</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>lte</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>nlte</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
</tbody>
</table>

### ComparableInt64OperationFilterInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>eq</strong></td>
<td valign="top"><a href="#long">Long</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>neq</strong></td>
<td valign="top"><a href="#long">Long</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>in</strong></td>
<td valign="top">[<a href="#long">Long</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>nin</strong></td>
<td valign="top">[<a href="#long">Long</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>gt</strong></td>
<td valign="top"><a href="#long">Long</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ngt</strong></td>
<td valign="top"><a href="#long">Long</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>gte</strong></td>
<td valign="top"><a href="#long">Long</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ngte</strong></td>
<td valign="top"><a href="#long">Long</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>lt</strong></td>
<td valign="top"><a href="#long">Long</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>nlt</strong></td>
<td valign="top"><a href="#long">Long</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>lte</strong></td>
<td valign="top"><a href="#long">Long</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>nlte</strong></td>
<td valign="top"><a href="#long">Long</a></td>
<td></td>
</tr>
</tbody>
</table>

### ConditionGroupInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>operator</strong></td>
<td valign="top"><a href="#conditiongroupoperator">ConditionGroupOperator</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>conditions</strong></td>
<td valign="top">[<a href="#conditioninput">ConditionInput</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>conditionGroups</strong></td>
<td valign="top">[<a href="#conditiongroupinput">ConditionGroupInput</a>!]!</td>
<td></td>
</tr>
</tbody>
</table>

### ConditionInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>fieldName</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dataFieldId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>operator</strong></td>
<td valign="top"><a href="#operator">Operator</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>value</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### CreateAccountGroupInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

255 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>permissionKeys</strong></td>
<td valign="top">[<a href="#string">String</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>lists</strong></td>
<td valign="top">[<a href="#string">String</a>!]</td>
<td></td>
</tr>
</tbody>
</table>

### CreateAccountInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

Unique name to reference the account. *Max length: 255*

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>streetAddressLine1</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>streetAddressLine2</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

50 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>city</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>state_Province</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>zip_PostalCode</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

15 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>country_Region</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>phone</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

25 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>website</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

255 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>defaultLanguage</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Must be a valid [culture code](https://docs.microsoft.com/en-us/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) or set to "Auto".

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>defaultTimezone</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Must be a valid [IANA timezone](https://www.iana.org/time-zones) or set to "Auto".

</td>
</tr>
</tbody>
</table>

### CreateArticleContentInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>mimeType</strong></td>
<td valign="top"><a href="#mimetype">MimeType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>content</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CreateArticleInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>folderId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>title</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>language</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Must be a valid [culture code](https://docs.microsoft.com/en-us/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) or set to "Auto".

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>defaultLayout</strong></td>
<td valign="top"><a href="#articledefaultlayout">ArticleDefaultLayout</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>category</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

50 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

255 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#string">String</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>contentBodies</strong></td>
<td valign="top">[<a href="#createarticlecontentinput">CreateArticleContentInput</a>!]</td>
<td></td>
</tr>
</tbody>
</table>

### CreateCampaignViewInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#string">String</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>statuses</strong></td>
<td valign="top">[<a href="#campaignsendstatus">CampaignSendStatus</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sendStartUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sendEndUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedStartUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedEndUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdStartUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdEndUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>groupBy</strong></td>
<td valign="top"><a href="#campaignfields">CampaignFields</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sortBy</strong></td>
<td valign="top"><a href="#campaignfields">CampaignFields</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPrivate</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CreateCategoryInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>categoryName</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CreateDataFieldInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>dataType</strong></td>
<td valign="top"><a href="#datatype">DataType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>fieldName</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

50 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dscr</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

200 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>required</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPublic</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>mergeTag</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

50 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>defaultValue</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

255 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>possibleValues</strong></td>
<td valign="top">[<a href="#createdatafieldvalueinput">CreateDataFieldValueInput</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>valueType</strong></td>
<td valign="top"><a href="#fieldvaluetype">FieldValueType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>minNbr</strong></td>
<td valign="top"><a href="#decimal">Decimal</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>maxNbr</strong></td>
<td valign="top"><a href="#decimal">Decimal</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>minDate</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>maxDate</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>allowOther</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>monthDayFormat</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberListId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CreateDataFieldLanguageLabelInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>language</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

Must be a valid [culture code](https://docs.microsoft.com/en-us/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>label</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
</tbody>
</table>

### CreateDataFieldValueInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>language</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>label</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>value</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>languageLabels</strong></td>
<td valign="top">[<a href="#createdatafieldlanguagelabelinput">CreateDataFieldLanguageLabelInput</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>displayOrder</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CreateExportInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>subscriberListId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>notificationEmail</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

320 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>delimiter</strong></td>
<td valign="top"><a href="#filedelimiter">FileDelimiter</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberStatus</strong></td>
<td valign="top"><a href="#subscriberstatus">SubscriberStatus</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>entireList</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>allFields</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>allBehaviors</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>groupIds</strong></td>
<td valign="top">[<a href="#string">String</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>fields</strong></td>
<td valign="top">[<a href="#string">String</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>behaviors</strong></td>
<td valign="top">[<a href="#string">String</a>!]</td>
<td></td>
</tr>
</tbody>
</table>

### CreateFileViewInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#string">String</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>types</strong></td>
<td valign="top">[<a href="#filetype">FileType</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedStartUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedEndUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdStartUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdEndUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>groupBy</strong></td>
<td valign="top"><a href="#filefields">FileFields</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sortBy</strong></td>
<td valign="top"><a href="#filefields">FileFields</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPrivate</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CreateFolderInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>parentId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

50 character limit

</td>
</tr>
</tbody>
</table>

### CreateFormInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#formtype">FormType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberListId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### CreateGroupInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

255 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPublic</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isDynamic</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sourceGroupIds</strong></td>
<td valign="top">[<a href="#string">String</a>!]!</td>
<td>

Use to combine groups previously created

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>criteria</strong></td>
<td valign="top"><a href="#conditiongroupinput">ConditionGroupInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberListId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CreateGroupSubscriberInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>groupId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>groupName</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CreateImportInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>subscriberListId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dataFileId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>groups</strong></td>
<td valign="top">[<a href="#string">String</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>columns</strong></td>
<td valign="top">[<a href="#datacolumninput">DataColumnInput</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteArea</strong></td>
<td valign="top"><a href="#importdeletearea">ImportDeleteArea</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>update</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>unsubscribe</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>skipFirstRow</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>confirmEmail</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

320 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>delimiter</strong></td>
<td valign="top"><a href="#filedelimiter">FileDelimiter</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CreatePaymentMethodInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>nickname</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isDefault</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>creditCardInfo</strong></td>
<td valign="top"><a href="#addcreditcardinfoinput">AddCreditCardInfoInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>billingAddress</strong></td>
<td valign="top"><a href="#addbillingaddressinput">AddBillingAddressInput</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CreateProfileFieldInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>dataFieldId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>labelText</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CreateQuestionCategoryInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>text</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>answers</strong></td>
<td valign="top">[<a href="#string">String</a>!]!</td>
<td></td>
</tr>
</tbody>
</table>

### CreateQuestionInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#questiontype">QuestionType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>text</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dataFieldId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>required</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>display</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>displayOrder</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>categories</strong></td>
<td valign="top">[<a href="#createquestioncategoryinput">CreateQuestionCategoryInput</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>answers</strong></td>
<td valign="top">[<a href="#string">String</a>!]</td>
<td></td>
</tr>
</tbody>
</table>

### CreateSenderDomainInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>domain</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

65 character limit

</td>
</tr>
</tbody>
</table>

### CreateSubscriberConversationInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>subscriberId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>fromSubscriber</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>message</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CreateSubscriberInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>subscriberIp</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Needs to be in valid Ip format (000.000.000.000)

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>longitude</strong></td>
<td valign="top"><a href="#decimal">Decimal</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>latitude</strong></td>
<td valign="top"><a href="#decimal">Decimal</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>city</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>state_Province</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>zip_PostalCode</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

15 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>country_Region</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>timeZone</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>cultureCode</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>email</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sendFormat</strong></td>
<td valign="top"><a href="#sendformat">SendFormat</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>optInDateTimeUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>optInIp</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>optOutDateTimeUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>optOutSource</strong></td>
<td valign="top"><a href="#optoutsource">OptOutSource</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>optOutIp</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>optOutReason</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberListId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>groups</strong></td>
<td valign="top">[<a href="#creategroupsubscriberinput">CreateGroupSubscriberInput</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>profile</strong></td>
<td valign="top">[<a href="#createprofilefieldinput">CreateProfileFieldInput</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#string">String</a>!]!</td>
<td></td>
</tr>
</tbody>
</table>

### CreateSubscriberListInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#string">String</a>!]</td>
<td>

50 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>companyName</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

255 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>streetAddressLine1</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>streetAddressLine2</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

50 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>city</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>state_Province</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>zip_PostalCode</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

15 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>country_Region</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>phone</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

25 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>groupIds</strong></td>
<td valign="top">[<a href="#string">String</a>!]</td>
<td></td>
</tr>
</tbody>
</table>

### CreateSubscriberListSecurityGroupInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>securityGroupId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberListId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CreateSubscriberListViewInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#string">String</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>minOpenRate</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>maxOpenRate</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>minClickRate</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>maxClickRate</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>groupBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sortBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPrivate</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CreateSubscriberNoteInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>subscriberId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>message</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

255 character limit

</td>
</tr>
</tbody>
</table>

### CreateTagInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>tagName</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CreateTemplateInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>referenceTemplateId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>listId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#string">String</a>!]</td>
<td></td>
</tr>
</tbody>
</table>

### CreateTemplateViewInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#string">String</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>types</strong></td>
<td valign="top">[<a href="#templatetype">TemplateType</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedStartUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedEndUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdStartUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdEndUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>groupBy</strong></td>
<td valign="top"><a href="#templatefields">TemplateFields</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sortBy</strong></td>
<td valign="top"><a href="#templatefields">TemplateFields</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPrivate</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CreateTransactionInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>groupName</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>settings</strong></td>
<td valign="top"><a href="#transactionsettingsinput">TransactionSettingsInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#string">String</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>metadata</strong></td>
<td valign="top">[<a href="#namevalueinput">NameValueInput</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>header</strong></td>
<td valign="top"><a href="#transactionheaderinput">TransactionHeaderInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>content</strong></td>
<td valign="top"><a href="#transactioncontentinput">TransactionContentInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>variables</strong></td>
<td valign="top">[<a href="#namevalueinput">NameValueInput</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>recipients</strong></td>
<td valign="top">[<a href="#transactionrecipientinput">TransactionRecipientInput</a>!]!</td>
<td></td>
</tr>
</tbody>
</table>

### CreateUrlFileInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>folderId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

100 character limit. If not passed, the file name will be used.

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>fileUrl</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#string">String</a>!]</td>
<td>

50 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>overwrite</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td>

Defaults to false if not passed.

</td>
</tr>
</tbody>
</table>

### CreateUserAccountGroupInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>groupId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CreateUserInviteInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>firstName</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>lastName</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>emailAddress</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

320 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>accountGroupIds</strong></td>
<td valign="top">[<a href="#string">String</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>message</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

255 character limit

</td>
</tr>
</tbody>
</table>

### DataColumnInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>skip</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>fieldName</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

50 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dataFieldId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### DeleteCategoryInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>categoryName</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### DeleteDataFieldInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberListId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### DeleteFormInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>formId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberListId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### DeleteGroupInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberListId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### DeleteSubscriberListSecurityGroupInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>securityGroupId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberListId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### DeleteSubscriberNoteInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### DeleteTagInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>tagName</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### DeleteUserAccountGroupInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>groupId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### EmailFilterInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>and</strong></td>
<td valign="top">[<a href="#emailfilterinput">EmailFilterInput</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>or</strong></td>
<td valign="top">[<a href="#emailfilterinput">EmailFilterInput</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>domain</strong></td>
<td valign="top"><a href="#stringoperationfilterinput">StringOperationFilterInput</a></td>
<td>

255 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>localPart</strong></td>
<td valign="top"><a href="#stringoperationfilterinput">StringOperationFilterInput</a></td>
<td>

65 character limit

</td>
</tr>
</tbody>
</table>

### ExportFormInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>formId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberListId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>style</strong></td>
<td valign="top"><a href="#formexportstyle">FormExportStyle</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>includeValidation</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>includePageHtml</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>includeArchiveLink</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### GetAllFilesInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>folderId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>fileViewId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>partialName</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

50 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#string">String</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>types</strong></td>
<td valign="top">[<a href="#filetype">FileType</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedStartUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedEndUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdStartUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdEndUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPrivate</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
</tbody>
</table>

### GetAllSubscriberListsInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>partialName</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberListViewId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#string">String</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>minOpenRate</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>maxOpenRate</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>minClickRate</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>maxClickRate</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>groupBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sortBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### GetAllTemplatesInfoInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>category</strong></td>
<td valign="top"><a href="#templatecategory">TemplateCategory</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subcategory</strong></td>
<td valign="top"><a href="#templatesubcategory">TemplateSubCategory</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#templatetype">TemplateType</a></td>
<td></td>
</tr>
</tbody>
</table>

### GetAllTemplatesInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>partialName</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>templateViewId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#string">String</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>types</strong></td>
<td valign="top">[<a href="#templatetype">TemplateType</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedStartUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedEndUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdStartUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdEndUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>groupBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sortBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPrivate</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
</tbody>
</table>

### GetArticleContentInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>recovery</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
</tbody>
</table>

### GetExportInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>subscriberListId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### GetQuestionInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>formId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### GetTemplateContentInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>recovery</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
</tbody>
</table>

### GroupInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#long">Long</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPublic</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isDynamic</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>totalSubscribers</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>totalActiveSubscribers</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>totalUnconfirmedSubscribers</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>totalUndeliverableSubscribers</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>totalUnsubscribedSubscribers</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>totalComplaintSubscribers</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>groupSubscribers</strong></td>
<td valign="top">[<a href="#groupsubscriberinput">GroupSubscriberInput</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### GroupSubscriberInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>subscriberId</strong></td>
<td valign="top"><a href="#long">Long</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>groupId</strong></td>
<td valign="top"><a href="#long">Long</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>group</strong></td>
<td valign="top"><a href="#groupinput">GroupInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>accountId</strong></td>
<td valign="top"><a href="#long">Long</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### InviteFilterInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>and</strong></td>
<td valign="top">[<a href="#invitefilterinput">InviteFilterInput</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>or</strong></td>
<td valign="top">[<a href="#invitefilterinput">InviteFilterInput</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#comparableint64operationfilterinput">ComparableInt64OperationFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>firstName</strong></td>
<td valign="top"><a href="#stringoperationfilterinput">StringOperationFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>lastName</strong></td>
<td valign="top"><a href="#stringoperationfilterinput">StringOperationFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>emailAddr</strong></td>
<td valign="top"><a href="#emailfilterinput">EmailFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>securityGroupIds</strong></td>
<td valign="top"><a href="#stringoperationfilterinput">StringOperationFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>inviteStatus</strong></td>
<td valign="top"><a href="#invitestatusoperationfilterinput">InviteStatusOperationFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdUtc</strong></td>
<td valign="top"><a href="#comparabledatetimeoperationfilterinput">ComparableDateTimeOperationFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>accountId</strong></td>
<td valign="top"><a href="#comparableint64operationfilterinput">ComparableInt64OperationFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>userId</strong></td>
<td valign="top"><a href="#comparableint64operationfilterinput">ComparableInt64OperationFilterInput</a></td>
<td></td>
</tr>
</tbody>
</table>

### InviteStatusOperationFilterInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>eq</strong></td>
<td valign="top"><a href="#invitestatus">InviteStatus</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>neq</strong></td>
<td valign="top"><a href="#invitestatus">InviteStatus</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>in</strong></td>
<td valign="top">[<a href="#invitestatus">InviteStatus</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>nin</strong></td>
<td valign="top">[<a href="#invitestatus">InviteStatus</a>!]</td>
<td></td>
</tr>
</tbody>
</table>

### ListFilterInputTypeOfServicePlanCreditItemFilterInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>all</strong></td>
<td valign="top"><a href="#serviceplancreditfilterinput">ServicePlanCreditFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>none</strong></td>
<td valign="top"><a href="#serviceplancreditfilterinput">ServicePlanCreditFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>some</strong></td>
<td valign="top"><a href="#serviceplancreditfilterinput">ServicePlanCreditFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>any</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
</tbody>
</table>

### ListFilterInputTypeOfServicePlanFeatureViewModelFilterInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>all</strong></td>
<td valign="top"><a href="#serviceplanfeaturefilterinput">ServicePlanFeatureFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>none</strong></td>
<td valign="top"><a href="#serviceplanfeaturefilterinput">ServicePlanFeatureFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>some</strong></td>
<td valign="top"><a href="#serviceplanfeaturefilterinput">ServicePlanFeatureFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>any</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
</tbody>
</table>

### ListFilterInputTypeOfServicePlanScaleFilterInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>all</strong></td>
<td valign="top"><a href="#serviceplanscalefilterinput">ServicePlanScaleFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>none</strong></td>
<td valign="top"><a href="#serviceplanscalefilterinput">ServicePlanScaleFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>some</strong></td>
<td valign="top"><a href="#serviceplanscalefilterinput">ServicePlanScaleFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>any</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
</tbody>
</table>

### NameValueInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>value</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### PublishFormInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>formId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberListId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### SendDomainInfoInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>domain</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

65 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>emailAddr</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

300 character limit

</td>
</tr>
</tbody>
</table>

### ServicePlanCreditFilterInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>and</strong></td>
<td valign="top">[<a href="#serviceplancreditfilterinput">ServicePlanCreditFilterInput</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>or</strong></td>
<td valign="top">[<a href="#serviceplancreditfilterinput">ServicePlanCreditFilterInput</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#comparableint64operationfilterinput">ComparableInt64OperationFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>qty</strong></td>
<td valign="top"><a href="#comparabledoubleoperationfilterinput">ComparableDoubleOperationFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>fee</strong></td>
<td valign="top"><a href="#comparabledoubleoperationfilterinput">ComparableDoubleOperationFilterInput</a></td>
<td></td>
</tr>
</tbody>
</table>

### ServicePlanFeatureFilterInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>and</strong></td>
<td valign="top">[<a href="#serviceplanfeaturefilterinput">ServicePlanFeatureFilterInput</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>or</strong></td>
<td valign="top">[<a href="#serviceplanfeaturefilterinput">ServicePlanFeatureFilterInput</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#stringoperationfilterinput">StringOperationFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#stringoperationfilterinput">StringOperationFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#stringoperationfilterinput">StringOperationFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>limit</strong></td>
<td valign="top"><a href="#comparableint32operationfilterinput">ComparableInt32OperationFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>limitDescription</strong></td>
<td valign="top"><a href="#stringoperationfilterinput">StringOperationFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>_do</strong></td>
<td valign="top"><a href="#comparableint32operationfilterinput">ComparableInt32OperationFilterInput</a></td>
<td>

Internal use only

</td>
</tr>
</tbody>
</table>

### ServicePlanFilterInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>and</strong></td>
<td valign="top">[<a href="#serviceplanfilterinput">ServicePlanFilterInput</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>or</strong></td>
<td valign="top">[<a href="#serviceplanfilterinput">ServicePlanFilterInput</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#stringoperationfilterinput">StringOperationFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#stringoperationfilterinput">StringOperationFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#stringoperationfilterinput">StringOperationFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>serviceType</strong></td>
<td valign="top"><a href="#servicetypeoperationfilterinput">ServiceTypeOperationFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>creditValue</strong></td>
<td valign="top"><a href="#comparabledoubleoperationfilterinput">ComparableDoubleOperationFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>_do</strong></td>
<td valign="top"><a href="#comparableint32operationfilterinput">ComparableInt32OperationFilterInput</a></td>
<td>

Internal use only

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>scales</strong></td>
<td valign="top"><a href="#listfilterinputtypeofserviceplanscalefilterinput">ListFilterInputTypeOfServicePlanScaleFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>credits</strong></td>
<td valign="top"><a href="#listfilterinputtypeofserviceplancredititemfilterinput">ListFilterInputTypeOfServicePlanCreditItemFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>features</strong></td>
<td valign="top"><a href="#listfilterinputtypeofserviceplanfeatureviewmodelfilterinput">ListFilterInputTypeOfServicePlanFeatureViewModelFilterInput</a></td>
<td></td>
</tr>
</tbody>
</table>

### ServicePlanScaleFilterInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>and</strong></td>
<td valign="top">[<a href="#serviceplanscalefilterinput">ServicePlanScaleFilterInput</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>or</strong></td>
<td valign="top">[<a href="#serviceplanscalefilterinput">ServicePlanScaleFilterInput</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#comparableint64operationfilterinput">ComparableInt64OperationFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>minLimit</strong></td>
<td valign="top"><a href="#comparableint32operationfilterinput">ComparableInt32OperationFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>maxLimit</strong></td>
<td valign="top"><a href="#comparableint32operationfilterinput">ComparableInt32OperationFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>fee</strong></td>
<td valign="top"><a href="#comparabledoubleoperationfilterinput">ComparableDoubleOperationFilterInput</a></td>
<td></td>
</tr>
</tbody>
</table>

### ServiceTypeOperationFilterInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>eq</strong></td>
<td valign="top"><a href="#servicetype">ServiceType</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>neq</strong></td>
<td valign="top"><a href="#servicetype">ServiceType</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>in</strong></td>
<td valign="top">[<a href="#servicetype">ServiceType</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>nin</strong></td>
<td valign="top">[<a href="#servicetype">ServiceType</a>!]</td>
<td></td>
</tr>
</tbody>
</table>

### StringOperationFilterInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>and</strong></td>
<td valign="top">[<a href="#stringoperationfilterinput">StringOperationFilterInput</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>or</strong></td>
<td valign="top">[<a href="#stringoperationfilterinput">StringOperationFilterInput</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>eq</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>neq</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>contains</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ncontains</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>in</strong></td>
<td valign="top">[<a href="#string">String</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>nin</strong></td>
<td valign="top">[<a href="#string">String</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>startsWith</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>nstartsWith</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>endsWith</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>nendsWith</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### SubmitAccountPaymentInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>invoiceId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>paymentMethodId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### TransactionAnalyticsInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>enable</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>parameters</strong></td>
<td valign="top">[<a href="#namevalueinput">NameValueInput</a>!]</td>
<td>

Name: 50 character limit  Value: 50 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>domains</strong></td>
<td valign="top">[<a href="#transactiondomainanalyticsinput">TransactionDomainAnalyticsInput</a>!]</td>
<td></td>
</tr>
</tbody>
</table>

### TransactionContentBodyInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>clickTracking</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>charset</strong></td>
<td valign="top"><a href="#charset">Charset</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>mimeType</strong></td>
<td valign="top"><a href="#mimetype">MimeType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>bodyContent</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### TransactionContentInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>templateId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Not currently supported

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>contentBodies</strong></td>
<td valign="top">[<a href="#transactioncontentbodyinput">TransactionContentBodyInput</a>!]!</td>
<td></td>
</tr>
</tbody>
</table>

### TransactionContentSettingsInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>autoGenerateText</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>autoGenerateHtml</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### TransactionDomainAnalyticsInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>domain</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

65 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>parameters</strong></td>
<td valign="top">[<a href="#namevalueinput">NameValueInput</a>!]</td>
<td>

Name: 50 character limit  Value: 50 character limit

</td>
</tr>
</tbody>
</table>

### TransactionFromInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

255 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>emailAddress</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

320 character limit

</td>
</tr>
</tbody>
</table>

### TransactionHeaderInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>subject</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

500 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>from</strong></td>
<td valign="top"><a href="#transactionfrominput">TransactionFromInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>replyTo</strong></td>
<td valign="top"><a href="#transactionreplytoinput">TransactionReplyToInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>customHeaders</strong></td>
<td valign="top">[<a href="#namevalueinput">NameValueInput</a>!]</td>
<td></td>
</tr>
</tbody>
</table>

### TransactionRecipientInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

255 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>emailAddress</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

320 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#recipienttype">RecipientType</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>metadata</strong></td>
<td valign="top">[<a href="#namevalueinput">NameValueInput</a>!]</td>
<td>

Name: 50 character limit  Value: 255 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>variables</strong></td>
<td valign="top">[<a href="#namevalueinput">NameValueInput</a>!]</td>
<td></td>
</tr>
</tbody>
</table>

### TransactionReplyToInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

255 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>emailAddress</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

320 character limit

</td>
</tr>
</tbody>
</table>

### TransactionSandboxInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>enable</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>errorType</strong></td>
<td valign="top"><a href="#sandboxerrortype">SandboxErrorType</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### TransactionSettingsInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>sendAtUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tracking</strong></td>
<td valign="top"><a href="#transactiontrackinginput">TransactionTrackingInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sendRepliesTo</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

320 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sendBccTo</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

320 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>showRecipients</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ignoreSuppressCheck</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sandbox</strong></td>
<td valign="top"><a href="#transactionsandboxinput">TransactionSandboxInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>content</strong></td>
<td valign="top"><a href="#transactioncontentsettingsinput">TransactionContentSettingsInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>enableViewOnline</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>analytics</strong></td>
<td valign="top"><a href="#transactionanalyticsinput">TransactionAnalyticsInput</a></td>
<td></td>
</tr>
</tbody>
</table>

### TransactionTrackingInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>opens</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>clicks</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>stripQueryString</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>replies</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### UpdateAccountGroupInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

255 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>permissionKeys</strong></td>
<td valign="top">[<a href="#string">String</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>lists</strong></td>
<td valign="top">[<a href="#long">Long</a>!]</td>
<td></td>
</tr>
</tbody>
</table>

### UpdateAccountInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>ownerId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

255 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>streetAddressLine1</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>streetAddressLine2</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

50 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>city</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>state_Province</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>zip_PostalCode</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

15 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>country_Region</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>phone</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

25 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>website</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

255 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>defaultLanguage</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Must be a valid [culture code](https://docs.microsoft.com/en-us/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) or set to "Auto".

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>defaultTimezone</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Must be a valid [IANA timezone](https://www.iana.org/time-zones) or set to "Auto".

</td>
</tr>
</tbody>
</table>

### UpdateAccountStatusInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>status</strong></td>
<td valign="top"><a href="#accountstatus">AccountStatus</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>reason</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

255 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>exportAccountData</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>customerSupportRating</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>

Number between 1 and 5

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>feedback</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

500 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>paymentMethodId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### UpdateArticleContentInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>mimeType</strong></td>
<td valign="top"><a href="#mimetype">MimeType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>content</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### UpdateArticleInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>folderId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>title</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>language</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Must be a valid [culture code](https://docs.microsoft.com/en-us/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) or set to "Auto".

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>defaultLayout</strong></td>
<td valign="top"><a href="#articledefaultlayout">ArticleDefaultLayout</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>category</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

50 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

255 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#string">String</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>contentBodies</strong></td>
<td valign="top">[<a href="#updatearticlecontentinput">UpdateArticleContentInput</a>!]</td>
<td></td>
</tr>
</tbody>
</table>

### UpdateBillingAddressInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>firstName</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>lastName</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>emailAddr</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

320 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>streetAddressLine1</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>streetAddressLine2</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

50 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>city</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>state_Province</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>zip_PostalCode</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

15 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>country_Region</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>phone</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

25 character limit

</td>
</tr>
</tbody>
</table>

### UpdateCampaignViewInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#string">String</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>statuses</strong></td>
<td valign="top">[<a href="#campaignsendstatus">CampaignSendStatus</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sendStartUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sendEndUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedStartUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedEndUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdStartUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdEndUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>groupBy</strong></td>
<td valign="top"><a href="#campaignfields">CampaignFields</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sortBy</strong></td>
<td valign="top"><a href="#campaignfields">CampaignFields</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPrivate</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
</tbody>
</table>

### UpdateCreditCardInfoInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>expirationMonth</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td>

1-12

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>expirationYear</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td>

yyyy format (ex: 2021)

</td>
</tr>
</tbody>
</table>

### UpdateDataFieldInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dataType</strong></td>
<td valign="top"><a href="#datatype">DataType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>fieldName</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

50 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dscr</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

200 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>required</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPublic</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>mergeTag</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

50 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>defaultValue</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

255 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>possibleValues</strong></td>
<td valign="top">[<a href="#updatedatafieldvalueinput">UpdateDataFieldValueInput</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>valueType</strong></td>
<td valign="top"><a href="#fieldvaluetype">FieldValueType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>minNbr</strong></td>
<td valign="top"><a href="#decimal">Decimal</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>maxNbr</strong></td>
<td valign="top"><a href="#decimal">Decimal</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>minDate</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>maxDate</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>allowOther</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>monthDayFormat</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberListId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### UpdateDataFieldValueInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>label</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>value</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>displayOrder</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### UpdateDoubleOptInContentInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>email</strong></td>
<td valign="top"><a href="#updatedoubleoptinemailinput">UpdateDoubleOptInEmailInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>pageHtml</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### UpdateDoubleOptInEmailInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>fromName</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>fromEmail</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subject</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>replyTo</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### UpdateFileInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>folderId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#string">String</a>!]</td>
<td></td>
</tr>
</tbody>
</table>

### UpdateFileViewInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#string">String</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>types</strong></td>
<td valign="top">[<a href="#filetype">FileType</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedStartUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedEndUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdStartUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdEndUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>groupBy</strong></td>
<td valign="top"><a href="#filefields">FileFields</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sortBy</strong></td>
<td valign="top"><a href="#filefields">FileFields</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPrivate</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
</tbody>
</table>

### UpdateFolderInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>parentId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### UpdateGroupInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

255 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPublic</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isDynamic</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sourceGroupIds</strong></td>
<td valign="top">[<a href="#string">String</a>!]!</td>
<td>

Use to combine groups previously created

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>criteria</strong></td>
<td valign="top"><a href="#conditiongroupinput">ConditionGroupInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberListId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### UpdateGroupSubscriberInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>groupId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>groupName</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### UpdatePaymentMethodInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>nickname</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isDefault</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>creditCardInfo</strong></td>
<td valign="top"><a href="#updatecreditcardinfoinput">UpdateCreditCardInfoInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>billingAddress</strong></td>
<td valign="top"><a href="#updatebillingaddressinput">UpdateBillingAddressInput</a></td>
<td></td>
</tr>
</tbody>
</table>

### UpdateProfileFieldInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>dataFieldId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>labelText</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### UpdateQuestionCategoryInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>text</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>answers</strong></td>
<td valign="top">[<a href="#string">String</a>!]!</td>
<td></td>
</tr>
</tbody>
</table>

### UpdateQuestionInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#questiontype">QuestionType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>text</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>dataFieldId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>required</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>display</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>displayOrder</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>categories</strong></td>
<td valign="top">[<a href="#updatequestioncategoryinput">UpdateQuestionCategoryInput</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>answers</strong></td>
<td valign="top">[<a href="#string">String</a>!]</td>
<td></td>
</tr>
</tbody>
</table>

### UpdateSubscriberInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberIp</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Needs to be in valid Ip format (000.000.000.000)

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>longitude</strong></td>
<td valign="top"><a href="#decimal">Decimal</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>latitude</strong></td>
<td valign="top"><a href="#decimal">Decimal</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>city</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>state_Province</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>zip_PostalCode</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

15 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>country_Region</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>timeZone</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>cultureCode</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>email</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sendFormat</strong></td>
<td valign="top"><a href="#sendformat">SendFormat</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>optInDateTimeUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>optInIp</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>optOutDateTimeUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>optOutSource</strong></td>
<td valign="top"><a href="#optoutsource">OptOutSource</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>optOutIp</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>optOutReason</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>subscriberListId</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>groups</strong></td>
<td valign="top">[<a href="#updategroupsubscriberinput">UpdateGroupSubscriberInput</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>profile</strong></td>
<td valign="top">[<a href="#updateprofilefieldinput">UpdateProfileFieldInput</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#string">String</a>!]!</td>
<td></td>
</tr>
</tbody>
</table>

### UpdateSubscriberListFormDialogInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#formdialogtype">FormDialogType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>message</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>thankYouIcon</strong></td>
<td valign="top"><a href="#formdialogicon">FormDialogIcon</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>iconColor</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>displayRedirectButton</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>redirectButtonText</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>redirectButtonUrl</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>redirectButtonColor</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>showRedirectButton</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>buttonText</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>redirectUrl</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>displayCloseButton</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>displayResults</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>displayAnswers</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
</tbody>
</table>

### UpdateSubscriberListFormInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>pageName</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>pageTitle</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>metaDescription</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>metaKeywords</strong></td>
<td valign="top">[<a href="#string">String</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>socialStoryImageUrl</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>defaultLanguage</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>translationLanguages</strong></td>
<td valign="top">[<a href="#string">String</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>requiredTextTranslation</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>formErrorTextTranslation</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>redirectUrl</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>submitAction</strong></td>
<td valign="top"><a href="#formaction">FormAction</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sendThankYou</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>groups</strong></td>
<td valign="top">[<a href="#groupinput">GroupInput</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#string">String</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sendNotificationEmail</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>attachmentFormat</strong></td>
<td valign="top"><a href="#formattachmentformat">FormAttachmentFormat</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>duplicateEmailAction</strong></td>
<td valign="top"><a href="#formduplicateemailaction">FormDuplicateEmailAction</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>duplicateEmailErrorAction</strong></td>
<td valign="top"><a href="#formaction">FormAction</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>duplicateEmailErrorRedirectUrl</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### UpdateSubscriberListFormPageInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#formpagetype">FormPageType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>content</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### UpdateSubscriberListInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#string">String</a>!]</td>
<td>

50 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>companyName</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

255 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>streetAddressLine1</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>streetAddressLine2</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

50 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>city</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>state_Province</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>zip_PostalCode</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

15 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>country_Region</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>phone</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

25 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>defaultFromName</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

50 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>defaultFromEmail</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

320 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>requireDoubleOptIn</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
</tbody>
</table>

### UpdateSubscriberListViewInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#string">String</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>minOpenRate</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>maxOpenRate</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>minClickRate</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>maxClickRate</strong></td>
<td valign="top"><a href="#float">Float</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>groupBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sortBy</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPrivate</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
</tbody>
</table>

### UpdateTemplateContentInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>mimeType</strong></td>
<td valign="top"><a href="#mimetype">MimeType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>content</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### UpdateTemplateInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>contentBodies</strong></td>
<td valign="top">[<a href="#updatetemplatecontentinput">UpdateTemplateContentInput</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#string">String</a>!]</td>
<td></td>
</tr>
</tbody>
</table>

### UpdateTemplateViewInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#string">String</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>types</strong></td>
<td valign="top">[<a href="#templatetype">TemplateType</a>!]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedStartUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>modifiedEndUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdStartUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createdEndUtc</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>groupBy</strong></td>
<td valign="top"><a href="#templatefields">TemplateFields</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sortBy</strong></td>
<td valign="top"><a href="#templatefields">TemplateFields</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPrivate</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
</tbody>
</table>

### UpdateUserInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>firstName</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>lastName</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

100 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>phoneNumber</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

25 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>language</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Must be a valid [culture code](https://docs.microsoft.com/en-us/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) or set to "Auto".

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isActive</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>timezone</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Must be a valid [IANA timezone](https://www.iana.org/time-zones) or set to "Auto".

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>theme</strong></td>
<td valign="top"><a href="#apptheme">AppTheme</a></td>
<td></td>
</tr>
</tbody>
</table>

### VerifySenderDomainInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>dkimSelector</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

255 character limit

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>domain</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td>

65 character limit

</td>
</tr>
</tbody>
</table>

## Enums

### AccountStatus

SUSPEND status can only be set by a system user

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>ACTIVE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>RELAX</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>HIBERNATE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>_SUSPEND</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>DELETE</strong></td>
<td></td>
</tr>
</tbody>
</table>

### AppTheme

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>LIGHT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>DARK</strong></td>
<td></td>
</tr>
</tbody>
</table>

### ApplyPolicy

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>BEFORE_RESOLVER</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>AFTER_RESOLVER</strong></td>
<td></td>
</tr>
</tbody>
</table>

### ArticleDefaultLayout

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>PTL_TTR_CBR</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PTR_TTL_CBL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PTC_TCC_CBC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PBC_TTC_CCC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PNA_TTL_CBL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PTL_TNA_CTR</strong></td>
<td></td>
</tr>
</tbody>
</table>

### CampaignFields

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>NAME</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SEND_DATE</strong></td>
<td></td>
</tr>
</tbody>
</table>

### CampaignSendStatus

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>NOT_SCHEDULED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PENDING</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>QUEUED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PROCESSING</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PAUSED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>STOPPED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SENT_PENDING_AB_WINNER</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>COMPLETED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SYSTEM_STOPPED</strong></td>
<td></td>
</tr>
</tbody>
</table>

### CardDeclineReason

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>NO_REASON</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>INSUFFICIENT_FUNDS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>EXPIRED</strong></td>
<td></td>
</tr>
</tbody>
</table>

### Charset

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>UTF8</strong></td>
<td></td>
</tr>
</tbody>
</table>

### ConditionGroupOperator

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>AND</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>OR</strong></td>
<td></td>
</tr>
</tbody>
</table>

### CreditCardNetwork

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>VISA</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>MASTERCARD</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>AMERICAN_EXPRESS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>DISCOVER</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>INTER_LINK</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>STAR</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ACCEL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>INTERAC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>VISA_READY_LINK</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PULSE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>JCB</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>DINERS_CLUB</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>UNKNOWN</strong></td>
<td></td>
</tr>
</tbody>
</table>

### DataType

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>TEXT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>DATE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>DATE_TIME</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>NUMBER</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>BIRTHDAY</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ZIP_CODE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PHONE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>INT_PHONE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>IMAGE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>URL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ADDRESS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>STATE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>COUNTRY</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>EMAIL</strong></td>
<td></td>
</tr>
</tbody>
</table>

### EmailEventType

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>DELIVERED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>OPEN</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CLICK</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>FEEDBACK</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>RATING</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CREATED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PROCESSED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>VIEW_ONLINE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SOCIAL_SHARE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>FORWARD</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>FORWARD_TO_FRIEND</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>VIEW_PROFILE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>VIEW_ARCHIVE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PRINT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>COMPLAINT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>UNSUBSCRIBED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>HARD</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SOFT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SOFT_SENDER_AUTH</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SOFT_IP</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SOFT_DNS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>BLOCK</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>BLOCK_CONTENT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>BLOCK_SENDER</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>DECLINED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>INVALID_EMAIL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SUPPRESSED</strong></td>
<td></td>
</tr>
</tbody>
</table>

### EventSourceType

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>CAMPAIGN</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>TRANSACTION</strong></td>
<td></td>
</tr>
</tbody>
</table>

### ExportStatus

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>ANY</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PENDING</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PROCESSING</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>COMPLETED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>FAILED</strong></td>
<td></td>
</tr>
</tbody>
</table>

### FieldValueType

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>ANY_VALUE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ONE_OF_MANY</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>MANY_OF_MANY</strong></td>
<td></td>
</tr>
</tbody>
</table>

### FileDelimiter

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>TAB</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>COMMA</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SEMICOLON</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PIPE</strong></td>
<td></td>
</tr>
</tbody>
</table>

### FileFields

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>NAME</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SIZE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>IS_PUBLISHED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PUBLISHED_UTC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CATEGORY</strong></td>
<td></td>
</tr>
</tbody>
</table>

### FileType

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>UNKNOWN</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>IMAGE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>FILE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ARTICLE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CONTENT_BLOCK</strong></td>
<td></td>
</tr>
</tbody>
</table>

### FormAction

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>DISPLAY_MESSAGE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>REDIRECT_TO_PAGE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>REDIRECT_TO_URL</strong></td>
<td></td>
</tr>
</tbody>
</table>

### FormAttachmentFormat

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>NO_ATTACHMENT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>JSON</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CSV</strong></td>
<td></td>
</tr>
</tbody>
</table>

### FormDialogIcon

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>CLIPBOARD</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CIRCLE_CHECK_MARK</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>THUMBS_UP</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CHECK_MARK</strong></td>
<td></td>
</tr>
</tbody>
</table>

### FormDialogType

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>SUBMIT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>DUPLICATE_EMAIL</strong></td>
<td></td>
</tr>
</tbody>
</table>

### FormDuplicateEmailAction

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>IGNORE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>UPDATE_SUBSCRIBER</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SHOW_ERROR</strong></td>
<td></td>
</tr>
</tbody>
</table>

### FormEventType

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>VIEW</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ABANDON</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SUBMIT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PARTIAL_SUBMIT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SHARE_EMAIL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SHARE_SOCIAL</strong></td>
<td></td>
</tr>
</tbody>
</table>

### FormExportStyle

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>BASIC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>STANDARD</strong></td>
<td></td>
</tr>
</tbody>
</table>

### FormPageType

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>SUBMIT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>DUPLICATE_EMAIL</strong></td>
<td></td>
</tr>
</tbody>
</table>

### FormType

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>SIGN_UP</strong></td>
<td></td>
</tr>
</tbody>
</table>

### ImportDeleteArea

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>NONE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SUBSCRIBER_LIST</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SELECTED_GROUPS</strong></td>
<td></td>
</tr>
</tbody>
</table>

### ImportStatus

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>ANY</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PENDING</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PROCESSING</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>COMPLETED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>FAILED</strong></td>
<td></td>
</tr>
</tbody>
</table>

### InviteStatus

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>PENDING</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ACCEPTED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>EXPIRED</strong></td>
<td></td>
</tr>
</tbody>
</table>

### InvoiceStatus

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>PAID</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PENDING</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PAYMENT_FAILED</strong></td>
<td></td>
</tr>
</tbody>
</table>

### MimeType

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>HTML</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>TEXT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>AMP</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>MARKDOWN</strong></td>
<td></td>
</tr>
</tbody>
</table>

### Operator

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>EQUAL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>NOT_EQUAL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>GREATER_THAN</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>GREATER_THAN_EQUAL_TO</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>LESS_THAN</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>LESS_THAN_EQUAL_TO</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>STARTS_WITH</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>NOT_START_WITH</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CONTAIN</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>NOT_CONTAIN</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>IS_BLANK</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>NOT_BLANK</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>MONTH_IS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>DAY_IS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>OPENED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>NOT_OPENED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CLICKED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>NOT_CLICKED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SENT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>NOT_SENT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>REPLIED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>NOT_REPLIED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>STARTED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>NOT_STARTED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>COMPLETED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>NOT_COMPLETED</strong></td>
<td></td>
</tr>
</tbody>
</table>

### OptInSource

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>FILE_IMPORT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>URL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>MANUAL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>EMAIL_LINK</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PROFILE_UPDATE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>API</strong></td>
<td></td>
</tr>
</tbody>
</table>

### OptOutSource

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>NONE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>FILE_IMPORT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>URL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>MANUAL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>EMAIL_LINK</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PROFILE_UPDATE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>API</strong></td>
<td></td>
</tr>
</tbody>
</table>

### PaymentStatus

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>APPROVED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>DECLINED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ERROR</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>HELD_FOR_REVIEW</strong></td>
<td></td>
</tr>
</tbody>
</table>

### QuestionType

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>SHORT_TEXT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>LONG_TEXT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>DROPDOWN</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CHECKBOX</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>RADIO</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>HTML_BLOCK</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>MATRIX_CHECKBOX</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>MATRIX_RADIO</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>GROUPS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>HIDDEN</strong></td>
<td></td>
</tr>
</tbody>
</table>

### RawDataType

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>STRING</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>NUMBER</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>DATE_TIME</strong></td>
<td></td>
</tr>
</tbody>
</table>

### RecipientType

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>TO</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>BCC</strong></td>
<td></td>
</tr>
</tbody>
</table>

### ResourceType

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>TEMPLATE</strong></td>
<td></td>
</tr>
</tbody>
</table>

### SandboxErrorType

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>NONE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ERROR</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>INVALID_EMAIL</strong></td>
<td></td>
</tr>
</tbody>
</table>

### SendFormat

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>ANY</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>HTML</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>TEXT</strong></td>
<td></td>
</tr>
</tbody>
</table>

### ServiceType

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>NOT_DEFINED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>EMAIL_MARKETING</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>EMAIL_MARKETING_PREPAY</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>TRANSACTION</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>TRANSACTION_PREPAY</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SMS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SMS_PREPAY</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>FILE_STORAGE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ADDITIONAL_IP</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PROFESSIONAL_SERVICES</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ADDITIONAL_SERVICES</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>EMAIL_MARKETING_DISCOUNT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>EMAIL_MARKETING_PRE_PAY_DISCOUNT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>TRANSACTION_DISCOUNT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>TRANSACTION_PRE_PAY_DISCOUNT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>FEE</strong></td>
<td></td>
</tr>
</tbody>
</table>

### Status

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>ACTIVE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>INACTIVE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>DELETED</strong></td>
<td></td>
</tr>
</tbody>
</table>

### SubscriberListMessageType

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>OPT_IN_CONFIRMATION</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>OPT_IN_NOTIFICATION</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>OPT_IN_WELCOME</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>OPT_OUT_CONFIRM</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>OUT_OUT_NOTIFICATION</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PROFILE_UPDATE_CONFIRM</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PROFILE_UPDATE_NOTIFICATION</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>FORWARD_TO_FRIEND</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>FORWARD_TO_FRIEND_NOTIFICATION</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CONVERSATION_RESPONSE</strong></td>
<td></td>
</tr>
</tbody>
</table>

### SubscriberStatus

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>ANY</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ACTIVE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>UNDELIVERABLE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>OPT_OUT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PENDING_CONFIRM</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SPAM</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CLEANED</strong></td>
<td></td>
</tr>
</tbody>
</table>

### TemplateCategory

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>LAYOUT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>TEMPLATE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CUSTOM_TEMPLATE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CODE_YOUR_OWN</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PREVIOUS_CAMPAIGNS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>START_FROM_SCRATCH</strong></td>
<td></td>
</tr>
</tbody>
</table>

### TemplateFields

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>NAME</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>DESCRIPTION</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>TYPE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CATEGORY</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CREATED_UTC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>MODIFIED_UTC</strong></td>
<td></td>
</tr>
</tbody>
</table>

### TemplateSubCategory

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>NONE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>NEWS_LETTER</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ECOMMERCE</strong></td>
<td></td>
</tr>
</tbody>
</table>

### TemplateType

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>STANDARD</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CUSTOM</strong></td>
<td></td>
</tr>
</tbody>
</table>

### UserStatus

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>ACTIVE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SUSPENDED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>DELETED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>INACTIVE</strong></td>
<td></td>
</tr>
</tbody>
</table>

## Scalars

### Boolean

The `Boolean` scalar type represents `true` or `false`.

### Byte

The `Byte` scalar type represents non-fractional whole numeric values. Byte can represent values between 0 and 255.

### DateTime

The `DateTime` scalar represents an ISO-8601 compliant date time type.

### Decimal

The built-in `Decimal` scalar type.

### Float

The `Float` scalar type represents signed double-precision fractional values as specified by [IEEE 754](http://en.wikipedia.org/wiki/IEEE_floating_point).

### Int

The `Int` scalar type represents non-fractional signed whole numeric values. Int can represent values between -(2^31) and 2^31 - 1.

### Long

The `Long` scalar type represents non-fractional signed whole 64-bit numeric values. Long can represent values between -(2^63) and 2^63 - 1.

### String

The `String` scalar type represents textual data, represented as UTF-8 character sequences. The String type is most often used by GraphQL to represent free-form human-readable text.

