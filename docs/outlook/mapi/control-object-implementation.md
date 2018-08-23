---
title: Implémentation d’un objet de contrôle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ad62ff0-c527-4e75-a2af-b5906a7588e8
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b4b225f7e048ef40a79c4b258629cb01b79368d7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565829"
---
# <a name="control-object-implementation"></a>Implémentation d’un objet de contrôle

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contrôler les objets ou les objets qui prennent en charge la [IMAPIControl : IUnknown](imapicontroliunknown.md) de l’interface, sont implémentés par les fournisseurs pour ajouter une fonctionnalité à un bouton qui s’affiche dans une boîte de dialogue MAPI. Objets de contrôle peuvent être implémentés uniquement pour les boutons. 
  
 **IMAPIControl** a trois méthodes : [GetLastError](imapicontrol-getlasterror.md) [GetState](imapicontrol-getstate.md)et [Activer](imapicontrol-activate.md). 
  
**GetState** pour déterminer s’il faut désactiver le bouton appels MAPI. **GetState** est appelée dans les situations suivantes : 
  
- Lorsque la boîte de dialogue dans laquelle s’affiche le bouton premier affichage.
    
- Lorsqu’une notification de la table affichage est émise pour le bouton. 
    
Définir le contenu du paramètre _lpulState_ pour MAPI_DISABLED si l’utilisateur ne peut pas interagir avec le bouton MAPI_ENABLED si l’utilisateur peut interagir. 
  
Lorsque l’utilisateur clique sur le bouton, **Activer**appels MAPI. **Activer** effectue la tâche qui a été associée avec le bouton. Cette tâche peut être tout ce qui convient pour votre fournisseur, telles qu’affichant une boîte de dialogue ou la mise à jour d’une propriété. Si la tâche échoue parce que l’utilisateur a annulé, renvoyer MAPI_E_USER_CANCEL. Pour d’autres causes d’échec, renvoie la valeur d’erreur appropriés. 
  
Si la tâche se déroule correctement, et elle est liée à un changement de propriété qui apparaissent dans un autre contrôle dans la boîte de dialogue, appelez [ITableData::HrNotify](itabledata-hrnotify.md). **HrNotify** est appelé pour émettre une notification de table complet avec la propriété **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) de la propriété modifiée dans la structure [TABLE_NOTIFICATION](table_notification.md) . Ne placez pas la nouvelle valeur de propriété dans la structure ; au lieu de cela, elle retourne lorsque [IMAPIProp::GetProps](imapiprop-getprops.md) est appelée. Généralement, une notification de la table affichage ne peut être utilisée pour désactiver ou activer un contrôle, il peut être utilisé avec un bouton. MAPI actualise le contrôle modifié pour répondre à la notification. 
  
MAPI appelle la méthode du contrôle **GetLastError** lorsque **Activate** renvoie une erreur autre que MAPI_E_USER_CANCEL. Si **GetLastError** place les informations d’erreur étendue dans la structure [MAPIERROR](mapierror.md) qu’elle renvoie le contenu du paramètre _lppMAPIError_ , MAPI affiche pour l’utilisateur. 
  
## <a name="see-also"></a>Voir aussi



[Fournisseurs de services MAPI](mapi-service-providers.md)

