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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 968768fe75286b93bf12e349a4845fdfaa1923e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784478"
---
# <a name="itabledata--iunknown"></a>ITableData : IUnknown

  
  
**S’applique à**: Outlook 
  
Fournit des méthodes utilitaires pour l’utilisation des tableaux. MAPI fournit des objets de données de table ou des objets qui implémentent **ITableData** pour aider les fournisseurs de services à effectuer la maintenance de la table. Pour obtenir un objet de données de table, les fournisseurs de services appellent la fonction [Create table](createtable.md) . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Exposés par :  <br/> |Objets de données de table  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Fournisseurs de services  <br/> |
|Identificateur de l’interface :  <br/> |IID_IMAPITableData  <br/> |
|Type de pointeur :  <br/> |LPTABLEDATA  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[HrGetView](itabledata-hrgetview.md) <br/> |Crée un affichage tableau, qui retourne un pointeur vers une implémentation [IMAPITable](imapitableiunknown.md) .  <br/> |
|[HrModifyRow](itabledata-hrmodifyrow.md) <br/> |Insérer une nouvelle ligne de tableau, en remplaçant éventuellement une ligne existante.  <br/> |
|[HrDeleteRow](itabledata-hrdeleterow.md) <br/> |Supprime une ligne de tableau.  <br/> |
|[HrQueryRow](itabledata-hrqueryrow.md) <br/> |Récupère une ligne de tableau.  <br/> |
|[HrEnumRow](itabledata-hrenumrow.md) <br/> |Récupère une ligne en fonction de sa position dans le tableau.  <br/> |
|[HrNotify](itabledata-hrnotify.md) <br/> |Envoie une notification pour une ligne de tableau.  <br/> |
|[HrInsertRow](itabledata-hrinsertrow.md) <br/> |Insère une ligne de tableau.  <br/> |
|[HrModifyRows](itabledata-hrmodifyrows.md) <br/> |Insère plusieurs lignes de tableau, remplaçant éventuellement les lignes existantes.  <br/> |
|[HrDeleteRows](itabledata-hrdeleterows.md) <br/> |Supprime plusieurs lignes de tableau.  <br/> |
   
## <a name="remarks"></a>Remarques

L’implémentation de MAPI de **ITableData** fonctionne avec des tableaux en maintenant les restrictions associées et toutes les données en mémoire, rendant inapproprié pour une utilisation avec des tables très volumineuses. Restrictions de grande taille et des opérations complexes, telles que la catégorisation ne sont pas pris en charge. 
  
Objets de données de table identifient les lignes à l’aide d’une colonne d’index, une propriété qui est la garantie d’avoir une valeur unique pour chaque ligne. La plupart des fournisseurs de services utilisent la propriété **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) en tant que colonne de l’index. Propriétés ayant plusieurs valeurs ne peuvent pas être utilisées comme une colonne d’index.
  
Objets de données de table de génèrent une notification unique quel que soit le nombre de lignes affectées par une modification ou la suppression. Si une ligne dans une opération cible n’existe pas, une ligne est ajoutée.
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

