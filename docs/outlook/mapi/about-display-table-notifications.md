---
title: Affichage des notifications de table
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 085151e9-4809-4d2b-ae4d-e318355e1f5a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 41e6a2c8b6856bf072972325e7e08aabe3e17446
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430013"
---
# <a name="about-display-table-notifications"></a>Affichage des notifications de table

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les notifications sur une table d’affichage sont envoyées par le fournisseur de services responsable de la création de la table d’affichage sur MAPI. MAPI s’inscrit pour ces notifications en appelant la méthode [IMAPITable::Advise](imapitable-advise.md) d’une table d’affichage et en spécifiant l’événement modifié de la table. 
  
Comme pour toutes les notifications de tableau, les notifications de tableau d’affichage incluent [TABLE_NOTIFICATION](table_notification.md) structure. Seuls **les membres ulTableEvent** et **propIndex** de cette structure sont significatifs ; les autres membres sont ignorés. Le **membre ulTableEvent** est définie sur TABLE_ROW_MODIFIED et le membre **propIndex** sur la valeur de la colonne **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) dans la ligne correspondante. MAPI répond à la notification en appelant la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) pour la propriété affichée dans le contrôle et en affichant la nouvelle valeur. 
  
Les notifications de tableau d’affichage peuvent être utilisées par un fournisseur de services pour coordonner les modifications apportées aux contrôles associés dans la boîte de dialogue. Par exemple, si l’implémentation de l’interface de propriétés doit actualiser un ou plusieurs champs dans la boîte de dialogue , peut-être en réponse à un autre contrôle qui a définie l’indicateur DT_SET_IMMEDIATE dans sa propriété **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)), elle peut générer une notification de tableau d’affichage. Une notification de tableau d’affichage peut avertir l’implémentation de l’interface de propriétés que la valeur d’un ou plusieurs contrôles doit être relue en raison d’une modification ou d’un événement externe qui se produit. 
  
Un fournisseur de services peut émettre des notifications de tableau d’affichage en :
  
- Appel [d’ITableData::HrNotify,](itabledata-hrnotify.md)si le tableau d’affichage a été créé avec un objet de données de table.
    
    - Ou -
    
- À l’aide de son propre code, si le tableau d’affichage a été créé avec l’implémentation **IMAPITable du** fournisseur. 
    
MAPI répond aux notifications de tableau d’affichage lorsque cela est nécessaire en relisant la valeur d’un contrôle à partir de l’implémentation de l’interface de propriétés. Le tableau suivant décrit les détails concernant la façon dont MAPI gère les notifications pour des types de contrôles spécifiques.
  
|**Contrôle**|**Action MAPI**|
|:-----|:-----|
|Bouton  <br/> |Appelle [IMAPIProp::OpenProperty](imapiprop-openproperty.md)pour récupérer l’objet de contrôle au moyen de la propriété représentée par le membre **ulPRControl** de la structure [DTBLBUTTON](dtblbutton.md) si l’appel a échoué précédemment. Appelle [IMAPIControl::GetState](imapicontrol-getstate.md) de l’objet de contrôle pour déterminer si le bouton doit être activé et active ou désactive le bouton en conséquence.  <br/> |
|Case à cocher  <br/> |Relecture la valeur du **membre ulPRPropertyName.**  <br/> |
|Zone de liste modifiable  <br/> |Rouvrez la table associée au **membre ulPRTableName** de la structure [DTBLCOMBOBOX.](dtblcombobox.md) Relecture toutes les lignes, y compris la valeur du membre **ulPRPropertyName.**  <br/> |
|Zone de liste liste  <br/> |Rouvrez la table associée au membre **ulPRTableName** de la structure [DTBLDDLBX](dtblddlbx.md) et lit à nouveau toutes les lignes. Appelle [IMAPIProp::GetProps](imapiprop-getprops.md) pour récupérer les valeurs des propriétés stockées dans les membres **ulPRDisplayProperty** et **ulPRSetProperty.**  <br/> |
|Modifier  <br/> |Relecture la propriété et les réélecture.  <br/> |
|Zone de groupe  <br/> |Ignore la notification.  <br/> |
|Étiquette  <br/> |Ignore la notification.  <br/> |
|Zone de liste à sélection multiple  <br/> |Si l’une des colonnes est un identificateur d’entrée, actualisez la zone de liste. L’objet correspondant n’est ni fermé ni rechargé.  <br/> |
|Zone de liste à sélection unique  <br/> |Lit la propriété set, en essayant de l’identifier.  <br/> |
|Zone de liste à valeurs multiples  <br/> |Relecture la propriété et retentre la zone de liste.  <br/> |
|Page à onglets  <br/> |Il n’existe aucune notification pour ce contrôle ; tout est statique.  <br/> |
|Bouton d’radio  <br/> |Relecture la propriété associée au bouton et est stockée dans le membre **ulPropTag** de la structure [DTBLRADIOBUTTON](dtblradiobutton.md) et effectue la sélection appropriée avec les contrôles.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [MAPI Tables](mapi-tables.md)

