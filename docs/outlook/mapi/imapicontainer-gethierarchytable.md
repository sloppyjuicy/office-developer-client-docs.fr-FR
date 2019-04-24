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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: efc7f7a2fa703004afe361d766e0209ba40ffe46
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286938"
---
# <a name="imapicontainergethierarchytable"></a>IMAPIContainer::GetHierarchyTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie un pointeur vers la table de hiérarchie du conteneur.
  
```cpp
HRESULT GetHierarchyTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle la manière dont les informations sont renvoyées dans le tableau. Les indicateurs suivants peuvent être définis:
    
CONVENIENT_DEPTH 
  
> Remplit la table de hiérarchie avec des conteneurs à partir de plusieurs niveaux. Si CONVENIENT_DEPTH n'est pas défini, la table de hiérarchie contient uniquement les conteneurs enfants immédiats du conteneur.
    
MAPI_DEFERRED_ERRORS 
  
> **GetHierarchyTable** peut être renvoyé correctement, éventuellement avant que la table soit mise à la disposition de l'appelant. Si la table n'est pas disponible, un appel de tableau ultérieur peut déclencher une erreur. 
    
MAPI_UNICODE 
  
> Demande que les colonnes contenant des données de chaîne soient renvoyées au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes doivent être renvoyées au format ANSI. 
    
SHOW_SOFT_DELETES
  
> Affiche les éléments qui sont actuellement marqués comme étant supprimés de manière récupérable, c'est-à-dire qu'ils se trouvent dans la phase de durée de rétention des éléments supprimés.
    
 _lppTable_
  
> remarquer Pointeur vers un pointeur vers la table de hiérarchie.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La table de hiérarchie a été correctement récupérée.
    
MAPI_E_BAD_CHARWIDTH 
  
> L'indicateur MAPI_UNICODE a été défini et l'implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n'a pas été défini et l'implémentation prend en charge uniquement Unicode.
    
MAPI_E_NO_SUPPORT 
  
> Le conteneur n'a pas de conteneurs enfants et ne peut pas fournir de table de hiérarchie.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIContainer:: GetHierarchyTable** renvoie un pointeur vers la table de hiérarchie d'un conteneur. Une table de hiérarchie contient des informations récapitulatives sur les conteneurs enfants dans le conteneur. Les tables de hiérarchie des dossiers contiennent des informations sur les sous-dossiers; tables de hiérarchie des carnets d'adresses contiennent des informations sur les conteneurs du carnet d'adresses enfants et les listes de distribution. 
  
Certains conteneurs peuvent ne pas avoir de conteneurs enfants. Ces conteneurs renvoient MAPI_E_NO_SUPPORT à partir de leurs implémentations de **GetHierarchyTable**.
  
Lorsque l'indicateur CONVENIENT_DEPTH est défini, chaque ligne de la table Hierarchy inclut également la propriété **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) sous la forme d'une colonne. **PR_DEPTH** indique le niveau de chaque conteneur par rapport au conteneur qui implémente la table. Les conteneurs enfants immédiats du conteneur d'implémentation sont à la profondeur zéro, les conteneurs enfants dans les conteneurs de profondeur zéro sont en profondeur un, et ainsi de suite. Les valeurs de **PR_DEPTH** augmentent de manière séquentielle au fur et à mesure que la hiérarchie de niveaux approfondi. 
  
Pour obtenir la liste complète des colonnes obligatoires et facultatives dans les tables de hiérarchie, reportez-vous à la rubrique [Hierarchy tables](hierarchy-tables.md).
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Si vous prenez en charge une table de hiérarchie pour votre conteneur, vous devez également effectuer les opérations suivantes:
  
- Prendre en charge un appel à la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) du conteneur pour ouvrir la propriété **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)).
    
- Renvoyer **PR_CONTAINER_HIERARCHY** d'un appel vers les méthodes [IMAPIProp:: GetPropList](imapiprop-getproplist.md) ou [IMAPIProp:: GetProps](imapiprop-getprops.md) du conteneur. 
    
## <a name="notes-to-callers"></a>Remarques pour les appelants

Les colonnes de table de contenu binaire et de chaîne peuvent être tronquées. En règle générale, les fournisseurs renvoient 255 caractères. Étant donné que vous ne pouvez pas savoir si une table comporte des colonnes tronquées, supposons qu'une colonne est tronquée si sa longueur est de 255 ou 510 octets. Vous pouvez toujours récupérer la valeur complète d'une colonne tronquée, si nécessaire, directement à partir de l'objet à l'aide de son identificateur d'entrée pour l'ouvrir, puis en appelant la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) . 
  
En fonction de l'implémentation du fournisseur, les restrictions et les opérations de tri peuvent s'appliquer à la chaîne entière ou à la version tronquée de cette chaîne. Par ailleurs, il n'est pas garanti que les fournisseurs de magasins respectent l'ordre de tri défini [SSortOrderSet](ssortorderset.md) spécifié pour les tables de hiérarchie. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|HierarchyTableTreeCtrl. cpp  <br/> |CHierarchyTableTreeCtrl:: GetHierarchyTable  <br/> |La classe CHierarchyTableTreeCtrl utilise **GetHierarchyTable** pour obtenir les tables de hiérarchie à afficher dans un contrôle Tree View.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[Propriété canonique PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

