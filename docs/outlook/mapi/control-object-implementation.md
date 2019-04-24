---
title: Implémentation d'un objet de contrôle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ad62ff0-c527-4e75-a2af-b5906a7588e8
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 8304021565638f8a5893d0be8cd6a94ed62a8d95
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335657"
---
# <a name="control-object-implementation"></a>Implémentation d'un objet de contrôle

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les objets Control, ou les objets qui prennent en charge l'interface [IMAPIControl: IUnknown](imapicontroliunknown.md) , sont implémentés par les fournisseurs pour ajouter des fonctionnalités à un bouton qui apparaît dans une boîte de dialogue MAPI. Les objets Control ne peuvent être implémentés que pour les boutons. 
  
 **IMAPIControl** possède trois méthodes: [GetLastError](imapicontrol-getlasterror.md), [GetState](imapicontrol-getstate.md)et [activer](imapicontrol-activate.md). 
  
MAPI appelle **GetState** pour déterminer si le bouton doit être désactivé ou non. **GetState** est appelé dans les situations suivantes: 
  
- Lorsque la boîte de dialogue dans laquelle apparaît le bouton s'affiche pour la première fois.
    
- Lorsqu'une notification de table d'affichage est générée pour le bouton. 
    
Définissez le contenu du paramètre _lpulState_ sur MAPI_DISABLED si l'utilisateur ne peut pas interagir avec le bouton et MAPI_ENABLED si l'utilisateur peut interagir. 
  
Lorsque l'utilisateur clique sur le bouton, **** MAPI appelle la méthode Activate. **Activate** effectue la tâche associée au bouton. Cette tâche peut être tout à fait appropriée pour votre fournisseur, telle que l'affichage d'une boîte de dialogue ou la mise à jour d'une propriété. Si la tâche échoue parce que l'utilisateur l'a annulée, retournez MAPI_E_USER_CANCEL. Pour les autres causes de l'échec, renvoyez la valeur d'erreur appropriée. 
  
Si la tâche réussit et qu'elle est liée à une modification de propriété qui apparaît dans un autre contrôle de la boîte de dialogue, appelez [ITableData:: HrNotify](itabledata-hrnotify.md). **HrNotify** est appelé pour émettre une notification de table d'affichage avec la propriété **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) de la propriété modifiée dans la structure [TABLE_NOTIFICATION](table_notification.md) . Ne placez pas la nouvelle valeur de la propriété dans la structure; à la place, renvoyez-le lorsque [IMAPIProp:: GetProps](imapiprop-getprops.md) est appelé. Bien qu'une notification de table d'affichage ne puisse pas être utilisée pour désactiver ou activer un contrôle, elle peut être utilisée avec un bouton. MAPI actualise le contrôle modifié pour répondre à la notification. 
  
MAPI appelle la méthode **GetLastError** du contrôle lorsque **** la méthode Activate renvoie une erreur autre que MAPI_E_USER_CANCEL. Si **GetLastError** place des informations d'erreur étendues dans la structure [MAPIERROR](mapierror.md) qu'il renvoie dans le contenu du paramètre _lppMAPIError_ , MAPI l'affiche pour l'utilisateur. 
  
## <a name="see-also"></a>Voir aussi



[Fournisseurs de services MAPI](mapi-service-providers.md)

