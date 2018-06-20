---
title: À propos des notifications d’affichage tableau
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 085151e9-4809-4d2b-ae4d-e318355e1f5a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a696357c97a85442bbfd5532892c06d570f6367c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782845"
---
# <a name="about-display-table-notifications"></a>À propos des notifications d’affichage tableau

**S’applique à**: Outlook 
  
Notifications sur une table d’affichage sont transmises par le fournisseur de services responsable de la création de la table d’affichage à MAPI. MAPI inscrit pour ces notifications à l’appel de méthode [d’IMAPITable::Advise](imapitable-advise.md) d’une table d’affichage et en spécifiant l’événement de modification de table. 
  
Comme avec toutes les notifications de table, afficher les notifications de table incluent une structure [TABLE_NOTIFICATION](table_notification.md) . Uniquement **ulTableEvent** ainsi que les membres **propIndex** de cette structure sont significatifs ; les autres membres sont ignorés. Le membre **ulTableEvent** est défini sur TABLE_ROW_MODIFIED et le membre **propIndex** est défini sur la valeur de la colonne **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) dans la ligne correspondante. MAPI répond à la notification en appelant la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) pour la propriété affichée dans le contrôle et en affichant la nouvelle valeur. 
  
Afficher les notifications de table peuvent être utilisées par un fournisseur de services pour coordonner les modifications apportées aux contrôles connexes dans la boîte de dialogue. Par exemple, si l’implémentation d’interface propriété doit actualiser un ou plusieurs champs dans la boîte de dialogue — par exemple en réponse à un autre contrôle qui a défini l’indicateur DT_SET_IMMEDIATE dans sa propriété **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) : Il peut générer une notification de tableau d’affichage. Une notification de la table affichage alerte l’implémentation d’interface de propriété la valeur d’un ou plusieurs contrôles doit être relu en raison d’une modification ou un événement externe se produisant. 
  
Un fournisseur de services peut émettre afficher les notifications de table par :
  
- L’appel [ITableData::HrNotify](itabledata-hrnotify.md), si le tableau d’affichage a été créé avec un objet de données de table.
    
    - Ou -
    
- À l’aide de son propre code, si le tableau d’affichage a été créé avec l’implémentation du fournisseur **IMAPITable** . 
    
MAPI répond pour afficher les notifications de table lorsque cela est nécessaire à relire la valeur d’un contrôle à partir de l’implémentation d’interface de propriété. Le tableau suivant décrit les détails relatifs à la MAPI gère les notifications pour des types spécifiques de contrôles.
  
|**Contrôle**|**Action MAPI**|
|:-----|:-----|
|Bouton  <br/> |Appelle [IMAPIProp::OpenProperty](imapiprop-openproperty.md)pour récupérer l’objet de contrôle par la propriété représentée par le membre **ulPRControl** de la structure [DTBLBUTTON](dtblbutton.md) si l’appel a précédemment échoué. Appelle [IMAPIControl::GetState](imapicontrol-getstate.md) pour déterminer si le bouton doit être activé et Active ou désactive le bouton en conséquence l’objet contrôle.  <br/> |
|Case à cocher  <br/> |Relit la valeur du membre **ulPRPropertyName** .  <br/> |
|Zone de liste modifiable  <br/> |Rouvre la table associée au membre de la structure [DTBLCOMBOBOX](dtblcombobox.md) **ulPRTableName** . Toutes les lignes, y compris la valeur du membre **ulPRPropertyName**relit.  <br/> |
|Zone de liste déroulante  <br/> |Rouvre la table associée au membre de la structure [DTBLDDLBX](dtblddlbx.md) **ulPRTableName** et relit toutes les lignes. Appelle [IMAPIProp::GetProps](imapiprop-getprops.md) pour récupérer les valeurs des propriétés stockées dans **ulPRDisplayProperty** ainsi que les membres **ulPRSetProperty** .  <br/> |
|Modifier  <br/> |Relit la propriété et réaffiche.  <br/> |
|Zone de groupe  <br/> |Ignore la notification.  <br/> |
|Étiquette  <br/> |Ignore la notification.  <br/> |
|Zone de liste Sélection multiple  <br/> |Si une des colonnes est un identificateur d’entrée, actualise la zone de liste. L’objet correspondant n’est pas fermé ou rechargé.  <br/> |
|Zone de liste de sélection unique  <br/> |Lit la propriété set, essayez d’identifier.  <br/> |
|Zone de liste à valeurs multiples  <br/> |Relit la propriété et remplit la zone de liste.  <br/> |
|Page à onglets  <br/> |Il n’y a aucune notification pour ce contrôle ; tout est statique.  <br/> |
|Case d’option  <br/> |Relit la propriété qui est associé au bouton et est stockée dans le membre **ulPropTag** de la structure [DTBLRADIOBUTTON](dtblradiobutton.md) et rend la sélection avec les contrôles appropriée.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Tables MAPI](mapi-tables.md)

