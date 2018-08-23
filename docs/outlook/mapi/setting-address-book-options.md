---
title: Définition des options de carnet d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9bd31233-fc8d-4e0a-9f1b-218c5ecb6d1b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 0d93fde7d654f0ee56dcda9f2fb69ad622e476dd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593619"
---
# <a name="setting-address-book-options"></a>Définition des options de carnet d’adresses

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Vous pouvez définir trois propriétés qui décrivent les options permettant d’utiliser le carnet d’adresses :
  
- **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))
    
    La propriété **PR_AB_SEARCH_PATH** est utilisée par [IAddrBook::ResolveName](iaddrbook-resolvename.md) pour déterminer les conteneurs à participer à la résolution de noms et l’ordre qu’ils doivent être impliqués. Pour chaque conteneur dans **PR_AB_SEARCH_PATH**, **IAddrBook::ResolveName** appelle la méthode [IABContainer::ResolveNames](iabcontainer-resolvenames.md) . Conteneurs au début de **PR_AB_SEARCH_PATH** sont recherchés avant les conteneurs à la fin de **PR_AB_SEARCH_PATH**. 
    
    L’ordre de recherche dans **PR_AB_SEARCH_PATH** est spécifié à l’aide d’une structure [SRowSet](srowset.md) , la même structure qui est utilisée pour représenter des lignes d’un tableau. Vous pouvez afficher le chemin de recherche actuel en appelant la méthode [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md) et mettez-le en appelant la méthode [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) . 
    
- **PR_AB_DEFAULT_DIR** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))
    
    La propriété **PR_AB_DEFAULT_DIR** est l’identificateur d’entrée du conteneur de carnet d’adresses à afficher à l’origine lorsque le carnet d’adresses est affichée. Le paramètre de répertoire par défaut reste en vigueur jusqu'à ce que vous changiez en appelant la méthode [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) . Vous pouvez afficher le répertoire par défaut en appelant la méthode [IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md) . 
    
- **PR_AB_DEFAULT_PAB** ([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))
    
Ces trois propriétés sont spéciales, car vous ne pouvez pas travailler avec eux à l’aide des méthodes **IMAPIProp** standard. Au lieu de cela, vous devez utiliser les méthodes **IAddrBook** . Car aucune de ces propriétés peut être modifiée avec **IMAPIProp::SetProps**, il est inutile d’appeler **IMAPIProp::SaveChanges** pour apporter des modifications permanentes. Modifications apportées à travers les méthodes **IAddrBook** prennent effet immédiatement. 
  
## <a name="see-also"></a>Voir aussi



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

