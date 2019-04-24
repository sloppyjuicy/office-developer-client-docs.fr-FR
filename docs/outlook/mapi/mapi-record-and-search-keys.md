---
title: Enregistrements MAPI et clés de recherche
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: caa7b7f3-a5a1-4f07-98c9-22652ecd5d21
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b1b4c0087cecd9164fc96ce7c5b5415f75dbfb03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328132"
---
# <a name="mapi-record-and-search-keys"></a>Enregistrements MAPI et clés de recherche

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les clés d'enregistrement et les clés de recherche sont des identificateurs binaires affectés à de nombreux objets MAPI. Contrairement à l'identificateur d'entrée d'un objet, son enregistrement ou sa clé de recherche est directement comparable et transmissible. 
  
## <a name="record-keys"></a>Clés d'enregistrement

Une clé d'enregistrement est utilisée pour comparer deux objets. Les objets de banque de messages et de carnet d'adresses doivent avoir des clés d'enregistrement, qui sont stockées dans leur propriété **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)). Étant donné qu'une clé d'enregistrement identifie un objet et non ses données, chaque instance d'un objet a une clé d'enregistrement unique. La portée d'une clé d'enregistrement pour les dossiers et les messages est la Banque de messages. L'étendue des conteneurs de carnet d'adresses, des utilisateurs de messagerie et des listes de distribution est l'ensemble des conteneurs de niveau supérieur fournis par MAPI pour une utilisation dans le carnet d'adresses intégré.
  
Les clés d'enregistrement peuvent être dupliquées dans une autre ressource. Par exemple, différents messages dans deux banques de messages différentes peuvent avoir la même clé d'enregistrement. Cette fonction est différente des identificateurs d'entrée à long terme; étant donné que les identificateurs d'entrée à long terme contiennent une référence au fournisseur de services, ils ont une étendue plus large. La clé d'enregistrement d'une banque de messages est semblable dans l'étendue à un identificateur d'entrée à long terme; il doit être unique dans tous les fournisseurs de banques de messages. Pour garantir cette unicité, les fournisseurs de banques de messages définissent généralement leur clé d'enregistrement sur une valeur qui est la combinaison de leur propriété **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) et un identificateur propre à la Banque de messages.
  
## <a name="search-keys"></a>Clés de recherche

Une clé de recherche est utilisée pour comparer les données de deux objets. La clé de recherche d'un objet est stockée dans sa propriété **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)). Étant donné qu'une clé de recherche représente les données d'un objet et non l'objet lui-même, deux objets différents avec les mêmes données peuvent avoir la même clé de recherche. Lors de la copie d'un objet, par exemple, l'objet d'origine et sa copie ont les mêmes données et la même clé de recherche.
  
Les messages et les utilisateurs de messagerie ont des clés de recherche. La clé de recherche d'un message est un identificateur unique des données du message. Les fournisseurs de banques de messages fournissent la propriété **PR_SEARCH_KEY** d'un message lors de la création du message. La clé de recherche d'une entrée de carnet d'adresses est calculée à partir de son type d'adresse (**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))) et de son adresse (**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))). Si l'entrée de carnet d'adresses est accessible en écriture, il se peut que sa clé de recherche ne soit pas disponible tant que le type d'adresse et l'adresse n'ont pas été définis à l'aide de la méthode [IMAPIProp:: SetProps](imapiprop-setprops.md) et que l'entrée ait été enregistrée à l'aide de la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) . Lorsque ces propriétés d'adresse changent, il est possible que la clé de recherche correspondante ne soit pas synchronisée avec les nouvelles valeurs tant que les modifications n'ont pas été validées avec un appel de **SaveChanges** . 
  
La valeur de la clé d'enregistrement d'un objet peut être identique ou différente de la valeur de sa clé de recherche, en fonction du fournisseur de services. Certains fournisseurs de services utilisent la même valeur pour la clé de recherche, la clé d'enregistrement et l'identificateur d'entrée d'un objet. Les autres fournisseurs de services attribuent des valeurs uniques pour chacun de ses identificateurs d'objets. 
  
## <a name="see-also"></a>Voir aussi



[D�veloppement d'applications MAPI](mapi-application-development.md)

