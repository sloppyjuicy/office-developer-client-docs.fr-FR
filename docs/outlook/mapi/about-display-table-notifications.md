---
title: Affichage des notifications de table
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 085151e9-4809-4d2b-ae4d-e318355e1f5a
description: Cet article fournit une description détaillée des notifications sur une table d’affichage.
ms.openlocfilehash: a9d943a221efb35f8946637a20a8a0f1e72e66f4
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816968"
---
# <a name="about-display-table-notifications"></a>Affichage des notifications de table

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les notifications sur une table d’affichage sont envoyées par le fournisseur de services responsable de la création de la table d’affichage à MAPI. MAPI s’inscrit à ces notifications en appelant la méthode [IMAPITable::Advise](imapitable-advise.md) d’une table d’affichage et en spécifiant l’événement de modification de table. 
  
Comme pour toutes les notifications de table, les notifications de table d’affichage incluent une structure [TABLE_NOTIFICATION](table_notification.md) . Seuls les **membres ulTableEvent** et **propIndex** de cette structure sont significatifs ; les autres membres sont ignorés. Le membre **ulTableEvent** est défini sur TABLE_ROW_MODIFIED et le membre **propIndex** est défini sur la valeur de la colonne **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) dans la ligne correspondante. MAPI répond à la notification en appelant la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) pour la propriété affichée dans le contrôle et en affichant la nouvelle valeur. 
  
Les notifications de table d’affichage peuvent être utilisées par un fournisseur de services pour coordonner les modifications apportées aux contrôles associés dans la boîte de dialogue. Par exemple, si l’implémentation de l’interface de propriété doit actualiser un ou plusieurs champs de la boîte de dialogue , peut-être en réponse à un autre contrôle qui a défini l’indicateur DT_SET_IMMEDIATE dans sa propriété **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)), il peut générer une notification de table d’affichage. Une notification de table d’affichage peut alerter l’implémentation de l’interface de propriété que la valeur d’un ou plusieurs contrôles doit être relue en raison d’une modification ou d’un événement externe qui se produit. 
  
Un fournisseur de services peut émettre des notifications de table d’affichage en :
  
- Appel [d’ITableData::HrNotify](itabledata-hrnotify.md), si la table d’affichage a été générée avec un objet de données de table.
    
    - Ou -
    
- À l’aide de son propre code, si la table d’affichage a été générée avec l’implémentation **IMAPITable** du fournisseur. 
    
MAPI répond à l’affichage des notifications de table si nécessaire en relisant la valeur d’un contrôle à partir de l’implémentation de l’interface de propriété. Le tableau suivant décrit les détails relatifs à la façon dont MAPI gère les notifications pour des types spécifiques de contrôles.
  
|**Contrôle**|**Action MAPI**|
|:-----|:-----|
|Bouton  <br/> |Appelle [IMAPIProp::OpenProperty](imapiprop-openproperty.md)pour récupérer l’objet de contrôle au moyen de la propriété représentée par le membre **ulPRControl** de la structure [DTBLBUTTON](dtblbutton.md) si l’appel avait échoué précédemment. Appelle [IMAPIControl::GetState](imapicontrol-getstate.md) de l’objet de contrôle pour déterminer si le bouton doit être activé et active ou désactive le bouton en conséquence. |
|Case à cocher  <br/> |Lit à nouveau la valeur du membre **ulPRPropertyName** . |
|Zone de liste modifiable  <br/> |Rouvre la table associée au membre **ulPRTableName** de la structure [DTBLCOMBOBOX](dtblcombobox.md) . Relire toutes les lignes, y compris la valeur du membre **ulPRPropertyName**. |
|Zone de liste déroulante  <br/> |Rouvre la table associée au membre **ulPRTableName** de la structure [DTBLDDLBX](dtblddlbx.md) et relire toutes les lignes. Appelle [IMAPIProp::GetProps](imapiprop-getprops.md) pour récupérer les valeurs des propriétés stockées dans **ulPRDisplayProperty** et les membres **ulPRSetProperty** . |
|Modifier  <br/> |Relire la propriété et les redisplays. |
|Zone de groupe  <br/> |Ignore la notification. |
|Étiquette  <br/> |Ignore la notification. |
|Zone de liste de sélection multiples  <br/> |Si l’une des colonnes est un identificateur d’entrée, actualise la zone de liste. L’objet correspondant n’est pas fermé ou rechargé. |
|Zone de liste de sélection unique  <br/> |Lit la propriété set, en essayant de l’identifier. |
|Zone de liste à valeurs multiples  <br/> |Lit à nouveau la propriété et remplit à nouveau la zone de liste. |
|Page à onglets  <br/> |Il n’existe aucune notification pour ce contrôle ; tout est statique. |
|Case d’option  <br/> |Lit à nouveau la propriété associée au bouton et est stockée dans le membre **ulPropTag** de la structure [DTBLRADIOBUTTON](dtblradiobutton.md) et effectue la sélection appropriée avec les contrôles. |
   
## <a name="see-also"></a>Voir aussi

- [MAPI Tables](mapi-tables.md)

