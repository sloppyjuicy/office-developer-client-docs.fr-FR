---
title: IMAPIContainerGetHierarchyTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIContainer.GetHierarchyTable
api_type:
- COM
ms.assetid: d0c54092-86a3-47e0-8133-72e119e74b65
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 44f03decbc2f673ffd36b95316075c803d8f11d4
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62781470"
---
# <a name="imapicontainergethierarchytable"></a>IMAPIContainer::GetHierarchyTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie un pointeur vers le tableau hiérarchique du conteneur.
  
```cpp
HRESULT GetHierarchyTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont les informations sont renvoyées dans le tableau. Les indicateurs suivants peuvent être définies :
    
CONVENIENT_DEPTH 
  
> Remplit la table de hiérarchie avec des conteneurs de plusieurs niveaux. Si CONVENIENT_DEPTH n’est pas définie, la table de hiérarchie contient uniquement les conteneurs enfants immédiats du conteneur.
    
MAPI_DEFERRED_ERRORS 
  
> **GetHierarchyTable** peut renvoyer correctement, éventuellement avant que la table soit disponible pour l’appelant. Si la table n’est pas disponible, un appel de table ultérieur peut occasioner une erreur. 
    
MAPI_UNICODE 
  
> Demande que les colonnes qui contiennent des données de chaîne soient renvoyées au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les chaînes doivent être renvoyées au format ANSI. 
    
SHOW_SOFT_DELETES
  
> Affiche les éléments qui sont actuellement marqués comme supprimés (supprimés (supprimés( en d’autres cas), ils sont dans la phase de rétention des éléments supprimés.
    
 _lppTable_
  
> [out] Pointeur vers un pointeur vers le tableau hiérarchique.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La table de hiérarchie a été récupérée avec succès.
    
MAPI_E_BAD_CHARWIDTH 
  
> L’indicateur MAPI_UNICODE a été définie et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et l’implémentation prend uniquement en charge Unicode.
    
MAPI_E_NO_SUPPORT 
  
> Le conteneur n’a pas de conteneurs enfants et ne peut pas fournir de table hiérarchique.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPIContainer::GetHierarchyTable** renvoie un pointeur vers la table hiérarchique d’un conteneur. Une table de hiérarchie contient des informations récapitulatifs sur les conteneurs enfants dans le conteneur. Les tables de hiérarchie de dossiers contient des informations sur les sous-dossiers . Les tables de hiérarchie de carnet d’adresses contenint des informations sur les conteneurs de carnet d’adresses et les listes de distribution enfants. 
  
Il est possible que certains conteneurs n’ont pas de conteneurs enfants. Ces conteneurs retournent MAPI_E_NO_SUPPORT à partir de leurs implémentations **de GetHierarchyTable**.
  
Lorsque l CONVENIENT_DEPTH est définie, chaque ligne de la table hiérarchique inclut également la propriété **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) en tant que colonne. **PR_DEPTH** indique le niveau de chaque conteneur par rapport au conteneur qui implémente la table. Les conteneurs enfants immédiats du conteneur d’implémentation sont à la profondeur zéro, les conteneurs enfants dans les conteneurs de profondeur zéro sont à la profondeur 1, et ainsi de suite. Les valeurs des **PR_DEPTH** augmentent de manière séquentielle à mesure que la hiérarchie des niveaux s’accroît. 
  
Pour obtenir la liste complète des colonnes obligatoires et facultatives dans les tableaux hiérarchiques, voir [Tables de hiérarchie](hierarchy-tables.md).
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Si vous prendre en charge une table hiérarchique pour votre conteneur, vous devez également :
  
- Prendre en charge un appel à la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du conteneur pour ouvrir la propriété **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)).
    
- **Renvoyer PR_CONTAINER_HIERARCHY** d’un appel aux méthodes [IMAPIProp::GetPropList](imapiprop-getproplist.md) ou [IMAPIProp::GetProps](imapiprop-getprops.md) du conteneur. 
    
## <a name="notes-to-callers"></a>Remarques pour les appelants

Les colonnes de table de contenu binaire et de chaîne peuvent être tronquées. En règle générale, les fournisseurs retournent 255 caractères. Comme vous ne pouvez pas savoir au préalable si un tableau inclut des colonnes tronquées, supposons qu’une colonne est tronquée si la longueur de la colonne est de 255 ou 510 octets. Vous pouvez toujours récupérer la valeur complète d’une colonne tronquée, si nécessaire, directement à partir de l’objet en utilisant son identificateur d’entrée pour l’ouvrir, puis en appelant la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) . 
  
Selon l’implémentation du fournisseur, les restrictions et les opérations de tri peuvent s’appliquer à la chaîne entière ou à la version tronquée de cette chaîne. En outre, il n’est pas garanti que les fournisseurs de magasins respectent le jeu d’ordre de tri [SSortOrderSet](ssortorderset.md) spécifié pour les tables hiérarchiques. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|HierarchyTableTreeCtrl.cpp  <br/> |CHierarchyTableTreeCtrl::GetHierarchyTable  <br/> |La classe CHierarchyTableTreeCtrl utilise **GetHierarchyTable** pour obtenir des tables hiérarchiques à afficher dans un contrôle d’arborescence. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[Propriété canonique PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

