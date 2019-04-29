---
title: MAPI des propri�t�s nomm�e
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 464b1297-9d90-47bd-afc4-3dc63b106cb7
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d83b98b4f06c648676852673a694a63b78f568b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435046"
---
# <a name="mapi-named-properties"></a>MAPI des propri�t�s nomm�e
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI fournit une fonctionnalité permettant d'affecter des noms aux propriétés, de mapper ces noms à des identificateurs uniques et de rendre ce mappage persistant. Le mappage de nom permanent au identificateur garantit que les noms de propriété restent valides entre les sessions.
  
Pour définir une propriété nommée, un client ou un fournisseur de services compose un nom et le stocke dans une structure [MAPINAMEID](mapinameid.md) . Étant donné que les noms sont composés d'un identificateur global unique (GUID) 32 bits, et soit d'une chaîne de caractères Unicode, soit d'une valeur numérique, les créateurs de propriétés nommées peuvent créer des noms significatifs sans crainte de duplication. Les noms sont uniques et peuvent être utilisés indépendamment de la valeur de leurs identificateurs. 
  
Pour prendre en charge les propriétés nommées, un fournisseur de services implémente deux méthodes ( [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) et [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md) ) pour effectuer une traduction entre les noms et les identificateurs et pour autoriser les [IMAPIProp:: GetProps](imapiprop-getprops.md) [ IMAPIProp:: SetProps](imapiprop-setprops.md) méthodes permettant de récupérer et de modifier les propriétés avec des identificateurs dans la plage de propriétés nommées. La plage pour les identificateurs de la propriété nommée est comprise entre 0x8000 et 0xFFFE. 
  
Tout objet qui implémente l'interface **IMAPIProp** peut prendre en charge des propriétés nommées. Les fournisseurs de carnets d'adresses qui permettent de copier des entrées d'autres fournisseurs dans leurs conteneurs et fournisseurs de banques de messages qui peuvent être utilisés pour créer des types de message arbitraires sont nécessaires pour fournir cette prise en charge. Il s'agit d'une option pour tous les autres fournisseurs de services. Les fournisseurs qui ne prennent pas en charge les propriétés nommées retournent MAPI_E_NO_SUPPORT à partir des méthodes **GetIDsFromNames** et **GetNamesFromIDs** et refusent de définir des propriétés avec des identificateurs de 0x8000 ou supérieur, en renvoyant MAPI_E_UNEXPECTED dans le ** SPropProblemarray**.
  
La création de noms pour les propriétés est un moyen pour les clients de définir de nouvelles propriétés pour les classes de message existantes ou personnalisées. Les fournisseurs de services peuvent utiliser des propriétés nommées pour exposer les fonctionnalités uniques de leurs systèmes de messagerie. Une autre utilisation pour les propriétés nommées est de fournir un autre moyen de faire référence à des propriétés avec des identificateurs sous 0x8000. 
  
Par exemple, un client peut utiliser un code similaire au code suivant pour récupérer les noms de toutes les propriétés nommées d'un objet:
  
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

Pour demander tous les noms à partir du jeu de propriétés PS_PUBLIC_STRINGS, un client remplace la valeur NULL dans le paramètre SET de la propriété par PS_PUBLIC_STRINGS comme suit: 
  
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

