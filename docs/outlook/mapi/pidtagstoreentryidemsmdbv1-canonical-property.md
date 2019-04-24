---
title: Propriété canonique PidTagStoreEntryIdEmsmdbV1
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 40161358-4d41-43cf-83c7-fdd843bec87b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c8bccbfeb7f04745a66831618deff490bc651b02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278770"
---
# <a name="pidtagstoreentryidemsmdbv1-canonical-property"></a>Propriété canonique PidTagStoreEntryIdEmsmdbV1

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l'ancien style (Microsoft Outlook 2002 et versions antérieures) de l'identificateur d'entrée d'une banque de messages Microsoft Exchange Server 2010 ou Exchange Server 2013.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_STORE_ENTRYID_EMSMDB_V1  <br/> |
|Identificateur :  <br/> |0x65F60102  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Propriétés ID  <br/> |
   
## <a name="remarks"></a>Remarques

À partir de Microsoft Outlook 2003, les noms de domaine complets du serveur ont été intégrés aux identificateurs d'entrée, ce qui permet d'éviter les appels RPC supplémentaires pour les redirections. Toutefois, cela complique davantage les ID d'entrée et présente des scénarios dans lesquels la méthode **CompareEntryIDs** doit être utilisée pour déterminer si deux identificateurs d'entrée sont équivalents. La propriété PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) accède à l'ancien format de l'ID d'entrée du serveur Exchange utilisé par Microsoft Outlook 2002 (Microsoft Office XP) et les versions antérieures. Cela permet d'économiser de l'espace et de réduire le nombre d'appels **CompareEntryIDs** nécessaires pour déterminer quand les ID d'entrée sont équivalents. Notez que l'utilisation des anciens ID d'entrée pour ouvrir une boîte aux lettres peut entraîner des appels RPC supplémentaires si une référence est requise. 
  
Pour accéder à la propriété PR_STORE_ENTRYID_EMSMDB_V1 en mode mis en cache, vous devez ignorer le cache à l'aide de l'indicateur MAPI_NO_CACHE avec la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) . Si **PR_STORE_ENTRYID_EMSMDB_V1** n'est pas disponible, le code doit revenir à PR_STORE_ENTRYID. Seul Outlook 2003 via Microsoft Outlook 2013 prend en charge la propriété PR_STORE_ENTRYID_EMSMDB_V1. 
  
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

