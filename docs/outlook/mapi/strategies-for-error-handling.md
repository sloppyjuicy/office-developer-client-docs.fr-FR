---
title: Stratégies de gestion des erreurs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: be941efd-04b3-48d0-9b9c-8195ad2bb58d
ms.openlocfilehash: 488d4cc4e506570062481c278b780cf928124bab
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63370630"
---
# <a name="strategies-for-error-handling"></a>Stratégies de gestion des erreurs

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Étant donné que les méthodes d’interface sont virtuelles, il n’est pas possible de connaître, en tant qu’appelant, l’ensemble complet des valeurs qui peuvent être renvoyées à partir d’un seul appel. Une implémentation d’une méthode peut renvoyer cinq valeurs ; un autre peut renvoyer huit. Les entrées de référence dans la documentation MAPI indiquent quelques valeurs qui peuvent être renvoyées pour chaque méthode . Voici les valeurs que votre client ou fournisseur de services peut vérifier et gérer, car elles ont des significations spéciales. D’autres valeurs peuvent être renvoyées, mais comme elles ne sont pas significatives, un code spécial pour les gérer n’est pas nécessaire. Une vérification simple de la réussite ou de l’échec est adéquate.
  
Quelques méthodes d’interface retournent des avertissements. Si une méthode que votre client ou fournisseur de services appelle peut renvoyer un avertissement, utilisez la macro **HR_FAILED** pour tester la valeur de retour plutôt qu’une vérification de zéro ou non zéro. Les avertissements, bien que non zéro, diffèrent des codes d’erreur en ce qu’ils n’ont pas le bit élevé. Si votre client ou fournisseur de services n’utilise pas la macro, il est probable qu’un avertissement soit confondu avec un échec. 
  
Bien que la plupart des méthodes et fonctions d’interface retournent des valeurs HRESULT, certaines fonctions retournent des valeurs longues non signées. En outre, certaines méthodes utilisées dans l’environnement MAPI proviennent de COM et retournent des valeurs d’erreur COM plutôt que des valeurs d’erreur MAPI. Gardez à l’esprit les instructions suivantes lors des appels :
  
- Ne vous appuyez jamais sur les valeurs de retour de **IUnknown::AddRef** ou **IUnknown::Release**. Ces valeurs de retour sont uniquement à des fins de diagnostic. 
    
- **IUnknown::QueryInterface** renvoie toujours des erreurs COM génériques lorsque la FACILITY_NULL ou FACILITY_RPC, plutôt que des erreurs MAPI. 
    
- Toutes les autres méthodes d’interface retournent des erreurs d’interface MAPI avec une FACILITY_ITF, FACILITY_RPC ou FACILITY_NULL erreurs.
    
Lorsqu’un appel est effectué à une méthode MAPI non prise en prise en place, l’une des quatre erreurs possibles peut être renvoyée : 
  
MAPI_E_NO_SUPPORT
  
MAPI_E_INTERFACE_NOT_SUPPORTED
  
MAPI_E_INVALID_PARAMETER
  
MAPI_E_VERSION. 
  

