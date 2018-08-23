---
title: IExchangeModifyTable IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable
api_type:
- COM
ms.assetid: 45a73c7b-5855-4b70-866b-facb41cb3c32
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 51a83e1e28534cc237419d9c4ae475c1d719c5de
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565073"
---
# <a name="iexchangemodifytable--iunknown"></a>IExchangeModifyTable : IUnknown

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Prend en charge l’accès aux objets de table de Microsoft Exchange Server, spécifiquement l’accès système contrôler des objets liste (SACL) du tableau objets de la table des dossiers Microsoft Exchange Server de la règle. Cette interface ressemble à la [IMAPITable : IUnknown](imapitableiunknown.md) interface, mais elle ajoute la prise en charge pour les structures spécifiques à Microsoft Exchange Server qui sont utilisés pour contrôler les règles et SACL. 
  
|||
|:-----|:-----|
|Exposés par :  <br/> |Aucun  <br/> |
|Implémentée par :  <br/> |Objets de table de serveur  <br/> |
|Appelée par :  <br/> |Applications MAPI et client  <br/> |
|Identificateur de l’interface :  <br/> |IID_IExchangeModifyTable  <br/> |
|Type de pointeur :  <br/> |LPEXCHANGEMODIFYTABLE  <br/> |
|Modèle de transaction :  <br/> |Traitées  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[GetLastError](iexchangemodifytable-getlasterror.md) <br/> |Retourne des informations sur la dernière erreur qui s’est produite dans un objet table.  <br/> |
|[GetTable](iexchangemodifytable-gettable.md) <br/> |Retourne un pointeur vers une interface pour un objet de table MAPI.  <br/> |
|[ModifyTable](iexchangemodifytable-modifytable.md) <br/> |Met à jour un objet de table MAPI.  <br/> |
   
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

Pour obtenir l’interface **IExchangeModifyTable** , appelez la méthode MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) sur une propriété de type PT_OBJECT sur un objet folder. Lorsque vous appelez la méthode **OpenProperty** , transmettez la valeur **IID_IExchangeModifyTable** dans le paramètre _lpiid_ . 
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

