---
title: Définition des options de carnet d'adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9bd31233-fc8d-4e0a-9f1b-218c5ecb6d1b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f72c916e917543b11089f8f5ef1aa4b9552a1b6a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417342"
---
# <a name="setting-address-book-options"></a>Définition des options de carnet d'adresses

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Vous pouvez définir trois propriétés qui décrivent les options d'utilisation du carnet d'adresses:
  
- **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))
    
    La propriété **PR_AB_SEARCH_PATH** est utilisée par [IAddrBook:: ResolveName](iaddrbook-resolvename.md) pour déterminer les conteneurs devant être impliqués dans la résolution de noms et l'ordre dans lequel ils doivent être impliqués. Pour chaque conteneur dans **PR_AB_SEARCH_PATH**, **IAddrBook:: ResolveName** appelle sa méthode [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) . Les conteneurs au début de **PR_AB_SEARCH_PATH** sont recherchés avant les conteneurs à la fin de **PR_AB_SEARCH_PATH**. 
    
    L'ordre de recherche dans **PR_AB_SEARCH_PATH** est spécifié à l'aide d'une structure [SRowSet](srowset.md) , qui est utilisée pour représenter les lignes d'un tableau. Vous pouvez afficher le chemin d'accès de recherche en cours en appelant la méthode [IAddrBook:: GetSearchPath](iaddrbook-getsearchpath.md) et le modifier en appelant la méthode [IAddrBook:: SetSearchPath](iaddrbook-setsearchpath.md) . 
    
- **PR_AB_DEFAULT_DIR** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))
    
    La propriété **PR_AB_DEFAULT_DIR** est l'identificateur d'entrée du conteneur de carnet d'adresses à afficher initialement lors de l'affichage du carnet d'adresses. Le paramètre de répertoire par défaut reste en vigueur jusqu'à ce que vous le modifiiez en appelant la méthode [IAddrBook:: SetDefaultDir](iaddrbook-setdefaultdir.md) . Vous pouvez afficher le répertoire par défaut en appelant la méthode [IAddrBook:: GetDefaultDir](iaddrbook-getdefaultdir.md) . 
    
- **PR_AB_DEFAULT_PAB** ([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))
    
Ces trois propriétés sont spéciales car vous ne pouvez pas les utiliser à l'aide des méthodes **IMAPIProp** standard. Au lieu de cela, vous devez utiliser les méthodes **IAddrBook** . Comme aucune de ces propriétés ne peut être modifiée avec **IMAPIProp:: SetProps**, il n'est pas nécessaire d'appeler **IMAPIProp:: SaveChanges** pour faire en sorte que les modifications soient permanentes. Les modifications apportées via les méthodes **IAddrBook** prennent effet immédiatement. 
  
## <a name="see-also"></a>Voir aussi



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

