---
title: MAPI des propri�t�s nomm�e
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 464b1297-9d90-47bd-afc4-3dc63b106cb7
ms.openlocfilehash: 32cfbb3270a1255b43d41edce4f36b446c9eb4ae
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63380710"
---
# <a name="mapi-named-properties"></a>MAPI des propri�t�s nomm�e
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI fournit une fonction permettant d’affecter des noms à des propriétés, de ma mappage de ces noms à des identificateurs uniques et de rendre ce mappage persistant. Le nom persistant au mappage d’identificateur garantit que les noms de propriété restent valides entre les sessions.
  
Pour définir une propriété nommée, un client ou un fournisseur de services constitue un nom et le stocke dans une structure [MAPINAMEID](mapinameid.md) . Étant donné que les noms sont composés d’un identificateur global unique (GUID) 32 bits et d’une chaîne de caractères Unicode ou d’une valeur numérique, les créateurs de propriétés nommées peuvent créer des noms significatifs sans craindre de duplication. Les noms sont uniques et peuvent être utilisés sans prendre en compte la valeur de leurs identificateurs. 
  
Pour prendre en charge les propriétés nommées, un fournisseur de services implémente deux méthodes : [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) et [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) , pour traduire entre les noms et les identificateurs et pour autoriser ses méthodes [IMAPIProp::GetPropsIMAPIProp](imapiprop-getprops.md)[::SetProps](imapiprop-setprops.md) à récupérer et modifier des propriétés avec des identificateurs dans la plage de propriétés nommée. La plage des identificateurs de propriété nommée est 0x8000 et 0xFFFE. 
  
Tout objet qui implémente l’interface **IMAPIProp** peut prendre en charge les propriétés nommées. Les fournisseurs de carnet d’adresses qui permettent la copie d’entrées d’autres fournisseurs dans leurs conteneurs et fournisseurs de magasins de messages qui peuvent être utilisés pour créer des types de messages arbitraires sont requis pour fournir cette prise en charge. Il s’agit d’une option pour tous les autres fournisseurs de services. Les fournisseurs qui ne prisent pas en charge les propriétés nommées retournent des MAPI_E_NO_SUPPORT à partir des méthodes **GetIDsFromNames** et **GetNamesFromIDs** et refusent de définir des propriétés avec des identificateurs de 0x8000 ou supérieur, renvoyant les MAPI_E_UNEXPECTED dans **le SPropProblemarray**.
  
La création de noms pour les propriétés est un moyen pour les clients de définir de nouvelles propriétés pour des classes de message existantes ou personnalisées. Les fournisseurs de services peuvent utiliser des propriétés nommées pour exposer des fonctionnalités uniques de leurs systèmes de messagerie. Une autre utilisation des propriétés nommées consiste à fournir une autre façon de faire référence aux propriétés avec des identificateurs sous 0x8000. 
  
Par exemple, un client peut utiliser du code semblable au code suivant pour récupérer les noms de toutes les propriétés nommées d’un objet :
  
```cpp
LPSPropTagArray FAR *    lppPropTags = NULL;
LPGUID                   lpPropSetGuid = NULL;
ULONG FAR *              lpcPropNames;
LPMAPINAMEID FAR * FAR * lpppPropNames;
lpMAPIProp->GetNamesFromIDs (lppPropTags,
                             lpPropSetGuid,
                             0,
                             lpcPropNames,
                             lpppPropNames);
 
```

Pour demander tous les noms du jeu PS_PUBLIC_STRINGS propriétés, un client remplace la valeur NULL dans le paramètre de jeu de propriétés PS_PUBLIC_STRINGS comme suit : 
  
```cpp
LPSPropTagArray FAR *    lppPropTags = NULL;
LPGUID                   lpPropSetGuid = &PS_PUBLIC_STRINGS;
ULONG FAR *              lpcPropNames;
LPMAPINAMEID FAR * FAR * lpppPropNames;
lpMAPIProp->GetNamesFromIDs (lppPropTags,
                             lpPropSetGuid,
                             0,
                             lpcPropNames,
                             lpppPropNames);
 
```

## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de la propriété MAPI](mapi-property-overview.md)

