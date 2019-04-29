---
title: Recherche dans le carnet d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 20ff2b63-e4a3-4ba9-bad0-2c1873fb69b5
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d40419291f4b09c5880a769ce231015511e8f269
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424370"
---
# <a name="searching-the-address-book"></a>Recherche dans le carnet d’adresses

**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI permet de fournisseurs de carnet d'adresses d'impl�menter deux niveaux de la fonctionnalit� de recherche :
  
- Niveau de base correspondant à un nom spécifié avec la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) des entrées du carnet d'adresses. Ce niveau permet aux utilisateurs, par exemple, pour afficher des listes de distribution dont les noms commencent par Northwest ou recherchez des utilisateurs de messagerie individuels dont le nom est Brown.
    
- Un niveau avanc� qui correspond aux propri�t�s de **PR_DISPLAY_NAME**. Ce niveau permet aux utilisateurs, par exemple, pour affiner leurs recherches et rechercher utilisateurs nomm�s Brown avec un type particulier d'adresse de messagerie.
    
Because address book providers can support searching for each of their containers at the basic level, at both levels, or choose not to support it at all, do not expect searching to be implemented as a standard feature. To determine if a particular container supports searches, attempt to establish search criteria in a call to its [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method. If **SetSearchCriteria** returns MAPI_E_NO_SUPPORT, the container does not support searches. 
  
In a container that supports searches, retrieve established criteria by calling [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md). You can also request that the user be prompted for search criteria before a container's contents table is displayed. Pour choisir cette option, définissez l'indicateur AB_FIND_ON_OPEN de la propriété **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) du conteneur. After the user enters the criteria, it is stored as a restriction and passed to the **SetSearchCriteria** method. Setting AB_FIND_ON_OPEN is particularly useful if you are using an online service or any address book provider that has a slow link to its data. 
  
### <a name="to-perform-a-basic-search-in-an-address-book-container"></a>Pour effectuer une recherche de base dans un conteneur de carnet d'adresses
  
1. Call the container's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to open its contents table. 
    
2. Choisissez une technique de recherche qui r�pond � vos besoins. Les choix possibles sont les suivantes :
    
   - [IMAPITable::FindRow](imapitable-findrow.md) to locate a specific row in the table. 
    
   - [IMAPITable::SortTable](imapitable-sorttable.md) to order rows in the table. 
    
   - [IMAPITable](imapitable-restrict.md) to limit the table view. 
    
   - Restriction de propriété à l'aide de la propriété **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) pour résoudre les noms ambigus. Appelez **IMAPITable** pour imposer � cette restriction. 
    
   - [IABContainer::ResolveNames](iabcontainer-resolvenames.md) to resolve ambiguous names. 
    
3. Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve any rows that meet your applied search criteria. **QueryRows** can return zero or more matching rows. 
    
Les m�thodes **FindRow**, **SortTable**et **Restrict** sont des m�thodes de tableau qui sont disponibles pour une table qui peut �tre cr��e par un client ou un fournisseur de services. La restriction de propriété **PR\_** et la méthode **IABContainer:: ResolveNames** sont spécifiques aux fournisseurs de carnet d'adresses et sont utilisées pour résoudre des noms ambigus. Noms ambigus sont entr�es dans une liste de destinataires qui ne poss�dent pas de propri�t� **PR_ENTRYID** leur sont associ�e. 
  
La **restriction\_PR ANR** appelle un algorithme qui sépare une chaîne de caractères en mots et fait correspondre ces mots avec les informations du carnet d'adresses à l'aide de la correspondance de préfixe. The information used for the matching depends on the address book provider. All address book providers are required to support the **PR_ANR** restriction for their address book containers. For more information, see [L'impl�mentation de la r�solution de noms](implementing-name-resolution.md).
  
**IABContainer::ResolveNames** effectue une restriction **PR_ANR** de traitement sur plusieurs noms sans n�cessiter de tableau de contenu du conteneur � ouvrir. L'appel de **ResolveNames** une fois pour résoudre plusieurs noms peut être beaucoup plus rapide que d'appeler une restriction de la fonction de **réservation\_ANR** plusieurs fois. Toutefois, fournisseurs de carnet d'adresses ne sont pas requis pour prendre en charge **ResolveNames**.
  

