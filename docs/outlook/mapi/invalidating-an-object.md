---
title: Invalidation d'un objet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7d601cee-ffc4-4c7c-8006-40b717dee247
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: bf7ef15ccfd9cd015771785bda9d6ad79415736b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407675"
---
# <a name="invalidating-an-object"></a>Invalidation d'un objet

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Dans le cadre du processus d'arrêt de votre fournisseur, il se peut que vous souhaitiez invalider un objet. L'invalidation d'un objet implique le remplacement de sa vtable par un vtable qui contient des implémentations pour les trois méthodes **IUnknown** : **AddRef**, **Release**et **QueryInterface**. Invalidez un objet en appelant [IMAPISupport:: MakeInvalid](imapisupport-makeinvalid.md), une méthode incluse dans l'objet de prise en charge de chacun des trois types de fournisseurs courants. Les fournisseurs effectuent généralement cet appel dans l'implémentation de la méthode de **fermeture** de session de leur objet d'ouverture de session. 
  
L'invalidation d'un objet confère à MAPI la responsabilité ultime de la libération de la mémoire associée à un objet. Vous pouvez libérer toutes les ressources connectées à un objet, puis appeler **MakeInvalid** pour invalider toutes les méthodes dans ses interfaces héritées. Les appels à l'une de ces méthodes renvoient MAPI_E_INVALID_OBJECT. L'utilisation de **MakeInvalid** est une option que de nombreux fournisseurs de services choisissent d'ignorer. 
  
## <a name="see-also"></a>Voir aussi



[Arrêt d'un fournisseur de services](shutting-down-a-service-provider.md)

