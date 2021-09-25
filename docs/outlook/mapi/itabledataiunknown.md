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
ms.openlocfilehash: ac60e3691f64ab932f7d8a53370f43efaa0fa9ce
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571562"
---
# <a name="itabledata--iunknown"></a>ITableData : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit des méthodes utilitaires pour travailler avec des tableaux. MAPI fournit des objets de données de table ou des objets qui implémentent **ITableData** pour aider les fournisseurs de services à effectuer la maintenance de table. Pour obtenir un objet de données de table, les fournisseurs de services appellent [la fonction CreateTable.](createtable.md) 
  
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
|[HrGetView](itabledata-hrgetview.md) <br/> |Crée une vue de tableau, renvoyant un pointeur vers une [implémentation IMAPITable.](imapitableiunknown.md)  <br/> |
|[HrModifyRow](itabledata-hrmodifyrow.md) <br/> |Insère une nouvelle ligne de tableau, éventuellement en remplaçant une ligne existante.  <br/> |
|[HrDeleteRow](itabledata-hrdeleterow.md) <br/> |Supprime une ligne de tableau.  <br/> |
|[HrQueryRow](itabledata-hrqueryrow.md) <br/> |Récupère une ligne de tableau.  <br/> |
|[HrEnumRow](itabledata-hrenumrow.md) <br/> |Extrait une ligne en fonction de sa position dans le tableau.  <br/> |
|[HrNotify](itabledata-hrnotify.md) <br/> |Envoie une notification pour une ligne de tableau.  <br/> |
|[HrInsertRow](itabledata-hrinsertrow.md) <br/> |Insère une ligne de tableau.  <br/> |
|[HrModifyRows](itabledata-hrmodifyrows.md) <br/> |Insère plusieurs lignes de tableau, en remplaçant éventuellement les lignes existantes.  <br/> |
|[HrDeleteRows](itabledata-hrdeleterows.md) <br/> |Supprime plusieurs lignes de tableau.  <br/> |
   
## <a name="remarks"></a>Remarques

L’implémentation MAPI **d’ITableData** fonctionne avec les tableaux en maintenant toutes les données et les restrictions associées en mémoire, ce qui la rend inadaptée pour une utilisation avec des tables très grandes. Les restrictions importantes et les opérations complexes telles que la catégorisation ne sont pas pris en charge. 
  
Les objets de données de tableau identifient les lignes à l’aide d’une colonne d’index, propriété dont la valeur est unique pour chaque ligne. La plupart des fournisseurs de services **utilisent la PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) comme colonne d’index. Les propriétés qui ont plusieurs valeurs ne peuvent pas être utilisées comme colonne d’index.
  
Les objets de données de tableau génèrent une notification unique, quel que soit le nombre de lignes affectées par une modification ou une suppression. Si une ligne cible dans une opération n’existe pas, une ligne est ajoutée.
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

