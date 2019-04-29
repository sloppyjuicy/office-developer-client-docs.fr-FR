---
title: Résolution d'un nom de destinataire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2baed391-85bd-4e88-8800-c19bc2d2d54a
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a3faed3dda2461cab749c824fc97c2074e62375f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405863"
---
# <a name="resolving-a-recipient-name"></a>Résolution d'un nom de destinataire

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsqu'un message est adressé, une liste de destinataires est créée avec des propriétés relatives à chaque destinataire. Lors de l'envoi du message, l'une de ces propriétés doit être l'identificateur d'entrée à long terme du destinataire. Pour vous assurer que chaque destinataire inclut la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), transmettez la structure [ADRLIST](adrlist.md) décrivant votre liste de destinataires dans le contenu du paramètre _lpAdrList_ dans un appel à [IAddrBook:: ResolveName](iaddrbook-resolvename.md).
  
 **ResolveName** commence le traitement en ignorant les entrées de la structure **ADRLIST** qui ont déjà été résolues, comme indiqué par la présence d'un identificateur d'entrée dans le **SPropValue** de la structure [ADRENTRY](adrentry.md) correspondante. Tableau. Ensuite, **ResolveName** affecte automatiquement des identificateurs d'entrée uniques à deux types de destinataires: 
  
- Destinataires avec une adresse au format d'adresse Internet
    
- Destinataires dont l'adresse est formatée comme suit:
    
     `displayname[address type:email address]`
    
Pour toutes les entrées restantes, **ResolveName** recherche dans le carnet d'adresses une correspondance exacte sur le nom complet. **ResolveName** utilise la propriété **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) pour déterminer l'ensemble de conteneurs à rechercher et l'ordre de recherche. MAPI appelle la méthode [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) de chaque conteneur pour tenter de résoudre tous les noms. Étant donné que certains conteneurs ne prennent pas en charge **ResolveNames**, si le conteneur renvoie MAPI_E_NO_SUPPORT, MAPI applique une restriction de propriété **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) par rapport à sa table de contenu. Tous les conteneurs de carnet d'adresses sont requis pour prendre en charge la résolution de noms avec cette restriction. Une fois que tous les noms sont résolus, aucun autre appel de conteneur n'est effectué. Si tous les conteneurs ont été appelés, mais que les noms ambigus ou non résolus restent, MAPI affiche une boîte de dialogue si possible pour inviter l'utilisateur à résoudre les noms restants.
  
La restriction **PR_ANR** établit une correspondance entre la valeur de la propriété **PR_ANR** et le nom complet de la structure **ADRLIST** . En limitant la vue de la table des matières d'un conteneur à l'aide de la restriction de propriété **PR_ANR** , le fournisseur de carnet d'adresses exécute un type de recherche «meilleure estimation», avec la mise en correspondance avec la propriété qui est logique pour le fournisseur. Par exemple, un fournisseur de carnet d'adresses peut toujours faire correspondre les noms de la liste des destinataires avec **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), tandis qu'un autre peut autoriser un administrateur à sélectionner la propriété.
  
 **Pour définir une restriction de propriété PR_ANR sur une table des matières d'un conteneur de carnet d'adresses**
  
1. Créez une structure [SRestriction](srestriction.md) comme illustré dans le code suivant: 
    
  ```cpp
  SRestriction SRestrict;
  SRestrict.rt = RES_PROPERTY;
  SRestrict.res.resProperty.relop = RELOP_EQ;
  SRestrict.res.resProperty.ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->Value.LPSZ = lpszName;
   
  ```

2. Appelez la méthode [IMAPITable:: Restrict](imapitable-restrict.md) du tableau contents, en transmettant la structure **SRestriction** en tant que paramètre _lpRestriction_ . 
    

