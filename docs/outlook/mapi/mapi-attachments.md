---
title: Pi�ces jointes MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6e6c6ad9-1e07-4234-a5ef-18020d7ce468
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 90fbec8b61499f383228823d69b041a21199a22e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417832"
---
# <a name="mapi-attachments"></a>Pi�ces jointes MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Certains fournisseurs de banque de messages permettent aux clients d'associer l'ajout d'informations sous la forme de fichiers, des objets OLE, des messages ou des donn�es binaires avec des messages. Ajout d'informations est appel� une pi�ce jointe d'un message. �tant donn� que les pi�ces jointes sont cr��s, g�r�s et accessibles uniquement par le biais de leurs messages, ils sont consid�r�s comme message sous-objets. Au lieu d'avoir un identificateur d'entr�e pour l'acc�s, les pi�ces jointes ont un autre num�ro s�quentiel comme un num�ro de pi�ce jointe. Ce num�ro identifie de mani�re unique la pi�ce jointe au sein de son message, mais pas n�cessairement au sein de la banque de messages. Deux messages diff�rents peuvent avoir diff�rentes pi�ces jointes ayant le m�me nombre de pi�ces jointes. Les numéros de pièce jointe sont valides uniquement tant que le message est ouvert et sont stockés dans la propriété **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)).
  
Pour acc�der � des informations r�capitulatives sur toutes les pi�ces jointes d'un message, les clients r�cup�rer sa table des pi�ces jointes. Le tableau de la pi�ce jointe consacr�e des informations que les clients peuvent utiliser pour acc�der � une pi�ce jointe directement, telles que son num�ro de pi�ce jointe et la cl� d'enregistrement. Les clients peuvent r�cup�rer un tableau des pi�ces jointes par :
  
- Calling **IMessage::GetAttachmentTable**. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).
    
- Calling **IMAPIProp::OpenProperty**. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
    
Message store providers are expected to support both of these approaches. **L’approche OpenProperty** nécessite que l’appelant spécifie IID_IMAPITable comme identificateur d’interface et **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) comme balise de propriété. **PR_MESSAGE_ATTACHMENTS** is a table object property that represents a message's attachment table. Message store providers are required to set **PR_MESSAGE_ATTACHMENTS** for each message and include it in the array of property tags returned from the **IMAPIProp::GetPropList** method. For more information, see [IMAPIProp::GetPropList](imapiprop-getproplist.md).
  
 **PR_MESSAGE_ATTACHMENTS** peuvent �tre utilis�es : 
  
- Avec **IMAPIProp::OpenProperty** pour acc�der � une table de pi�ce jointe ou un destinataire. 
    
- With **IMAPIProp::CopyTo** or **IMAPIProp::CopyProps** to exclude or include attachments when copying. For more information, see [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md).
    
- Une restriction sous-objet pour indiquer que la restriction de l'enfant doit appliquer aux pi�ces jointes.
    
For more information, see [Tables des pi�ces jointes](attachment-tables.md).
  

