---
title: IMAPIContainerGetHierarchyTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetHierarchyTable
api_type:
- COM
ms.assetid: d0c54092-86a3-47e0-8133-72e119e74b65
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 88b6f220f812f419b3f881aaa7f70a22186b589e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563799"
---
# <a name="imapicontainergethierarchytable"></a>IMAPIContainer::GetHierarchyTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Retourne un pointeur vers la table de hiérarchie du conteneur.
  
```cpp
HRESULT GetHierarchyTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont les informations sont retournées dans le tableau. Les indicateurs suivants peuvent être définis :
    
CONVENIENT_DEPTH 
  
> Remplit la table de hiérarchie avec des conteneurs de plusieurs niveaux. Si CONVENIENT_DEPTH n’est pas définie, la table de hiérarchie contient uniquement les conteneurs enfant immédiat du conteneur.
    
MAPI_DEFERRED_ERRORS 
  
> **GetHierarchyTable** peut renvoyer avec succès, probablement que le tableau soit disponible à l’appelant. Si le tableau n’est pas disponible, l’émission d’un appel de la table suivante peut déclencher une erreur. 
    
MAPI_UNICODE 
  
> Demandes de renvoyer les colonnes qui contiennent des données de type chaîne au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes doivent être retournées au format ANSI. 
    
SHOW_SOFT_DELETES
  
> Affiche les éléments qui sont actuellement marqués comme logicielles supprimés — autrement dit, ils sont dans la rétention des éléments supprimés phase de temps.
    
 _lppTable_
  
> [out] Pointeur vers un pointeur vers la table de hiérarchie.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La table de hiérarchie a été récupérée correctement.
    
MAPI_E_BAD_CHARWIDTH 
  
> Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été défini et l’implémentation prend en charge Unicode uniquement.
    
MAPI_E_NO_SUPPORT 
  
> Le conteneur a les conteneurs enfants et ne peuvent pas fournir une table de hiérarchie.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIContainer::GetHierarchyTable** renvoie un pointeur vers la table de hiérarchie d’un conteneur. Une table de hiérarchie conserve des informations récapitulatives concernant les conteneurs enfants dans le conteneur. Tables de hiérarchie de dossier contiennent des informations sur les sous-dossiers ; tables de hiérarchie adresse livre contiennent des informations sur les enfants conteneurs de carnet d’adresses et listes de distribution. 
  
Il est possible pour certains conteneurs pour que les conteneurs enfants. Ces conteneurs renvoient MAPI_E_NO_SUPPORT à partir de leurs implémentations de **GetHierarchyTable**.
  
Lorsque l’indicateur CONVENIENT_DEPTH est défini, chaque ligne dans la table de hiérarchie inclut également la propriété **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) en tant que colonne. **PR_DEPTH** indique le niveau de chaque conteneur par rapport à du conteneur qui implémente le tableau. Enfant immédiat du conteneur d’application sont des conteneurs au niveau de profondeur de zéro, les conteneurs enfants dans les conteneurs de profondeur zéro sont en profondeur un et ainsi de suite. Les valeurs de **PR_DEPTH** augmentent en séquence comme approfondit la hiérarchie de niveaux. 
  
Pour une liste complète des colonnes obligatoires et facultatifs dans les tables de hiérarchie, voir les [Tables de hiérarchie](hierarchy-tables.md).
  
## <a name="notes-to-implementers"></a>Remarques à l’attention des responsables de l’implémentation

Si vous prenez en charge une table de hiérarchie de votre conteneur, vous devez également procédez comme suit :
  
- Prend en charge un appel à la méthode de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du conteneur pour ouvrir la propriété **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)).
    
- Retourner **PR_CONTAINER_HIERARCHY** à partir d’un appel aux méthodes de [IMAPIProp::GetPropList](imapiprop-getproplist.md) ou [IMAPIProp::GetProps](imapiprop-getprops.md) du conteneur. 
    
## <a name="notes-to-callers"></a>Notes aux appelants

Colonnes de tableau contenu chaîne et binaires peuvent être tronqués. En règle générale, les fournisseurs retournent 255 caractères. Car vous ne pouvez pas savoir au préalable si une table inclut des colonnes tronqués, supposons qu’une colonne est tronquée si la longueur de la colonne est 255 ou 510 octets. Vous pouvez toujours récupérer la valeur complète d’une colonne tronquée, si nécessaire, directement à partir de l’objet à l’aide de son identificateur d’entrée pour l’ouvrir, puis en appelant la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) . 
  
Selon l’implémentation du fournisseur, les restrictions et les opérations de tri peuvent appliquer à la chaîne entière ou à la version tronquée de cette chaîne. En outre, les fournisseurs de magasins ne sont pas nécessairement de respecter l’ensemble d’ordre de tri [que ssortorderset](ssortorderset.md) spécifiée pour les tables de hiérarchie. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|HierarchyTableTreeCtrl.cpp  <br/> |CHierarchyTableTreeCtrl::GetHierarchyTable  <br/> |La classe CHierarchyTableTreeCtrl utilise **GetHierarchyTable** pour obtenir des tables de hiérarchie à afficher dans un contrôle d’arborescence.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[Propriété canonique PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

