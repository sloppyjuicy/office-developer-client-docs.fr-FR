---
title: Autorisations pour les propriétés et objets MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 32669cbe-5460-4043-99cc-c609608f48da
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 11c8a58e6cfe0719e8683c4e7a0fd966972117c4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569378"
---
# <a name="permissions-for-mapi-objects-and-properties"></a>Autorisations pour les propriétés et objets MAPI

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Autorisation d’accès ou l’ensemble des opérations permise, peut être une caractéristique d’objets MAPI et des propriétés individuelles pris en charge par ces objets. Accès aux objets est déterminée par le parent d’un objet. Pour un message, son dossier détermine les autorisations d’accès. Pour un utilisateur de messagerie ou une liste de distribution, le conteneur de carnet d’adresses pour ce faire. Lorsqu’un objet tel qu’un message se trouve dans deux dossiers, les autorisations pour les deux copies de l’objet peuvent être différentes. 
  
Clients à l’aide de ces objets peuvent demander le niveau d’accès autorisé pour l’objet en définissant l’indicateur MAPI_BEST_ACCESS sur l’appel de [IMAPISession::OpenEntry](imapisession-openentry.md) le plus élevé. Selon le fournisseur de services qui implémente l’objet, le client peut ou ne peut pas être accordé le niveau d’accès nécessaires. Les clients peuvent déterminer le niveau d’accès qu’ils ont été accordées en appelant la méthode **GetProps** pour récupérer la propriété **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) l’objet. Toutefois, étant donné que le fournisseur de services doit générer dynamiquement la valeur de cette propriété, il est recommandé que les clients récupérer uniquement lorsque cela est nécessaire. 
  
Pour déterminer si un conteneur tel qu’un dossier, un conteneur de carnet d’adresses ou une liste de distribution permet de modifier, appelez la méthode **GetProps** pour récupérer la propriété **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)). Niveau d’accès conteneur affecte les clients en termes de leur mode d’affichage de leurs interfaces utilisateur. Elle affecte également les implémenteurs d’objets conteneurs en termes de leur affichage de l’interface utilisateur et leur mise en œuvre général. 
  
Accès à une propriété particulière est déterminée par le schéma de propriété configurer par MAPI pour l’objet qui possède la propriété. Schémas de propriété spécifient l’ensemble des propriétés obligatoires et facultatifs d’un objet et leur autorisation d’accès. Contrairement à l’accès aux objets qui est déterminé par le parent de l’objet, l’accès à la propriété est global. Chaque objet, indépendamment du parent de l’objet, les conditions d’accès possède les mêmes autorisations pour la propriété, tel que déterminé par le schéma.
  
Lorsqu’une propriété est en lecture seule, il sera toujours disponible avec un appel **GetProps** ou **OpenProperty** . Toutefois, en fonction de l’implémentation de l’objet prenant en charge la propriété, il existe deux réponses possibles pour la méthode **SetProps** pour modifier une propriété et la méthode **DeleteProps** à sa suppression : 
  
- Échouer et retourner MAPI_E_NO_ACCESS
    
- Réussir avec aucune action entreprise
    
Propriété et aux objets peuvent également récupérer ou à définir à l’aide de l’interface [IPropData](ipropdataimapiprop.md) qui hérite de l’interface **IMAPIProp** . MAPI fournit une implémentation **IPropData** qui est basé sur des données en mémoire. Fournisseurs de services permet de mettre en œuvre **IMAPIProp** dans certaines circonstances, telles que pour l’objet de leur état **IPropData** ou s’ils utilisent une base de données qui n’a pas de transactions intégrées. **IPropData** fonctionne en mode exclusif en mémoire, rendant ainsi inutile verrouiller et déverrouiller les données. 
  
## <a name="see-also"></a>Voir aussi



[Vue d’ensemble de la propriété MAPI](mapi-property-overview.md)

