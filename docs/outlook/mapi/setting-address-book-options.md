---
title: Définition des options du carnet d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 9bd31233-fc8d-4e0a-9f1b-218c5ecb6d1b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5b1cabe090b9cb34b86cee3690c71ca0173fd721
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624229"
---
# <a name="setting-address-book-options"></a>Définition des options du carnet d’adresses

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Vous pouvez définir trois propriétés qui décrivent les options d’utilisation du carnet d’adresses :
  
- **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))
    
    La **PR_AB_SEARCH_PATH** est utilisée par [IAddrBook::ResolveName](iaddrbook-resolvename.md) pour déterminer les conteneurs à utiliser dans la résolution de noms et l’ordre dans le cas où ils doivent être impliqués. Pour chaque conteneur dans **PR_AB_SEARCH_PATH,** **IAddrBook::ResolveName** appelle sa méthode [IABContainer::ResolveNames.](iabcontainer-resolvenames.md) Les conteneurs au début de **la PR_AB_SEARCH_PATH** sont recherchés avant les conteneurs à la fin de **la PR_AB_SEARCH_PATH**. 
    
    L’ordre de **recherche PR_AB_SEARCH_PATH** est spécifié à l’aide d’une structure [SRowSet,](srowset.md) la même structure que celle utilisée pour représenter les lignes d’un tableau. Vous pouvez afficher le chemin de recherche actuel en appelant la méthode [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md) et le modifier en appelant la méthode [IAddrBook::SetSearchPath.](iaddrbook-setsearchpath.md) 
    
- **PR_AB_DEFAULT_DIR** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))
    
    La **PR_AB_DEFAULT_DIR** est l’identificateur d’entrée du conteneur de carnet d’adresses à afficher initialement lors de l’affichage du carnet d’adresses. Le paramètre de répertoire par défaut reste en vigueur jusqu’à ce que vous le modifiez en appelant la méthode [IAddrBook::SetDefaultDir.](iaddrbook-setdefaultdir.md) Vous pouvez afficher le répertoire par défaut en appelant la [méthode IAddrBook::GetDefaultDir.](iaddrbook-getdefaultdir.md) 
    
- **PR_AB_DEFAULT_PAB** ([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))
    
Ces trois propriétés sont spéciales, car vous ne pouvez pas les utiliser à l’aide des méthodes **IMAPIProp** standard. Au lieu de cela, vous devez utiliser **les méthodes IAddrBook.** Étant donné qu’aucune de ces propriétés ne peut être modifiée avec **IMAPIProp::SetProps,** il n’est pas nécessaire d’appeler **IMAPIProp::SaveChanges** pour rendre les modifications permanentes. Les modifications apportées via **les méthodes IAddrBook** prennent effet immédiatement. 
  
## <a name="see-also"></a>Voir aussi



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

