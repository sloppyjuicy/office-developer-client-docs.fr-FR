---
title: Invalidation d’un objet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 7d601cee-ffc4-4c7c-8006-40b717dee247
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 28db490d9acff055705fc75ff2d45741ddf651fd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571639"
---
# <a name="invalidating-an-object"></a>Invalidation d’un objet

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Dans le cadre du processus d’arrêt de votre fournisseur, vous pouvez invalider un objet. Invalidating an object involves replacing its vtable with a vtable that contains implementations for the three **IUnknown** methods: **AddRef**, **Release**, and **QueryInterface**. Invalidez un objet en appelant [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md), une méthode incluse dans l’objet de prise en charge de chacun des trois types de fournisseurs courants. Les fournisseurs font généralement cet appel dans l’implémentation de la méthode **Logoff** de leur objet d’accès. 
  
L’invalidation d’un objet donne à MAPI la responsabilité ultime de libérer la mémoire associée à un objet. Vous pouvez libérer toutes les ressources connectées à un objet, puis appeler **MakeInvalid** pour invalider toutes les méthodes dans ses interfaces héritées. Les appels à l’une de ces méthodes retournent MAPI_E_INVALID_OBJECT. **L’utilisation de MakeInvalid** est une option que de nombreux fournisseurs de services choisissent d’ignorer. 
  
## <a name="see-also"></a>Voir aussi



[Arrêt d’un fournisseur de services](shutting-down-a-service-provider.md)

