---
title: Enregistrement MAPI et les clés de recherche
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: caa7b7f3-a5a1-4f07-98c9-22652ecd5d21
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 1e1b05be64029f80ec8a7379ed7b313b9cf645fd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784677"
---
# <a name="mapi-record-and-search-keys"></a>Enregistrement MAPI et les clés de recherche

  
  
**S’applique à**: Outlook 
  
Clés d’enregistrement et clés de recherche sont les identificateurs binaires qui sont affectés à de nombreux objets MAPI. À la différence d’identificateur d’entrée d’un objet, sa clé d’enregistrement ou de la recherche est directement comparables ainsi transmissible. 
  
## <a name="record-keys"></a>Clés d’enregistrement

Une clé d’enregistrement est utilisée pour comparer deux objets. Banque de messages et l’adresse objets book doivent posséder des clés d’enregistrement, qui sont stockés dans leur propriété **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)). Étant donné que la clé d’un enregistrement identifie un objet et pas ses données, chaque instance d’un objet a une clé d’enregistrement unique. L’étendue d’une clé d’enregistrement pour les dossiers et messages est la banque de messages. L’étendue des conteneurs de carnet d’adresses, les utilisateurs de messagerie et les listes de distribution est l’ensemble des conteneurs de niveau supérieur fournis par MAPI pour une utilisation dans le carnet d’adresses intégré.
  
Clés d’enregistrement peuvent être reproduites dans une autre ressource. Par exemple, des messages différents dans deux messages différents magasins peuvent avoir la même clé d’enregistrement. Cela diffère des identificateurs d’entrée à long terme ; Étant donné que les identificateurs d’entrée à long terme contient une référence au fournisseur de services, ils ont une étendue plus large. Clé d’enregistrement d’une banque de messages est similaire à un identificateur d’entrée à long terme ; Il doit être unique parmi tous les fournisseurs de banque de messages. Pour garantir cette unicité, les fournisseurs de magasins de message généralement définie leur clé d’enregistrement à une valeur qui est la combinaison de leur propriété **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) et un identificateur unique pour la banque de messages.
  
## <a name="search-keys"></a>Clés de recherche

Une clé de recherche est utilisée pour comparer les données dans deux objets. Clé de recherche d’un objet est stockée dans sa propriété **clé PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)). Étant donné que la clé de recherche représente les données d’un objet et non l’objet lui-même, deux objets différents avec les mêmes données peuvent avoir la même clé de recherche. Lorsqu’un objet est copié, par exemple, l’objet d’origine et sa copie ont les mêmes données et la même clé de recherche.
  
Les messages et les utilisateurs de messagerie ont clés de recherche. La clé de recherche d’un message est un identificateur unique de données du message. Fournisseurs de banque de message proposent **clé PR_SEARCH_KEY** , propriété d’un message au moment de la création de message. La clé de recherche d’une entrée de carnet d’adresses est calculée à partir de son type d’adresse (**TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))) et l’adresse (**ADRESSE_EMAIL_PR** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))). Si l’entrée du carnet d’adresses est accessible en écriture, sa clé de recherche peuvent ne pas être disponible jusqu'à ce que le type d’adresse et l’adresse ont été définies à l’aide de la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) et l’entrée a été enregistrée à l’aide de la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . Modification des propriétés adresse, il est possible de la clé de recherche correspondant ne pas à synchroniser avec les nouvelles valeurs jusqu'à ce que les modifications ont été validées par un appel de **SaveChanges** . 
  
La valeur de la clé d’enregistrement d’un objet peut être identique ou différente de la valeur de sa clé de recherche, selon le fournisseur de services. Certains fournisseurs de services utilisent la même valeur de clé de recherche d’un objet, la clé d’enregistrement et identificateur d’entrée. Autres fournisseurs de services assignent des valeurs uniques pour chacune des identificateurs de ses objets. 
  
## <a name="see-also"></a>Voir aussi



[D�veloppement d'applications MAPI](mapi-application-development.md)

