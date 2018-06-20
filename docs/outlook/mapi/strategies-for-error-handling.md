---
title: Stratégies de gestion des erreurs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be941efd-04b3-48d0-9b9c-8195ad2bb58d
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: e778df216d0fe9b901cd9f7136c8014a6b8f0d0a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787260"
---
# <a name="strategies-for-error-handling"></a>Stratégies de gestion des erreurs

  
  
**S’applique à**: Outlook 
  
Méthodes d’interface sont virtuelles, il n’est pas possible de savoir, en tant qu’un appelant, l’ensemble de valeurs qui peut être renvoyé à partir de n’importe quel un appel. Une implémentation d’une méthode peut retourner les cinq valeurs ; un autre peut retourner huit. Les entrées de référence dans la documentation de MAPI répertorient quelques valeurs pouvant être renvoyés pour chaque méthode ; Voici les valeurs que votre client ou fournisseur de services peut rechercher et traiter, car elles ont une signification spéciale. Autres valeurs peuvent être renvoyées, mais, car ils ne sont pas significatives, code spécial pour gérer ces n’est pas nécessaire. Un contrôle simple pour la réussite ou l’échec est approprié.
  
Quelques méthodes de l’interface renvoient des avertissements. Si une méthode qui appelle votre client ou fournisseur de services peut retourner un message d’avertissement, utilisez la macro **HR_FAILED** pour tester la valeur de retour plutôt que d’une vérification de zéro ou différente de zéro. Avertissements, bien que différent de zéro, diffèrent des codes d’erreur en ce sens qu’ils n’ont pas le bit élevé à définir. Si votre client ou fournisseur de services n’utilise pas de la macro, il est probable que d’avertissement peut être confondue avec une défaillance. 
  
Bien que la plupart des méthodes d’interface et les fonctions renvoient des valeurs HRESULT, certaines fonctions renvoient des valeurs de type longs non signés. En outre, certaines méthodes utilisés dans l’environnement MAPI provenant de COM et renvoyer les valeurs d’erreur COM plutôt que les valeurs d’erreur MAPI. Gardez à l’esprit les instructions suivantes lors d’appels :
  
- Ne jamais s’appuient sur ou utilisez les valeurs de retour de **IUnknown::AddRef** ou **IUnknown::Release**. Ces valeurs renvoyées sont uniquement à des fins de diagnostic. 
    
- **IUnknown::QueryInterface** renvoie toujours les erreurs COM génériques où la fonctionnalité est FACILITY_NULL ou FACILITY_RPC, plutôt que des erreurs MAPI. 
    
- Toutes les autres méthodes d’interface retournent les erreurs de l’interface MAPI avec une installation de FACILITY_ITF ou FACILITY_RPC ou erreurs FACILITY_NULL.
    
Lorsqu’un appel est effectué à une méthode MAPI non pris en charge, un des quatre erreurs possibles peut être renvoyé : 
  
MAPI_E_NO_SUPPORT
  
MAPI_E_INTERFACE_NOT_SUPPORTED
  
MAPI_E_INVALID_PARAMETER
  
MAPI_E_VERSION. 
  

