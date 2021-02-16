---
title: MAPI Record and Search Keys
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: caa7b7f3-a5a1-4f07-98c9-22652ecd5d21
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b1b4c0087cecd9164fc96ce7c5b5415f75dbfb03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434563"
---
# <a name="mapi-record-and-search-keys"></a>MAPI Record and Search Keys

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les clés d’enregistrement et les clés de recherche sont des identificateurs binaires qui sont affectés à de nombreux objets MAPI. Contrairement à l’identificateur d’entrée d’un objet, son enregistrement ou sa clé de recherche est directement comparable et transmetable. 
  
## <a name="record-keys"></a>Clés d’enregistrement

Une clé d’enregistrement permet de comparer deux objets. Les objets de magasin de messages et de carnet d’adresses doivent avoir des clés d’enregistrement, qui sont stockées dans **leur PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)). Étant donné qu’une clé d’enregistrement identifie un objet et non ses données, chaque instance d’un objet possède une clé d’enregistrement unique. L’étendue d’une clé d’enregistrement pour les dossiers et les messages est la magasin de messages. L’étendue des conteneurs de carnet d’adresses, des utilisateurs de messagerie et des listes de distribution est l’ensemble de conteneurs de niveau supérieur fourni par MAPI pour être utilisé dans le carnet d’adresses intégré.
  
Les clés d’enregistrement peuvent être dupliquées dans une autre ressource. Par exemple, différents messages dans deux magasins de messages différents peuvent avoir la même clé d’enregistrement. Il est différent des identificateurs d’entrée à long terme ; étant donné que les identificateurs d’entrée à long terme contiennent une référence au fournisseur de services, ils ont une portée plus large. L’étendue de la clé d’enregistrement d’une magasin de messages est similaire à celle d’un identificateur d’entrée à long terme . Il doit être unique pour tous les fournisseurs de magasins de messages. Pour garantir cet unicité, les fournisseurs de magasins de messages définissent généralement leur clé d’enregistrement sur une valeur qui est la combinaison de leur propriété **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) et d’un identificateur propre à la magasin de messages.
  
## <a name="search-keys"></a>Clés de recherche

Une clé de recherche est utilisée pour comparer les données dans deux objets. La clé de recherche d’un objet est stockée dans sa **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)). Étant donné qu’une clé de recherche représente les données d’un objet et non l’objet lui-même, deux objets différents avec les mêmes données peuvent avoir la même clé de recherche. Lorsqu’un objet est copié, par exemple, l’objet d’origine et sa copie ont les mêmes données et la même clé de recherche.
  
Les messages et les utilisateurs de messagerie ont des clés de recherche. La clé de recherche d’un message est un identificateur unique des données du message. Les fournisseurs de magasins de messages fournissent la propriété PR_SEARCH_KEY **message** au moment de la création du message. La clé de recherche d’une entrée de carnet d’adresses est calculée à partir de son type d’adresse (**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))) et de son adresse (**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))). Si l’entrée du carnet d’adresses est accessible en écriture, sa clé de recherche risque de ne pas être disponible tant que le type d’adresse et l’adresse n’ont pas été définies à l’aide de la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) et que l’entrée a été enregistrée à l’aide de la méthode [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) Lorsque ces propriétés d’adresse changent, il est possible que la clé de recherche correspondante ne soit pas synchronisée avec les nouvelles valeurs tant que les modifications n’ont pas été déterminées avec un appel **SaveChanges.** 
  
La valeur de la clé d’enregistrement d’un objet peut être identique ou différente de la valeur de sa clé de recherche, selon le fournisseur de services. Certains fournisseurs de services utilisent la même valeur pour la clé de recherche, la clé d’enregistrement et l’identificateur d’entrée d’un objet. D’autres fournisseurs de services affectent des valeurs uniques pour chacun des identificateurs de ses objets. 
  
## <a name="see-also"></a>Voir aussi



[D�veloppement d'applications MAPI](mapi-application-development.md)

