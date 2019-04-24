---
title: Stratégies de gestion des erreurs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be941efd-04b3-48d0-9b9c-8195ad2bb58d
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 9e76ae3f292d8348b9dc64cb54bffae96b96e871
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327215"
---
# <a name="strategies-for-error-handling"></a>Stratégies de gestion des erreurs

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Étant donné que les méthodes d'interface sont virtuelles, il n'est pas possible de connaître, en tant qu'appelant, l'ensemble complet des valeurs qui peuvent être renvoyées à partir d'un appel. Une implémentation d'une méthode peut renvoyer cinq valeurs; un autre peut renvoyer huit. Les entrées de référence dans la documentation MAPI répertorient quelques valeurs qui peuvent être renvoyées pour chaque méthode; Il s'agit des valeurs que votre client ou fournisseur de services peut vérifier et gérer, car ils ont des significations spéciales. D'autres valeurs peuvent être renvoyées, car elles ne sont pas significatives, le code spécial permettant de les gérer n'est pas nécessaire. Une vérification simple de la réussite ou de l'échec est suffisante.
  
Quelques-unes des méthodes de l'interface retournent des avertissements. Si une méthode que votre client ou fournisseur de services appelle peut renvoyer un avertissement, utilisez la macro **HR_FAILED** pour tester la valeur de retour plutôt qu'une vérification pour zéro ou une valeur différente de zéro. Bien que non nul, les avertissements diffèrent des codes d'erreur en ce qu'ils n'ont pas le bit supérieur défini. Si votre client ou fournisseur de services n'utilise pas la macro, il est probable qu'un avertissement peut être confondu pour une défaillance. 
  
Bien que la plupart des méthodes et fonctions d'interface retournent des valeurs HRESULT, certaines fonctions renvoient des valeurs de type long non signées. Par ailleurs, certaines méthodes utilisées dans l'environnement MAPI proviennent de COM et renvoient des valeurs d'erreur COM plutôt que des valeurs d'erreur MAPI. Gardez à l'esprit les instructions suivantes lors de l'appel:
  
- Ne reposez jamais sur ou utilisez les valeurs de retour de **IUnknown:: AddRef** ou **IUnknown:: Release**. Ces valeurs de retour sont uniquement à des fins de diagnostic. 
    
- **IUnknown:: QueryInterface** renvoie toujours des erreurs com génériques lorsque l'installation est FACILITY_NULL ou FACILITY_RPC, plutôt que des erreurs MAPI. 
    
- Toutes les autres méthodes d'interface renvoient des erreurs d'interface MAPI avec une installation de FACILITY_ITF ou des erreurs FACILITY_RPC ou FACILITY_NULL.
    
Lorsqu'un appel est effectué vers une méthode MAPI non prise en charge, l'une des quatre erreurs possibles peut être renvoyée: 
  
MAPI_E_NO_SUPPORT
  
MAPI_E_INTERFACE_NOT_SUPPORTED
  
MAPI_E_INVALID_PARAMETER
  
MAPI_E_VERSION. 
  

