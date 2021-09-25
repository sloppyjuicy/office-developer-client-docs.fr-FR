---
title: Propriété canonique PidTagStoreEntryIdEmsmdbV1
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 40161358-4d41-43cf-83c7-fdd843bec87b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: fe99dced15540813434b3486a46c547528f820e2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578955"
---
# <a name="pidtagstoreentryidemsmdbv1-canonical-property"></a>Propriété canonique PidTagStoreEntryIdEmsmdbV1

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’ancien style (Microsoft Outlook 2002 et versions antérieures) de l’identificateur d’entrée d’un magasin de messages Microsoft Exchange Server 2010 ou Exchange Server 2013.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_STORE_ENTRYID_EMSMDB_V1  <br/> |
|Identificateur :  <br/> |0x65F60102  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Propriétés de l’ID  <br/> |
   
## <a name="remarks"></a>Remarques

À partir de Microsoft Outlook 2003, les FQDN du serveur étaient intégrés aux ID d’entrée, évitant ainsi d’autres RPCs pour les références. Toutefois, cela rend les ID d’entrée plus longs et introduit d’autres scénarios où la méthode **CompareEntryIDs** doit être utilisée pour déterminer si deux ID d’entrée sont équivalents. La propriété PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) accède à l’ancien format de l’ID d’entrée Exchange Server utilisé par Microsoft Outlook 2002 (Microsoft Office XP) et les versions antérieures. Cela permet de gagner de l’espace et de réduire le nombre d’appels **CompareEntryIDs** nécessaires pour déterminer à quel moment les ID d’entrée sont équivalents. Notez que l’utilisation des anciens ID d’entrée pour ouvrir une boîte aux lettres peut incurer des RPCs supplémentaires si une référence est requise. 
  
Pour accéder à la propriété PR_STORE_ENTRYID_EMSMDB_V1 en mode mis en cache, vous devez contourner le cache à l’aide de l’indicateur MAPI_NO_CACHE avec la méthode [IMAPIProp::GetProps.](imapiprop-getprops.md) Si **PR_STORE_ENTRYID_EMSMDB_V1** n’est pas disponible, le code doit revenir à PR_STORE_ENTRYID. Seuls Outlook 2003 à 2003 Microsoft Outlook 2013 la PR_STORE_ENTRYID_EMSMDB_V1 propriété. 
  
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

