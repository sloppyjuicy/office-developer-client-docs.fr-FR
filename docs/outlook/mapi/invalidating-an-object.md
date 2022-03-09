---
title: Invalidation d’un objet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 7d601cee-ffc4-4c7c-8006-40b717dee247
ms.openlocfilehash: 52f42ac23e904a911ff7a76a3177847c4f83876a
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63370798"
---
# <a name="invalidating-an-object"></a>Invalidation d’un objet

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Dans le cadre du processus d’arrêt de votre fournisseur, vous souhaitez peut-être invalider un objet. L’invalidation d’un objet implique de remplacer son vtable par un vtable qui contient des implémentations pour les trois méthodes **IUnknown** : **AddRef**, **Release** et **QueryInterface**. Invalidez un objet en appelant [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md), une méthode incluse dans l’objet de prise en charge de chacun des trois types de fournisseurs courants. Les fournisseurs font généralement cet appel dans l’implémentation de la méthode **Logoff** de leur objet d’accès. 
  
L’invalidation d’un objet donne à MAPI la responsabilité ultime de libérer la mémoire associée à un objet. Vous pouvez libérer toutes les ressources connectées à un objet, puis appeler **MakeInvalid** pour invalider toutes les méthodes dans ses interfaces héritées. Les appels à l’une de ces méthodes retournent MAPI_E_INVALID_OBJECT. **L’utilisation de MakeInvalid** est une option que de nombreux fournisseurs de services choisissent d’ignorer. 
  
## <a name="see-also"></a>Voir aussi



[Arrêt d’un fournisseur de services](shutting-down-a-service-provider.md)

