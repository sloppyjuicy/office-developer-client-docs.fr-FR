---
title: Invalidation d’un objet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7d601cee-ffc4-4c7c-8006-40b717dee247
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2346ec8541e1a8b7f5ea198722833447f9f5a289
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566473"
---
# <a name="invalidating-an-object"></a>Invalidation d’un objet

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Dans le cadre du processus d’arrêt de votre fournisseur, vous voudrez peut-être invalider un objet. Invalidation d’un objet implique de remplacer son vtable avec un vtable qui contient des implémentations pour les trois méthodes **IUnknown** : **QueryInterface**, **AddRef**et **Release**. Invalider un objet en appelant [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md), une méthode qui est incluse dans l’objet de prise en charge de chacun des trois types de fournisseurs courantes. Fournisseurs de rendre généralement cet appel dans l’implémentation de la méthode de **fermeture de session** de l’objet de leur ouverture de session. 
  
Invalidation d’un objet donne MAPI la responsabilité ultime pour libérer la mémoire associée à un objet. Vous pouvez libérer toutes les ressources liées à un objet, puis appelez **MakeInvalid** pour invalider toutes les méthodes dans les interfaces héritées. Les appels à une de ces méthodes renvoient MAPI_E_INVALID_OBJECT. À l’aide de **MakeInvalid** est une option choisir de nombreux fournisseurs de services d’ignorer. 
  
## <a name="see-also"></a>Voir aussi



[Arrêt d’un fournisseur de services](shutting-down-a-service-provider.md)

