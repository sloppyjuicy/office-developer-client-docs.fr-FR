---
title: ITableData IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData
api_type:
- COM
ms.assetid: ac7ae09f-ce19-45cf-8963-fad5bba75452
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3992bea899239ee5975505dec366490d6bbe1698
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430594"
---
# <a name="itabledata--iunknown"></a>ITableData : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit des méthodes utilitaires pour utiliser des tableaux. MAPI fournit des objets de données de tableau ou des objets qui implémentent **ITableData** pour aider les fournisseurs de services à effectuer la maintenance des tables. Pour obtenir un objet de données de table, les fournisseurs de services appellent la fonction [CreateTable](createtable.md) . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
|Exposé par:  <br/> |Objets de données de tableau  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Fournisseurs de services  <br/> |
|Identificateur de l'interface:  <br/> |IID_IMAPITableData  <br/> |
|Type de pointeur:  <br/> |LPTABLEDATA  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[HrGetView](itabledata-hrgetview.md) <br/> |Crée un affichage tableau en renvoyant un pointeur vers une implémentation [IMAPITable](imapitableiunknown.md) .  <br/> |
|[HrModifyRow](itabledata-hrmodifyrow.md) <br/> |Insère une nouvelle ligne de tableau, éventuellement en remplaçant une ligne existante.  <br/> |
|[HrDeleteRow](itabledata-hrdeleterow.md) <br/> |Supprime une ligne de tableau.  <br/> |
|[HrQueryRow](itabledata-hrqueryrow.md) <br/> |Récupère une ligne de tableau.  <br/> |
|[HrEnumRow](itabledata-hrenumrow.md) <br/> |Récupère une ligne en fonction de sa position dans le tableau.  <br/> |
|[HrNotify](itabledata-hrnotify.md) <br/> |Envoie une notification pour une ligne de tableau.  <br/> |
|[HrInsertRow](itabledata-hrinsertrow.md) <br/> |Insère une ligne de tableau.  <br/> |
|[HrModifyRows](itabledata-hrmodifyrows.md) <br/> |Insère plusieurs lignes de tableau, susceptibles de remplacer des lignes existantes.  <br/> |
|[HrDeleteRows](itabledata-hrdeleterows.md) <br/> |Supprime plusieurs lignes de tableau.  <br/> |
   
## <a name="remarks"></a>Remarques

L'implémentation MAPI de **ITableData** fonctionne avec les tableaux en stockant toutes les données et toutes les restrictions associées dans la mémoire, ce qui rend l'utilisation inappropriée avec des tables très volumineuses. Les restrictions importantes et les opérations complexes telles que la catégorisation ne sont pas prises en charge. 
  
Les objets de données de tableau identifient les lignes à l'aide d'une colonne d'index, une propriété dont la valeur est garantie pour chaque ligne. La plupart des fournisseurs de services utilisent la propriété **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) en tant que colonne d'index. Les propriétés qui ont plusieurs valeurs ne peuvent pas être utilisées en tant que colonne d'index.
  
Les objets de données de tableau génèrent une seule notification, quel que soit le nombre de lignes affectées par une modification ou une suppression. S'il n'existe pas de ligne cible dans une opération, une ligne est ajoutée.
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

