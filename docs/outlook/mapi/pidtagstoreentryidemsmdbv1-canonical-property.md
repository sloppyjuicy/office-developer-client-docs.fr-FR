---
title: Propriété canonique PidTagStoreEntryIdEmsmdbV1
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 40161358-4d41-43cf-83c7-fdd843bec87b
description: Contient l’ancien style (Outlook 2002 et versions antérieures) de l’identificateur d’entrée d’une Microsoft Exchange Server 2010 ou Exchange Server 2013.
ms.openlocfilehash: b83ad82e3af54d56b47a0ff116a7f4b0a33d05ce
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455999"
---
# <a name="pidtagstoreentryidemsmdbv1-canonical-property"></a>Propriété canonique PidTagStoreEntryIdEmsmdbV1

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’ancien style (Microsoft Outlook 2002 et versions antérieures) de l’identificateur d’entrée d’un magasin de messages Microsoft Exchange Server 2010 ou Exchange Server 2013.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_STORE_ENTRYID_EMSMDB_V1  <br/> |
|Identificateur :  <br/> |0x65F60102  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Propriétés de l’ID  <br/> |
   
## <a name="remarks"></a>Remarques

À partir de Microsoft Outlook 2003, les FQDN du serveur étaient intégrés dans les ID d’entrée, évitant ainsi des RPCs supplémentaires pour les références. Toutefois, cela rend les ID d’entrée plus longs et introduit d’autres scénarios où la méthode **CompareEntryIDs** doit être utilisée pour déterminer si deux ID d’entrée sont équivalents. La propriété PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) accède à l’ancien format de l’ID d’entrée Exchange Server utilisé par Microsoft Outlook 2002 (Microsoft Office XP) et les versions antérieures. Cela permet d’économiser de l’espace et de réduire le nombre d’appels **CompareEntryIDs** nécessaires pour déterminer à quel moment les ID d’entrée sont équivalents. Notez que l’utilisation des anciens ID d’entrée pour ouvrir une boîte aux lettres peut encourir des RPCs supplémentaires si une référence est requise. 
  
Pour accéder à la propriété PR_STORE_ENTRYID_EMSMDB_V1 en mode mis en cache, vous devez contourner le cache à l’aide de l’indicateur MAPI_NO_CACHE avec la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) . Si **PR_STORE_ENTRYID_EMSMDB_V1** n’est pas disponible, le code doit revenir à PR_STORE_ENTRYID. Seuls Outlook 2003 à 2003 Microsoft Outlook 2013 la PR_STORE_ENTRYID_EMSMDB_V1 propriété. 
  
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

