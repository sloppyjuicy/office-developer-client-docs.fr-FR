---
title: Autorisations pour les objets et propriétés MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 32669cbe-5460-4043-99cc-c609608f48da
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 4efa9cd1596cffe19a19a62059f81fa553343d77
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436173"
---
# <a name="permissions-for-mapi-objects-and-properties"></a>Autorisations pour les objets et propriétés MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’autorisation d’accès, ou l’ensemble d’opérations permissables, peut être une caractéristique des objets MAPI et des propriétés individuelles pris en charge par ces objets. L’accès aux objets est déterminé par le parent d’un objet. Pour un message, son dossier détermine les autorisations d’accès. Pour un utilisateur de messagerie ou une liste de distribution, son conteneur de carnet d’adresses effectue cette détermination. Lorsqu’un objet tel qu’un message réside dans deux dossiers, les autorisations pour les deux copies de l’objet peuvent être différentes. 
  
Les clients qui utilisent ces objets peuvent demander le niveau d’accès le plus élevé autorisé pour l’objet en fixant l’indicateur MAPI_BEST_ACCESS sur l’appel [IMAPISession::OpenEntry.](imapisession-openentry.md) Selon le fournisseur de services qui implémente l’objet, le client peut ou non se faire accorder le niveau d’accès nécessaire. Les clients peuvent déterminer le niveau d’accès qui leur a été accordé en appelant la méthode **GetProps** d’objet pour récupérer la propriété **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)). Toutefois, étant donné que le fournisseur de services doit générer dynamiquement la valeur de cette propriété, il est recommandé que les clients ne la récupèrent que si nécessaire. 
  
Pour déterminer si un conteneur tel qu’un dossier, un conteneur de carnet d’adresses ou une liste de distribution autorise la modification, appelez sa méthode **GetProps** pour récupérer la propriété **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)). L’accès au niveau du conteneur affecte les clients en termes d’affichage de leurs interfaces utilisateur. Elle a également un impact sur les implémenteurs d’objets au sein des conteneurs en termes d’affichage de leur interface utilisateur et de leur implémentation générale. 
  
L’accès à une propriété particulière est déterminé par le schéma de propriétés mis en place par MAPI pour l’objet propriétaire de la propriété. Les schémas de propriété spécifient l’ensemble des propriétés obligatoires et facultatives d’un objet et leur autorisation d’accès. Contrairement à l’accès aux objets qui est déterminé par le parent de l’objet, l’accès aux propriétés est global. Chaque objet, quelles que soient les exigences d’accès du parent de l’objet, dispose des mêmes autorisations pour la propriété que déterminées par le schéma.
  
Lorsqu’une propriété est en lecture seule, elle est toujours disponible avec un appel **GetProps** ou **OpenProperty.** Toutefois, selon l’implémentation de l’objet qui la prise en charge, il existe deux résultats possibles pour la méthode **SetProps** pour la modification d’une propriété et la méthode **DeleteProps** pour la supprimer : 
  
- Échec et retour des MAPI_E_NO_ACCESS
    
- Réussir sans action
    
L’accès aux propriétés et aux objets peut également être récupéré ou définie à l’aide de l’interface [IPropData](ipropdataimapiprop.md) qui hérite de l’interface **IMAPIProp.** MAPI fournit une implémentation **d’IPropData** basée sur les données en mémoire. Les fournisseurs de services peuvent utiliser **IPropData** pour implémenter **IMAPIProp** dans certaines circonstances, par exemple pour leur objet d’état ou s’ils utilisent une base de données qui ne contient pas de transactions intégrées. **IPropData fonctionne exclusivement** en mémoire, ce qui rend inutile le verrouillage et le déverrouillage des données. 
  
## <a name="see-also"></a>Voir aussi



[Vue d’ensemble de la propriété MAPI](mapi-property-overview.md)

