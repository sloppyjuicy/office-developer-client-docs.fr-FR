---
title: Résolution d’un nom de destinataire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2baed391-85bd-4e88-8800-c19bc2d2d54a
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d9b52edf7f4633fdf9c925a8d8db4953590713b3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22562931"
---
# <a name="resolving-a-recipient-name"></a>Résolution d’un nom de destinataire

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Lorsqu’un message est adressé, une liste de destinataires est générée avec les propriétés relatives à chaque destinataire. Au moment où que le message est envoyé, une de ces propriétés doit être l’identificateur d’entrée du destinataire à long terme. Pour vous assurer que chaque destinataire inclut la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), passez la structure [ADRLIST](adrlist.md) décrivant votre liste de destinataires dans le contenu du paramètre _lpAdrList_ dans un appel à [IAddrBook :: ResolveName](iaddrbook-resolvename.md).
  
 **ResolveName** commence le traitement en ignorant les entrées de la structure **ADRLIST** qui ont déjà été résolues, comme indiqué par la présence d’un identificateur d’entrée dans la structure [ADRENTRY](adrentry.md) correspondant **SPropValue** tableau. Ensuite, **ResolveName** affecte automatiquement les identificateurs d’entrée unique à deux types de destinataires : 
  
- Destinataires dont l’adresse mise en forme comme une adresse Internet
    
- Destinataires dont l’adresse mise en forme comme suit :
    
     `displayname[address type:email address]`
    
Pour toutes les entrées restantes, **ResolveName** recherche une correspondance exacte sur le nom complet du carnet d’adresses. **ResolveName** utilise la propriété **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) pour déterminer l’ensemble des conteneurs à la recherche et l’ordre de recherche. La méthode [IABContainer::ResolveNames](iabcontainer-resolvenames.md) de chaque conteneur pour essayer de résoudre tous les noms des appels MAPI. Étant donné que certains conteneurs ne prennent pas en charge **ResolveNames**, si le conteneur renvoie MAPI_E_NO_SUPPORT, MAPI applique une restriction de propriété **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) par rapport à sa table des matières. Tous les conteneurs de carnet d’adresses sont requis pour prendre en charge la résolution de noms avec cette restriction. Une fois que tous les noms sont résolus, aucune autre conteneur appels sont effectuées. Si tous les conteneurs ont été appelées, mais restent noms ambigus ou non résolues, MAPI affiche une boîte de dialogue si possible pour inviter l’utilisateur à résoudre les noms restants.
  
La restriction de **PR_ANR** correspond à la valeur de la propriété **PR_ANR** sur le nom complet de la structure **ADRLIST** . Limitation de l’affichage du tableau de contenu d’un conteneur avec la restriction de propriété **PR_ANR** entraîne le fournisseur de carnet d’adresses effectuer un type de « deviner mieux » de la recherche, en correspondance avec la propriété qui est significatif pour le fournisseur. Par exemple, un fournisseur de carnet d’adresses peut toujours correspondre les noms dans la liste de destinataires par rapport à **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) tandis qu’une autre peut autoriser un administrateur à sélectionner la propriété.
  
 **Pour définir une restriction de propriété PR_ANR sur tableau de contenu d’un conteneur carnet d’adresses**
  
1. Créez une structure [SRestriction](srestriction.md) comme indiqué dans le code suivant : 
    
  ```cpp
  SRestriction SRestrict;
  SRestrict.rt = RES_PROPERTY;
  SRestrict.res.resProperty.relop = RELOP_EQ;
  SRestrict.res.resProperty.ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->Value.LPSZ = lpszName;
   
  ```

2. Appelez le contenu [IMAPITable](imapitable-restrict.md) méthode du tableau, en passant la structure **SRestriction** en tant que paramètre _lpRestriction_ . 
    

