---
title: IMAPIContainerGetHierarchyTable
description: IMAPIContainerGetHierarchyTable retourne un pointeur vers la table de hiérarchie du conteneur. Cet article décrit sa syntaxe, ses paramètres, sa valeur de retour et ses remarques.
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
ms.openlocfilehash: 94ff4209540449eb8cdb29b1bf24fdefdc3d0358
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816366"
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

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôle la façon dont les informations sont retournées dans la table. Les indicateurs suivants peuvent être définis :
    
CONVENIENT_DEPTH 
  
> Remplit la table de hiérarchie avec des conteneurs de plusieurs niveaux. Si CONVENIENT_DEPTH n’est pas définie, la table de hiérarchie contient uniquement les conteneurs enfants immédiats du conteneur.
    
MAPI_DEFERRED_ERRORS 
  
> **GetHierarchyTable** peut retourner correctement, éventuellement avant que la table ne soit mise à la disposition de l’appelant. Si la table n’est pas disponible, l’exécution d’un appel de table ultérieur peut générer une erreur. 
    
MAPI_UNICODE 
  
> Demande que les colonnes qui contiennent des données de chaîne soient retournées au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas défini, les chaînes doivent être retournées au format ANSI. 
    
SHOW_SOFT_DELETES
  
> Affiche les éléments actuellement marqués comme supprimés de manière réversible, c’est-à-dire qu’ils sont dans la phase de durée de rétention des éléments supprimés.
    
 _lppTable_
  
> [out] Pointeur vers un pointeur vers la table de hiérarchie.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La table de hiérarchie a été récupérée avec succès.
    
MAPI_E_BAD_CHARWIDTH 
  
> Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, soit MAPI_UNICODE n’a pas été défini et l’implémentation prend uniquement en charge Unicode.
    
MAPI_E_NO_SUPPORT 
  
> Le conteneur n’a pas de conteneurs enfants et ne peut pas fournir de table de hiérarchie.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIContainer::GetHierarchyTable** retourne un pointeur vers la table hiérarchique d’un conteneur. Une table de hiérarchie contient des informations récapitulatives sur les conteneurs enfants dans le conteneur. Les tables de hiérarchie de dossiers contiennent des informations sur les sous-dossiers ; Les tables de hiérarchie de carnet d’adresses contiennent des informations sur les conteneurs de carnets d’adresses enfants et les listes de distribution. 
  
Il est possible que certains conteneurs n’aient pas de conteneurs enfants. Ces conteneurs retournent MAPI_E_NO_SUPPORT de leurs implémentations de **GetHierarchyTable**.
  
Lorsque l’indicateur CONVENIENT_DEPTH est défini, chaque ligne de la table de hiérarchie inclut également la propriété **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) en tant que colonne. **PR_DEPTH** indique le niveau de chaque conteneur par rapport au conteneur qui implémente la table. Les conteneurs enfants immédiats du conteneur d’implémentation sont à la profondeur zéro, les conteneurs enfants dans les conteneurs de profondeur zéro sont à la profondeur 1, et ainsi de suite. Les valeurs de **PR_DEPTH** augmentent séquentiellement à mesure que la hiérarchie des niveaux s’approfondit. 
  
Pour obtenir la liste complète des colonnes obligatoires et facultatives dans les tables de hiérarchie, consultez [Tables hiérarchiques](hierarchy-tables.md).
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Si vous prenez en charge une table de hiérarchie pour votre conteneur, vous devez également effectuer les opérations suivantes :
  
- Prenez en charge un appel à la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du conteneur pour ouvrir la propriété **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)).
    
- **Retournez PR_CONTAINER_HIERARCHY** à partir d’un appel aux méthodes [IMAPIProp::GetPropList](imapiprop-getproplist.md) ou [IMAPIProp::GetProps](imapiprop-getprops.md) du conteneur. 
    
## <a name="notes-to-callers"></a>Remarques pour les appelants

Les colonnes de table de contenu binaire et de chaîne peuvent être tronquées. En règle générale, les fournisseurs retournent 255 caractères. Étant donné que vous ne pouvez pas savoir au préalable si une table inclut des colonnes tronquées, supposons qu’une colonne est tronquée si la longueur de la colonne est de 255 ou 510 octets. Vous pouvez toujours récupérer la valeur complète d’une colonne tronquée, si nécessaire, directement à partir de l’objet en utilisant son identificateur d’entrée pour l’ouvrir, puis en appelant la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) . 
  
Selon l’implémentation du fournisseur, les restrictions et les opérations de tri peuvent s’appliquer à la chaîne entière ou à la version tronquée de cette chaîne. En outre, il n’est pas garanti que les fournisseurs de magasin respectent le jeu d’ordres de tri [SSortOrderSet](ssortorderset.md) spécifié pour les tables de hiérarchie. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|HierarchyTableTreeCtrl.cpp  <br/> |CHierarchyTableTreeCtrl::GetHierarchyTable  <br/> |La classe CHierarchyTableTreeCtrl utilise **GetHierarchyTable** pour obtenir des tables de hiérarchie à afficher dans un contrôle d’arborescence. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[Propriété canonique PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

