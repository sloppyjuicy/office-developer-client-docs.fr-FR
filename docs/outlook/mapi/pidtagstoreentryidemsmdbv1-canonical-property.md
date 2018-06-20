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
ms.openlocfilehash: 74626b735599a5f1485b26fcb65d907b552b3089
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786837"
---
# <a name="pidtagstoreentryidemsmdbv1-canonical-property"></a>Propriété canonique PidTagStoreEntryIdEmsmdbV1

  
  
**S’applique à**: Outlook 
  
Contient l’ancien style (Microsoft Outlook 2002 et versions antérieures) de l’identificateur d’entrée d’une banque de messages Microsoft Exchange Server 2010 ou Exchange Server 2013.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_STORE_ENTRYID_EMSMDB_V1  <br/> |
|Identificateur :  <br/> |0x65F60102  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |Propriétés ID  <br/> |
   
## <a name="remarks"></a>Remarques

À partir de Microsoft Outlook 2003, le nom de domaine complet ont été intégrées aux identificateurs d’entrée, en évitant RPC supplémentaires pour les redirections. Toutefois, cela rend plus identificateurs d’entrée et présente d’autres scénarios où la méthode **CompareEntryIDs** doit être utilisée pour déterminer si l’entrée deux ID sont équivalentes. Le PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) propriété accède à l’ancien format de l’identificateur d’entrée Exchange Server utilisé par Microsoft Outlook 2002 (Microsoft Office XP) et les versions antérieures. Vous pouvez économiser de l’espace et également réduire le nombre d’appels **CompareEntryIDs** nécessaires pour déterminer le moment de l’entrée ID sont équivalentes. Notez que pour ouvrir une boîte aux lettres à l’aide de l’identificateur d’entrée plus ancien peut entraîner des appels RPC supplémentaires si une référence est requise. 
  
Pour accéder à la propriété PR_STORE_ENTRYID_EMSMDB_V1 en mode mis en cache, vous devez ignorer le cache à l’aide de l’indicateur MAPI_NO_CACHE avec la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) . Si **PR_STORE_ENTRYID_EMSMDB_V1** n’est pas disponible, le code doit revient à PR_STORE_ENTRYID. Uniquement Outlook 2003 par le biais de Microsoft Outlook 2013 prend en charge la propriété PR_STORE_ENTRYID_EMSMDB_V1. 
  
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

