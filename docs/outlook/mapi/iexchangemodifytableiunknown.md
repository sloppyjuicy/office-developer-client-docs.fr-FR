---
title: IExchangeModifyTable IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IExchangeModifyTable
api_type:
- COM
ms.assetid: 45a73c7b-5855-4b70-866b-facb41cb3c32
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 095345eb42a269d8bdf0f952ece20b2fc35b3df1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616823"
---
# <a name="iexchangemodifytable--iunknown"></a>IExchangeModifyTable : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Prend en charge l’accès Microsoft Exchange Server objets table, en particulier les objets de table de liste de contrôle d’accès système (SACL) et les objets de table de règles sur Microsoft Exchange Server dossiers. Cette interface ressemble à l’interface [IMAPITable : IUnknown,](imapitableiunknown.md) mais elle ajoute la prise en charge des structures spécifiques Microsoft Exchange Server utilisées pour contrôler les règles et les saclabes. 
  
|||
|:-----|:-----|
|Exposé par :  <br/> |Aucun  <br/> |
|Implémenté par :  <br/> |Objets de table de serveur  <br/> |
|Appelé par :  <br/> |MAPI et applications clientes  <br/> |
|Identificateur d’interface :  <br/> |IID_IExchangeModifyTable  <br/> |
|Type de pointeur :  <br/> |LPEXCHANGEMODIFYTABLE  <br/> |
|Modèle de transaction :  <br/> |Transacted  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[GetLastError](iexchangemodifytable-getlasterror.md) <br/> |Renvoie des informations sur la dernière erreur qui s’est produite dans un objet table.  <br/> |
|[GetTable](iexchangemodifytable-gettable.md) <br/> |Renvoie un pointeur vers une interface pour un objet table MAPI.  <br/> |
|[ModifyTable](iexchangemodifytable-modifytable.md) <br/> |Met à jour un objet table MAPI.  <br/> |
   
|**Propriétés utilisées pour modifier une table de règles**|**Access**|
|:-----|:-----|
|**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))  <br/> |Lecture seule  <br/> |
   
|**Propriétés utilisées pour modifier une table SACL**|**Access**|
|:-----|:-----|
|**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))  <br/> |Lecture seule  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir l’interface **IExchangeModifyTable,** appelez la méthode MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) sur une propriété de type PT_OBJECT sur un objet dossier. Lorsque vous appelez **la méthode OpenProperty,** passez la **valeur IID_IExchangeModifyTable** dans le _paramètre lpiid._ 
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

