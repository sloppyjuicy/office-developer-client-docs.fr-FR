---
title: Résolution d’un nom de destinataire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 2baed391-85bd-4e88-8800-c19bc2d2d54a
ms.openlocfilehash: 892425e631f5168d504640cbd3b96213cf0f6d3d
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63372814"
---
# <a name="resolving-a-recipient-name"></a>Résolution d’un nom de destinataire

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsqu’un message est adressé, une liste de destinataires est construite avec des propriétés relatives à chaque destinataire. Au moment où le message est envoyé, l’une de ces propriétés doit être l’identificateur d’entrée à long terme du destinataire. Pour vous assurer que chaque destinataire inclut la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), passez la structure [ADRLIST](adrlist.md) décrivant votre liste des destinataires dans le contenu du paramètre  _lpAdrList_ dans un appel à [IAddrBook::ResolveName](iaddrbook-resolvename.md).
  
 **ResolveName** commence le traitement en ignorant les entrées de la structure **ADRLIST** qui ont déjà été résolues, comme indiqué par la présence d’un identificateur d’entrée dans le tableau **SPropValue** de la structure [ADRENTRY](adrentry.md) correspondante. Ensuite, **ResolveName** affecte automatiquement des identificateurs d’entrée uniques à deux types de destinataires : 
  
- Destinataires avec une adresse formatée en tant qu’adresse Internet
    
- Destinataires avec une adresse mise en forme comme suit :
    
     `displayname[address type:email address]`
    
Pour toutes les entrées restantes, **ResolveName** recherche dans le carnet d’adresses une correspondance exacte sur le nom complet. **ResolveName utilise** la **propriété PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) pour déterminer l’ensemble de conteneurs à rechercher et l’ordre de recherche. MAPI appelle la [méthode IABContainer::ResolveNames](iabcontainer-resolvenames.md) de chaque conteneur pour tenter de résoudre tous les noms. Certains conteneurs ne supportant pas **ResolveNames**, si le conteneur renvoie MAPI_E_NO_SUPPORT, MAPI applique une restriction de propriété **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) à sa table des matières. Tous les conteneurs de carnet d’adresses sont requis pour prendre en charge la résolution de noms avec cette restriction. Une fois tous les noms résolus, aucun autre appel de conteneur n’est effectué. Si tous les conteneurs ont été appelés, mais que des noms ambigus ou non résolus restent, MAPI affiche une boîte de dialogue si possible pour inviter l’utilisateur à résoudre les noms restants.
  
La **restriction PR_ANR** la valeur de la **propriété PR_ANR** par rapport au nom d’affichage dans la structure **ADRLIST** . En limitant l’affichage de la table des matières d’un conteneur avec la restriction de propriété PR_ANR, le fournisseur de carnets d’adresses effectue un type de recherche de « meilleure estimation », correspondant à la propriété qui **est** logique pour le fournisseur. Par exemple, un fournisseur de carnet d’adresses peut toujours faire correspondre les noms de la liste des destinataires par rapport à **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), tandis qu’un autre peut autoriser un administrateur à sélectionner la propriété.
  
 **Pour définir une restriction PR_ANR de propriété de carnet d’adresses sur la table des matières d’un conteneur de carnet d’adresses**
  
1. Créez [une structure SRestriction](srestriction.md) comme illustré dans le code suivant : 
    
  ```cpp
  SRestriction SRestrict;
  SRestrict.rt = RES_PROPERTY;
  SRestrict.res.resProperty.relop = RELOP_EQ;
  SRestrict.res.resProperty.ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->Value.LPSZ = lpszName;
   
  ```

2. Appelez la méthode [IMAPITable::Restrict](imapitable-restrict.md) de la table des matières, en passant la structure **SRestriction** comme  _paramètre lpRestriction_ . 
    

