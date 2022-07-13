---
title: MAPI des propri�t�s nomm�e
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 464b1297-9d90-47bd-afc4-3dc63b106cb7
ms.openlocfilehash: 758f2eea5f127ddcea706260eb770af30fb5ff44
ms.sourcegitcommit: b8c11491410ea058cfb559c2b83030d94c072bd7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/13/2022
ms.locfileid: "66755561"
---
# <a name="mapi-named-properties"></a>MAPI des propri�t�s nomm�e
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI fournit une fonctionnalité permettant d’attribuer des noms à des propriétés, de mapper ces noms à des identificateurs uniques et de rendre ce mappage persistant. Le mappage du nom persistant à l’identificateur garantit que les noms de propriétés restent valides entre les sessions.
  
Pour définir une propriété nommée, un client ou un fournisseur de services compose un nom et le stocke dans une structure [MAPINAMEID](mapinameid.md) . Étant donné que les noms sont constitués d’un identificateur global unique 128 bits, ou GUID, et d’une chaîne de caractères Unicode ou d’une valeur numérique 32 bits, les créateurs de propriétés nommées peuvent créer des noms explicites sans crainte de duplication. Les noms sont uniques et peuvent être utilisés sans tenir compte de la valeur de leurs identificateurs. 
  
Pour prendre en charge les propriétés nommées, un fournisseur de services implémente deux méthodes : [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) et [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) , pour traduire entre les noms et les identificateurs et permettre à ses méthodes [IMAPIProp::GetProps](imapiprop-getprops.md)[IMAPIProp::SetProps](imapiprop-setprops.md) de récupérer et de modifier des propriétés avec des identificateurs dans la plage de propriétés nommée. La plage des identificateurs de propriété nommés est comprise entre 0x8000 et 0xFFFE. 
  
Tout objet qui implémente l’interface **IMAPIProp** peut prise en charge des propriétés nommées. Les fournisseurs de carnets d’adresses qui permettent aux entrées d’autres fournisseurs d’être copiées dans leurs conteneurs et les fournisseurs de magasins de messages qui peuvent être utilisés pour créer des types de messages arbitraires sont nécessaires pour fournir cette prise en charge. Il s’agit d’une option pour tous les autres fournisseurs de services. Les fournisseurs qui ne prennent pas en charge les propriétés nommées retournent MAPI_E_NO_SUPPORT des méthodes **GetIDsFromNames** et **GetNamesFromIDs** et refusent de définir des propriétés avec des identificateurs de 0x8000 ou supérieur, en retournant MAPI_E_UNEXPECTED dans **SPropProblemarray**.
  
La création de noms pour les propriétés est un moyen pour les clients de définir de nouvelles propriétés pour les classes de messages existantes ou personnalisées. Les fournisseurs de services peuvent utiliser des propriétés nommées pour exposer des fonctionnalités uniques de leurs systèmes de messagerie. Une autre utilisation des propriétés nommées consiste à fournir une autre façon de faire référence aux propriétés avec des identificateurs ci-dessous 0x8000. 
  
Par exemple, un client peut utiliser du code similaire au code suivant pour récupérer les noms de toutes les propriétés nommées d’un objet :
  
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

Pour demander tous les noms du jeu de propriétés PS_PUBLIC_STRINGS, un client remplace la valeur NULL du paramètre de jeu de propriétés par PS_PUBLIC_STRINGS comme suit : 
  
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

