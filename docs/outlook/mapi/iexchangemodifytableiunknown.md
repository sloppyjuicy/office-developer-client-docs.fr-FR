---
title: IExchangeModifyTable IUnknown
description: IExchangeModifyTableIUnknown prend en charge l’accès aux objets de table Microsoft Exchange Server, en particulier aux objets de table SACL et aux objets de table de règles.
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
ms.openlocfilehash: 0dd333c8470441ef79d28fff50e4746465146d1b
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65812318"
---
# <a name="iexchangemodifytable--iunknown"></a>IExchangeModifyTable : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Prend en charge l’accès aux objets de table Microsoft Exchange Server, en particulier aux objets de liste de contrôle d’accès système (SACL) et aux objets de table de règles sur Microsoft Exchange Server dossiers. Cette interface ressemble à l’interface [IMAPITable : IUnknown](imapitableiunknown.md), mais elle ajoute la prise en charge des structures spécifiques à Microsoft Exchange Server qui sont utilisées pour contrôler les règles et les protocoles SACL. 
  
|Propriété |Valeur |
|:-----|:-----|
|Exposé par :  <br/> |Aucun  <br/> |
|Implémenté par :  <br/> |Objets de table de serveur  <br/> |
|Appelé par :  <br/> |MAPI et applications clientes  <br/> |
|Identificateur d’interface :  <br/> |IID_IExchangeModifyTable  <br/> |
|Type de pointeur :  <br/> |LPEXCHANGEMODIFYTABLE  <br/> |
|Modèle de transaction :  <br/> |Traitées  <br/> |
   
## <a name="vtable-order"></a>Ordre des tables virtuelles

|Member |Description |
|:-----|:-----|
|[Getlasterror](iexchangemodifytable-getlasterror.md) <br/> |Retourne des informations sur la dernière erreur qui s’est produite dans un objet table. |
|[GetTable](iexchangemodifytable-gettable.md) <br/> |Retourne un pointeur vers une interface pour un objet de table MAPI. |
|[ModifyTable](iexchangemodifytable-modifytable.md) <br/> |Met à jour un objet de table MAPI. |
   
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

Pour obtenir l’interface **IExchangeModifyTable** , appelez la méthode [MAPI IMAPIProp::OpenProperty](imapiprop-openproperty.md) sur une propriété de type PT_OBJECT sur un objet de dossier. Lorsque vous appelez la méthode **OpenProperty** , transmettez la valeur **IID_IExchangeModifyTable** dans le paramètre _lpiid_ . 
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

