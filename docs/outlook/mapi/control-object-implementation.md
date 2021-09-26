---
title: Implémentation de l’objet Control
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 4ad62ff0-c527-4e75-a2af-b5906a7588e8
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5484aeca5b09578fbfb6dd4758217b98cba9ac67
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611024"
---
# <a name="control-object-implementation"></a>Implémentation de l’objet Control

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les objets de contrôle, ou les objets qui prendre en charge l’interface [IMAPIControl : IUnknown,](imapicontroliunknown.md) sont implémentés par les fournisseurs pour ajouter des fonctionnalités à un bouton qui apparaît dans une boîte de dialogue MAPI. Les objets de contrôle ne peuvent être implémentés que pour les boutons. 
  
 **IMAPIControl a** trois méthodes : [GetLastError](imapicontrol-getlasterror.md), [GetState](imapicontrol-getstate.md)et [Activate](imapicontrol-activate.md). 
  
MAPI appelle **GetState** pour déterminer si le bouton est désactivé ou non. **GetState** est appelé dans les situations suivantes : 
  
- Lorsque la boîte de dialogue sur laquelle le bouton apparaît s’affiche pour la première fois.
    
- Lorsqu’une notification de tableau d’affichage est émise pour le bouton. 
    
Définissez le contenu du paramètre  _lpulState_ sur MAPI_DISABLED si l’utilisateur ne peut pas interagir avec le bouton et MAPI_ENABLED si l’utilisateur peut interagir. 
  
Lorsque l’utilisateur clique sur le bouton, MAPI appelle **Activate**. **Activate** effectue la tâche qui a été associée au bouton. Cette tâche peut être tout ce qui convient à votre fournisseur, comme l’affichage d’une boîte de dialogue ou la mise à jour d’une propriété. Si la tâche échoue parce que l’utilisateur l’a annulée, renvoyez MAPI_E_USER_CANCEL. Pour les autres causes d’échec, renvoyer la valeur d’erreur appropriée. 
  
Si la tâche réussit et qu’elle est liée à une modification de propriété qui est reflétée dans un autre contrôle de la boîte de dialogue, appelez [ITableData::HrNotify](itabledata-hrnotify.md). **HrNotify est** appelé pour émettre une notification de table d’affichage avec la propriété **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) dans la structure [TABLE_NOTIFICATION](table_notification.md) modifiée. Ne placez pas la nouvelle valeur de propriété dans la structure ; à la place, renvoyez-la [lorsque IMAPIProp::GetProps](imapiprop-getprops.md) est appelé. Bien qu’il soit généralement impossible d’utiliser une notification de tableau d’affichage pour désactiver ou activer un contrôle, elle peut être utilisée avec un bouton. MAPI actualise le contrôle modifié pour répondre à la notification. 
  
MAPI appelle la méthode **GetLastError** du contrôle lorsque **Activate** renvoie une erreur autre que MAPI_E_USER_CANCEL. Si **GetLastError** place des informations d’erreur étendues dans la structure [MAPIERROR](mapierror.md) qu’il renvoie dans le contenu du paramètre  _lppMAPIError,_ MAPI l’affiche pour l’utilisateur. 
  
## <a name="see-also"></a>Voir aussi



[Fournisseurs de services MAPI](mapi-service-providers.md)

