---
title: ITableData IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITableData
api_type:
- COM
ms.assetid: ac7ae09f-ce19-45cf-8963-fad5bba75452
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2218b3d0140c99e1a8028c060b9883b1aec25709
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62783942"
---
# <a name="itabledata--iunknown"></a>ITableData : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit des méthodes utilitaires pour travailler avec des tableaux. MAPI fournit des objets de données de table ou des objets qui implémentent **ITableData** pour aider les fournisseurs de services à effectuer la maintenance de table. Pour obtenir un objet de données de table, les fournisseurs de services appellent [la fonction CreateTable](createtable.md) . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Exposé par :  <br/> |Objets de données de tableau  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Fournisseurs de services  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPITableData  <br/> |
|Type de pointeur :  <br/> |LPTABLEDATA  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[HrGetView](itabledata-hrgetview.md) <br/> |Crée une vue de tableau, renvoyant un pointeur vers une [implémentation IMAPITable](imapitableiunknown.md) . |
|[HrModifyRow](itabledata-hrmodifyrow.md) <br/> |Insère une nouvelle ligne de tableau, éventuellement en remplaçant une ligne existante. |
|[HrDeleteRow](itabledata-hrdeleterow.md) <br/> |Supprime une ligne de tableau. |
|[HrQueryRow](itabledata-hrqueryrow.md) <br/> |Récupère une ligne de tableau. |
|[HrEnumRow](itabledata-hrenumrow.md) <br/> |Extrait une ligne en fonction de sa position dans le tableau. |
|[HrNotify](itabledata-hrnotify.md) <br/> |Envoie une notification pour une ligne de tableau. |
|[HrInsertRow](itabledata-hrinsertrow.md) <br/> |Insère une ligne de tableau. |
|[HrModifyRows](itabledata-hrmodifyrows.md) <br/> |Insère plusieurs lignes de tableau, en remplaçant éventuellement les lignes existantes. |
|[HrDeleteRows](itabledata-hrdeleterows.md) <br/> |Supprime plusieurs lignes de tableau. |
   
## <a name="remarks"></a>Remarques

L’implémentation MAPI **d’ITableData** fonctionne avec les tables en maintenant toutes les données et les restrictions associées en mémoire, ce qui la rend inadaptée pour une utilisation avec des tableaux très grands. Les restrictions importantes et les opérations complexes telles que la catégorisation ne sont pas pris en charge. 
  
Les objets de données de tableau identifient les lignes à l’aide d’une colonne d’index, propriété dont la valeur est unique pour chaque ligne. La plupart des fournisseurs de services **utilisent la PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) comme colonne d’index. Les propriétés qui ont plusieurs valeurs ne peuvent pas être utilisées comme colonne d’index.
  
Les objets de données de tableau génèrent une notification unique, quel que soit le nombre de lignes affectées par une modification ou une suppression. Si une ligne cible dans une opération n’existe pas, une ligne est ajoutée.
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

