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
ms.openlocfilehash: 5a6ba7af5e497ba59b43e9b80cfc9595961ed10e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579542"
---
# <a name="mapi-named-properties"></a>MAPI des propri�t�s nomm�e
 
**S’applique à**: Outlook 2013 | Outlook 2016 
  
MAPI fournit un procédé pour l’affectation de noms aux propriétés, pour le mappage de ces noms à des identificateurs uniques et pour rendre ce mappage permanente. Nom permanent au mappage de l’identificateur garantit que les noms de propriété valides entre les sessions.
  
Pour définir une propriété nommée, un client ou fournisseur de services constitue un nom et la stocke dans une structure [MAPINAMEID](mapinameid.md) . Étant donné que les noms sont composés d’un identificateur global unique 32 bits, ou GUID et soit un caractère numérique ou chaîne valeur Unicode, créateurs de propriétés nommées peuvent créer des noms explicites sans risque de duplication. Les noms sont uniques et ils peuvent être utilisés, indépendamment de la valeur de leurs identificateurs. 
  
Pour prendre en charge des propriétés nommées, un fournisseur de services implémente deux méthodes : [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) et [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) — pour traduire des noms et identificateurs et pour permettre son [IMAPIProp::GetProps](imapiprop-getprops.md) [ IMAPIProp::SetProps](imapiprop-setprops.md) méthodes pour récupérer et modifier des propriétés avec des identificateurs de la plage de la propriété nommée. La plage pour les identificateurs de propriété nommée est comprise entre 0 x 8000 et 0xFFFE. 
  
Tout objet qui implémente l’interface **IMAPIProp** peut prendre en charge des propriétés nommées. Fournisseurs de carnet d’adresses qui permettent de stockent les entrées à partir d’autres fournisseurs à copier dans leurs conteneurs et le message fournisseurs qui peuvent servir à créer des types de message arbitraires sont requises pour fournir cette prise en charge. Il est possible pour tous les autres fournisseurs de services. Fournisseurs ne prenant pas en charge les propriétés nommées renvoyer MAPI_E_NO_SUPPORT des méthodes **GetIDsFromNames** et **GetNamesFromIDs** et refusent définir des propriétés avec des identificateurs de 0 x 8000 ou supérieur, renvoi MAPI_E_UNEXPECTED dans les ** SPropProblemarray**.
  
Créez des noms de propriétés est un moyen pour les clients à définir de nouvelles propriétés pour les classes de message existant ou personnalisé. Fournisseurs de service peuvent utiliser propriétés nommées pour exposer les fonctionnalités uniques de leurs systèmes de messagerie. Encore une autre utilisation pour les propriétés nommées est de fournir une autre façon de faire référence à des propriétés avec des identificateurs ci-dessous 0 x 8000. 
  
Par exemple, un client peut utiliser le code similaire au code suivant pour récupérer les noms de tous les propriétés nommées d’un objet :
  
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

Pour demander tous les noms de l’ensemble de la propriété PS_PUBLIC_STRINGS, un client remplace la valeur NULL dans le paramètre set propriété PS_PUBLIC_STRINGS comme suit : 
  
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

