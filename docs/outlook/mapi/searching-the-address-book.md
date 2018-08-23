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
ms.openlocfilehash: 0d3fb5d2ce5036c6491e24bba8d3541b123eaab1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595124"
---
# <a name="searching-the-address-book"></a>Recherche dans le carnet d’adresses

**S’applique à**: Outlook 2013 | Outlook 2016 
  
MAPI permet de fournisseurs de carnet d'adresses d'impl�menter deux niveaux de la fonctionnalit� de recherche :
  
- Un niveau de base qui correspond à un nom spécifié avec la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) des entrées de carnet d’adresses. Ce niveau permet aux utilisateurs, par exemple, pour afficher des listes de distribution dont les noms commencent par Northwest ou recherchez des utilisateurs de messagerie individuels dont le nom est Brown.
    
- Un niveau avanc� qui correspond aux propri�t�s de **PR_DISPLAY_NAME**. Ce niveau permet aux utilisateurs, par exemple, pour affiner leurs recherches et rechercher utilisateurs nomm�s Brown avec un type particulier d'adresse de messagerie.
    
Because address book providers can support searching for each of their containers at the basic level, at both levels, or choose not to support it at all, do not expect searching to be implemented as a standard feature. To determine if a particular container supports searches, attempt to establish search criteria in a call to its [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method. If **SetSearchCriteria** returns MAPI_E_NO_SUPPORT, the container does not support searches. 
  
In a container that supports searches, retrieve established criteria by calling [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md). You can also request that the user be prompted for search criteria before a container's contents table is displayed. Pour choisir cette option, définir l’indicateur AB_FIND_ON_OPEN de la propriété du conteneur **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)). After the user enters the criteria, it is stored as a restriction and passed to the **SetSearchCriteria** method. Setting AB_FIND_ON_OPEN is particularly useful if you are using an online service or any address book provider that has a slow link to its data. 
  
### <a name="to-perform-a-basic-search-in-an-address-book-container"></a>Pour effectuer une recherche de base dans un conteneur de carnet d'adresses
  
1. Call the container's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to open its contents table. 
    
2. Choisissez une technique de recherche qui r�pond � vos besoins. Les choix possibles sont les suivantes :
    
   - [IMAPITable::FindRow](imapitable-findrow.md) to locate a specific row in the table. 
    
   - [IMAPITable::SortTable](imapitable-sorttable.md) to order rows in the table. 
    
   - [IMAPITable](imapitable-restrict.md) to limit the table view. 
    
   - Restriction de propriété à l’aide de la propriété **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) pour la résolution des noms ambigus. Appelez **IMAPITable** pour imposer � cette restriction. 
    
   - [IABContainer::ResolveNames](iabcontainer-resolvenames.md) to resolve ambiguous names. 
    
3. Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve any rows that meet your applied search criteria. **QueryRows** can return zero or more matching rows. 
    
Les m�thodes **FindRow**, **SortTable**et **Restrict** sont des m�thodes de tableau qui sont disponibles pour une table qui peut �tre cr��e par un client ou un fournisseur de services. Le **PR\_ANR** restriction de propriété et la méthode **IABContainer::ResolveNames** sont spécifiques aux fournisseurs de carnet d’adresses et sont utilisés pour la résolution des noms ambigus. Noms ambigus sont entr�es dans une liste de destinataires qui ne poss�dent pas de propri�t� **PR_ENTRYID** leur sont associ�e. 
  
Le **PR\_ANR** restriction appelle un algorithme qui sépare une chaîne de caractères en mots et établit une correspondance avec les mots avec des informations dans le carnet d’adresses à l’aide de la correspondance des préfixes. The information used for the matching depends on the address book provider. All address book providers are required to support the **PR_ANR** restriction for their address book containers. For more information, see [L'impl�mentation de la r�solution de noms](implementing-name-resolution.md).
  
**IABContainer::ResolveNames** effectue une restriction **PR_ANR** de traitement sur plusieurs noms sans n�cessiter de tableau de contenu du conteneur � ouvrir. **ResolveNames** une fois l’appel pour résoudre les noms de plusieurs peut être beaucoup plus rapide que l’appelant un **PR\_ANR** restriction plusieurs fois. Toutefois, fournisseurs de carnet d'adresses ne sont pas requis pour prendre en charge **ResolveNames**.
  

