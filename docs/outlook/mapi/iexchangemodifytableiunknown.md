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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 333e1d5cacc069ee1faef01426a1c0a60ef07f8e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418105"
---
# <a name="iexchangemodifytable--iunknown"></a>IExchangeModifyTable : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Prend en charge l'accès aux objets de tableau Microsoft Exchange Server, en particulier les objets de table de liste de contrôle d'accès système (SACL) et les objets de tableau de règles sur les dossiers Microsoft Exchange Server. Cette interface ressemble à l'interface [IMAPITable: IUnknown](imapitableiunknown.md) , mais elle ajoute la prise en charge des structures propres à Microsoft Exchange Server utilisées pour contrôler les listes SACL et les règles. 
  
|||
|:-----|:-----|
|Exposé par:  <br/> |Aucun  <br/> |
|Implémenté par :  <br/> |Objets table de serveur  <br/> |
|Appelé par :  <br/> |Applications MAPI et clientes  <br/> |
|Identificateur de l'interface:  <br/> |IID_IExchangeModifyTable  <br/> |
|Type de pointeur:  <br/> |LPEXCHANGEMODIFYTABLE  <br/> |
|Modèle de transaction:  <br/> |Traitées  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[Généré](iexchangemodifytable-getlasterror.md) <br/> |Renvoie des informations sur la dernière erreur qui s'est produite dans un objet table.  <br/> |
|[GetTable](iexchangemodifytable-gettable.md) <br/> |Renvoie un pointeur vers une interface pour un objet table MAPI.  <br/> |
|[ModifyTable](iexchangemodifytable-modifytable.md) <br/> |Met à jour un objet table MAPI.  <br/> |
   
|**Propriétés utilisées pour modifier un tableau de règles**|**Accès**|
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
   
|**Propriétés utilisées pour modifier une table SACL**|**Accès**|
|:-----|:-----|
|**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))  <br/> |Lecture seule  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir l'interface **IExchangeModifyTable** , appelez la méthode MAPI [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) sur une propriété de type PT_OBJECT sur un objet Folder. Lorsque vous appelez la méthode **OpenProperty** , transmettez la valeur **IID_IExchangeModifyTable** dans le paramètre _lpiid_ . 
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

